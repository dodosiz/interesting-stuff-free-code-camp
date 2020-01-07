# HTML Accessibility

## Add a Text Alternative to Images for Visually Impaired Accessibility

Good **alt** text provides the reader a brief description of the image. You should always include an **alt** attribute on your image. Per HTML5 specification, this is now considered mandatory.

```html
<img src="karate.jpeg" alt="I am doing Karate">
```

## Know When Alt Text Should be Left Blank

In the last challenge, you learned that including an alt attribute when using img tags is mandatory. However, sometimes images are grouped with a caption already describing them, or are used for decoration only. In these cases alt text may seem redundant or unnecessary.

```html
<img src="visualDecoration.jpeg" alt="">
```

## Use Headings to Show Hierarchical Relationships of Content

It is important for the heading tags in your markup to have semantic meaning and relate to each other, not be picked merely for their size values.

Headings with equal (or higher) rank start new implied sections, headings with lower rank start subsections of the previous one.

As an example, a page with an **h2** element followed by several subsections labeled with **h4** tags would confuse a screen reader user.

One final point, each page should always have one (and only one) **h1** element, which is the main subject of your content. This and the other headings are used in part by search engines to understand the topic of the page.

## Jump Straight to the Content Using the main Element

The **main** element is used to wrap (you guessed it) the main content, and there should be only one per page. It's meant to surround the information that's related to the central topic of your page. It's not meant to include items that repeat across pages, like navigation links or banners.

The **main** tag also has an embedded landmark feature that assistive technology can use to quickly navigate to the main content. If you've ever seen a "Jump to Main Content" link at the top of a page, using a main tag automatically gives assistive devices that functionality.

## Wrap Content in the article Element

**article** is another one of the new HTML5 elements that adds semantic meaning to your markup. **article** is a sectioning element, and is used to wrap independent, self-contained content. The tag works well with blog entries, forum posts, or news articles.

**Note** about **section** and **div**
The **section** element is also new with HTML5, and has a slightly different semantic meaning than **article**. An **article** is for standalone content, and a **section** is for grouping thematically related content. They can be used within each other, as needed. For example, if a book is the **article**, then each chapter is a **section**. When there's no relationship between groups of content, then use a **div**.

```html
<div> - groups content
<section> - groups related content
<article> - groups independent, self-contained content
```

## Make Screen Reader Navigation Easier with the header Landmark

The next HTML5 element that adds semantic meaning and improves accessibility is the **header** tag. It's used to wrap introductory information or navigation links for its parent tag and works well around content that's repeated at the top on multiple pages.

## Make Screen Reader Navigation Easier with the nav Landmark

The **nav** element is another HTML5 item with the embedded landmark feature for easy screen reader navigation. This tag is meant to wrap around the main navigation links in your page.

## Make Screen Reader Navigation Easier with the footer Landmark

Similar to **header** and **nav**, the **footer** element has a built-in landmark feature that allows assistive devices to quickly navigate to it. It's primarily used to contain copyright information or links to related documents that usually sit at the bottom of a page.

## Improve Chart Accessibility with the figure Element

HTML5 introduced the **figure** element, along with the related **figcaption**. Used together, these items wrap a visual representation (like an image, diagram, or chart) along with its caption. This gives a two-fold accessibility boost by both semantically grouping related content, and providing a text alternative that explains the **figure**.

Here's an example - note that the **figcaption** goes inside the **figure** tags and can be combined with other elements:

```html
<figure>
  <img src="roundhouseDestruction.jpeg" alt="Photo of Camper Cat executing a roundhouse kick">
  <br>
  <figcaption>
    Master Camper Cat demonstrates proper form of a roundhouse kick.
  </figcaption>
</figure>
```

## Improve Form Field Accessibility with the label Element

The **label** tag wraps the text for a specific form control item, usually the name or label for a choice. This ties meaning to the item and makes the form more readable. The **for** attribute on a **label** tag explicitly associates that **label** with the form control and is used by screen readers.

The value of the **for** attribute must be the same as the value of the **id** attribute of the form control. Here's an example:

```html
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name">
</form>
```

## Wrap Radio Buttons in a fieldset Element for Better Accessibility

The next form topic covers accessibility of radio buttons. Each choice is given a label with a for attribute tying to the id of the corresponding item as covered in the last challenge. Since radio buttons often come in a group where the user must choose one, there's a way to semantically show the choices are part of a set.

The fieldset tag surrounds the entire grouping of radio buttons to achieve this. It often uses a legend tag to provide a description for the grouping, which is read by screen readers for each choice in the fieldset element.

