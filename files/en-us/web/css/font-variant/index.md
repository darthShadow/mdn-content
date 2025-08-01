---
title: font-variant
slug: Web/CSS/font-variant
page-type: css-shorthand-property
browser-compat: css.properties.font-variant
sidebar: cssref
---

The **`font-variant`** CSS [shorthand property](/en-US/docs/Web/CSS/CSS_cascade/Shorthand_properties) allows you to set all the font variants for a font.

You can also set the `<font-variant-css2>` values of `font-variant` defined in CSS Level 2.1, (that is, `normal` or `small-caps`), by using the [`font`](/en-US/docs/Web/CSS/font) shorthand.

{{InteractiveExample("CSS Demo: font-variant")}}

```css interactive-example-choice
font-variant: normal;
```

```css interactive-example-choice
font-variant: no-common-ligatures proportional-nums;
```

```css interactive-example-choice
font-variant: common-ligatures tabular-nums;
```

```css interactive-example-choice
font-variant: small-caps slashed-zero;
```

```html interactive-example
<section id="default-example">
  <div id="example-element">
    <p>Difficult waffles</p>
    <table>
      <tr>
        <td><span class="tabular">0O</span></td>
      </tr>
      <tr>
        <td><span class="tabular">3.14</span></td>
      </tr>
      <tr>
        <td><span class="tabular">2.71</span></td>
      </tr>
    </table>
  </div>
</section>
```

```css interactive-example
@font-face {
  font-family: "Fira Sans";
  src:
    local("FiraSans-Regular"),
    url("/shared-assets/fonts/FiraSans-Regular.woff2") format("woff2");
  font-weight: normal;
  font-style: normal;
}

section {
  font-family: "Fira Sans", sans-serif;
  margin-top: 10px;
  font-size: 1.5em;
}

#example-element table {
  margin-left: auto;
  margin-right: auto;
}

.tabular {
  border: 1px solid;
}
```

## Constituent properties

This property is a shorthand for the following CSS properties:

- [`font-variant-alternates`](/en-US/docs/Web/CSS/font-variant-alternates)
- [`font-variant-caps`](/en-US/docs/Web/CSS/font-variant-caps)
- [`font-variant-east-asian`](/en-US/docs/Web/CSS/font-variant-east-asian)
- [`font-variant-emoji`](/en-US/docs/Web/CSS/font-variant-emoji)
- [`font-variant-ligatures`](/en-US/docs/Web/CSS/font-variant-ligatures)
- [`font-variant-numeric`](/en-US/docs/Web/CSS/font-variant-numeric)
- [`font-variant-position`](/en-US/docs/Web/CSS/font-variant-position)

## Syntax

```css
font-variant: small-caps;
font-variant: common-ligatures small-caps;

/* Global values */
font-variant: inherit;
font-variant: initial;
font-variant: revert;
font-variant: revert-layer;
font-variant: unset;
```

### Values

- `normal`
  - : Specifies a normal font face. Each longhand property has an initial value of `normal`.

- `none`
  - : Sets the value of the [`font-variant-ligatures`](/en-US/docs/Web/CSS/font-variant-ligatures) as `none` and the values of the other longhand properties as `normal`, their initial value.

- `<common-lig-values>`, `<discretionary-lig-values>`, `<historical-lig-values>`, `<contextual-alt-values>`
  - : Specifies the keywords related to the [`font-variant-ligatures`](/en-US/docs/Web/CSS/font-variant-ligatures) longhand property. The possible values are `common-ligatures`, `no-common-ligatures`, `discretionary-ligatures`, `no-discretionary-ligatures`, `historical-ligatures`, `no-historical-ligatures`, `contextual`, and `no-contextual`.

- `stylistic()`, `historical-forms`, `styleset()`, `character-variant()`, `swash()`, `ornaments()`, `annotation()`
  - : Specifies the keywords and functions related to the [`font-variant-ligatures`](/en-US/docs/Web/CSS/font-variant-ligatures) longhand property.

- `small-caps`, `all-small-caps`, `petite-caps`, `all-petite-caps`, `unicase`, `titling-caps`
  - : Specifies the keywords and functions related to the [`font-variant-caps`](/en-US/docs/Web/CSS/font-variant-caps) longhand property. The `small-caps` value is the only non-`normal` font variant valid within the {{cssxref("font")}} shorthand property.

- `<numeric-figure-values>`, `<numeric-spacing-values>`, `<numeric-fraction-values>`, `ordinal`, `slashed-zero`
  - : Specifies the keywords related to the [`font-variant-numeric`](/en-US/docs/Web/CSS/font-variant-numeric) longhand property. The possible values are `lining-nums`, `oldstyle-nums`, `proportional-nums`, `tabular-nums`, `diagonal-fractions`, `stacked-fractions`, `ordinal`, and `slashed-zero`.

- `<east-asian-variant-values>`, `<east-asian-width-values>`, `ruby`
  - : Specifies the keywords related to the [`font-variant-east-asian`](/en-US/docs/Web/CSS/font-variant-east-asian) longhand property. The possible values are `jis78`, `jis83`, `jis90`, `jis04`, `simplified`, `traditional`, `full-width`, `proportional-width`, and `ruby`.

- `sub`, `super`
  - : Specifies the keywords and functions related to the [`font-variant-position`](/en-US/docs/Web/CSS/font-variant-position) longhand property.

- `text`, `emoji`, `unicode`
  - : Specifies the keywords and functions related to the [`font-variant-emoji`](/en-US/docs/Web/CSS/font-variant-emoji) longhand property.

## Formal definition

{{cssinfo}}

## Formal syntax

{{csssyntax}}

## Examples

### Setting the small-caps font variant

#### HTML

```html
<p class="normal">Firefox rocks!</p>
<p class="small">Firefox rocks!</p>
```

#### CSS

```css
p.normal {
  font-variant: normal;
}
p.small {
  font-variant: small-caps;
}
```

#### Result

{{ EmbedLiveSample('Setting the small-caps font variant') }}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{cssxref("text-transform")}}
- {{cssxref("text-combine-upright")}}
- {{cssxref("text-orientation")}}
- SVG {{SVGAttr("font-variant")}} attribute
