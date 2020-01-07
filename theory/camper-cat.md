# Accessibility with Camper Cat's blog

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

[Back to navigation](../README.md)