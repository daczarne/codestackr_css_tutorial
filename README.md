# codeSTACKr's CSS tutorial


Notes from codeSTACKr's HTML tutorial. You can watch the tutorial [here](https://www.youtube.com/watch?v=Tfjd5yzCaxk).


Table of content:

[What is CSS?](#what-is-css)  
[CSS Usage](#css-usage)  
[Anatomy of a CSS selector](#anatomy-of-a-css-selector)  
[Colors](#colors)  
[Fonts](#fonts)  

## What is CSS?

CSS stands for Cascading Style Sheets and, just like HTML, it's not a programming language. CSS is a styling languague and it's used for website layout and design.

The main idea behind CSS is that we can use a *selector* to target an HTML element, and apply to it the style defined in the `.css`. This style is defined with key-value paris called *attributes* and it changes how the element is displayed on the web page.

## CSS usage

There are three ways of using CSS:

1. **Inline:** we can add a `style` attribute to HTML tags and define the style in there. This is extremedly discouraged!! With inline each element needs to be styled separately.

2. **Internal:** we can add a `<style>` element in the `<head>` element of our webpage. This is not the recommended practice since it makes files larger and the styles defined can only be used in one HTML file.

3. **External:** we use a separate `.css` file and link the HTML page or pages that we want to use this styles using a `<link>` tag with a `href="style.css"` in the HTML `<head>`. This makes the CSS file reusable across multiple pages, makes the HTML code file lighter and easier to mantain, and achieves *separation of concerns*.

## Anatomy of a CSS selector

First we name the selector. Next comes the declaration block. This block is delimited by `{}`. Inside of it we'll place property-value pairs separated by a colon `:`. Each property-value pair ends with a semi-colon `;` and should take up it's own line. 

![](img/css-selector-anatomy.png)

Selectors come in many forms. We can select all instances of an HTML tag, all instances of a class, ids, or combinations of them. You can find the complete list of selectors [here](https://www.w3schools.com/cssref/css_selectors.asp).

## Colors

The are several different ways in which we can define color values for all color-related properties.

- HTML color names: some colors have names like `black`, `white`, `blue`, etc. There's over 140 defined HTML colors. You can find a complete list of HTML color names [here](https://www.codestackr.com/blog/html-color-names/).

- HEX values: this are 3 or 6 digit long alphanumerical combinations that represent hexadecimal numbers prefixed by a `#` sign.

- rgb/rgba: *rgb* stands for `red, green and blue`. Here we specify the amound of each color that our color should take in a 0 to 255 scale. So, for example, `red = rgb(255, 0, 0)`, or `white = rgb(255, 255, 255)`. *rgba* is similar but adds the *alpha* value or transparency value for our color. Alpha ranges from 0 to 1 where 0 is complete transparency and 1 if total opacity.

## Fonts

There are several different fonts that can be used. Two of the most common are `Serif` (fancier and with more details) and `Sans Serif` (modern and plain). When choosing a font we need to make sure that it's `Web Safe Fonts` since not all fonts will work in all browsers. If we choose a font that is not WSF, make sure to include the necessary code in the HTML `<head>` to import it. 

When choose a font in CSS we use the `font-family` property and pass a list of different fonts. The browser will try using the first one and, if it can't, it will default to the next one on the list and so on.

``` css
selector {
  font-family: Arial, Helvetica, sans-serif;
}
```
