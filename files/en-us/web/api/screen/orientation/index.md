---
title: Screen.orientation
slug: Web/API/Screen/orientation
page-type: web-api-instance-property
tags:
  - API
  - CSSOM View
  - Experimental
  - Property
  - Read-only
  - Screen Orientation
  - screen
browser-compat: api.Screen.orientation
---
{{APIRef("Screen Orientation API")}}

The **`orientation`** read-only property of the
{{DOMxRef("Screen")}} interface returns the current orientation of the screen.

## Value

An instance of {{DOMxRef("ScreenOrientation")}} representing the orientation of the
screen.

Note that older, prefixed versions returned a string equivalent to
{{DOMxRef("ScreenOrientation.type")}}.

## Examples

```js
var orientation = (screen.orientation || {}).type || screen.mozOrientation || screen.msOrientation;

if (orientation === "landscape-primary") {
  console.log("That looks good.");
} else if (orientation === "landscape-secondary") {
  console.log("Mmmh… the screen is upside down!");
} else if (orientation === "portrait-secondary" || orientation === "portrait-primary") {
  console.log("Mmmh… you should rotate your device to landscape");
} else if (orientation === undefined) {
  console.log("The orientation API isn't supported in this browser :(");
}
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{DOMxRef("ScreenOrientation")}}
- {{DOMxRef("Screen.orientationchange_event", "orientationchange")}} event
- [Managing screen orientation](/en-US/docs/Web/API/CSS_Object_Model/Managing_screen_orientation)
