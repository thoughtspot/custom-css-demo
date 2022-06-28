# Custom Styling in ThoughtSpot Everywhere (Embed)

Guideline to override ThoughtSpot's style to match the parent application's defaults.

## Installation

### 1. Customizing the application.
Thoughtspot supports customization of key UI components, such as application logo & favicon, font style for charts and tables, background color for the UI, background color of the navigation panel, the color palette for your charts, and a few more. To learn how to use these controls, kindly refer to the follow section of the product documentation: [Customize layout and styles](https://developers.thoughtspot.com/docs/?pageid=customize-style).

### 2. Customizing the application style guide

This feature lets developers override the CSS in their embed deployment, effectively allowing them to thoroughly customize the look and feel of their embedded analytics to better align with their parent app's branding and styling guidelines.
As this is CSS based, this can be used to customize most parts of the UI visually.

To try this out in the Developer Playground:
1. Go to Full App Embed in [The Developer Playground](https://try-everywhere.thoughtspot.cloud/v2/#/everywhere/playground/fullApp)
2. In the _init_ part of the code block in the bottom left part of the page, add one line to point to our template css file (initiated via the **customCssUrl** call):

```js
// Initialize embed configuration
init({
  thoughtSpotHost:
    /*param-start-hosturl*/"https://try-everywhere.thoughtspot.cloud"/*param-end-hosturl*/,
  authType: AuthType.None,
  customCssUrl:"cdn.jsdelivr.net/gh/thoughtspot/custom-css-demo/complete.css"
});
```
#### Important note: This feature directly overrides CSS in the application. As such, these overrides may stop functioning in future cluster updates and this method is not fully supported. The ThoughtSpot team is working on a long term solution to provide a framework to these overrides. Reach out to us to provide feedback!
