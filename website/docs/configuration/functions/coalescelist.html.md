---
layout: "functions"
page_title: "coalescelist function"
sidebar_current: "docs-funcs-collection-coalescelist"
description: |-
  The coalescelist function takes any number of list arguments and returns the
  first one that isn't empty.
---

# `coalescelist` Function

`coalescelist` takes any number of list arguments and returns the first one
that isn't empty.

## Examples

```
> coalesce(["a", "b"], ["c", "d"])
[
  "a",
  "b",
]
> coalesce([], ["c", "d"])
[
  "c",
  "d",
]
```

To perform the `coalesce` operation with a list of lists, use the `...`
symbol to expand the outer list as arguments:

```
> coalesce([[], ["c", "d"]]...)
[
  "c",
  "d",
]
```

## Related Functions

* [`coalesce`](./coalesce.html) performs a similar operation with string
  arguments rather than list arguments.
