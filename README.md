# Simple Selector

1. [Universal selector](https://github.com/CuongDuong2710/learning-html-css-javascript/blob/master/README.md#simple-selector-1)
2. [Type selector](https://github.com/CuongDuong2710/learning-html-css-javascript/blob/master/README.md#type-selector)
3. Class selector
4. ID selector
5. Attribute selector
6. Grouping selector

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


