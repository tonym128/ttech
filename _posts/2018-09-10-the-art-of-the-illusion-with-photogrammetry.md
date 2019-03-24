---
id: 180
title: The art of the illusion with photogrammetry
date: 2018-09-10T23:42:22+00:00
author: tony
layout: post
guid: http://ttech.mamacos.media/?p=180
ampforwp_custom_content_editor:
  - ""
ampforwp_custom_content_editor_checkbox:
  - ""
ampforwp-amp-on-off:
  - default
amazon_polly_audio_link_location:
  - https://s3.us-east-1.amazonaws.com/audio-for-wordpress-17069432435aa889ef033eb26aa48aa297fdf8f7/2018/09/amazon_polly_180.mp3?version=1536828998
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
    
    The art of the illusion with photogrammetry. **AMAZONPOLLY*SSML*BREAK*time=***1s***SSML**  **AMAZONPOLLY*SSML*BREAK*time=***1s***SSML**
    The Problem
    This was one of the most amazing finds of the last year for me. As someone with no real classical artistic talent, I find the idea of taking real world assets and getting them into computers fascinating.
    There are many different ways of doing this and processes for it. There is a way of animating called Rotoscoping in which you take a stream of pictures and trace movement to get a life like feel for animation.
    Image: horse. Rotoscoping
    There is cel shading which is the idea of taking an image and transforming it into something that looks more two dimensional and flat.
    Image: Toon-shader.
    Of all of them, the most magical to me has always been photogrammetry.
    Photogrammetry is the science of making measurements from photographs, especially for recovering the exact positions of surface points. Photogrammetry is as old as modern photography, dating to the mid-19th century and in the simplest example, the distance between two points that lie on a plane parallel to the photographic image plane, can be determined by measuring their distance on the image, if the scale (s) of the image is known.
    In 2008 Microsoft released a service in beta called PhotoSynth. I recall the service being deemed as the next big thing in Photography and it was truly magical, given enough two dimensional normal camera photographs it would calculate a 3d point cloud which could be used to model the images in 3d space, much like 100's of Minecraft blocks. There was an idea, that one day, you would be able to take you one photo and with the massive resources of PhotoSynth behind you, you could augment your photo's and have them turn into 3d models.
    I took my ~200 photo's of a statue in Cannizaro Park of Dianna and the Fawn and I turned these photo's into the most amazing 3d model, which I could spin around and view from absolutely any angle, it was like magic.
    Image: Photosynth2011Synth. PhotoSynth
    Unfortunately this was not to last and the service got degraded in time, to be a (very good) photo stitching service.
    The problem was with this service gone, there was no easy way for me to take my beautiful flat 2d images and turn them into a fantastical amazing model and they sat, dormant, sad and unanimated since 2010.
    Image: Cannizaro Park 023. Diana and the Fawn
    The Solution
    Fast forward to a week ago and I found a wonderful program called Meshroom by Alice Vision.
    Image: anim-meshroom-once.gif.Meshroom
    This program promised the same goodness as Microsofts PhotoSynth, but all run locally using the power of your single local computer.
    I was able to bring my images back to life using Meshroom and Blender.
    Image: Logo_Blender.svg.Blender
    And following an amazing video by CG Geek.
    Loading my ~200  images into Meshroom with default setting and hitting go resulted in a lot of waiting, but a pretty spectacular result.
    Image: photos.jpg. A small sub section of the images
    Image: Meshroom. Loaded into Meshroom
    And two hours later I had a 3d model with texture mapped onto all created from my 2d images.
    There's a couple things that are important using this technology :
    Good high quality images, without blurA camera which is known by Meshroom or willing to add it.About 60% overlap between photos to allow the algorithm to workWillingness to learn a bit of Blender (which was pretty complicated for me)Patience
    The most rewarding part of this project for me was the ability to bring back to life my photo's from a previous project of mine, they were uploaded to Google Photo's at some point and there they have sat for 8 years. They are stored using the free version which does introduce some additional compression, but they seem to have weathered time well enough.
    Once I imported the Obj Model from Meshroom into Blender I was greeted with a lot of complicated screens and information.
    Image: Blender2.JPG.
    There a 3D Model which included some of the surroundings and 4 texture atlasses for the scene which is essentially a flat texture with information for how to project it onto your model, kind of like throwing a carpet over a manequin but doing it in a specific way everytime to end up with the same result.
    I was very pleased with the model.
    Image: WireFrame.JPG. 3D Wireframe Model
    And the texture look wasn't looking too bad either
    Image: Textured.JPG. Textured in Blender
    Unfortunately my final rendered output was looking like it was in need of a bit of attention.
    Image: Dianna 1.JPG. A very cement look and a lot of additional scenery
    I was able to animate this and get a result out into video, which I was very pleased with
    But there was more work to be done, the grounds around the statue didn't look very good, but it was a quick step to remove all that additional scenery and put some lights into the scene to polish it up.
    Since I had taken these photos in normal daylight without a flash, the idea was to light the model up as evenly as possible, but not introduce any new shadows, which was just a check box inside Blender for the lights.
    And this took me to my final output
    This video is a more dynamic pan around to show that I can now view any angle  I want, and while it is a little too shiny still, it does represent the statue much better now.
    Where to from here
    The next steps for me are to see if Meshroom can map an indoor area properly with better photo's. Indoors pose a unique problem that a lot of these algorithms work on the texture or object to work out how they are moving in a scene and single colour painted walls do not represent well, so you need to have interesting rooms if you hope for this to succeed.
    I think it is amazing how far this technology has come, and what you can now do with Open Source projects which are out in the wild for anyone to try. I'm quite keen to see about how much of my world I can map.
    With mapping technology like Google Maps and Bing Maps, how long is it until they can apply this to our StreetView photos and give us a literal like for like 3D View of what we would see and could walk around.
    How much more immersive would Google Earth be with technology like this behind it ?
    They are using similar technology already, but if you could source ground level data, this could essentially turn our whole world Virtual.
    Imagine deciding to play Grand Theft Auto or Just Cause and choosing your last holiday as the location or your local neighbourhood, because no longer are the artists going to be constrained by the environment, they're going to focus on making dynamic stories which adapt to the environment you choose to play in.
    We're not quite there yet, but how about Tower Defence on Google Maps
