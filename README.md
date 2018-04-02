# lightslider
Here we have a light Slider very easy to adapt to our website’s look, and it has a light code.  It only uses jQuery, CSS and HTML5.

Test [here](http://www.antiax.org/lightslider).

jQuery key:

Movement effect:
```
    $( ".dot" ).removeClass( "active" );
    $("#dot-" + n).addClass("active");
    $(".dot, .prev, .next").unbind("click");
    $( "#slide-" + sliderIndex ).hide("slide", { direction: "left" }, animationTime);
    $( "#slide-" + n ).show("slide", { direction: "right" }, animationTime, function () { 
        sliderIndex = n; 
        $(".dot").bind("click", dotHandler);
        $(".prev").on("click", prevHandler);
        $(".next").on("click", nextHandler);
    });
```
CSS keys:

- slider
    - slider-container (position relative)
        - slide (position absolute)
        - ....
        - slide (position absolute)
    - footer

Only one slide is visible at a time.
Slides are 1000x350 
```
.slider{
    float: left;
    width: 100%;

    text-align: center; /* FOOTER CENTER WHEN WIDTH IS UNKNOW */
}
.slides-container {
  position: relative;
  width: 1000px;
  height: 350px;

  display: block;
  margin: 0 auto;
  overflow: hidden; /* CENTER WHEN WIDTH IS KNOWN */
}
.slide {
    position: absolute;
    left: 0px;
    top: 0px;
    
    display: none;
}
.slider footer {
    display: inline-block; /* CENTER WHEN WIDTH IS UNKNOWN */
}
```
