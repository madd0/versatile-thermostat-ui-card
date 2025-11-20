# Developer Guide

## Quick Start with GitHub Codespaces

The fastest way to get started is using GitHub Codespaces:

1. Click the **Code** button on the repository
2. Select **Codespaces** tab
3. Click **Create codespace on [branch-name]**

The Codespace will automatically:
- Install Node.js 20
- Install all npm dependencies
- Set up recommended VS Code extensions
- Configure the development environment

Once ready, run:
```bash
npm start
```

## Local Development Setup

### Prerequisites

- Node.js 20.x or higher
- npm 9.x or higher

### Installation

1. Clone the repository:
```bash
git clone https://github.com/jmcollin78/versatile-thermostat-ui-card.git
cd versatile-thermostat-ui-card
```

2. Install dependencies:
```bash
npm install
```

### Development Commands

- **`npm start`** - Start development server with hot reload
- **`npm run build`** - Build for production
- **`npm run format`** - Format code with Prettier

### Project Structure

```
src/
├── versatile-thermostat-ui.ts          # Main card component
├── versatile-thermostat-ui-card-editor.ts  # Card editor
├── climate-card-config.ts              # Configuration types
├── const.ts                            # Constants
├── ha/                                 # Home Assistant utilities
└── localize/                           # Translation files
    ├── localize.ts                     # Localization logic
    └── languages/                      # Translation JSON files
```

### Working with Translations

This project uses [inlang](https://inlang.com/) for managing translations.

**Using Sherlock VS Code Extension (Recommended):**
1. The extension is automatically installed in Codespaces
2. Inline translation editing in your JSON files
3. See missing translations highlighted

**Using Fink Web Editor:**
```bash
# Open the inlang editor in your browser
npx @inlang/cli open editor
```

**Available Languages:**
- English (en) - Source language
- 23+ other languages (see `project.inlang.json`)

**Adding/Editing Translations:**
1. Edit files in `src/localize/languages/`
2. Use nested keys like: `"editor.card.climate.disable_circle"`
3. Run the inlang editor to see missing translations

### Building for Production

```bash
npm run build
```

This creates `dist/versatile-thermostat-ui-card.js` ready for distribution.

### Testing in Home Assistant

1. Build the card: `npm run build`
2. Copy `dist/versatile-thermostat-ui-card.js` to your HA config:
   ```
   <config>/www/community/versatile-thermostat-ui-card/
   ```
3. Refresh your browser with cache clear (Ctrl+F5)

### Code Style

- Uses Prettier for formatting
- Run `npm run format` before committing
- Format on save is enabled in VS Code

### Contributing

1. Create a new branch for your feature
2. Make your changes
3. Run `npm run format`
4. Test the build with `npm run build`
5. Submit a pull request

## Troubleshooting

**`npm install` fails:**
- Ensure you're using Node.js 20.x: `node --version`
- Delete `node_modules` and `package-lock.json`, then retry

**Build errors:**
- Check TypeScript errors: `npx tsc --noEmit`
- Ensure all dependencies are installed

**Translation issues:**
- Check `project.inlang.json` configuration
- Verify JSON syntax in language files

## Resources

- [Main Integration](https://github.com/jmcollin78/versatile_thermostat)
- [Home Assistant Developer Docs](https://developers.home-assistant.io/)
- [Lit Element Docs](https://lit.dev/)
- [inlang Documentation](https://inlang.com/documentation)
