---
id: 232
title: WordPress, how many ways can I say hello ?
date: 2018-10-22T23:15:15+00:00
author: tony
layout: post
guid: http://ttech.mamacos.media/?p=232
amazon_polly_audio_link_location:
  - https://s3.us-east-1.amazonaws.com/audio-for-wordpress-17069432435aa889ef033eb26aa48aa297fdf8f7/2018/10/amazon_polly_232.mp3?version=1540243759
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
amazon_polly_transcript_en:
  - |
    
    WordPress, how many ways can I say hello ?. **AMAZONPOLLY*SSML*BREAK*time=***1s***SSML**  **AMAZONPOLLY*SSML*BREAK*time=***1s***SSML**
    I find it funny that I can write programs that can calculate risk on a share portfolio, do heavy math calculations on tiny hardware devices, help write programs that massive enterprise businesses use to stock take , but putting up my first WordPress blog, was just as massive en devour to get something I was happy with.
    It didn't involve writing a line of code, but there were a lot of lessons!
    What did I want to accomplish ?
    Mostly was super keen to get a nice website up, quickly and easily to share information with people. I have always heard ... things... about WordPress, so I thought it a good opportunity to give it a go.
    I had a few things I really wanted to get into the project
    Self hostedSSLEasy to updateSome sort of database for the articlesPotentially multi user for one dayFollow web best practicesSmall and fastThemed as a bonus for a ever changing look
    What did I learn early on ?
    I started by testing on Wordpress.com just to see if I could be happy enough, and I was, but onto the first point, self hosted. So I decided to move over to old faithful Amazon Web Services and to use a really cheap Lightsail instance.
    BitNami provide a nicely packaged Wordpress image you can spin up at the touch of a button in Lightsail.
    Image: .
    Image: .
    WordPress.com and WordPress.org are slightly different beasts, I had a few assumptions about being able to easily transfer between the two, but if you could it was more complicated than I could figure out in the time I was willing to invest. I think if you upgrade you account you can.
    Image: .
    Self Hosted, Easy to Update, Follows Web Best Practices, Themed, Database driven, Multi-User
    Image: .
    SSL, Small and Fast.
    Not doing too bad at the moment, only two things remaining on my little check lists, or at least I thought!
    The lists of things started then, getting it hosted on domain, making it load faster than it was, getting SSL up and running, and getting a nice book type read to it. So just a couple things :)
    I got a Domain setup pretty quickly using AWS Route 53, the hardest part was waiting 5 minutes, for it to come up.
    Image: .
    SSL took me a while but using LetsEncrypt , a very cool project to provide safe and free SSL certificates to encrypt all the things, and following a guide here got me over the line.
    There were a ton of amazing plugins that I played with along the way, but I really enjoyed a few that pushed some new technologies that I was interested in into the blog.
    Yeost SEO, Glue for Yeost SEO and AMP, Amazon Polly, All-in-One WP Migration, All In One SEO Pack, WP Mail SMTP.
    Image: .
    Image: .
    Getting Google Analytics up was a good idea, mostly makes me cry, but a good idea none the less. I think this was all through Yeost SEO, but I used a few along the way.
    Image: .
    The most fascinating time sink was AMP and getting that to work. It's a special technology developed by Google to make pages load really quickly. Similar to Facebook Instant Articles.
    I used almost all the plugins I could find for Wordpress and eventually settled on a defunct AMP one, but have since converted to Glue for Yeost SEO and AMP.
    Image: .
    Amazon Polly transcription was pretty easy to integrate and I find it fun listening to her drone my own words back at me, so much so that I've left it enabled :) I really liked that it uploads the article MP3's into a AWS S3 Bucket which it can then pull them from just as MP3 files!
    Where too from here ?
    Image: .
    I think the site looks pretty good now, has a few good features and mostly gets out the way to let me write new content quickly and get it out there.
    What's in store for the future ?
    I think that cool changes are coming soon, from the new Gutenberg editor for Wordpress which I'm finding really cool after a few tries using it. To the new Headless CMS movement, which is a bit of a off shoot of the whole React Website with a API / Database sitting behind it.
    I am honestly still tempted to roll my own, but that's offset to let me rather keep exploring and sharing new technologies and my first forays into them.
    I hope you enjoy the articles and potentially set up you own blog or experiment with something you learnt here.
