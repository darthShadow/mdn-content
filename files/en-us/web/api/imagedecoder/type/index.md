---
title: "ImageDecoder: type property"
short-title: type
slug: Web/API/ImageDecoder/type
page-type: web-api-instance-property
browser-compat: api.ImageDecoder.type
---

{{securecontext_header}}{{APIRef("WebCodecs API")}}{{AvailableInWorkers("window_and_dedicated")}}

The **`type`** read-only property of the {{domxref("ImageDecoder")}} interface reflects the [MIME type](/en-US/docs/Web/HTTP/Guides/MIME_types) configured during construction.

## Value

A string containing the configured [MIME type](/en-US/docs/Web/HTTP/Guides/MIME_types).

## Examples

The following example prints the value of `type` to the console.

```js
console.log(imageDecoder.type);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
