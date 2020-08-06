# B-ScrollUp

B-ScrollUp is jQuery / Javascript plugin which adds `scroll to top` button to your website.
- [Online demo](http://b-codestudio.com/b-scrollUp-demo/)

### Compatibility
B-ScrollUp is fully functional plugin with all modern browsers and even with old browsers like IE10 and Opera 12.1.

### How to use
After files are downloaded, you need to go to `src` folder and copy **jquery.BScrollUp.js** file and paste it to your `js` folder. Now open your root file such as `index.html` and paste this line of code next to your other `<script></script>` codes:

```
//Your other script tags
<script src="your js folder path/jquery.BScroll.js"></script> 
```
### initialization
Initilize the plugin like other jQuery plugins, like below:

```
$(document).ready(function() {
  $("body").BScrollUp({
    // Option goes here
  });			
});
```
**Notice:** You need to select `body` to use B-ScrollUp plugin.

### Options
- `scrollDuration:` (Default: 300) Set duration of scroll movement in milliseconds. If you set it zero, then it acts like normal browser behaviour.
```
$("body").BScrollUp({		
  scrollDuration: 1800					
});
```

- `scrollDistance:` (Default: 0) Set the distance without any suffix like `px` or `%`, just numeric value. `Header` animation and `scroll to top button` action happen after this certain distance.
```
$("body").BScrollUp({		
  scrollDuration: 1800,
  scrollDistance: 1000
});
```

- `scrollEasing:` (Default: linear) Scroll easing has long range of variety and is compatible with all modern and old browsers. Make sure put scroll easing name between `""` when you set it. List of easing:
  - linear
  - easeInQuad
  - easeOutQuad
  - easeInOutQuad
  - easeInCubic
  - easeOutCubic
  - easeInOutCubic
  - easeInQuart
  - easeOutQuart
  - easeInOutQuart
  - easeInQuint
  - easeOutQuint
  - easeInOutQuint
  - easeInSine
  - easeOutSine
  - easeInOutSine
  - easeInExpo
  - easeOutExpo
  - easeInOutExpo
  - easeInCirc
  - easeOutCirc
  - easeInOutCirc
  - easeInElastic
  - easeOutElastic
  - easeInOutElastic
  - easeInBack
  - easeOutBack
  - easeInOutBack
  - easeInBounce
  - easeOutBounce
  - easeInOutBounce
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart"
});
```


- `makeButton:` (Default: true) If you set this `true` then the plugin create the `scroll to top` button and append it to body. And if you set it false then it means you already created 'scroll to top' button.
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart",  
  
  makeButton: true
});
```

- `upButtonID:` (Default: 'BScrollUp') You can set and `id` for `scroll top top` button to have more control on it.
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart",
  
  makeButton: true,
  upButtonID: 'go-upButton'
});
```
**Notice:** If you already have `scroll to top` button and set `makeButton` false then you have to set `upButtonID`.

- `upButtonText:` (Default: 'top') You can use text, HTML tags or even both to customize `scroll to top` button.
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart",
 
  makeButton: true,
  upButtonID: 'go-upButton',
  upButtonText: '<div><span></span></div>'
});
```

- `upButtonScrollTo:` (Default: '#') Set the destination for `scroll to top` button. You can set `id` or `#`. 
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart",
  
  makeButton: true,
  upButtonID: 'go-upButton',
  upButtonText: '<div><span></span></div>',
  upButtonScrollTo: "#section1"
});
```
**Notice:** If you set `#` then `scroll to top` button scroll to top of the page.

- `upButtonClass:` (Default: '') If you need to animate `scroll to top` button by class then set it by your animation class name.
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart",
  
  makeButton: true,
  upButtonID: 'go-upButton',
  upButtonText: '<div><span></span></div>',
  upButtonScrollTo: "#section1",
  upButtonClass: 'animateScrollToTop'
});
```

- `upButtonInlineStyle:` (Default: {bottom: '15px', right: '15px'}) Use this option to add inline `css style`.
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart",
 
  makeButton: true,
  upButtonID: 'go-upButton',
  upButtonText: '<div><span></span></div>',
  upButtonScrollTo: "#section1",
  upButtonClass: 'animateScrollToTop',
  upButtonInlineStyle: {bottom: '25px', right: '25px'}
});
```
**Notice:** If you set `makeButton` false then you can not use `upButtonInlineStyle`.