amazon_polly_transcript_source_lan:
  - en
ampforwp_custom_content_editor:
  - '<p><br data-mce-bogus="1"></p>'
ampforwp_custom_content_editor_checkbox:
  - ""
ampforwp-amp-on-off:
  - default
ampforwp-ia-on-off:
  - default
ampforwp-redirection-on-off:
  - enable
image: /wp-content/uploads/2018/10/Wordpress.png
categories:
  - Uncategorized
tags:
  - aws
  - blog
  - cloud
  - wordpress
---
I find it funny that I can write programs that can calculate risk on a share portfolio, do heavy math calculations on tiny hardware devices, help write programs that massive enterprise businesses use to stock take , but putting up my first WordPress blog, was just as massive en devour to get something I was happy with.

It didn&#8217;t involve writing a line of code, but there were a lot of lessons!

## What did I want to accomplish ?

Mostly was super keen to get a nice website up, quickly and easily to share information with people. I have always heard &#8230; things&#8230; about WordPress, so I thought it a good opportunity to give it a go.

I had a few things I really wanted to get into the project

  * Self hosted  
    
  * SSL  
    
  * Easy to update
  * Some sort of database for the articles
  * Potentially multi user for one day
  * Follow web best practices
  * Small and fast
  * Themed as a bonus for a ever changing look  
    

## What did I learn early on ?

I started by testing on **WordPress.com** just to see if I could be happy enough, and I was, but onto the first point, self hosted. So I decided to move over to old faithful **Amazon Web Services** and to use a really cheap **Lightsail** instance.

**BitNami** provide a nicely packaged **WordPress** image you can spin up at the touch of a button in **Lightsail**.

<div class="wp-block-image">
  <figure class="alignleft is-resized"><img src="https://ttech.mamacos.media/wp-content/uploads/2018/10/bitnamilogo.png" alt="" class="wp-image-234" width="150" height="79" srcset="http://localhost:8080/wp-content/uploads/2018/10/bitnamilogo.png 310w, http://localhost:8080/wp-content/uploads/2018/10/bitnamilogo-300x158.png 300w" sizes="(max-width: 150px) 100vw, 150px" /></figure>
</div>

<div class="wp-block-image">
  <figure class="aligncenter is-resized"><img src="https://ttech.mamacos.media/wp-content/uploads/2018/10/lightsail.png" alt="" class="wp-image-235" width="282" height="68" /></figure>
</div>



**WordPress.com** and **WordPress.org** are slightly different beasts, I had a few assumptions about being able to easily transfer between the two, but if you could it was more complicated than I could figure out in the time I was willing to invest. I think if you upgrade you account you can.

<div class="wp-block-image">
  <figure class="alignleft is-resized"><img src="http://localhost:8080/wp-content/uploads/2018/10/check.png" alt="" class="wp-image-236" width="36" height="36" /></figure>
</div>

Self Hosted, Easy to Update, Follows Web Best Practices, Themed, Database driven, Multi-User  


<div class="wp-block-image">
  <figure class="alignleft is-resized"><img src="https://ttech.mamacos.media/wp-content/uploads/2018/10/Cross.png" alt="" class="wp-image-237" width="34" height="34" /></figure>
</div>

SSL, Small and Fast.



Not doing too bad at the moment, only two things remaining on my little check lists, or at least I thought!

The lists of things started then, getting it hosted on domain, making it load faster than it was, getting **SSL** up and running, and getting a nice book type read to it. So just a couple things 🙂