The fieldset wrapper and legend tag are not necessary when the choices are self-explanatory, like a gender selection. Using a label with the for attribute for each radio button is sufficient.

An example:

```html
<form>
  <fieldset>
    <legend>Choose one of these three items:</legend>
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choice One</label><br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choice Two</label><br>
    <input id="three" type="radio" name="items" value="three">
    <label for="three">Choice Three</label>
  </fieldset>
</form>
```

## Add an Accessible Date Picker

Forms often include the input field, which can be used to create several different form controls. The type attribute on this element indicates what kind of input will be created.

You may have noticed the text and submit input types in prior challenges, and HTML5 introduced an option to specify a date field. Depending on browser support, a date picker shows up in the input field when it's in focus, which makes filling in a form easier for all users.

For older browsers, the type will default to text, so it helps to show users the expected date format in the label or as placeholder text just in case.

Here's an example:

```html
<label for="input1">Enter a date:</label>
<input type="date" id="input1" name="input1">
```

## Standardize Times with the HTML5 datetime Attribute

Continuing with the date theme, HTML5 also introduced the time element along with a datetime attribute to standardize times. This is an inline element that can wrap a date or time on a page. A valid format of that date is held by the datetime attribute. This is the value accessed by assistive devices. It helps avoid confusion by stating a standardized version of a time, even if it's written in an informal or colloquial manner in the text.

Here's an example:

```html
<p>
  Master Camper Cat officiated the cage match between Goro and Scorpion 
  <time datetime="2013-02-13">last Wednesday</time>,
  which ended in a draw.
</p>
```

## Improve Accessibility of Audio Content with the audio Element

HTML5's **audio** element gives semantic meaning when it wraps sound or audio stream content in your markup. Audio content also needs a text alternative to be accessible to people who are deaf or hard of hearing. This can be done with nearby text on the page or a link to a transcript.

The **audio** tag supports the **controls** attribute. This shows the browser default play, pause, and other controls, and supports keyboard functionality. This is a boolean attribute, meaning it doesn't need a value, its presence on the tag turns the setting on.

Here's an example:

```html
<audio id="meowClip" controls>
  <source src="audio/meow.mp3" type="audio/mpeg" />
  <source src="audio/meow.ogg" type="audio/ogg" />
</audio>
```

## Give Links Meaning by Using Descriptive Link Text

Screen readers do this by reading the link text, or what's between the anchor (**a**) tags. Having a list of "click here" or "read more" links isn't helpful. Instead, you should use brief but descriptive text within the **a** tags to provide more meaning for these users.

## Make Links Navigable with HTML Access Keys

HTML offers the **accesskey** attribute to specify a shortcut key to activate or bring focus to an element. This can make navigation more efficient for keyboard-only users.

HTML5 allows this attribute to be used on any element, but it's particularly useful when it's used with interactive ones. This includes links, buttons, and form controls.

Here's an example:

```html
<button accesskey="b">Important Button</button>
```

## Use tabindex to Add Keyboard Focus to an Element

The HTML tabindex attribute has three distinct functions relating to an element's keyboard focus. When it's on a tag, it indicates that element can be focused on. The value (an integer that's positive, negative, or zero) determines the behavior.

Certain elements, such as links and form controls, automatically receive keyboard focus when a user tabs through a page. It's in the same order as the elements come in the HTML source markup. This same functionality can be given to other elements, such as div, span, and p, by placing a tabindex="0" attribute on them. Here's an example:

```html
<div tabindex="0">I need keyboard focus!</div>
```

**Note:** A negative tabindex value (typically -1) indicates that an element is focusable, but is not reachable by the keyboard. This method is generally used to bring focus to content programmatically (like when a div used for a pop-up window is activated).

**Bonus:** using tabindex also enables the CSS pseudo-class :focus

## Use tabindex to Specify the Order of Keyboard Focus for Several Elements

The tabindex attribute also specifies the exact tab order of elements. This is achieved when the value of the attribute is set to a positive number of 1 or higher.

Setting a tabindex="1" will bring keyboard focus to that element first. Then it cycles through the sequence of specified tabindex values (2, 3, etc.), before moving to default and tabindex="0" items.

It's important to note that when the tab order is set this way, it overrides the default order (which uses the HTML source). This may confuse users who are expecting to start navigation from the top of the page. This technique may be necessary in some circumstances, but in terms of accessibility, take care before applying it.

[Back to navigation](../README.md)