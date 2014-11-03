---
layout: post
title: Web Components
---

Ok, so this is a difficult topic to wrap the noggin around.  But I think I have the gist, and I like what I'm understanding.  Web components, primarily Shadow DOM and Custom elements are coming (or are already here) to a website near you.  Yes, they require a Javascript dependency, but hey, what doesn't require a dependency these days?  At least it's your own work your depending on.

What's really cool about the opening of the shadow DOM and browser registration of Custom elements is that the power previously held only in the hands of browser developers is now in the hands of the work a day developer.  With some up front effort, you can now define an API for your own handy element and implement it by importing a file and using the tag.  You can create completely from scratch using an the HTML element prototype, or extend the functionality of a pre-existing HTML element by extending from that elements prototype.  

The Shadow DOM keeps your work encapsulated so someone implementing your element will only have the access you allow, which is great when you consider its application in a production environment.  This is a lovely OOP principle that works hand in hand with the good 'ol separation of concern.  Now you can define your API and release it into the wild.  I see gorgeous UX elements that have that special "Designed by Maria" feel, with the added bonus of my anal love of CONTROL!
