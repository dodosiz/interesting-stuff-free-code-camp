# CSS Variables

Declare a css variable with two hyphens.

```css
---black-color: #000;
```

The variable is inherited from the selector defined to all descendants. It is so best practice
to define it in the pseudo selector :root for the whole html document.

```css
:root {
    ---black-color: #000;
}
```

To use the variable apply the var function, the first parameter should be the variable name and the
second a fallback if the variable is not defined.

```css
h1 {
    background-color: var(--black-color, black);
}
```

IE does not support css variables, so if you need IE compatibility you have to define the property
without a variable, before the property with the variable is declared.

```css
h1 {
    background-color: black;
    background-color: var(--black-color, black);
}
```

[Back to navigation](../README.md)