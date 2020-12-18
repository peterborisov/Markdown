# CSS Grid
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
  grid-template-columns: 40px 50px auto 50px 40px;
  grid-template-rows: 25% 100px auto;
}
```
**grid-template-areas**
```
.container {
  grid-template-areas: 
    "header header header header"
    "main main . sidebar"
    "footer footer footer footer";
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
  grid-template-columns: 100px 50px 100px;
  grid-template-rows: 80px auto 80px; 
  column-gap: 10px;
  row-gap: 15px;
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
  grid-column: 3 / span 2;
  grid-row: third-line / 4;
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
Sets both the align-self and justify-self properties in a single declaration.
```

```