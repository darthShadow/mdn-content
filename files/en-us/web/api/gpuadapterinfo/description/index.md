---
title: "GPUAdapterInfo: description property"
short-title: description
slug: Web/API/GPUAdapterInfo/description
page-type: web-api-instance-property
browser-compat: api.GPUAdapterInfo.description
---

{{APIRef("WebGPU API")}}{{SecureContext_Header}}{{AvailableInWorkers}}

The **`description`** read-only property of the
{{domxref("GPUAdapterInfo")}} interface returns a human-readable string describing the adapter, or an empty string if it is not available.

## Value

A string.

## Examples

```js
const adapter = await navigator.gpu.requestAdapter();
if (!adapter) {
  throw Error("Couldn't request WebGPU adapter.");
}

const adapterInfo = adapter.info;
console.log(adapterInfo.description);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- The [WebGPU API](/en-US/docs/Web/API/WebGPU_API)
