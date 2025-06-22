# Advanced CSS

## CSS Display

Three different display values:
- inline (As much space as the element needs)
- block (The block takes the full width of the page)
- inline-block (it allows to set the height and width and elements can align next to each other, a mix of both)

The span takes by default the inline value

## CSS Float

It allows to wrap text around an element, Helps achieve L shaped text that are wrapped around an image

```css
 img{
    float:left;
 }
```

The text will now wrap around the image on the right.

```css
 footer{
    clear: left;
 }
```

it allows the element to not wrap around the floated image if we don't want to.

However floats are not recommended due to new technologies, bootstrap, grids and others.

## Responsiveness

The layout should change depending on the screen sizes, desktop, mobiles, tablets and others.

4 ways to achieve responsiveness:
- Media Queries
- CSS Grid
- CSS FlexBox
- External Frameworks: bootstrap...

### Media Queries

```css
    @media (max-width: 900px) {
        css at width <= 900px;
    }
```

This is how media queries look like

### Grid containers

```css
    .grid-container{
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 100px 200px 200px;
        gap: 30px;
    }

    .cell1{
        grid-column: span 2;
    }

    .others {

    }
```
The grid is a 2x3 as you can see from the template values, the fr means 1 fraction which is a unit, or you can use the px which is used for the rows. the gap will set the spacing between each cell

This will make a cell that spans across 2 columns and under it multiple cells.

### FlexBox

```css
    .flex-container{
        display: flex;
    }

    .card{
        flex: 1
    }
    .card2{
        flex: 0.5;
    }

```

the flex is the weight distribution of the cell, so card 1 is double the size of card 2. You can use flex-containers to display everything in a single row or column

### Bootstrap
Bootstrap has preset classes that once applied to your element their styling will be automatically applied, however bootstrap is an external library so you would have to import it into your HTML file.

Bootstrap is built on flex-box, where the website is divided on 12 portions thats how their units work

## Media Queries

You can combine media queries to have a specific range of width:

```css
    @media (min-width: 600px) and (max-width: 900px){
        /* CSS */
    }
```

Some people use screen orientation however it is not recommended

```css
    @media screen(orientation: landscape){
        /* CSS */
    }
```

or print which is the same as screen

```css
    @media print(orientation: landscape){
        /* CSS */
    }
```

## Web Design Agency project
<a href="./7.3 Flag Project/7.3 CSS Flag Project/index.html">Final project for this section</a>
