# Intermediate CSS

## CSS Cascades

When multiple CSS rules conflict (target the same element) the one higher in the hierarchy is the style that will get chosen.

The hierarchy works in this order:

1. Inline Style
2. Internal Styles
3. External Stylesheet

You can understand how the cascade works by these 4 factors:
- Position (Two properties in a row, it takes the one lower)
- Specificity
    1. IDs
    2. Elements with attribute
    3. Classes
    4. Elements
- Type
    1. Inline CSS
    2. Internal CSS
    3. External CSS
- Importance (if it contains the !important keyword)

## Combining CSS Selectors

We can combine the Selectors to target specific elements

```css
    div p{
        color: red;
    }
```

This will target all paragraph elements that are inside a div no matter how deep it is in the hierarchy

You can even combine it with classes IDs or attributes

or you can target multiple element using comma

```css
div, p {
    color: blue;
}
```
This will target all divs AND paragraphs

You can use > in order to target a direct child
```css
    div > p {
        color: blueviolet;
    }
```
All p tags that are direct child of the div will be targeted

Chaining is used to target specific elements, it makes sure all selectors are true
```css
    div.box.purple{
        background-color: purple;
    }
```

It looks for a div that ALSO has the class box AND the class purple

You can Combine all of these methods together to target something even more specific

## CSS Positioning

There are 4 types of positions:
- Static
- Relative
- Absolute
- Z-index
- Fixed

### Static
This mean that the element will flow as the default HTML elements would

### Relative
The element would be positioned relatively to its default (Static) position

### Absolute
The element would be positioned relatively to its ancestor (the parent element), if there is no parent element the position would relative to the body tag which is to top left corner of the page.

If the ancestor has no relative position then it would move to a higher ancestor until it find one or reaches the body

### Z-index
It is the layering of the elements AKA which element goes on top of the other

### Fixed
Functions the same way as absolute however it stays in the same position even after scrolling.

## Flag project
<a href="./7.3 Flag Project/7.3 CSS Flag Project/index.html">Final project for this section</a>
