---
layout: post
title: sv-glide Web Component
---

This component allows you to make a quick Ux element composed of two svg triangles that you can customize a bit.  Hover over the element and they "glide" away revealing your custom background image or gif that may also be used as a link!  Need a bit of text to describe your element, certainly!

### Customizable attributes include:
  - `<sv-glide>` element Height and Width
  - Triangle left color, Triangle right color
  - Background image URL
  - `<a>` tag `href` attribute
  - A block of text

### To use the web component:
Grab the file for [svg-glide](http://iam.colum.edu/students/maria.faulisi/ewt/svGlide/svGlideTest.html) and use the html import in the head of your document to link to the file like so:

{% highlight html %}
<head>
<link rel="import" href="svGlide.html">
</head>
{% endhighlight html %}

Currently there is only one way to configure the component:
{% highlight html %}
<sv-glide
    data-background = "url(//ImALinkJustLikeYouUseInCSS)"
    data-link = "placeThePathAsYouWouldInsideOfAnAnchorTagHref"
    data-svgWidth = "Numberpx"
    data-svgHeight = "Numberpx"
    data-leftFill = "color"
    data-rightFill = "color"> //end of opening tag
    
        <span class = "words">Your Text Here.</span>
    </sv-glide> //closing tag
{% endhighlight html %}

### Notes

Things to keep in mind:

* The `data-svgWidth` and `data-svgHeight` must be in px format.
* `data-leftFill` and `data-rightFill` can be in any acceptable CSS format. (ie: hexcode, rgb, rgba, color name).
* You do not have to use a span tag, any tag for text will work but you do need to assign the tag the class "words".
* You do not need to include text or a link.

**Enjoy!**

