---
id: 111
title: Slownet :-( , Fasternet? Raspinet!
date: 2018-03-26T23:01:58+00:00
author: tony
layout: post
guid: http://ttech.tonym128.com/?p=111
amazon_polly_audio_link_location:
  - https://s3.us-east-1.amazonaws.com/audio-for-wordpress-17069432435aa889ef033eb26aa48aa297fdf8f7/2018/03/amazon_polly_111.mp3?version=1536824792
amazon_polly_audio_location:
  - s3
amazon_polly_enable:
  - "1"
amazon_polly_voice_id:
  - Amy
amazon_polly_sample_rate:
  - "22050"
amazon_polly_settings_hash:
  - 6778c89b2df9c7e35627cc39ce0e91fa
image: /wp-content/uploads/2018/03/Raspberry-Pi-3.jpg
categories:
  - Uncategorized
tags:
  - hacking
  - raspberry pi
---
## The problem

My internet was under performing quite severly and I didn&#8217;t know why. Occasionally for periods of time from a few minutes to hours at a time our internet would become unusable.

First thing was isolating the problem . I installed all the monitoring tools I could to find to narrow down the problem to an application or device.

I managed to find the app causing all my issues, it was [Google Photo](http://photos.google.com/)&#8216;s but there were no throttling options in the software to stop it.

<img class="irc_mi aligncenter" src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4f/Google_Photos_icon.svg/2000px-Google_Photos_icon.svg.png" alt="Image result for google photos logo" width="222" height="222" /> 

I was honestly so surprised, but anytime a device in our house came home to land on the WiFi, we couldn&#8217;t browse the web until it was done uploading it&#8217;s photo&#8217;s.

The worst thing about the problem is that we love Google Photo&#8217;s and couldn&#8217;t live without. From the free uploads at a great quality to the AI on the image categorization and knowing all the photos I&#8217;m in with my favourite people.

Back to the cons! No internet for quite a substantial portion of time until videos and photos were uploaded snugly and safely to the web vault, was not something we wanted to live with.

## What I wanted to solve

I wanted internet all the time, I didn&#8217;t want to manually have to throttle all connections on the network, install software on each device to do the same.

<img class="irc_mi aligncenter" src="https://img.memecdn.com/slow-internet_o_1592157.jpg" alt="Image result for slow internet meme" width="500" height="388" /> 

I wanted something to automatically take care of an issue I couldn&#8217;t solve inside the Google Photo&#8217;s app. I had an idea that I could setup a device which would automatically share the bandwidth fairly between all our users and programs fairly.

## The solution

The [Raspberry Pi](https://www.raspberrypi.org/products/) is an awesome piece of hardware, anytime I have a IT household problem to solve it usually has just what I need. From the earliest iteration it was a phenomenal piece of hardware in a bite size format and a teeny tiny price of just $35.

A brief investigation into the Raspberry Pi 3 showed that you can run it in a [Access Point](https://en.wikipedia.org/wiki/Wireless_access_point) mode, and with the Ethernet wired into the network, the rest would be software.

<img class="irc_mi aligncenter" src="https://fthmb.tqn.com/8e-qS4qOpYhOsqr77j9ndkq9NH8=/735x0/linksys_wap54g-400-56a1ad223df78cf7726cf853.jpg" alt="Image result" width="735" height="671" /> 

The initial problem was to setup the Pi as a WiFi router, which is quite well documented on the web, I followed this [guide](https://frillip.com/using-your-raspberry-pi-3-as-a-wifi-access-point-with-hostapd/).

This will help you setup a Wifi Access Point, [DHCP](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol) and [DNS](https://en.wikipedia.org/wiki/Domain_Name_System) and absolutely nothing was solved yet&#8230; no [QoS](https://en.wikipedia.org/wiki/Quality_of_service).

<img class="irc_mi aligncenter" src="https://pickmyroutercdn1-q9wpjck7cns8nft.netdna-ssl.com/wp-content/uploads/2016/03/qos_1440-1024x1024.png" alt="Image result for qos logo" width="330" height="330" /> 

The last piece of the puzzle. I was actually quite surprised that a piece of software called [IP Tables](https://en.wikipedia.org/wiki/Iptables), which is normally used for directing traffic was actually able do quality management and throttling.

<img class="mw-mmv-final-image svg mw-mmv-dialog-is-open" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/37/Netfilter-packet-flow.svg/1450px-Netfilter-packet-flow.svg.png" alt="" crossorigin="anonymous" /> 

The IP Tables result was actually pretty great, but was quite complicated to setup, I modified a [guide](http://lartc.org/howto/lartc.cookbook.fullnat.intro.html) I found and &#8230; we now have the best internet we ever had at home, even though the line is quite slow, it&#8217;s never felt slow for us again.

## A little bit more technical stuff

Using Traffic Control (tc) command you can setup discovery queues which allow traffic to be classified into classes.

<pre class="SCREEN">tc qdisc add dev eth0 root handle 1: htb default 15</pre>

<pre class="SCREEN">tc class add dev eth0 parent 1:1 classid 1:10 htb rate 80kbit ceil 80kbit prio 0
</pre>

Inside the classes you can classify traffic filters, which will put your traffic into buckets.

Once you have your traffic classified into buckets you start prioritizing which buckets will get bandwidth allocation.

<pre class="SCREEN">tc filter add dev eth0 parent 1:0 protocol ip prio 1 handle 1 fw classid 1:10</pre>

And you can also prioritize certain packets, normally ones that are critical but never actually use a lot of bandwidth, some like SSH which is text only for controlling servers and SYN, which is handshaking packets, giving these the highest priorities should never take away from your top download speed, but does give you much better response times on websites.

<pre class="SCREEN">iptables -t mangle -I PREROUTING -p tcp -m tcp --tcp-flags SYN,RST,ACK SYN -j MARK --set-mark 0x1
iptables -t mangle -I PREROUTING -p tcp -m tcp --tcp-flags SYN,RST,ACK SYN -j RETURN</pre>

I did have a few issues getting it to start on boot, which was quite a pain due to all the commands, but did eventually get it to start up in init.d

## Where to from here

I could have used some expensive off the shelf hardware to fix the problem, or buy faster internt, but it was actually great being able to take hardware I had around the house and fix a problem I was having.

This actually accomplished everything I wanted, but there were a few things that would have been nice to add. Since I had the WiFi router functioning on a full linux computer, getting some metrics off it would have been great.

  * View bandwidth usage by PC, Protocol, Country, Website.
  * Setup a user login and guest system for logins and turn this into an open hotspot, with only unused capacity being shared.
  * Thresholds for certain services, like limit Netflix automatically so it only streams at 720p and not 1080p.

Back to cat memes!

<img class="irc_mi aligncenter" src="https://s-media-cache-ak0.pinimg.com/originals/51/b4/80/51b4802111d0f287b1fa7c914e3e8fe0.jpg" alt="Image result for cat soul starve" width="460" height="226" /> 

<img class="irc_mut iK_OHzPE9y7c-HwpH6ZlgJaI aligncenter" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ1fo8JCCBJQowPgSKgwdTSPDywYoFc-JhJL7U9Z01IKzaJA-zL" alt="Related image" width="500" height="371" /><img class="irc_mi aligncenter" src="https://memegenerator.net/img/instances/500x/67836469/hes-so-high-speed.jpg" alt="Image result for high speed cat meme" width="499" height="355" />