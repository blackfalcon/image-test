# hi dpi vs standard res

The last part of the designer in me just officially died 

### The point of this exercise 

Image quality and clarity has been something of a mystery to me as I do not actually have to deal with pixel based image assets in my day to day work. Nearly all of my visuals are created using CSS. This left we with a hole of understanding. 

What is presented in this repo is a series of, now proven in my mind, techniques for displaying quality assets to different resolution devices. 

### The result of the exercise 

The end result is that dpi has no baring on quality of an asset at all between standard and hi-def devices. In the end, it is the density of the device pixels and if the asset matches up to that density. Regardless of the dpi of the asset, it is it's ability to match the hardware pixel density that will define it's clarity. 

To prove this point, in the example view there is a Star Wars poster. This asset has a physical width of 800x1123 and a dpi of 10px. Really, 10px. Using the HTML attribute of width I am resizing the asset to 400px wide. Saving this file with no jpg compression produced an asset that is 858k. 

The second Star Wars image is the same 800x1123 with a default of 72dpi from Photoshop, but this time using 100% image compression. That's right, I moved the slider all the way over. The end result was an image asset size of 66k. That is a almost a 93% reduction file size. And the quality, I will let you decide. 

### What does this mean for responsive?

This is an interesting question. In this scenario, "responsive" is in the context of responding to the resolution of a device, not the size of the device or the speed in which a device and download an asset. But what this is telling me is that if you can get a relatively large full color image to look really good on a hi-dpi device and it's physical size is only 66k, that's pretty damn good. 

An average handheld device download is say 3 megabit per/sec, that roughly equates to 375k per/sec (don't flame me on the math), so I say using this process you can use the same physical asset for low-res, hi-res and mobile devices. 