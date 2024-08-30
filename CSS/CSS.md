# CSS
`Covering creating Cascading Style Sheets, attaching them to your HTML, and basic targeting and styling of websites.`

#### `Attaching a CSS file`
```
<head>
  <link href="css/main.css" rel="stylesheet">
</head>
```
#### `Anatomy of CSS`
**rule set** — a grouping of CSS styles that design a certain set of elements.<br/>
**declaration** — a single line of CSS that adds some design.<br/>
**selector** — the targeted item in your HTML document to design.<br/>
**property** — the type of design you want to add, like color, border.<br/>
**value** — how to change the design property.<br/>

## `CSS selectors & units`
#### Selectors
**Tag** (html {}, h1 {})<br/>
**Class** (.nav {}, .wrapper {})<br/>
**Id** (#top {}, #bottom {})<br/>
**Descendant** (ul li {}, nav a {})<br/>
**Child** (ul > li {})<br/>
**Adjacent sibling** (h1 + p {})<br/>
**General sibling** (p ~ p {})<br/>
**Attribute** ([data-state="active"] {})<br/>

## `Pseudo classes`
:first-child,<br/> :last-child,<br/> :only-child,<br/> :nth-child(),<br/> :nth-last-child(),<br/> :nth-of-type(),<br/> :nth-last-of-type(),<br/> :first-of-type,<br/> :last-of-type,<br/> :only-of-type,<br/> :empty,<br/> :disabled,<br/> :checked,<br/> :target,<br/> :not() 

## `Pseudo elements`
::before,<br/> ::after,<br/> ::first-line,<br/> ::first-letter,<br/> ::selection

## `Interaction selectors`
:link,<br/> :visited,<br/> :hover,<br/> :focus,<br/> :active

## `Units`
px,<br/> em (Based on the font-size of the parent),<br/> rem (Based on the font-size set in the html element.), <br/>vh (Viewport height),<br/>vw (Viewport width)

# The Box Model

**padding** — space between the content & box edge.<br/> 
**border** — line around the edge of the box.<br/>
**margin** — space outside the box, pushing other boxes away; can see through margin to what’s behind.<br/>

## `Box dimensions`
**margin** - Create space outside the box, pushing other boxes.<br/>
**margin** - Create space outside the box, pushing other boxes.<br/>
**width** - Control the horizontal space of a box.<br/>
**height** - Controls the vertical space of a box.<br/>
**min-width**<br/>
**min-height**<br/>
**overflow** - Control how elements that break out the edges of the box are dealt with.<br/>
**calc()**

## `Box sizing systems`
**box-sizing: content-box** - Do not use content-box.<br/>
**box-sizing: border-box** - Always use border-box<br/>

## `Display & layout`
**display: inline** - Flows content together, fitting on the same line if possible.(margin, padding, width don’t work).<br/>
**display: block** - Takes up a whole line by itself.(margin, padding, width do work).<br/>
**display: inline-block** - A hybrid between block & inline: fits on the same line, allows padding, width, etc.<br/>
**display: none** - Completely hide the element from the page.

# Flex
 [Background](#background)<br/>
 [Basics & Terminology](#basics-&-terminology)<br/>
 [Properties for flex container](#properties-for-flex-container)<br/>
 [Properties for flex items](#properties-for-flex-items)<br/>

## `background`
```
The Flexbox Layout (Flexible Box) module (a W3C Candidate Recommendation 
as of October 2017) aims at providing a more efficient way to lay out, 
align and distribute space among items in a container, even when their 
size is unknown and/or dynamic (thus the word “flex”).
The main idea behind the flex layout is to give the container the ability to alter its items’ width/height (and order) to best fill the available space.
Flexbox layout is most appropriate to the components of an application, 
and small-scale layouts, while the Grid layout is intended for larger 
scale layouts.
```

## `basics & terminology`
**flex container** - parent element.<br/>
**flex items** - child elements.<br/>
**flex-flow directions** - the flex layout is based on it.<br/>
**main axis** – the primary axis along which flex items are laid out. Beware, it is not necessarily horizontal, it depends on the flex-direction property.<br/>
**main-start | main-end** – The flex items are placed within the container starting from main-start and going to main-end.<br/>
**main size** – A flex item’s width or height.<br/>
**cross axis** – The axis perpendicular to the main axis is called the cross axis. Its direction depends on the main axis direction.<br/>
**cross-start | cross-end** – Flex lines are filled with items and placed into the container starting on the cross-start side of the flex container and going toward the cross-end side.<br/>
**cross size** – The width or height of a flex item, whichever is in the cross dimension.<br/>

## `properties for flex container`
**display** - This defines a flex container, inline or block depending on the given value.<br/>
```
display: flex; /* or inline-flex */
```
**flex-direction** - This establishes the main-axis.<br/>
```
flex-direction: row | row-reverse | column | column-reverse
```
**flex-wrap** - By default, flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property.<br/>
```
flex-wrap: nowrap | wrap | wrap-reverse
```
**flex-flow** - This is a shorthand for the flex-direction and flex-wrap properties.<br/>
```
flex-flow: column wrap;
```
**justify-content** - This defines the alignment along the main axis.
```
justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right ... + safe | unsafe
```
**align-items** - This defines the default behavior for how flex items are laid out along the cross axis.<br/>
```
  align-items: stretch | flex-start | flex-end | center | baseline | first baseline | last baseline | start | end | self-start | self-end + ... safe | unsafe;
```
**align-content** - This aligns a flex container’s lines within when there is extra space in the cross-axis.<br/>
```
  align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch | start | end | baseline | first baseline | last baseline + ... safe | unsafe;
```

## `properties for flex items`
**order** -  Controls the order in which they appear in the flex container.<br/>
```
 order: 5; /* default is 0 */
```
**flex-grow** - This defines the ability for a flex item to grow if necessary.<br/>
```
 flex-grow: 4; /* default 0 */
```
**flex-shrink** - 
```
flex-shrink: 3; /* default 1 */
```
**flex-basis** - This defines the default size of an element before the remaining space is distributed.<br/>
```
  flex-basis:  | auto; /* default auto */
```
**flex** - This is the shorthand for flex-grow, flex-shrink and flex-basis combined.<br/>
```
  flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
```
**align-self** - This allows the default alignment.<br/>
```
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
```

https://tobiasahlin.com/blog/common-flexbox-patterns/<br/>
https://www.quackit.com/css/flexbox/examples/<br/>
https://www.freecodecamp.org/news/flexbox-the-ultimate-css-flex-cheatsheet/

# Grid
`CSS Grids are a two-dimensional layout framework: using both columns & rows.`

## `Terminology`
**Line** — The horizontal or vertical breaks within a grid structure.<br>
**Cell** — The box surrounded by multiple grid lines.<br/>
**Track** — A grouping of grid cells.<br/>
**Column** — A grouping of grid cells on the vertical axis.<br/>
**Row** — A grouping of grid cells on the horizontal axis.<br/>
**Area** — A bundle of vertical and/or horizontal grid cells.<br/>

## `Parents`
**display**<br/>
`grid` – generates a block-level grid<br/>
`inline-grid` – generates an inline-level grid
```
.container {
  display: grid | inline-grid;
}
```
**grid-template-columns**<br/>
**grid-template-rows**<br/>
Defines the columns and rows of the grid with a space-separated list of values. Using the fr unit.
```
.container {
  /* 3 columns, equal size */
  grid-template-columns: 1fr 1fr 1fr;
  /* 2 rows, equal size */
  grid-template-rows: 1fr 1fr;
}
```
**grid-template-areas**
```
.container {
    /* 3 columns, 3 rows
    * Areas spanning more than 1 column/row
    */
    grid-template-areas:
    "masthead masthead toolbar"
    "main     main     sidebar"
    "footer   footer   sidebar";
}
```
**grid-template**<br/>
A shorthand for setting grid-template-rows, grid-template-columns, and grid-template-areas in a single declaration.
```
.container {
  grid-template:
    [row1-start] "header header header" 25px [row1-end]
    [row2-start] "footer footer footer" 25px [row2-end]
    / auto 50px auto;
}
```
**grid-column-gap**<br/>
**grid-row-gap**
```
.container {
    /* Between columns & rows */
    gap: 1rem;
    /* Between columns */
    column-gap: 1rem;
    /* Between rows */
    row-gap: 1rem;
}
```
**grid-gap**<br/>
A shorthand for row-gap and column-gap
```
.container {
  grid-template-columns: 100px 50px 100px;
  grid-template-rows: 80px auto 80px; 
  gap: 15px 10px;
}
```
**justify-items**
```
.container {
  justify-items: start | end | center | stretch;
}
```
**align-items**
```
.container {
  align-items: start | end | center | stretch;
}
```
**place-items**<br/>
Sets both the align-items and justify-items properties in a single declaration.
```
<align-items> / <justify-items> – The first value sets align-items, the second value justify-items
```
**justify-content**
```
.container {
  justify-content: start | end | center | stretch | space-around | space-between | space-evenly;    
}
```
**align-content**
```
.container {
  align-content: start | end | center | stretch | space-around | space-between | space-evenly;    
}
```
**place-content**<br/>
Sets both the align-content and justify-content properties in a single declaration.
```
<align-content> / <justify-content> – The first value sets align-content, the second value justify-content.
```
**grid-auto-columns**<br/>
**grid-auto-rows**
```
.item-a {
  grid-column: 1 / 2;
  grid-row: 2 / 3;
}
```
**grid-auto-flow** - 
```
.container {
  grid-auto-flow: row | column | row dense | column dense;
}
```
**grid**<br/>
grid-template-rows, grid-template-columns, grid-template-areas, grid-auto-rows, grid-auto-columns, and grid-auto-flow in single declaration
```
The following two code blocks are equivalent:

.container {
  grid: 100px 300px / 3fr 1fr;
}

.container {
  grid-template-rows: 100px 300px;
  grid-template-columns: 3fr 1fr;
}
```

## `Child items`
The children (i.e. direct descendants) of the grid container.

**grid-column-start**<br/>
**grid-column-end**<br/>
**grid-row-start**<br/>
**grid-row-end**<br/>
```
.item-a {
  grid-column-start: 2;
  grid-column-end: five;
  grid-row-start: row1-start;
  grid-row-end: 3;
}
```
**grid-column**<br/>
**grid-row**<br/>
Shorthand for grid-column-start + grid-column-end, and grid-row-start + grid-row-end, respectively.
```
.item-c {
    /* Start at line 2, go to line 6 */
    grid-column: 2 / 6;
    /* Start at line 2, go to line 6 */
    grid-row: 2 / 6;
}
```
**grid-area**<br/>
```
.item {
  grid-area: <name> | <row-start> / <column-start> / <row-end> / <column-end>;
}
```
**justify-self**<br/>
```
.item {
  justify-self: start | end | center | stretch;
}
```
**align-self**<br/>
```
.item {
  align-self: start | end | center | stretch;
}
```
**place-self**<br/>
```
Sets both the align-self and justify-self properties in a single declaration.

```

https://gridbyexample.com/examples/<br/>
https://www.freecodecamp.org/news/intro-to-css-grid-layout/
https://www.codecademy.com/learn/learn-css/modules/learn-css-grid/cheatsheet

# SASS

## `Preprocessing`
Sass lets you use features that don't exist in CSS yet like variables, nesting, mixins, inheritance and other nifty goodies that make writing CSS fun again.<br/>

## `Variables`
```
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```

## `Nesting`
```
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

## `Partials`
You can create partial Sass files that contain little snippets of CSS that you can include in other Sass files.<br/>
This is a great way to modularize your CSS and help keep things easier to maintain.<br/>
A partial is a Sass file named with a leading underscore.<br/>
You might name it something like _partial.scss.<br/>
The underscore lets Sass know that the file is only a partial file and that it should not be generated into a CSS file.<br/>
Sass partials are used with the @use rule.

## `Modules`
You don't have to write all your Sass in a single file. You can split it up however you want with the @use rule. This rule loads another Sass file as a module.
```
SCSS SYNTAX
// _base.scss
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```
```
// styles.scss
@use 'base';

.inverse {
  background-color: base.$primary-color;
  color: white;
}
```

## `Mixins`
A mixin lets you make groups of CSS declarations that you want to reuse throughout your site.
```
SCSS SYNTAX
@mixin transform($property) {
  -webkit-transform: $property;
  -ms-transform: $property;
  transform: $property;
}
.box { @include transform(rotate(30deg)); }
```

## `Extend/Inheritance`
Using @extend lets you share a set of CSS properties from one selector to another.
```
/* This CSS will print because %message-shared is extended. */
%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

// This CSS won't print because %equal-heights is never extended.
%equal-heights {
  display: flex;
  flex-wrap: wrap;
}

.message {
  @extend %message-shared;
}
```

## `Operators`
Sass has a handful of standard math operators like +, -, *, /, and %.
```
SCSS SYNTAX
.container {
  width: 100%;
}

article[role="main"] {
  float: left;
  width: 600px / 960px * 100%;
}

aside[role="complementary"] {
  float: right;
  width: 300px / 960px * 100%;
}
```
