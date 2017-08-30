# Creating responsive full screen background video - part 1 - VIDEO SCRIPT

G'day, My name is Russ Weakley from Max Design

Over two short videos, I am going to show you how to add HTML5 video as a backgrounds to web pages.

In this first video, we will look at the HTML5 VIDEO element, and also how to add background video across the entire page.

In the second video, we going to look at how to add background video to specific areas of your web page.

Let's start with a quick look at the VIDEO element.

Now, HTML5 video allows us to add video into our web pages - without the need for external plugins - like Flash, RealPlayer.

The VIDEO element is supported by all modern browsers including IE9 and upwards. It is also supported by iOS and Android browsers. It is not supported by Opera Mini at this point.

Now, We can write the VIDEO using the VIDEO start tag and VIDEO end tag.

And with this VIDEO element, we can add a range of different attributes. 

For example, we could add a SOURCE attribute, but we are going to use a different method of applying video source, so we won't use this attribute.

The CONTROLS attribute allows us to add browser default controls to the video. Now, the controls attribute must always be included if you want your users to be able to interact with the video.

In our case, as we will be adding the video as a background, we do not need this attribute.

The PRELOAD attribute allows you to preload video. Now we're not going to use that in this case as we have just one large background video.

The AUTOPLAY attribute allows us to autoplay video. Now, we're going to use this attribute as it allows the video to play in the background automatically.

The LOOP attribute allows you to loop or continuous play video. Now, we will using this attribute as it will allow the video to continuously loop in the background.

The MUTED attribute allows us to define if the video is muted or not. Basically, will it play audio. Now, we will add this attribute as we do not want any audio to play with the background video.

The POSTER attribute points to an image that is visible sometimes before or after the video is played.

The WIDTH and HEIGHT attributes can also be applied to the VIDEO element, but in our case we do not want these attributes as we want to stretch the video to fit the entire viewport.

Next up, we need to add the SOURCE element. Now, this element allows us to specify multiple media resources inside the VIDEO element.

But why do we need multiple resources? Well, different browsers support different video formats. To make sure our video can play across a wide range of browsers, we need to include at least two different types or two different versions of the video. And they are MP4 and WEBM.

We can start by adding the MP4 video. First we add the source element, and then the src attribute which points to our video. We also need to include the type attribute, and set the value to video/mp4.

And then we can add the WEBM video. So, we can copy and paste the one from above, and change the file extension to webm and the type will be video/webm

But what about older browsers that do not support the VIDEO element? Well, in our case, as we are only using the video as a decorative background, we do not need to worry too much. However, we're still going to add a "still" background image behind the video.

Let's take a quick look in the browser. And if we reload you can see, the video can be seen if we scroll down.

But now we need to move it behind our page. We can do this using CSS.

First of all, we need to write a rule for our container, and the class is ""video-container".

Then, we need to set this container to "position: absolute" which will take it out of normal flow and yup off the page.

We then need to set the z-index to it needs to be a minus number so the video will set behind the page content.

Then, we need to stretch our container to the full width and height of the viewport.

We also need to set "overflow: hidden" so that no scrollbars appear when we add the video.

And, we're going to give the container a background-image, as a fallback for browsers that do not support the video element. 

Now, when we are setting the background-image we should set the background-size to cover, so that the image spreads across the element.

Now to style the VIDEO element, the selector will be video-container space video.

We need to set this video to "position: absolute", and position it in the top left corner of the parent element.

Then we need to make sure it stretches out to fit the width of the parent container.

Let's take a look in the browser. Now as you can see, the video is now sitting nicely behind the content. It is also playing automatically.

However, the video looks very bright and it's quite distracting. As this is a background, we really want it to be softer.

Rather than going and editing the video itself, we can solve this by adding a mask over the top of the video.

So, we need to add a new element into our HTML file, inside the video-container element. It will be an empty DIV with a class of "video-mask".

Next we need to style this element. To save time, we can copy the video ruleset from above, and change some of the declarations.

The class is going to be "video-mask".

Then we need to set the background to black and we're going to set the opacity to .5.

So, this mask container is sitting over the top of our video and it's going to have a black background which is semi-transparent.

Now, this mask is really handy thing. It means we can quickly change the background color or opacity as needed - without having to touch the actual video files.

Let's take a look in the browser. 

Now as you can see, the banner text color is really hard to read. so, we can quickly change this to white.

Back in our CSS file, we can scroll up to the ".banner" and we can change the color to white.

Now if we reload again you can see the banner text is now clearly visible. 

Now, if we move the viewport in, you can see that the video resizes as needed.

Now, you could choose to hide this VIDEO element entirely at small screen sizes if you were worried about mobiles and bandwidth. These devices could be given a specific background-image instead. It's entirely up to you.

So, there you have it. A very quick demo showing how to create responsive full screen background videos.

In the next movie we will look at applying background video to specific elements rather than the entire page.

END