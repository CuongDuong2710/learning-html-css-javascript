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