- `upButtonStartingStyle:` (Default: {visibility: 'hidden', opacity: 0}) To animate `scroll to top` button with `inline` style not `css`, use this option. This option is for starting point styles such as `visibility: hidden`.
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart",
  
  makeButton: true,
  upButtonID: 'go-upButton',
  upButtonText: '<div><span></span></div>',
  upButtonScrollTo: "#section1", 
  upButtonInlineStyle: {bottom: '25px', right: '25px'},
  upButtonStartingStyle: {visibility: 'hidden', right: "-100px"}
});
```
**Notice:** If you use `upButtonClass` then you can not use `upButtonStartingStyle`. You need to use `upButtonStartingStyle` with `upButtonEndingStyle` to run inline animation.

- `upButtonEndingStyle:` (Default: {visibility: 'visible', opacity: 1}) To animate `scroll to top` button with `inline` style not `css`, use this option. This option and `upButtonStartingStyle` need to work together to run inline animation. This option is for ending point styles such as `visibility: visible`.
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart",
  ,
  makeButton: true,
  upButtonID: 'go-upButton',
  upButtonText: '<div><span></span></div>',
  upButtonScrollTo: "#section1", 
  upButtonInlineStyle: {bottom: '25px', right: '25px'},
  upButtonStartingStyle: {visibility: 'hidden', right: "-100px"},
  upButtonEndingStyle: {visibility: 'visible', right: '25px'}
});
```
**Notice:** If you use `upButtonClass` then you can not use `upButtonEndingStyle`.

- `upButtonZIndex:` (Default: 999999) Set `z-index` based on you desing.
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart",
 
  makeButton: true,
  upButtonID: 'go-upButton',
  upButtonText: '<div><span></span></div>',
  upButtonScrollTo: "#section1", 
  upButtonInlineStyle: {bottom: '25px', right: '25px'},
  upButtonStartingStyle: {visibility: 'hidden', right: "-100px"},
  upButtonEndingStyle: {visibility: 'visible', right: '25px'},
  upButtonZIndex: 999
});
```

- `animationSpeed:` (Default: 300) Set transition speed for `scroll to top` button. Animation speed is in millisecond.
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart",
 
  makeButton: true,
  upButtonID: 'go-upButton',
  upButtonText: '<div><span></span></div>',
  upButtonScrollTo: "#section1", 
  upButtonInlineStyle: {bottom: '25px', right: '25px'},
  upButtonStartingStyle: {visibility: 'hidden', right: "-100px"},
  upButtonEndingStyle: {visibility: 'visible', right: '25px'},
  upButtonZIndex: 999,
  
  animationSpeed: 300
});
```
**Notice:** This option only works with `upButtonStartingStyle` and `upButtonEndingStyle`.

- `css3Easing:` (Default: 'ease') Set transition timing function for `scroll to top` button. This is css transition easing. List of easing:
  - ease
  - linear
  - ease-in
  - ease-out
  - ease-in-out
  - cubic-bezier(n,n,n,n)
  
```
$("body").BScrollUp({		
  scrollDuration: 800,
  scrollDistance: 50,
  scrollEasing: "easeOutQuart",
  
  makeButton: true,
  upButtonID: 'go-upButton',
  upButtonText: '<div><span></span></div>',
  upButtonScrollTo: "#section1", 
  upButtonInlineStyle: {bottom: '25px', right: '25px'},
  upButtonStartingStyle: {visibility: 'hidden', right: "-100px"},
  upButtonEndingStyle: {visibility: 'visible', right: '25px'},
  upButtonZIndex: 999,
  
  animationSpeed: 300,
  css3Easing: 'ease'
});
```
**Notice:** This option only works with `upButtonStartingStyle` and `upButtonEndingStyle`.

### Reporting issues
f you have any issues or any code improvement, please feel free to share it with me.
