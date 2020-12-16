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