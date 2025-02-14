---
title: GPUShaderModule.label
slug: Web/API/GPUShaderModule/label
page-type: web-api-instance-property
status:
  - experimental
browser-compat: api.GPUShaderModule.label
---

{{APIRef("WebGPU API")}}{{SeeCompatTable}}

The **`label`** property of the
{{domxref("GPUShaderModule")}} interface provides a label that can be used to identify the object, for example in {{domxref("GPUError")}} messages or console warnings.

This can be set by providing a `label` property in the descriptor object passed into the originating {{domxref("GPUDevice.createShaderModule()")}} call, or you can get and set it directly on the `GPUShaderModule` object.

## Value

A string. If this has not been previously set as described above, it will be an empty string.

## Examples

Setting and getting a label via `GPUShaderModule.label`:

```js
// ...

const shaderModule = device.createShaderModule({
  code: shaders,
});

shaderModule.label = "myshader";

console.log(shaderModule.label); // "myshader"
```

Setting a label via the originating {{domxref("GPUDevice.createShaderModule()")}} call, and then getting it via `GPUShaderModule.label`:

```js
// ...

const shaderModule = device.createShaderModule({
  code: shaders,
  label: "myshader",
});

console.log(shaderModule.label); // "myshader"
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- The [WebGPU API](/en-US/docs/Web/API/WebGPU_API)
