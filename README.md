# IMPORTANT

**This service has been ported to the official WebdriverIO v5 repo. Please see https://github.com/webdriverio/v5/tree/master/packages/wdio-applitools-service for future usage**

# wdio-applitools-service

This service sets up [applitools.eyes](https://applitools.atlassian.net/wiki/spaces/Java/pages/1540328/Selenium+-+JavaScript#Selenium-JavaScript-002) with WebdriverIO

# Installation

`npm install --save wdio-applitools-service`

# Configuration

Replace MY_API_KEY with the API key of your account (you can find it in your signup Email).

```js
// wdio.conf.js
export.config = {
  applitools: {
    apiKey: "MY_API_KEY",
    matchTimeout: 2000,
    matchLevel: "Strict",
    forceFullPageScreenshot: false,
    hideScrollbars: true,
    useHttpProxy
  },
  // ...
  services: ['applitools'],
  // ...
};
```

browser.checkWindow(windowName, matchTimeout);
browser.checkElement(selector, matchTimeout, "tag");
browser.checkRegion(selector, "window_name", matchTimeout);
browser.checkFrame(selector, matchTimeout, "tag");
browser.checkRegionInFrame(selector, matchTimeout, "tag", isScrollable);

eyes.setMatchLevel("Level");
eyes.setSaveNewTests(true/false);
