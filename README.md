# quintype-node-fonts
Simple Utility to Inline Fonts Without Affecting Server Response Time

## Usage

```javascript
import {FontCache} from "@quintype/fonts";

const fontCache = new FontCache();

// First time
fontCache.get("https://fonts.googleapis.com/css?family=Merriweather:300,400,700|Open+Sans:300,400,600,700")
// <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Merriweather:300,400,700|Open+Sans:300,400,600,700" />

// After some time
fontCache.get("https://fonts.googleapis.com/css?family=Merriweather:300,400,700|Open+Sans:300,400,600,700")
// <style type="text/css">inline-css-here</style>
```
