[CSS Specificity](https://web.dev/learn/css/specificity/)

## Scoring each selector type

Each selector type earns points. You add all of these points up to calculate a selector's overall specificity.

### Universal selector

A `universal selector (*)` has no specificity and gets `0 points`. This means that any rule with 1 or more points will override it

```sh
* {
  color: red;
}
```

### Element or pseudo-element selector

An `element (type)` or `pseudo-element` selector gets `1 point of specificity`.

- Type selector

```sh
div {
  color: red;
}
```

- Pseudo-element selector

```sh
::selection {
  color: red;
}
```

### Class, pseudo-class, or attribute selector

A `class`, `pseudo-class` or `attribute` selector gets `10 points of specificity`.

- Class selector

```sh
.my-class {
  color: red;
}
```

- Pseudo-class selector

```sh
:hover {
  color: red;
}
```

- Attribute selector

```sh
[href='#'] {
  color: red;
}
```

The `:not()` pseudo-class itself adds nothing to the specificity calculation. However, `the selectors passed in as arguments` do get added to the specificity calculation.

```sh
div:not(.my-class) {
  color: red;
}
```

This sample would have `11 points of specificity` because it has `one type selector (div)` and `one class inside the :not()`.

- ID selector

An `ID` selector gets `100 points of specificity`, as long as you use an ID selector (`#myID`) and not an attribute selector ([id="myID"]).

```sh
#myID {
  color: red;
}
```

- Inline style attribute

CSS applied directly to the `style` attribute of the HTML element, gets a `specificity score of 1,000 points`. This means that in order to override it in CSS, you have to write an extremely specific selector.

```sh
<div style="color: red"></div>
```

- !important rule

Lastly, an `!important` at the end of a CSS value gets a specificity score of `10,000 points`. This is the highest specificity that one individual item can get.

An `!important` rule is applied to a CSS property, so everything in the overall rule (selector and properties) does not get the same specificity score.

```sh
.my-class {
  color: red !important; /* 10,000 points */
  background: white; /* 10 points */
}
```




















