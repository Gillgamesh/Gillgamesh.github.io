---
layout: post
title: "Stop Saving Images to Disk."
description: "Seriously, we really don't need to do that, like, ever."
date: 2019-10-30
tags: python
comments: true
---

One of my biggest pet peeves when working with people on projects that involve proccessing images from a user or from one library/API to another, is when files end up getting saved to disk.

For example, say you're working on a Python project that uses a PIL-based image structure (say from a webcam screenshot) to another format, like an Azure/AWS/Google Cloud-based API for some sort of computer vision task, that uses an alternate format.
There's effectively three different approaches that you can take:

* Hope there's some sort of direct conversion provided by one of the libraries you're using, or an indirect one throw numpy RGB arrays or PIL images.
* Do the conversions yourself, probably through numpy arrays.
* Save the files in some intermediete format like PNG or PPM, then re-read it through the second system.


While the first two approaches are preffered in a lot of cases for being more direct, sometimes you'll have to do number 3, or it will otherwise make sense. For example, if you have a PIL/numpy formatted image, and you want to pass it up to the Google Cloud Vision API, they (and your bandwidth usage) would like you to send decently compressed JPEGs over, so you need to do the conversion somehow.

On initial glance, I've noticed a lot of the time people will just save the file to disk, then re-open it, because it works and is probably fast enough. However, outside of even speed, saving files to disk even temporarily is annoying--you have to worry about deleting them, worry about name uniqueness, overwriting, local R/W permissions, where you run the program, etc. So while it may look briefer on initial impression, it'll just be a lot more work for you.

So here's a small example, mainly for my future Hackathon buddies, so I can take a nap instead of deciding to make a big deal of this overall small issue if I'm forced to notice it.

Say you want to save an image to file, say one named `file` then send it over. The saving part in Pillow and loading with the vision library would be something like this:
```python
image_obj.save(file, "JPEG") # save the image to disk

# .....

with io.open(filename, 'rb') as image_file:
    content = image_file.read()

image = vision.types.Image(content=content)
```

However, you can avoid saving to disk by using either a `BytesIO` or `StringIO` buffer, which avoids all the problems we discussed earlier:


```python

buf = io.BytesIO()
image_obj.save(buf, "JPEG") # save into a BUFFER, which acts mostly like a file in Python* except it's actually in memory
image = vision.types.Image(content=buf.getvalue()) # now instead of reading the content from the saved file, you do it directly from the buffer, in the correct format to upload to the API, etc.


```
