---
id: 69
title: Toe Dabbing in ESP8266
date: 2018-03-02T13:38:28+00:00
author: tony
layout: post
guid: http://ttech.tonym128.com/?p=69
amazon_polly_audio_link_location:
  - https://s3.us-east-1.amazonaws.com/audio-for-wordpress-17069432435aa889ef033eb26aa48aa297fdf8f7/2018/03/amazon_polly_69.mp3?version=1536824822
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
image: /wp-content/uploads/2018/02/mother-board-electronics-computer-board-39290-e1519399533759.jpeg
categories:
  - Uncategorized
tags:
  - hacking
  - hardware
  - iot
---
<article class="markdown-body"> 

# The start of something small</article> 

I&#8217;ve always had a dream of learning electronics and I&#8217;ve had a [ESP8266](https://en.wikipedia.org/wiki/ESP8266) sitting around on my desk for a quite a while now.<figure id="attachment_82" aria-describedby="caption-attachment-82" style="width: 556px" class="wp-caption alignnone">

<img class="wp-image-82 " src="http://ttech.tonym128.com/wp-content/uploads/2018/03/ESP-01-300x300.jpg" alt="By Sparkfun Electronics - https://c1.staticflickr.com/1/494/19681470919_9a9bcd5692_z.jpg, CC BY 2.0, https://commons.wikimedia.org/w/index.php?curid=57331438" width="556" height="556" srcset="http://localhost:8080/wp-content/uploads/2018/03/ESP-01-300x300.jpg 300w, http://localhost:8080/wp-content/uploads/2018/03/ESP-01-150x150.jpg 150w, http://localhost:8080/wp-content/uploads/2018/03/ESP-01.jpg 600w" sizes="(max-width: 556px) 100vw, 556px" /> <figcaption id="caption-attachment-82" class="wp-caption-text">By Sparkfun Electronics &#8211; https://c1.staticflickr.com/1/494/19681470919\_9a9bcd5692\_z.jpg, CC BY 2.0, https://commons.wikimedia.org/w/index.php?curid=57331438</figcaption></figure> 

