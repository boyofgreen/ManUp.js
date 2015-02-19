# ManUp.js

version 0.7

##What is it?
ManUp.js is a polyfill to support the [Manifest for Web Apps](http://w3c.github.io/manifest/).  The Manifest for Web App allows you to build one simple JSON object that contains all the meta data (app name, icons, presentaiton, etc.) instead of having to build out a myrid of meta tags and link tags to suppor each platform.
### Sample Manifest for Web Apps

```javascript
    
   {
  "name": "ManUp! JS, the Manifest Polyfill",
  "short_name": "ManUP! JS",
  "icons": [
      {
      "src": "images/tiny.png",
      "sizes": "70x70",
      "type": "image/png"
    },
    {
      "src": "images/square.png",
      "sizes": "150x150",
      "type": "image/png"
    },
    {
      "src": "images/widelogo.310x150.png",
      "sizes": "310x150",
      "type": "image/png"
    },
    {
      "src": "images/large-win.png",
      "sizes": "310x310",
      "type": "image/png"
    },
    {
      "src": "images/apple-touch-icon-72x72-precomposed.png",
      "sizes": "72x72",
      "type": "image/png",
      "density": "1.5"
    },
    {
      "src": "images/apple-touch-icon-57x57-precomposed.png",
      "sizes": "57x57",
      "type": "image/png",
      "density": "2.0"
    },
    {
      "src": "images/apple-touch-icon-76x76-precomposed.png",
      "sizes": "76x76",
      "type": "image/png",
      "density": "1.5"
    },
    {
      "src": "images/apple-touch-icon-60x60-precomposed.png",
      "sizes": "60x60",
      "type": "image/png",
      "density": "2.0"
    },
    {
      "src": "images/apple-touch-icon-120x120-precomposed.png",
      "sizes": "120x120",
      "type": "image/png",
      "density": "1.5"
    },
    {
      "src": "images/apple-touch-icon-152x152-precomposed.png",
      "sizes": "152x152",
      "type": "image/png",
      "density": "2.0"
    },
    {
      "src": "images/apple-touch-icon-114x114-precomposed.png",
      "sizes": "114x114",
      "type": "image/png",
      "density": "3.0"
    },
    {
      "src": "images/nice-highres.png",
      "sizes": "192x192",
      "type": "image/png",
      "density": "4.0"
    },
    {
      "src": "images/niceicon.png",
      "sizes": "128x128",
      "type": "image/png",
      "density": "4.0"
    }
  ],
  "start_url": "index.html",
  "display": "standalone",
  "orientation": "landscape"
}

```


## What does it do?
ManUp.js lets your write to the simple  [Manifest for Web Apps](http://w3c.github.io/manifest/) spec, and then builds the necessary tags to add as many app like features as are supported in your browser.

##How do I use it?

*Step 1*: Add the manifest file to your site with a link tag like so:

```html

    <link rel="manifest" href="manifest.json">

```

*Step 2*: Add the manup.min.js file to your page (we recommend the bottom of the page, but just make it somewhere below the manifest file) like so:

```html

<script src="manup.js"></script>

```


*Step 3*: Make sure you web server is configured to properly serve the manifest file with the proper mimetype of "application/manifest+json".  In IIS you just add a web.config file to the root of your server and add this:
```xml

<?xml version="1.0"?>
<configuration>
  <system.webServer>
    <staticContent>
      <remove fileExtension=".json"/>
      <mimeMap fileExtension=".json" mimeType="application/manifest+json"/>
    </staticContent>
  </system.webServer>
  <system.web>
    <compilation debug="true"/>
  </system.web>
</configuration>

```
##Demo Page
View a demo at http://manupjs.azurewebsites.net/


##Know support

#### Browsers that support W3C Manifest for Web Apps
 - Chrome for Android 38+

### Browsers that benifit from the polyfill
  - Chrome for Android 
  - Android Browser
  - Safari for iOS
  - Windows Phone 8
  - Windows 8
  - FireFox OS 1.1+

