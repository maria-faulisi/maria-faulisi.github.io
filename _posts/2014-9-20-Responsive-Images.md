---
layout: post
title: Responsive Images!
---

##What are they and why do I need 'em?

When you surf the web, how big is your board (size of your screen)?  Do you surf using your phone?  What about your neighbors tablet, or your mom's Gateway computer desktop?  Think of all the screens you've ever viewed a web page on (go ahead, I'll wait).  Okay now think about all the times you've waited patiently for images to load on any of those devices, remember how sad it made you?  Yea, well you've just thought about why we need responsive images.  We need them to help us enjoy what we see no matter how we're seeing it and to see it as quickly and efficiently as possible.


##Okay so let's use them you say?

The problem is that for every device you use to surf, you also have a different browser serving up those hot-n-ready web pages, and while they are getting better and better, they still don't officially support responsive images.  Which means awesome web developers must hack the browser's current capabilities to get you what you need. Currently, we have two options: CSS media queries and an new element on the brink of browser support, the picture element which uses a picture tag. (This is a well developed JavaScript solution from [The Responsive Images Community Group](http://www.responsiveimages.org).

So let's look at our CSS solution.  In CSS we need to use the `@media` query to notify the browser that you need to swap out an image (currently only works on background images) if it is within your specification.

```
@media(min-width: 768px){
  background-image: url('medium-image.jpg');
}
```

Here we've said that we want to use the medium-image.jpg when the screen size has a minimum width of 768px.

To use the picture element, we must use an html shiv: 


```
<script>
document.createElement('picture');
</script>
```


and import the picturefill.js `<script>` placing both in the `<header>` of our html file.

Inside of our html, we can now use regular images rather than background images that change according to our specification.  We wrap the `<img>` in a `<picture>` tag which uses the `<img>` as a fall back and allows us to use a `<source>` tag with it's media attribute in the same way we used `@media` in CSS.  It sounds hairy, but makes sense when you see it. (Look below)


```
<picture>
  <source media="(min-width: 768)" srcset="medium-image.jpg"></source>
  <img srcset="fullImage-size.jpg" alt="Wish I had right sized image">
</picture>
```


Now you can enjoy serving up the right image for the board (device) you're surfing with.  You're using data wisely and your viewers will be happy cuz they can see what they want as quickly and efficently as possible.  Way to go!  You're awesome ;)