I got a Domain setup pretty quickly using **[AWS Route 53](https://aws.amazon.com/route53/)**, the hardest part was waiting 5 minutes, for it to come up.

<div class="wp-block-image">
  <figure class="alignleft is-resized"><img src="https://ttech.mamacos.media/wp-content/uploads/2018/10/lets.png" alt="" class="wp-image-244" width="114" height="94" /></figure>
</div>

**SSL** took me a while but using **[LetsEncrypt](https://letsencrypt.org/)** [](https://letsencrypt.org/), a very cool project to provide safe and free SSL certificates to encrypt all the things, and following a guide [here](https://medium.com/unicorn-supplies/ssl-for-aws-lightsail-wordpress-8053359a774f)&nbsp;got me over the line.

There were a ton of amazing plugins that I played with along the way, but I really enjoyed a few that pushed some new technologies that I was interested in into the blog.

**Yeost SEO, Glue for Yeost SEO and AMP, Amazon Polly, All-in-One WP Migration, All In One SEO Pack, WP Mail SMTP**.  


<div class="wp-block-image">
  <figure class="alignleft is-resized"><img src="https://ttech.mamacos.media/wp-content/uploads/2018/10/Analytics.png" alt="" class="wp-image-240" width="221" height="72" /></figure>
</div>

<div class="wp-block-image">
  <figure class="aligncenter is-resized"><img src="https://ttech.mamacos.media/wp-content/uploads/2018/10/Analytics2.png" alt="" class="wp-image-241" width="210" height="115" srcset="http://localhost:8080/wp-content/uploads/2018/10/Analytics2.png 456w, http://localhost:8080/wp-content/uploads/2018/10/Analytics2-300x164.png 300w" sizes="(max-width: 210px) 100vw, 210px" /></figure>
</div>

Getting **Google Analytics** up was a good idea, mostly makes me cry, but a good idea none the less. I think this was all through **Yeost SEO**, but I used a few along the way.

<div class="wp-block-image">
  <figure class="alignleft"><img src="https://ttech.mamacos.media/wp-content/uploads/2018/10/AMP.png" alt="" class="wp-image-242" /></figure>
</div>

The most fascinating time sink was **[AMP](https://www.ampproject.org/)** [](https://www.ampproject.org/)and getting that to work. It&#8217;s a special technology developed by Google to make pages load really quickly. Similar to Facebook Instant Articles. 

I used almost all the plugins I could find for WordPress and eventually settled on a defunct AMP one, but have since converted to **Glue for Yeost SEO and AMP**.

<div class="wp-block-image">
  <figure class="alignright"><img src="https://ttech.mamacos.media/wp-content/uploads/2018/10/Polly.png" alt="" class="wp-image-243" /></figure>
</div>

[Amazon Polly](https://aws.amazon.com/polly/) transcription was pretty easy to integrate and I find it fun listening to her drone my own words back at me, so much so that I&#8217;ve left it enabled 🙂 I really liked that it uploads the article **MP3**&#8216;s into a **[AWS S3 Bucket](https://aws.amazon.com/s3/)** [](https://aws.amazon.com/s3/)which it can then pull them from just as MP3 files!

## Where too from here ?<figure class="wp-block-image">

<img src="https://ttech.mamacos.media/wp-content/uploads/2018/10/TTech.png" alt="" class="wp-image-239" srcset="http://localhost:8080/wp-content/uploads/2018/10/TTech.png 1076w, http://localhost:8080/wp-content/uploads/2018/10/TTech-300x243.png 300w, http://localhost:8080/wp-content/uploads/2018/10/TTech-768x622.png 768w, http://localhost:8080/wp-content/uploads/2018/10/TTech-1024x829.png 1024w" sizes="(max-width: 1076px) 100vw, 1076px" /> </figure> 

I think the site looks pretty good now, has a few good features and mostly gets out the way to let me write new content quickly and get it out there.

## What&#8217;s in store for the future ?

I think that cool changes are coming soon, from the new [Gutenberg editor for WordPress](https://wordpress.org/gutenberg/) which I&#8217;m finding really cool after a few tries using it. To the new [Headless CMS](https://medium.com/tech-tajawal/why-headless-cms-is-becoming-so-popular-57d262b1e096) movement, which is a bit of a off shoot of the whole React Website with a API / Database sitting behind it.

I am honestly still tempted to roll my own, but that&#8217;s offset to let me rather keep exploring and sharing new technologies and my first forays into them.

I hope you enjoy the articles and potentially set up you own blog or experiment with something you learnt here.