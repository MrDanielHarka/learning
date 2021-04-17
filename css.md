# CSS

## Q & A

Q1: What is the best way of applying CSS to HTML?\
A1: It is by using external style sheets. Best practice to separate different parts of the code. This way the CSS can be applied to multiple html pages.

## Notes

### General

CSS (Cascading Style Sheets) is a language for describing how documents are presented visually, how they are arranged and styled.

### CSS Rules

Almost everything we do in CSS follows this pattern:

``` css
selector {
    property: value;
}
```

Ways of including CSS:
- Inline (Not recommended)
- The \<style> element (Not recommended)
- External Style Sheet (Recommended)

**Semi colons are crucial for applying styles!**

### Selectors

**Universal Selector**

Selects everything.

``` css
* {
    property: value;
}
```

**Element Selector**

Selects all elements of the chosen type.

``` css
img {
    property: value;
}
```

**Selector list**

Selects multiple elements.

``` css
h1, h2 {
    property: value;
}
```

**ID Selector**

Selects elements with an id.

``` css
#my-id {
    property: value;
}
```

**Class Selector**

Selects elements with a class.

``` css
.my-class {
    property: value;
}
```

**Descendent Selectors**

Selects \<a> nested inside an \<li>.

``` css
li a {
    property: value;
}
```

**Adjacent Selector**

Selects only paragraphs that are immediately followed by an \<h1>.

``` css
h1 + p {
    property: value;
}
```

**Direct Child Selector**

Selects only the \<li>s that are direct children of a \<div> element.

``` css
div > li {
    property: value;
}
```

**Attribute Selector**

Selects all input elements where the type attribute is set to "text".

``` css
input[type="text"] {
    property: value;
}
```

### Pseudo Classes

Keyword added to a selector that specifies a special state of the selected element(s).

**Hover**

Selects any \<a> when hovered.

``` css
button:hover {
    property: value;
}
```

**Active**

Selects any \<a> when being activated.

``` css
a:active {
    property: value;
}
```
**Checked**

Selects any checkbox and radio button when being activated.

``` css
input[type="radio"]:checked,
input[type="checkbox"]:checked {
    property: value;
}
```

Selects any n-th .class element with the specified type.

``` css
.class:n-th-of-type(3) {
    property: value;
}
```

### Psuedo Elements