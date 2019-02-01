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
```

```
```

```
```

