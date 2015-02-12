# ManUp.js

##What is it?
ManUp.js is a polyfill to support the [Manifest for Web Apps](http://w3c.github.io/manifest/).  The Manifest for Web App allows you to build one simple JSON object that contains all the meta data (app name, icons, presentaiton, etc.) instead of having to build out a myrid of meta tags and link tags to suppor each platform.

## What does it do?
ManUp.js lets your write to the simple  [Manifest for Web Apps](http://w3c.github.io/manifest/) spec, and then builds the necessary tags to add as many app like features as are supported in your browser.

##How do I use it?

*Step 1*: Add the manifest file to your site with a link tag like so:

*Step 2*: Add the manup.min.js file to your page (we recommend the bottom of the page, but just make it somewhere below the manifest file) like so:

*Step 3*: Make sure you web server is configured to properly serve the manifest file with the proper mimetype of "application/manifest+json".  In IIS you just add a web.config file to the root of your server and add this:



##Know support

