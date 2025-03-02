# Monochrome image filters in CSS
 
Demo code. Should be adapted to the needs of your project.

```
	:has( > img.monochrome) {
		background-color: #f1357a;
	}

	img.monochrome { 
		filter: grayscale(100%);
		mix-blend-mode: luminosity;
	}
```
```
	<div><img class="monochrome src="…"></div>
```

Demo at: [adriencater.github.io/monochrome/](https://adriencater.github.io/monochrome/)

- - - - -

```
/* 
	TLDR: wrap your img.monochrome in a <div>.

	- - -
	
	This requires a parent element.

	The image gets a greyscale filter, 
	so we cannot set a background color on the image,
	because then the background color would be grey too!

	We set the background color on the parent element.
	It can be any <tag>, we use the has: selector, 
	which selects the parent element.
*/
```

This example uses a class `monochrome` on the `<img>` elements to be modified.

It is important that the images be wrapped in a `<div>` or other parent element: this is where the color will applied, as a background.

A ‘parent selector’ `*:has( > img.monochrome)` is used to select the enclosing parent elemnts of .monochrome images. By using a ‘parent selector’, the .monochrome class only needs to be applied once, and on the image element directly.

A default color will apply to all images. This can be changed or overriden with other declarations.

The CSS **`filter`** and **`mix-blend-mode`** to combines the image and the parent background color – these should be adapted to the needs of the project. 

Applying `filter: grayscale(100%);` gives a standard effect, but other filters can be used or added for different effects. 

I like `filter: grayscale(100%) contrast(67%) brightness(115%);`

The mix-blend-mode can be tuned give different results depending on the original image (brighness, contrast) and the desired effect.

`mix-blend-mode: luminosity;` gives wider range of black – color – white.

`mix-blend-mode: overlay;` gives a less contrasty range of lighter color – darker color

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