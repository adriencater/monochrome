# Monochrome image filters in CSS
 
Demo code. Should be adapted to the needs of your project.

```
	:has( > img.monochrome) {
		background-color: #f1357a; /* default color */
	}

	img.monochrome { 
		filter: grayscale(100%);
		mix-blend-mode: overlay;
	}
```

Demo at: [adriencater.github.io/monochrome/](https://adriencater.github.io/monochrome/)

- - - - -

This example uses a class `monochrome` on the `<img>` elements to be modified.

It is important that the images be wrapped in a `<div>` or other parent element: this is where the color will applied, as a background.

This example uses a ‘parent selector’ `*:has( > img.monochrome)` to select the enclosing parent elemnts of .monochrome images. By using a ‘parent selector’, the .monochrome class only needs to be applied once, and on the image element directly.

In the example above, the default color will apply to all images. This can be changed or overriden with other declarations.

This example uses the CSS **`filter`** and **`mix-blend-mode`** to combine the image and background color – these should be adapted to the needs of the project. 

Applying `filter: grayscale(100%);` gives a standard effect, but other filters can be used or added for different effects.

The mix-blend-mode can be tuned give different results depending on the original image (brighness, contrast) and the desired effect.

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