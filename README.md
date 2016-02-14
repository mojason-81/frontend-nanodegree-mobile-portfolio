# Udacity Frontend Nanodegree Website Optimization
===============================


### Website Optimization Challenge

In this repo there is a `src` folder containing the the files profided to me and a `dist` folder containing my modifictions.  The goal was to score over 90 on [Google PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/?url=mojason.com%2Fperformance&tab=mobile) on the `index.html` in the root folder and to make pizza.html in the views folder run at 60FPS.

#### Browser requirements.

Successfully tested using up-to-date versions of Chrome (as of 12 Feb 2016).

#### To view the site:

Simply open `index.html` from the root directory in your browser.
You can also type the complete path into the address bar of your browser.  i.e. `/home/jason/projects/performance/index.html`  If for some reason, that doesn't work, try preceding the path with `'file://'` as follows: `file:///home/jason/projects/performance/index.html`

Additionally, you can view the site live [here](http://www.mojason.com/performance/index.html).


### My Modifictions

`index.html`
Move media query for smartphones into it's own `.css` file and only load it when needed.  Do the same with the media query for print.  Move all other styles into head of HTML doc.
Delete web font link.
Delete analytics.
Add `async` attribute to call to perfmatters.js.
Images were compressed / resized quite a bit.

`pizza.html` & `main.js`
Set `will-change: transform;` property for moving pizzas and use `transform: translateX()` to move pizzas.  Added `backface-visibliity` and `transform` properties as well.  Defined several variables in the global scope so they didn't have to be looked up / calculated every time.  Removed `determineDX()` and changed widths to `%`s instead of `px`.  Replaced `querySelectorAll()` with `getElementsByClassName()`.  Replaced `querySelector()` with `getElementById`  Used `requestAnimationFrame()` for the moving pizzas.  Removed some calculations from `for` loops that only needed to be done once.  Decreased the number of moving pizzas on-screen to 24.
