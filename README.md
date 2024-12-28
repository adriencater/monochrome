# Monochrome image filters in CSS
 
Demo code. Should be adapted to the needs of your project.

```
	:has( > img.monochrome){
		background-color: #f1357a; /* default color */
	}

	img.monochrome{ 
		filter: grayscale(100%); 
		mix-blend-mode: overlay;
	}
```

- - - - -

We use a class `monochrome` on the `<img>` elements we want to modify.

It is important that they be wrapped in a `<div>` or other parent element: this is where we will apply the color.

This example uses a 'parent selector' `*:has( > img.monochrome)` to select the enclosing parent elemnts of monochrome images and give them a background color. (that way, you can use any parent elements you want/have, and you only need to apply the monochrome class once, on the image itself.)

The default color will apply to all images. Override this with other declarations as necesary if more variety is necessary.

We use CSS color filters and mix-blend-modes to mix the image and background color, which should be adapted to the needs of your project. 

Applying `filter: grayscale(100%);` is a good idea, but you can add other filters if you need.

The mix-blend-mode will give different results depending on the original image (brighness, contrast) and the desired effect.

- - - - --

https://developer.mozilla.org/en-US/docs/Web/CSS/filter
- filter: grayscale(100%) brightness(110%);
- filter: grayscale(100%) contrast(80%);
- filter: grayscale(100%) invert(100%);

https://developer.mozilla.org/en-US/docs/Web/CSS/mix-blend-mode
- mix-blend-mode: multiply;
- mix-blend-mode: screen;
- mix-blend-mode: overlay;
- mix-blend-mode: darken;
- mix-blend-mode: lighten;
- mix-blend-mode: color-dodge;
- mix-blend-mode: color-burn;
- mix-blend-mode: hard-light;
- mix-blend-mode: soft-light;
- mix-blend-mode: difference;
- mix-blend-mode: exclusion;
- mix-blend-mode: luminosity;
- mix-blend-mode: plus-darker;
- mix-blend-mode: plus-lighter;


- - - - -

12-bit rainbow palette by Kate Morley
https://iamkate.com/data/12-bit-rainbow/

#817
#a35
#c66
#e94
#ed0
#9d5
#4d8
#2cb
#0bc
#09c
#36b
#639