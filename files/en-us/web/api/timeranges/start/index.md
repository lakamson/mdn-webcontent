---
title: "TimeRanges: start() method"
short-title: start()
slug: Web/API/TimeRanges/start
page-type: web-api-instance-method
browser-compat: api.TimeRanges.start
---

{{APIRef("DOM")}}

The **`start()`** method of the {{domxref("TimeRanges")}} interface returns the time offset (in seconds) at which a specified time range begins.

## Syntax

```js-nolint
start(index)
```

### Parameters

- `index`
  - : The range number to return the starting time for.

### Return value

A number.

### Exceptions

- `IndexSizeError` {{domxref("DOMException")}}
  - : Thrown if the specified index doesn't correspond to an
    existing range.

## Examples

Given a video element with the ID "myVideo":

```js
const v = document.getElementById("myVideo");

const buf = v.buffered;

const numRanges = buf.length;

if (buf.length === 1) {
  // only one range
  if (buf.start(0) === 0 && buf.end(0) === v.duration) {
    // The one range starts at the beginning and ends at
    // the end of the video, so the whole thing is loaded
  }
}
```

This example looks at the time ranges and looks to see if the entire video has been
loaded.

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
