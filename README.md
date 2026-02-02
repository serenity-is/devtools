# Serenity Developer Tools

A Chromium DevTools extension for inspecting and debugging [Serenity](https://serenity.is/) applications.

![Serenity DevTools](src/devtools/devtools.png)

## Features

- Widget Inspector: Browse and inspect Serenity widgets in your application
- Element Picker: Click on elements to find their corresponding widget
- Property Viewer: View widget properties, options, and state
- DOM Highlighting: Highlight DOM elements associated with widgets
- Scroll Into View: Quickly navigate to widget elements in the page
- View Source: Instantly inspect the source code for widget constructors and methods.

## Installation

### From Chrome Web Store
[Download from Chrome Web Store](https://chromewebstore.google.com/detail/serenity-developer-tools/andpiimofmnbnphjdcknpgdhkgamlggh)

### From Source

1. Clone this repository
2. Install dependencies:
   ```bash
   pnpm install
   ```
3. Build the extension:
   ```bash
   pnpm run build
   ```
4. Load the extension in Chrome:
   - Navigate to `chrome://extensions`
   - Enable "Developer mode"
   - Click "Load unpacked"
   - Select the `dist` folder

### Development

Start the development server with hot reload:

```bash
pnpm run watch
```

Run with a test browser:

```bash
pnpm run dev:chromium
```

## Usage

1. Open Chrome DevTools (F12).
2. Navigate to the `Serenity` panel.
3. Browse the widget tree or use the inspector to select widgets on the page, or press <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>X</kbd> to toggle inspect widget mode.
5. Click on any widget to view its details, properties, and associated DOM element. The selected widget is saved to the developer console as `$$0`.

## Scripts

| Command | Description |
|---------|-------------|
| `pnpm run build` | Build for production |
| `pnpm run watch` | Development mode with hot reload |
| `pnpm run dev:chromium` | Run in Chromium with web-ext |
| `pnpm run lint` | Run ESLint |
| `pnpm run check` | TypeScript type checking |

