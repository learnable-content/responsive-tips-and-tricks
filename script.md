# Creating responsive full screen background video - part 2 - VIDEO SCRIPT

G'day, My name is Russ Weakley from Max Design.

In this second video, we will look at how to add background video to specific areas of your web page, rather than the entire page.

The first thing we are going to do is move the "video-container" element up inside the banner element.

We also need to add a new class to the content container inside the banner. The class is gonig to be called "banner-content".

Now before we start styling these element, we need to understand the stacking order that we need to create.

At the back is the banner itself. As we are absolutely positioning elements inside the banner, we need to give this element position-relative. now this means that child elements will be positioned relative to this banner.

On top of this element is the "video-container". This is set to position absolute and and we're going to spread out the the full width and height of the banner.

On top of this is the VIDEO itself, which is again going to be positioned absolute, 

and again, it's going to spread out to the full width and height of the, in this case of the "video-container".

On top of this is the "video-mask". Again, "position: absolute" and again, spread out to the full width and height of the "video-container".

And finally, on top of all of these elements is going to be the "banner-content".

Now, we're going to give the banner "position: relative" rather than absolute positioning. And the rason is that we want the element in normal flow.

If we set absolute positioning on this element, the entire banner will now be positioned out off the page, and the rest of the page content below will alide up underneath the banner and be hidden.

Now for this example, we don't actually need z-index to control the stacking order. The reason is that if none of these elements have z-index, they will be positioned in stacking order based on the order that they are written in the HTML file. 

So, the later thay are written in the HTML file, the higher they are in stack order.

Let's start styling.

First of all, we need to add some new rules to the banner. We going set it to "positioning: relative", "overflow: hidden" and a "min-height" - in this case "290px". 

Now, this is just in case the content becomes shorter in the future and the banner then does not have enough height.

Next up we need to style the "video-container". We can set this with "position: absolute".

now we need to put it in the top left corner of the "banner" so we set it to "top: 0" and "left: 0".

We also need to set the width and height to 100%, so it spreads to the full width and height of the banner.

And, as before, we can add a background-image as a fallback.

And we can set the background-size to "cover"

Next up, we can style the video element itself using a selector of ".video-container video".

As before, we can set it with "position: absolute", "top: 0", "left: 0". WE can also set the min-width and min-height to "100%". 

Now, if we reload in the browser, as you can see that the video is now being cut off. Ideally, we want to center the video inside the video-container. And we can do this in two steps.

First of all, we need to set the left and top values to 50%. Now this is going to move the top left corner of the VIDEO into the center of the "video-container" element.

And now whatwe need to do is to shift the VIDEO back across to the left and top. And we can do this using the "transform" property. The first version is "webkit-transform", and the value is "translate". Inside the brackets we need to add an "x" and "y" value separated by a comma. 

In both cases, we're going to set them to "-50%". That will move it back to the left -50 and up -50.

Now we can copy this declaration again, and simply take off the "webkit" prefix.

Now, if we look in the browser, you can see that the video is now centred.

For the "video-mask" container, we're going to set it to "position: absolute", "left: 0", "top: 0", "min-width: 100%, "min-height: 100%". And then we're going to add a background.

Now instrad of using a background-color and opacity like we did in the last example, we're going to use a background-image. And that will allow us to create a nice little screen effect.

If we look in the browser, you can see that the video is now softer and there is a nice screen texture over the top.


Finally, we need to get the "banner-content" on top of all of these layers. And, we can do this by creating a class of "banner-content". And this can be set with "position: relative".

Let's have a look in a browser. And if we reload you can see that the "banner-content" is now sitting on top of the video.

So, there you have it. A quick demonstration of how to create responsive background videos inside specific elements.