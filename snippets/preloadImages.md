---
title: Preload images
tags: array, string, browser
expertise: beginner
firstSeen: 2022-07-18T21:30:00-05:00
---

Preloads given images to prevent displaying empty parts on a website to improve user experince.

- Script must be in header. Pass the name/source/path of your images to the `preloadImages()`function as string parameters.
- The function `preloadImages()` interates over the given arguments and creates for each string a new Image in the global defined `images` Array with given source.
- The pictures are accessible in the `images` Array. As an example: `<img src="logo.jpg"></img>` .

```js
let images = new Array();

function preloadImages() {
  for (var i in arguments) {
    images[i] = new Image();
    images[i].src = arguments[i];
  }
}
```

```js
preloadImages("logo.jpg", "header.jpg", "banner.jpg", "profile_pic.jpg");
```
```
