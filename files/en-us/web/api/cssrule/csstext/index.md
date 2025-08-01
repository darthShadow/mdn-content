---
title: "CSSRule: cssText property"
short-title: cssText
slug: Web/API/CSSRule/cssText
page-type: web-api-instance-property
browser-compat: api.CSSRule.cssText
---

{{APIRef("CSSOM") }}

The **`cssText`** property of the {{domxref("CSSRule")}}
interface returns the actual text of a {{domxref("CSSStyleSheet")}} style-rule.

> [!NOTE]
> Do not confuse this property with element-style
> {{domxref("CSSStyleDeclaration.cssText")}}.

Be aware that this property used to be mutable but is now read-only. Attempting to
set it _does absolutely nothing_, and doesn't even emit a warning or error.
Furthermore, it has no settable sub-properties. Therefore, to modify it, use the
stylesheet's {{domxref("CSSRuleList", "cssRules[index]")}} properties
{{domxref("CSSStyleRule.selectorText", ".selectorText")}} and
{{domxref("CSSStyleRule.style", ".style")}} (or its sub-properties). See [Using dynamic styling information](/en-US/docs/Web/API/CSS_Object_Model/Using_dynamic_styling_information) for details.

## Value

A string containing the actual text of the {{domxref("CSSStyleSheet")}} rule.

## Examples

```css
body {
  background-color: darkblue;
}
```

```js
let stylesheet = document.styleSheets[0];
console.log(stylesheet.cssRules[0].cssText); // body { background-color: darkblue; }
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
