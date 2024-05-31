## Introduction

On the web everthing is a box literally everything all the elements, images, buttons, paragraphs, videos, and everything. With everything being a box it has a BOX MODEL applied. So what is a CSS BOX MODEL?

 <!-- Example img of a section of a web page -->

![GSAP-everything-is-box-on-web](https://github.com/J11tendra/NerdNarratives/blob/main/learn-css-box-model/assets/webpage-box.png?raw=true)

## What is a BOX MODEL?

_The CSS box model as a whole applies to block boxes and defines how the different parts of a box — margin, border, padding, and content — work together to create a box that you can see on a page. Inline boxes use just some of the behavior defined in the box model._ - mdn web docs

The BOX MODEL consists of the content, padding, border and margin.

 <!-- Image of a BOX MODEL -->

![Box-Model-CSS](https://github.com/J11tendra/NerdNarratives/blob/main/learn-css-box-model/assets/box-model-css.png?raw=true)

## Parts of a box

Making up a block box in css we have this:

- Content box: In this box your actual content is displayed; you can alter this using properties like <u>height</u> and <u>width</u>.

<!-- Image of a content box and example -->
<iframe src="https://codesandbox.io/embed/trglgq?view=editor+%2B+preview&module=%2Fstyles.css"
     style="width:100%; height: 500px; border:0; border-radius: 4px; overflow:hidden;"
     title="serverless-rain-trglgq"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

- Padding box: The padding is the area around the content as white space; you can alter it using <u>padding</u> and related properties. Basically padding is creates a space inside an element.

<!-- Image of a padding box and example -->
<iframe src="https://codesandbox.io/embed/xcj98z?view=editor+%2B+preview&module=%2Fstyles.css"
     style="width:100%; height: 500px; border:0; border-radius: 4px; overflow:hidden;"
     title="learn-padding-css"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

- Border box: The border box wraps around padding box if any otherwise on the content box; size it using <u>border</u> and related properties.

<!-- Image of a border box and example -->
<iframe src="https://codesandbox.io/embed/tqw8wk?view=editor+%2B+preview&module=%2Fstyles.css"
     style="width:100%; height: 500px; border:0; border-radius: 4px; overflow:hidden;"
     title="border-box-model-css"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

- Margin box: The margin is the outermost layer around the content, padding, and border as whitespace between this box and other elements; you can size it using <u>margin</u> and related properties.

<!-- Image of a margin box and example -->
<iframe src="https://codesandbox.io/embed/fnlqch?view=editor+%2B+preview&module=%2Fstyles.css"
     style="width:100%; height: 500px; border:0; border-radius: 4px; overflow:hidden;"
     title="learn-margin-css"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

## The standard CSS BOX MODEL

In the standard box model, if you set height and width property value on a box, these values defines the height and width of the _content box_. Any padding and borders are then added to get the actual size of the box.

**Note: However, the margin takes space on the page it is not counted towards the size of the box.**

If we assume that we have the following box with some CSS properties:

<!-- CSS properties -->

```css
.box {
  width: 300px;
  height: 200px;
  margin: 25px;
  padding: 10px;
  border: 5px solid magenta;
}
```

The actual size of the box will be width (horizontal)(300 + 10 + 10 + 5 + 5) and height (vertical)(200 + 10 + 10 + 5 + 5).

<!-- Image of the content -->

## The alternate CSS BOX MODEL

In the alternate box model, the size is of the box is just the simple width and height of the box.

To apply the alternate box model, we use `box-sizing` property on it.

```css
.alternate {
  box-sizing: border-box;
}
```

If we assume that we have the following box with some CSS properties:

<!-- CSS properties -->

```css
.box {
  width: 300px;
  height: 200px;
  margin: 25px;
  padding: 10px;
  border: 5px solid magenta;
}
```

The actual size of the box will be width (horizontal)(300) and height (vertical)(200).

<!-- Image of the content -->

**The alternate box model is popular among developers and here is how you can apply to the elemets:**

<!-- CSS code box sizing inherit after before -->

```css
html {
  box-sizng: border-box;
}

*,
*::after,
*::before {
  box-sizing: inherit;
}
```

## Play with CSS BOX MODEL

Ignore the boilerplate, I create two divs with class name <u>box</u>. I also add one more class <u>alternate</u> to the second div. Now both the divs will have same properties except the alternate class.

The class **box** has following CSS properties:

<!-- CSS box properties -->

```css
.box {
  width: 200px;
  height: 150px;
  margin: 10px;
  padding: 25px;
  border: 5px solid magenta;
}
```

The class **alternate** has following CSS properties:

<!-- CSS alternate properties -->

```css
.alternate {
  box-sizing: border-box;
}
```

<!-- Example of a standard vs alternate box model -->

<iframe src="https://codesandbox.io/embed/kx38jx?view=editor+%2B+preview&module=%2Fstyles.css"
     style="width:100%; height: 500px; border:0; border-radius: 4px; overflow:hidden;"
     title="learn-css-playground"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

## Conclusion

That's it for BOX MODEL; As everything on web is a box it is very important to learn the fundamentals of CSS. Learning box modeling enables you to manipulate and structure elements on the page.

Thanks for this reading!! If you find this helpful; drop your reactions and share this piece with others.

You can also stay connected with me by following me here and on [X](https://twitter.com/JiitendraC), [LinkedIn](https://www.linkedin.com/in/jiitendrachoudhary/).
