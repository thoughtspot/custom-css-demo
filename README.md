# Custom Styling in ThoughtSpot Everywhere (Embed)

Guideline to override ThoughtSpot's default styles to match the parent application's defaults.

## Installation

### 1. Customizing the application.
Thoughtspot supports customization of key UI components today, such as application logo & favicon, font style for charts and tables, background color for the UI, background color of the navigation panel, the color palette for your charts, and a few more. To learn how to use these controls, kindly refer to the product documentation: [Customize layout and styles](https://developers.thoughtspot.com/docs/?pageid=customize-style)

### 2. Customizing the application style guide

This feature lets developers override the CSS in their embed deployment, effectively allowing them to thoroughly customize the look and feel of their ThoughtSpot embedded analytics to better align with their general app's branding and styling guidelines.
As this is CSS based, this can be used to customize most parts of the UI visually (not behaviorally).

To try this out in the Developer Playground:
1. Go to Full App Embed in [The Developer Playground](https://try-everywhere.thoughtspot.cloud/v2/#/everywhere/playground/fullApp)
2. In the _init_ part of the code block, add a pointer to our template css file (initiated via the **CustomCss** call):

```js
// Write Javascript code!
init({
  thoughtSpotHost:
    /*param-start-hosturl*/"https://try-everywhere.thoughtspot.cloud"/*param-end-hosturl*/,
  authType: AuthType.None,
  customCssUrl:"cdn.jsdelivr.net/gh/thoughtspot/custom-css-demo/complete.css"
});
```