This board is a marvel of technology, originally it was designed as a WiFi chip, but it was made so well and flexibly, that hackers learnt that you could program this small chip to do wonderful amazing low power things via the serial port using just the [AT command set](https://en.wikipedia.org/wiki/Hayes_command_set), which is how they used to talk to modems, way back when.

An entire eco-system of tools formed around this and a community of hardware aficionados who wanted to build small pervasive electronics were born.

## The dream

<img class="alignnone wp-image-72" src="http://ttech.tonym128.com/wp-content/uploads/2018/02/pexels-photo-279467-300x200.jpeg" alt="" width="618" height="412" srcset="http://localhost:8080/wp-content/uploads/2018/02/pexels-photo-279467-300x200.jpeg 300w, http://localhost:8080/wp-content/uploads/2018/02/pexels-photo-279467-768x512.jpeg 768w, http://localhost:8080/wp-content/uploads/2018/02/pexels-photo-279467-1024x683.jpeg 1024w, http://localhost:8080/wp-content/uploads/2018/02/pexels-photo-279467.jpeg 1125w" sizes="(max-width: 618px) 100vw, 618px" /> 

My dream was always to build small &#8216;throw away&#8217; electronic devices cheaply that could form some sort of network and provide access to metrics of some sort, light levels, temperatures, air pressure and layer them throughout a room and then build displays of this data. An example that I&#8217;ve seen recently isn&#8217;t quite this but it is similar in a popular supermarket chain that shows their electricity and water usage on real time updated graphs at the entrance.

I find this sort of information which is kinda mundane being turned into something useful, fascinating.

## Turn it into a reality

<img class="alignnone wp-image-73" src="http://ttech.tonym128.com/wp-content/uploads/2018/02/pexels-photo-533189-300x225.jpeg" alt="" width="570" height="428" srcset="http://localhost:8080/wp-content/uploads/2018/02/pexels-photo-533189-300x225.jpeg 300w, http://localhost:8080/wp-content/uploads/2018/02/pexels-photo-533189-768x576.jpeg 768w, http://localhost:8080/wp-content/uploads/2018/02/pexels-photo-533189-1024x768.jpeg 1024w, http://localhost:8080/wp-content/uploads/2018/02/pexels-photo-533189-1568x1176.jpeg 1568w" sizes="(max-width: 570px) 100vw, 570px" /> 

To find a project there first needs to be something to do&#8230; so the simplest project for the ESP is to set it up as a [WiFi Access Point](https://gist.github.com/Cyclenerd/7c9cba13360ec1ec9d2ea36e50c7ff77), pretty advanced functionality for a single chip, or you can make it connect to an existing wifi network and display a button on a website to click [on and off](https://create.arduino.cc/projecthub/jaiprak/control-led-from-web-app-using-esp8266-serial-wifi-module-cdf419) . Once it&#8217;s connected with this example above, it should serve a website to you regardless of where you try to browse, regardless of where you try to browse to.

The board I got has a micro usb port with a serial port chip, two buttons and easy pin outs for doing additional things like adding sensors or servos&#8217;<article class="markdown-body"> 

## The first steps into the new brave world.

<img class="alignnone wp-image-71" src="http://localhost:8080/wp-content/uploads/2018/02/Arduino.png" alt="" width="574" height="381" /> 

The chip arrives blank so I had to first program the firmware using a [flasher](https://en.wikipedia.org/wiki/Firmware#Flashing) and a [ROM](https://en.wikipedia.org/wiki/Read-only_memory).

This was relatively scary as I always find my heart skips a beat when it comes time to click the flash button.

Once we have the firmware, which is only actually writing some code. I installed the [Arduino IDE](https://www.arduino.cc/en/Main/Software) and a few plugins to make it work with the ESP8266.

I found the [online code sample](https://gist.github.com/Cyclenerd/7c9cba13360ec1ec9d2ea36e50c7ff77) for doing exactly what I wanted and the code was simple enough to copy paste while still understanding every line, so that made it perfect.

<img class="alignnone wp-image-80" src="http://ttech.tonym128.com/wp-content/uploads/2018/03/Code-300x288.png" alt="" width="519" height="498" srcset="http://localhost:8080/wp-content/uploads/2018/03/Code-300x288.png 300w, http://localhost:8080/wp-content/uploads/2018/03/Code.png 649w" sizes="(max-width: 519px) 100vw, 519px" /> </article> 

## Up and running.

With the code deployed and live on the ESP, I can fire up the wireless connection wizard on my PC (and my phone) and can connect to the new WiFi network (<span class="pl-s">IoT &#8212; Free WiFi</span>).

And it displays this page when you try to browse anything!

<img class="alignnone size-full wp-image-79" src="http://localhost:8080/wp-content/uploads/2018/03/Im-just-a-bottle-WiFi.png" alt="" width="239" height="42" /> 

No too exciting, but pretty good for a tiny little board.

## Where to from here ?

Now that I have an ESP8266 up and running and doing something useful, what more could I do ?

There&#8217;s some hardware like the [Sonoff Basic ](http://sonoff.itead.cc/en/products/sonoff/sonoff-basic) 

<img class="alignnone wp-image-81" src="http://ttech.tonym128.com/wp-content/uploads/2018/03/Sonoff-300x300.jpg" alt="" width="473" height="473" srcset="http://localhost:8080/wp-content/uploads/2018/03/Sonoff-300x300.jpg 300w, http://localhost:8080/wp-content/uploads/2018/03/Sonoff-150x150.jpg 150w, http://localhost:8080/wp-content/uploads/2018/03/Sonoff-768x768.jpg 768w, http://localhost:8080/wp-content/uploads/2018/03/Sonoff.jpg 1000w" sizes="(max-width: 473px) 100vw, 473px" /> 

which can let you switch electrical switches on and off using a simple programmable interface.

Getting the whole house hooked up to be controlled from a mobile phone is something that I find fascinating, control sound, appliances, moods, lighting.

You could for instance have a temperature sensor which knows what times of day to activate a heater for when you get home to a nice and cosy lounge.

You can have movement sensors that could play music which follows you around the house, but only in the room you&#8217;re in.

The world becomes yours to control and gamify. A future I look forwards too and I&#8217;m glad I have dabbled my toes, and will definitely be back to dive in, in the coming years!

&nbsp;