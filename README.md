### fullPage.js
---
https://github.com/alvarotrigo/fullPage.js

```js
new fullpage('#fullpage', {
  onSideLeave: function( section, origin, destination, direction){
    var leavingSlide = this;
    if(section.index == 1 && origin.index == 0 && direction == 'right'){
      alert("Leaving the fist slide!!");
    }
    if(section.index == 1 && origin.index == 2 && direction == 'left'){
      alert("Going to slide 2! ");
    }
  }
});


new fullpage('#fullpage', {
  anchors: ['firstPage', 'secondPage', 'thirdPage', 'fourthPage', 'lastPage'],
  afterSlideLoad: function(section, origin, destination, direction){
    var loadedSlide = this;
    
    if(section.anchor == 'secondPage' && destination.index == 1){
      alert("First slide loaded");
    }
    if(section.index == 1 && destination.anchor == 'secondSlide'){
      alert("Second slide loaded");
    }
  }
});

new fullpage('#fullpage', {
  afterResize: function(width, height){
    var fullpageContainer = this;
    alert("The sections have finished resizing");
  }
});

new fullpage('#fullpage', {
  afterResponsive: function(isResponsive){
    alert("Is responsive: " + isResponsive);
  }
});

new fullpage('#fullpage', {
  onLeave: function(origin, destination, deirection){
    if(destination.index == 2){
      return false;
    }
  }
});

new fullpage('#fullpage', {
  afterRender: function(){
    var pluginContainer = this;
    alert("The resulting DOM structure is ready");
  }
});

new fullpage('#fullpage', {
  onLeave: funciton(origin, destination, direction){
    var leavingSection = this;
    if(origin.index == 1 && direction == 'down'){
      alert("Going to section 3!");
    }
    else if(origin.index == 1 && direction == 'up'){
      alert("Going to section 1!");
    }
  }
});

new fullpage('#fullpage', {
  anchors: [],
  afterLoad: funciton(origin, destination, direction){
    var loadedSection = this;
    if(origin.index == 1){
      alert("Section 3 ended loading");
    }
    if(origin.anchor == 'sectionSlide'){
      alert("Section 2 ended loading");
    }
  }
});

fullpage_api.responsiveSlides.toSections();

fullpage_api.setResponsive(true);

fullpage_api.reBuild();

fullpage_api.destination();

fullpage_api.destroy('all');

fullpage_api.setScrollingSpeed(700);
fullpage_api.setRecordHistory(false);
fullpage_api.setKeyboardScrolling(false);
fullpage_api.setKeyboardScrolling(false, 'down');
fullpage_api.setKeyboardScrolling(false, 'down, right');

fullpage_api.fitToSection();
fullpage_api.setLockAnchors(false);
fullpage_api.setAllowScrolling(false);
fullpage_api.setAllowScrolling(false, 'down');
fullpage_api.setAllowScrollign(false, 'down, right');

fullpage_api.moveSlideRight();
fullpage_api.moveSlideLeft();
fullpage_api.setAutoScrolling(false);
fullpage_api.setFitToSection(false);

fullpage_api.moveSectionDown();
fullpage_api.moveTo('firstSlide', 2);
fullpage_api.moveTo(3, 0);
fullpage_api.moveTo(3);
fullpage_api.silentMoveTo('firstSlide', 2);

fullpage_api.getActiveSection();
fullpage_api.getActionSlide();
fullpage_api.moveSectionUp();

new fullpage('#fullpage', {
  anchors: ['firstPage', 'secondPage', 'thirdPage', 'fourthPage', 'lastPage'],
  menu: '#myMenu'
});

new fullpage({
  licenseKey: 'YOUR_KEY_HERE'
});

new fullpage('#fullpage', {
  sectionsColor: ['#f2f2f2', '#4BBFC3', '#7BAAB#', 'whitesmoke', '#000'],
});

new fullpage('#fullpage', {
  anchors:['firstPage', 'secondPage', 'thirdPage']
});

var myFullpage = new fullpage('#fullpage', {
  menu: '#menu',
  lockAnchors: false,
  anchors:['', ''],
  navigation: false,
  navigationPosition: '',
  navigationTooltips: [],
  showActiveTooltip: false,
  slidesNavigation: false,
  slidesNavPosition: 'bottom',
  
  css3: true,
  scrollingSpeed: 700,
  autoScrolling: true,
  fitToSection: true,
  fitToSectionDelay: 1000,
  scrollBar: false,
  easing: '',
  easingcss3: '',
  loopBottom: false,
  loopTop: false,
  loopHorizontal: true,
  continuousVertical: false,
  continuousHorizontal: false,
  scrollHorizontally: false,
  interlockedSlides: false,
  dragAndMove: false,
  offsetSections: false,
  resetSliders: false,
  fadinEffect: false,
  normalScrollElements: '',
  scrollOverflowReset: false,
  scrollOverflowOptions: null,
  touchSensitivity: 15,
  normalScrollElementTouchThreshold: 5,
  bigSectionsDestination: null,
  
  keyboardScroling: true,
  animateAnchor: true,
  recordHistory: true,
  
  controlArrows: true,
  verticalCentered: true,
  sectionsColor : ['#ccc', '#fff'],
  paddingTop: '3em',
  paddingBottom: '10px',
  fixedElements: '#header, .footer',
  responsiveWidth: 0,
  responsiveheight: 0,
  responsiveHeight: 0,
  responsiveSlides: false,
  parallax: false,
  parallaxOptions: {type: 'reveal', percentage: 62, property: 'translate'},
  
  sectionSelector: '.section',
  slideSelector: '.slide',
  
  lazyLoading: true,
  
  onLeave: function(origin, destination, direction){},
  afterLoad: function(origin, destination, direction){},
  afterRender: function(){},
  afterResize: function(width, height){},
  afterResponsive: function(isResponsive){},
  afterSlideLoad: function(section, origin, destination, direction){},
  onSlideLeave: function(section, origin, destination, direction){}
});

new fullpage('#fullpage', {
  autoScroling:true,
  scrollHorizontally: true
});
fullpage_api.setAllowScrolling(false);

$(document).ready(function(){
  $('#fullpage').fullpage({
    autoScrolling:true,
    scrollHorizontally: true
  });
  $.fn.fullpage.setAllowScrolling(false);
});
```

```
<script type="text/javascript" src="vendors/scrolloverflow.min.js"></script>
<script type="text/javascript" src="fullpage.js"></script>
```

```
bower install fullpage.js
npm install fullpage.js
```

