# Card Layout Core Principles

## Text align

Use the **text-align** property to align text.

|text-align | Effect |
|-----------|--------|
|**justify**|Causes all lines of text except the last line to meet the left and right edges of the line box.|
|**center**|Centers the text.|
|**right**|Right-aligns the text.|
|**left**|Left-aligns the text **(the default)**.|

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

## Opacity property

Use the opacity property on an element like an image or text to change it's opacity.

```css
a {
    opacity: 0.7;
}
```

## Text transform to transform text

|text-transform|Result|
|---|---|
|lowercase|"transform me"|
|uppercase|"TRANSFORM ME"|
|capitalize|"Transform Me"|
|initial|Use the default value|
|inherit|Use the **text-transform** value from the parent element|
|none|**Default:** Use the original text|

[Back to navigation](../README.md)