#Welcome to RWD!

By this point, as super-master-frontend wizards, you might be thinking, "But what if I want to see my beautiful page on my iPhone/Android/iPad/Kindle/Generic Mobile Device?" Well, now's your time. Welcome to the wonderful world of Responsive Web Design.

##What is RWD?

RWD, or Responsive Web Design is the practice of making your webiste or webapp *respond* to different environments that it finds itself in, and adapt accordingly. So how do we acheive this? There are a few ways to do this, but the two main ways are through relative units and media queries.

###Relitive Units
In RWD, it is necessary to use relative units. In today's tech world, pixel sizes are getting smaller and smaller by the day. So, a border of 3px might look right on your screen, but on another monitor it might look too big or too small. So we want to use a unit called REMs for height, and percentage values for width.

####REMs
REMs are a unit of height that are relative to your browser's default font size. Most browsers have a default font size of 16px. On those browsers, 1rem is equal to 1px.

####Percentages
Percentages are a very useful unit of measurement, and should always be used for width. They do not work for height yet, but they are invaluable for RWD. Percentages are a bit finicky, because they have cascading properties. If you have an upper level div with width of 50%, it will take up 50% of the screen's width. However, if you put another div with width of 50% inside the outer div, the inner one will take up 50% of the outer div, but only 25% of the window.

###Media Queries
A Media Query is a special kind of CSS selector. It contains styles that are only activated once certain conditions are met. The idea is to create styles that are only activated when the page has attributes that only happen when they are being displayed on a mobile device. So how do media queries work? Well, there are many kinds, but a very common one looks something like this:

```CSS
@media screen and (max-width: 480px){
	//some CSS
}
```

But what exactly does that mean? Well, let's break it down.

`@media` is the prefix that lets the browser know "Hey, this is a media query."

`screen` is the first condition that we're setting. We're making sure that it is being displayed on a screen. Well, what's the point of this? Web pages can be displayed in may more ways that a screen, the best example being a printed page. So, if we wanted our page to look different when printed out, we could use a `print` condition.

`and` is just an operator that tells the browser that there's more on the way.

`(max-width: 480px)` is the real meat of the query. This is saying that these styles should only be activated when the browser window has a width of less than 480 pixels.  Many smartphones have a screen width of around 480px, so 480 is a good ballpark guess for screen size.

Then, inside the `{}`, you put all of the CSS styles that should be applied. Use the normal syntax of CSS in the query's body.

###Multiple Media Queries
If you want, you can have multiple queries in a single stylesheet, to cover landscape/portrait and tablets.


##Your Challenge
Stored in this git repo is a bare-bones HTML page with some very basic styling. Your job is to add media queries so the all of the elements line up vertically on the page when displayed on an iPhone-sized window.

![Ref image]
(res.png)

##Bonus Challenge
Make the page look good.
