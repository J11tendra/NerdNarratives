# Learn CSS Background

## Introduction

We can do some really cool things with CSS background property such as creating a hero image or using it to do some really cool parallax effects. In this article, we'll pretty much everything you need to know about CSS background property.

## CSS Background-color Property

Below you have a simple box with class "container"; you can directly set the background color of the container by applying `background-color: <any color you want, lets say violet>` to the container itself. That's it its that simple to change the background-color, however you can use many different colors like rgb, rgba, hex, and hsl.

<!-- Codesandbox e.g. background-color property -->

## CSS Background-image Property

Now you have to change the background image so you gonna set the background image of the container. You use `background-image: url(<paste the url of the image; assets/lion.png>)`. You can see the box has a background image but it is not what we expected. this is because the size of the image is much smaller than the size of box or you can say the width and height of the box. So by default it tends to fill up the empty space by repeating the same image vertically (on y-axis) and horizontally (on x-axis) until it covers the whole space.

<!-- Codesandbox e.g. background-image property -->

## CSS Background-repeat Property

Like you expected to have a single image in the box and not allowing the image to repeat; this can achieved by using `background-repeat: no-repeat` here you have bunch of option such `background-repeat: repeat-x` and `background-repeat: repeat-y`.

<!-- Codesandbox e.g. background-repeat property -->

## Conclusion
