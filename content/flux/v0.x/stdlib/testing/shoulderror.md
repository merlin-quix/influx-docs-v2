---
title: testing.shouldError() function
description: >
  `testing.shouldError()` calls a function catches any error and checks that the error matches the expected value.
menu:
  flux_0_x_ref:
    name: testing.shouldError
    parent: testing
    identifier: testing/shouldError
weight: 101
flux/v0.x/tags: [tests]
introduced: 0.174.0
---

<!------------------------------------------------------------------------------

IMPORTANT: This page was generated from comments in the Flux source code. Any
edits made directly to this page will be overwritten the next time the
documentation is generated. 

To make updates to this documentation, update the function comments above the
function definition in the Flux source code:

https://github.com/influxdata/flux/blob/master/stdlib/testing/testing.flux#L256-L260

Contributing to Flux: https://github.com/influxdata/flux#contributing
Fluxdoc syntax: https://github.com/influxdata/flux/blob/master/docs/fluxdoc.md

------------------------------------------------------------------------------->

`testing.shouldError()` calls a function catches any error and checks that the error matches the expected value.



##### Function type signature

```js
(fn: () => A, want: string) => stream[{v: string, _diff: string}]
```

{{% caption %}}For more information, see [Function type signatures](/flux/v0.x/function-type-signatures/).{{% /caption %}}

## Parameters

### fn
({{< req >}})
Function to call.



### want
({{< req >}})
Expected error string.




## Examples

### Test die function errors

```js
import "testing"

testing.shouldError(fn: () => die(msg: "error message"), want: "error message")

```
