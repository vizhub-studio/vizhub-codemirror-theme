# vizhub-codemirror-theme

A custom CodeMirror 6 theme designed for VizHub, providing a modern and visually appealing syntax highlighting experience.

## Development and supported scope

The package name is **`@vizhub/codemirror-theme`**. Its checked-in source is [`src/index.ts`](src/index.ts) and [`src/colors.ts`](src/colors.ts). Build the CommonJS and ESM outputs with:

```bash
npm ci
npm run build
```

**Test status:** `npm test` in the current package is a placeholder that deliberately exits with an error. There is no verified automated test suite to run; use an editor integration for visual review and check the exported symbols before publishing examples. This theme does not itself supply CodeMirror's editor, language extensions or collaboration backend.

## Installation

```bash
npm install @vizhub/codemirror-theme
```

## Usage

```javascript
import { vizhubTheme } from "@vizhub/codemirror-theme";
import { EditorView } from "codemirror";

// Use in CodeMirror setup
new EditorView({
  extensions: [vizhubTheme],
  // ... other configuration
});
```

## Features

- Modern, carefully chosen color palette
- Optimized for readability and visual hierarchy
- Support for matching/non-matching bracket highlighting
- Semi-bold weight for keywords and important syntax elements
- Customized colors for:
  - Keywords and operators
  - Strings and numbers
  - Functions and variables
  - Comments and metadata
  - And more...

## Customization

You can customize the theme by using the underlying `vizhubThemeInit` function:

```javascript
import { vizhubThemeInit } from "@vizhub/codemirror-theme";

const customizedTheme = vizhubThemeInit({
  theme: "dark", // or 'light'
  settings: {
    // Override default settings
  },
  styles: [
    // Add custom styles
  ],
});
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT © [Curran Kelleher](https://github.com/curran)
