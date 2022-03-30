# custom-css-demo
Custom CSS Demo

```js
import { init, AuthType } from "@thoughtspot/visual-embed-sdk";

// Initialize ThoughtSpot Visual embed sdk
init({
  thoughtSpotHost: "<host>",
  authType: AuthType.NONE,
  customCssUrl: "cdn.jsdelivr.net/gh/thoughtspot/custom-css-demo/complete.css"
});

// .. Embedding goes here.
```