amazon_polly_transcript_source_lan:
  - en
ampforwp-redirection-on-off:
  - enable
image: /wp-content/uploads/2018/09/Textured.jpg
categories:
  - Uncategorized
tags:
  - 3d
  - blender
  - github
  - gpu
  - graphics
  - meshroom
  - photogrammetry
  - programming
---
## The Problem 

This was one of the most amazing finds of the last year for me. As someone with no real classical artistic talent, I find the idea of taking real world assets and getting them into computers fascinating. 

There are many different ways of doing this and processes for it. There is a way of animating called [Rotoscoping](https://en.wikipedia.org/wiki/Rotoscoping) in which you take a stream of pictures and trace movement to get a life like feel for animation. 

<div class="wp-block-image">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/horse.gif" alt="horse" class="wp-image-183" /><figcaption> Rotoscoping </figcaption></figure>
</div>

There is [cel shading](https://en.wikipedia.org/wiki/Cel_shading) which is the idea of taking an image and transforming it into something that looks more two dimensional and flat.

<div class="wp-block-image">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/Toon-shader.jpg" alt="Toon-shader" class="wp-image-184" srcset="http://localhost:8080/wp-content/uploads/2018/09/Toon-shader.jpg 312w, http://localhost:8080/wp-content/uploads/2018/09/Toon-shader-300x231.jpg 300w" sizes="(max-width: 312px) 100vw, 312px" /></figure>
</div>

Of all of them, the most magical to me has always been [photogrammetry](https://en.wikipedia.org/wiki/Photogrammetry). 

<blockquote class="wp-block-quote">
  <p>
    <strong>Photogrammetry</strong> is the science of making measurements from photographs, especially for recovering the exact positions of surface points. Photogrammetry is as old as modern <a href="https://en.wikipedia.org/wiki/Photography">photography</a>, dating to the mid-19th century and in the simplest example, the distance between two points that lie on a plane parallel to the photographic <a href="https://en.wikipedia.org/wiki/Image_plane">image plane</a>, can be determined by measuring their distance on the image, if the <a href="https://en.wikipedia.org/wiki/Scale_(map)">scale</a> (<em>s</em>) of the image is known.
  </p>
  
  <cite>https://en.wikipedia.org/wiki/Photogrammetry<br type="_moz" /></cite>
</blockquote>

In 2008 Microsoft released a service in beta called [PhotoSynth](https://en.wikipedia.org/wiki/Photosynth). I recall the service being deemed as the next big thing in Photography and it was truly magical, given enough two dimensional normal camera photographs it would calculate a 3d point cloud which could be used to model the images in 3d space, much like 100&#8217;s of Minecraft blocks. There was an idea, that one day, you would be able to take you one photo and with the massive resources of PhotoSynth behind you, you could augment your photo&#8217;s and have them turn into 3d models. 

I took my ~200 photo&#8217;s of a statue in Cannizaro Park of [Dianna and the Fawn](https://historicengland.org.uk/listing/the-list/list-entry/1286374) and I turned these photo&#8217;s into the most amazing 3d model, which I could spin around and view from absolutely any angle, it was like magic. 

<div class="wp-block-image">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/Photosynth2011Synth.jpg" alt="Photosynth2011Synth" class="wp-image-185" srcset="http://localhost:8080/wp-content/uploads/2018/09/Photosynth2011Synth.jpg 385w, http://localhost:8080/wp-content/uploads/2018/09/Photosynth2011Synth-300x202.jpg 300w" sizes="(max-width: 385px) 100vw, 385px" /><figcaption> PhotoSynth </figcaption></figure>
</div>

Unfortunately this was not to last and the service got degraded in time, to be a (very good) photo stitching service.

The problem was with this service gone, there was no easy way for me to take my beautiful flat 2d images and turn them into a fantastical amazing model and they sat, dormant, sad and unanimated since 2010.

<div class="wp-block-image">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/Cannizaro-Park-023.jpg" alt="Cannizaro Park 023" class="wp-image-186" srcset="http://localhost:8080/wp-content/uploads/2018/09/Cannizaro-Park-023.jpg 800w, http://localhost:8080/wp-content/uploads/2018/09/Cannizaro-Park-023-300x200.jpg 300w, http://localhost:8080/wp-content/uploads/2018/09/Cannizaro-Park-023-768x512.jpg 768w" sizes="(max-width: 800px) 100vw, 800px" /><figcaption> Diana and the Fawn </figcaption></figure>
</div>

## The Solution

Fast forward to a week ago and I found a wonderful program called [Meshroom](https://alicevision.github.io/) by Alice Vision. 

<div class="wp-block-image">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/anim-meshroom-once.gif" alt="anim-meshroom-once.gif" class="wp-image-187" /><figcaption>Meshroom</figcaption></figure>
</div>

This program promised the same goodness as Microsofts PhotoSynth, but all run locally using the power of your single local computer.

I was able to bring my images back to life using Meshroom and Blender.

<div class="wp-block-image">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/Logo_Blender.svg_.png" alt="Logo_Blender.svg" class="wp-image-188" srcset="http://localhost:8080/wp-content/uploads/2018/09/Logo_Blender.svg_.png 2000w, http://localhost:8080/wp-content/uploads/2018/09/Logo_Blender.svg_-300x79.png 300w, http://localhost:8080/wp-content/uploads/2018/09/Logo_Blender.svg_-768x202.png 768w, http://localhost:8080/wp-content/uploads/2018/09/Logo_Blender.svg_-1024x269.png 1024w, http://localhost:8080/wp-content/uploads/2018/09/Logo_Blender.svg_-1568x412.png 1568w" sizes="(max-width: 2000px) 100vw, 2000px" /><figcaption>Blender</figcaption></figure>
</div>

And following an amazing video by [CG Geek](https://www.youtube.com/channel/UCG8AxMVa6eutIGxrdnDxWpQ). <figure class="wp-block-embed-youtube wp-block-embed is-type-video is-provider-youtube"> </figure> 

Loading my ~200 images into Meshroom with default setting and hitting go resulted in a lot of waiting, but a pretty spectacular result.  


<div class="wp-block-image alignnone size-full wp-image-189">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/photos.jpg" alt="photos.jpg" class="wp-image-189" srcset="http://localhost:8080/wp-content/uploads/2018/09/photos.jpg 800w, http://localhost:8080/wp-content/uploads/2018/09/photos-300x112.jpg 300w, http://localhost:8080/wp-content/uploads/2018/09/photos-768x286.jpg 768w" sizes="(max-width: 800px) 100vw, 800px" /><figcaption> A small sub section of the images</figcaption></figure>
</div>

<div class="wp-block-image alignnone size-full wp-image-190">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/Meshroom.jpg" alt="Meshroom" class="wp-image-190" srcset="http://localhost:8080/wp-content/uploads/2018/09/Meshroom.jpg 1282w, http://localhost:8080/wp-content/uploads/2018/09/Meshroom-300x176.jpg 300w, http://localhost:8080/wp-content/uploads/2018/09/Meshroom-768x450.jpg 768w, http://localhost:8080/wp-content/uploads/2018/09/Meshroom-1024x601.jpg 1024w" sizes="(max-width: 1282px) 100vw, 1282px" /><figcaption> Loaded into Meshroom</figcaption></figure>
</div>

And two hours later I had a 3d model with texture mapped onto all created from my 2d images.

There&#8217;s a couple things that are important using this technology :

  * Good high quality images, without blur
  * A camera which is known by Meshroom or willing to add it.
  * About 60% overlap between photos to allow the algorithm to work
  * Willingness to learn a bit of Blender (which was pretty complicated for me)
  * Patience

The most rewarding part of this project for me was the ability to bring back to life my photo&#8217;s from a previous project of mine, they were uploaded to Google Photo&#8217;s at some point and there they have sat for 8 years. They are stored using the free version which does introduce some additional compression, but they seem to have weathered time well enough.

Once I imported the Obj Model from Meshroom into Blender I was greeted with a lot of complicated screens and information.

<div class="wp-block-image">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/Blender2.jpg" alt="Blender2.JPG" class="wp-image-191" srcset="http://localhost:8080/wp-content/uploads/2018/09/Blender2.jpg 1903w, http://localhost:8080/wp-content/uploads/2018/09/Blender2-300x155.jpg 300w, http://localhost:8080/wp-content/uploads/2018/09/Blender2-768x396.jpg 768w, http://localhost:8080/wp-content/uploads/2018/09/Blender2-1024x528.jpg 1024w, http://localhost:8080/wp-content/uploads/2018/09/Blender2-1568x809.jpg 1568w" sizes="(max-width: 1903px) 100vw, 1903px" /></figure>
</div>

There a 3D Model which included some of the surroundings and 4 texture atlasses for the scene which is essentially a flat texture with information for how to project it onto your model, kind of like throwing a carpet over a manequin but doing it in a specific way everytime to end up with the same result.

I was very pleased with the model.

<div class="wp-block-image alignnone size-full wp-image-195">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/WireFrame.jpg" alt="WireFrame.JPG" class="wp-image-195" srcset="http://localhost:8080/wp-content/uploads/2018/09/WireFrame.jpg 781w, http://localhost:8080/wp-content/uploads/2018/09/WireFrame-297x300.jpg 297w, http://localhost:8080/wp-content/uploads/2018/09/WireFrame-768x777.jpg 768w" sizes="(max-width: 781px) 100vw, 781px" /><figcaption> 3D Wireframe Model</figcaption></figure>
</div>

And the texture look wasn&#8217;t looking too bad either

<div class="wp-block-image alignnone size-full wp-image-196">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/Textured.jpg" alt="Textured.JPG" class="wp-image-196" srcset="http://localhost:8080/wp-content/uploads/2018/09/Textured.jpg 748w, http://localhost:8080/wp-content/uploads/2018/09/Textured-282x300.jpg 282w" sizes="(max-width: 748px) 100vw, 748px" /><figcaption> Textured in Blender</figcaption></figure>
</div>

Unfortunately my final rendered output was looking like it was in need of a bit of attention.

<div class="wp-block-image alignnone size-full wp-image-192">
  <figure class="aligncenter"><img src="http://localhost:8080/wp-content/uploads/2018/09/Dianna-1.jpg" alt="Dianna 1.JPG" class="wp-image-192" srcset="http://localhost:8080/wp-content/uploads/2018/09/Dianna-1.jpg 955w, http://localhost:8080/wp-content/uploads/2018/09/Dianna-1-300x172.jpg 300w, http://localhost:8080/wp-content/uploads/2018/09/Dianna-1-768x440.jpg 768w" sizes="(max-width: 955px) 100vw, 955px" /><figcaption> A very cement look and a lot of additional scenery</figcaption></figure>
</div>

I was able to animate this and get a result out into video, which I was very pleased with<figure class="wp-block-embed-youtube wp-block-embed is-type-video is-provider-youtube"> </figure> 

But there was more work to be done, the grounds around the statue didn&#8217;t look very good, but it was a quick step to remove all that additional scenery and put some lights into the scene to polish it up.

Since I had taken these photos in normal daylight without a flash, the idea was to light the model up as evenly as possible, but not introduce any new shadows, which was just a check box inside Blender for the lights.

And this took me to my final output<figure class="wp-block-embed-youtube wp-block-embed is-type-video is-provider-youtube"> </figure> 

This video is a more dynamic pan around to show that I can now view any angle  I want, and while it is a little too shiny still, it does represent the statue much better now.

## Where to from here

The next steps for me are to see if Meshroom can map an indoor area properly with better photo&#8217;s. Indoors pose a unique problem that a lot of these algorithms work on the texture or object to work out how they are moving in a scene and single colour painted walls do not represent well, so you need to have interesting rooms if you hope for this to succeed.

I think it is amazing how far this technology has come, and what you can now do with Open Source projects which are out in the wild for anyone to try. I&#8217;m quite keen to see about how much of my world I can map.

With mapping technology like Google Maps and Bing Maps, how long is it until they can apply this to our StreetView photos and give us a literal like for like 3D View of what we would see and could walk around.

How much more immersive would Google Earth be with technology like this behind it ?

They are using similar technology already, but if you could source ground level data, this could essentially turn our whole world Virtual.

Imagine deciding to play Grand Theft Auto or Just Cause and choosing your last holiday as the location or your local neighbourhood, because no longer are the artists going to be constrained by the environment, they&#8217;re going to focus on making dynamic stories which adapt to the environment you choose to play in.

We&#8217;re not quite there yet, but how about [Tower Defence on Google Maps](https://www.mapstd.com/)