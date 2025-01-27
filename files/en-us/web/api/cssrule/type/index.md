---
title: CSSRule.type
slug: Web/API/CSSRule/type
page-type: web-api-instance-property
tags:
  - API
  - CSSOM
  - Property
  - Reference
  - Read-only
  - Deprecated
browser-compat: api.CSSRule.type
---
{{APIRef("CSSOM")}}{{Deprecated_header}}

The read-only **`type`** property of the
{{domxref("CSSRule")}} interface is a deprecated property that returns an integer
indicating which type of rule the {{domxref("CSSRule")}} represents.

If you need to distinguish different types of CSS rule, a good alternative is to use [`constructor.name`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/name):

```js
const sheets = Array.from(document.styleSheets);
const rules = sheets.map((sheet) => Array.from(sheet.cssRules)).flat();

for (const rule of rules) {
  console.log(rule.constructor.name);
}
```

## Value

An integer which will be one of the type constants listed in the table below.

<table class="no-markdown">
  <tbody>
    <tr>
      <th>Type</th>
      <th>Value</th>
      <th>Rule-specific interface</th>
      <th>Comments and examples</th>
    </tr>
    <tr>
      <td><code>CSSRule.STYLE_RULE</code></td>
      <td><code>1</code></td>
      <td>{{domxref("CSSStyleRule")}}</td>
      <td>
        The most common kind of rule:<br /><code
          >selector { prop1: val1; prop2: val2; }</code
        >
      </td>
    </tr>
    <tr>
      <td><code>CSSRule.IMPORT_RULE</code></td>
      <td><code>3</code></td>
      <td>{{domxref("CSSImportRule")}}</td>
      <td>
        An {{cssxref("@import")}} rule. (Until the documentation is
        completed, see the interface definition in the Mozilla source code:
        <a
          href="http://mxr.mozilla.org/mozilla-central/source/dom/interfaces/css/nsIDOMCSSImportRule.idl#9"
          >nsIDOMCSSImportRule</a
        >.)
      </td>
    </tr>
    <tr>
      <td><code>CSSRule.MEDIA_RULE</code></td>
      <td><code>4</code></td>
      <td>{{domxref("CSSMediaRule")}}</td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.FONT_FACE_RULE</code></td>
      <td><code>5</code></td>
      <td>{{domxref("CSSFontFaceRule")}}</td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.PAGE_RULE</code></td>
      <td><code>6</code></td>
      <td>{{domxref("CSSPageRule")}}</td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.KEYFRAMES_RULE</code></td>
      <td><code>7</code></td>
      <td>
        {{domxref("CSSKeyframesRule")}}
        {{experimental_inline}}
      </td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.KEYFRAME_RULE</code></td>
      <td><code>8</code></td>
      <td>
        {{domxref("CSSKeyframeRule")}}
        {{experimental_inline}}
      </td>
      <td></td>
    </tr>
    <tr>
      <td><em>Reserved for future use</em></td>
      <td><code>9</code></td>
      <td></td>
      <td>Should be used to define color profiles in the future</td>
    </tr>
    <tr>
      <td><code>CSSRule.NAMESPACE_RULE</code></td>
      <td><code>10</code></td>
      <td>
        {{domxref("CSSNamespaceRule")}}
        {{experimental_inline}}
      </td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.COUNTER_STYLE_RULE</code></td>
      <td><code>11</code></td>
      <td>
        {{domxref("CSSCounterStyleRule")}}
        {{experimental_inline}}
      </td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.SUPPORTS_RULE</code></td>
      <td><code>12</code></td>
      <td>{{domxref("CSSSupportsRule")}}</td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.DOCUMENT_RULE</code></td>
      <td><code>13</code></td>
      <td>
        {{domxref("CSSDocumentRule")}}
        {{experimental_inline}}
      </td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.FONT_FEATURE_VALUES_RULE</code></td>
      <td><code>14</code></td>
      <td>{{domxref("CSSFontFeatureValuesRule")}}</td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.VIEWPORT_RULE</code></td>
      <td><code>15</code></td>
      <td>
        {{domxref("CSSViewportRule")}}
        {{experimental_inline}}
      </td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.REGION_STYLE_RULE</code></td>
      <td><code>16</code></td>
      <td>
        {{domxref("CSSRegionStyleRule")}}
        {{experimental_inline}}
      </td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.UNKNOWN_RULE</code></td>
      <td><code>0</code></td>
      <td>
        {{domxref("CSSUnknownRule")}} {{deprecated_inline}}
      </td>
      <td></td>
    </tr>
    <tr>
      <td><code>CSSRule.CHARSET_RULE</code></td>
      <td><code>2</code></td>
      <td><code>CSSCharsetRule</code> {{deprecated_inline}}</td>
      <td>(Removed in most browsers.)</td>
    </tr>
  </tbody>
</table>

## Examples

```js
let myRules = document.styleSheets[0].cssRules;
console.log(myRules[0].type);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
