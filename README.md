# Simple Selector

1. [Universal selector](https://github.com/CuongDuong2710/learning-html-css-javascript/blob/master/README.md#simple-selector-1)
2. [Type selector](https://github.com/CuongDuong2710/learning-html-css-javascript/blob/master/README.md#type-selector)
3. [Class selector(]https://github.com/CuongDuong2710/learning-html-css-javascript/blob/master/README.md#class-selector)
4. [ID selector](https://github.com/CuongDuong2710/learning-html-css-javascript/blob/master/README.md#id-selector)
5. [Attribute selector](https://github.com/CuongDuong2710/learning-html-css-javascript/blob/master/README.md#attribute-selector)
6. [Grouping selector](https://github.com/CuongDuong2710/learning-html-css-javascript/blob/master/README.md#grouping-selector)

# Pseudo-classes and pseudo-elements

1. Pseudo-classes
2. Pseudo-elements

# Complex selector

1. Combinators
2. Compound selectors

---

# Simple Selector

## Universal selector

A universal selector—also known as a wildcard—matches any element.

```sh
* {
  color: hotpink;
}
```

This rule causes every HTML element on the page to have hotpink text.

## Type selector

A type selector matches a HTML element directly.

```sh
section {
  padding: 2em;
}
```

This rule causes every `<section>` element to have 2em of padding on all sides.

## Class selector

A HTML element can have one or more items defined in their `class` attribute. The class selector matches any element that has that class applied to it.

```sh
<div class="my-class"></div>
<button class="my-class"></button>
<p class="my-class"></p>
```

Any element that has the class applied to it will get colored red:

```sh
.my-class {
  color: red;
}
```

## ID selector

An HTML element with an `id` attribute should be the only element on a page with that ID value. You select elements with an ID selector like this:

```sh
#rad {
  border: 1px solid blue;
}
```

This CSS would apply a blue border to the HTML element that has an id of rad, like this:

```sh
<div id="rad"></div>
```

## Attribute selector

You can look for elements that have a certain HTML attribute, or have a certain value for an HTML attribute. nstruct CSS to look for attributes by wrapping the selector with square brackets (`[ ]`).

```sh
[data-type='primary'] {
  color: red;
}
```

This CSS looks for all elements that have an attribute of data-type with a value of primary, like this:

```sh
<div data-type="primary"></div>
```

Instead of looking for a specific value of data-type, you can also look for elements with the attribute present

```sh
[data-type] {
  color: red;
}
```

```sh
<div data-type="primary"></div>
```

Both of these `<div>` elements will have red text.


<div data-type="secondary"></div>

Along with case operators, you have access to operators that match portions of strings inside attribute values.

```sh
/* A href that contains "example.com" */
[href*='example.com'] {
  color: red;
}

/* A href that starts with https */
[href^='https'] {
  color: green;
}

/* A href that ends with .com */
[href$='.com'] {
  color: blue;
}
```

## Grouping selectors

A selector doesn't have to match only a single element. You can group multiple selectors by separating them with commas:

```sh
strong,
em,
.my-class,
[lang] {
  color: red;
}
```

This example extends the color change to both `<strong>` elements and `<em>` elements. It's also extended to a class named `.my-class`, and an element that has a `lang` attribute.

