# Animations

## The basics

To animate an element, you need to know about the animation properties and the **@keyframes** rule. The animation properties control how the animation should behave and the **@keyframes** rule controls what happens during that animation. There are eight animation properties in total. This challenge will keep it simple and cover the two most important ones first:

**animation-name** sets the name of the animation, which is later used by **@keyframes** to tell CSS which rules go with which animations.

**animation-duration** sets the length of time for the animation.

**@keyframes** is how to specify exactly what happens within the animation over the duration. This is done by giving CSS properties for specific "frames" during the animation, with percentages ranging from 0% to 100%. If you compare this to a movie, the CSS properties for 0% is how the element displays in the opening scene. The CSS properties for 100% is how the element appears at the end, right before the credits roll. Then CSS applies the magic to transition the element over the given duration to act out the scene. Here's an example to illustrate the usage of **@keyframes** and the animation properties:

```css
#anim {
  animation-name: colorful;
  animation-duration: 3s;
}

@keyframes colorful {
  0% {
    background-color: blue;
  }
  100% {
    background-color: yellow;
  }
}
```

## How to use animation on hover

You can use CSS **@keyframes** to change the color of a button in its hover state.

Here's an example of changing the width of an image on hover:

```css
img:hover {
    animation-name: width;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
}

@keyframes width {
    100% {
        width: 40px;
    }
}
```

The **animation-fill-mode: forwards** sets the desired property to stay at the end of the animation.

## Move an element

When elements have a specified position, such as **fixed** or **relative**, the CSS offset properties **right**, **left**, **top**, and **bottom** can be used in animation rules to create movement.

As shown in the example below, you can push the item downwards then upwards by setting the top property of the 50% **keyframe** to 50px, but having it set to 0px for the first (0%) and the last (100%) **keyframe**.

```css
@keyframes rainbow {
  0% {
    background-color: blue;
    top: 0px;
  }
  50% {
    background-color: green;
    top: 50px;
  }
  100% {
    background-color: yellow;
    top: 0px;
  }
}
```

## Controll the amount of times an animation plays

The previous examples covered how to use some of the animation properties and the **@keyframes** rule. Another animation property is the **animation-iteration-count**, which allows you to control how many times you would like to loop through the animation. Here's an example:

```css
animation-iteration-count: 3;
```

In this case the animation will stop after running 3 times, but it's possible to make the animation run continuously by setting that value to **infinite**.

## Change the animation timing

In CSS animations, the **animation-timing-function** property controls how quickly an animated element changes over the duration of the animation. If the animation is a car moving from point A to point B in a given time (your **animation-duration**), the **animation-timing-function** says how the car accelerates and decelerates over the course of the drive.

There are a number of predefined keywords available for popular options. For example, the default value is **ease**, which starts slow, speeds up in the middle, and then slows down again in the end. Other options include **ease-out**, which is quick in the beginning then slows down, **ease-in**, which is slow in the beginning, then speeds up at the end, or **linear**, which applies a constant animation speed throughout.

[Back to navigation](../README.md)