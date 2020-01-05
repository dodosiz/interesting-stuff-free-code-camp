# Transformations

## Change the scale of an element

To change the scale of an element, CSS has the **transform** property, along with its **scale()** function. The following code example doubles the size of all the paragraph elements on the page:

```css
p {
  transform: scale(2);
}
```

The **transform** property has a variety of functions that let you scale, move, rotate, skew, etc., your elements. When used with pseudo-classes such as **:hover** that specify a certain state of an element, the transform property can easily add interactivity to your elements.

Here's an example to scale the paragraph elements to 2.1 times their original size when a user hovers over them:

```css
p:hover {
  transform: scale(2.1);
}
```

## Skew an element

The next function of the **transform** property is **skewX()**, which skews the selected element along its X (horizontal) axis by a given degree or the **skewY()** for the Y (vertical) axis.

The following code skews the paragraph element by -32 degrees along the X-axis.

```css
p {
  transform: skewX(-32deg);
}
```

## Using ::before and ::after

hese pseudo-elements are used to add something before or after a selected element. In the following example, a **::before** pseudo-element is used to add a rectangle to an element with the class heart:

```css
.heart::before {
  content: "";
  background-color: yellow;
  border-radius: 25%;
  position: absolute;
  height: 50px;
  width: 70px;
  top: -50px;
  left: 5px;
}
```

For the **::before** and **::after** pseudo-elements to function properly, they must have a defined content property. This property is usually used to add things like a photo or text to the selected element. When the **::before** and **::after**** pseudo-elements are used to make shapes, the content property is still required, but it's set to an empty string. In the above example, the element with the class of heart has a **::before** pseudo-element that produces a yellow rectangle with height and width of 50px and 70px, respectively. This rectangle has round corners due to its 25% border radius and is positioned absolutely at 5px from the left and 50px above the top of the element.

[Back to navigation](../README.md)