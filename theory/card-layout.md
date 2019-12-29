# Card Layout Core Principles

## Text align

Use the **text-align** property to align text.

```css
/* Causes all lines of text except the last line to meet the left and right edges of the line box. */
text-align: justify;
/* Centers the text. */
text-align: center;
/* Right-aligns the text. */
text-align: right;
/* Left-aligns the text (the default). */
text-align: left;
```

## Box shadow looks nice in card elements

The box-shadow property takes values for

* **offset-x** (how far to push the shadow horizontally from the element),
* **offset-y** (how far to push the shadow vertically from the element),
* **blur-radius**,
* **spread-radius** and
* **color**, in that order.

The blur-radius and spread-radius values are optional.

Multiple box-shadows can be created by using commas to separate properties of each box-shadow element.

```css
box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
```