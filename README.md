# myo-remark-example

It appears that connecting the Myo with your remark presentation trivial:



```
var slideshow = remark.create();

var myo = Myo.create();

myo.on('wave_out', function (edge) {
  if (edge) {
    slideshow.gotoNextSlide();
  }
});

myo.on('wave_in', function (edge) {
  if (edge) {
    slideshow.gotoPreviousSlide();
  }
});
```

