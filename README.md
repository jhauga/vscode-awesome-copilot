# Awesome GitHub Copilot Browser

Source Extension [![VS Marketplace](https://img.shields.io/visual-studio-marketplace/v/timheuer.awesome-copilot?label=VS%20Code%20Marketplace&color=brightgreen&logo=visualstudiocode)](https://marketplace.visualstudio.com/items?itemName=TimHeuer.awesome-copilot)

A VS Code extension that allows you to browse, preview, and download GitHub Copilot customizations from the [awesome-copilot repository](https://github.com/github/awesome-copilot).

## Features

- **🔍 Browse**: Explore chat modes, instructions, prompts, agents, and skills in a convenient tree view
- **� Search**: Quickly find files with real-time filtering across all categories
- **📖 Preview**: View file content before downloading
- **⬇️ Download**: Save files to appropriate `.github/` folders in your workspace
- **🔃 Refresh**: Update repository data with manual refresh
- **💾 Caching**: Smart caching for better performance

| Browse and Search | | Cache Management, Download, Preview, and Refresh |
| --- | --- | --- |
| ![Search Feature Demo](resources/searchFeature.gif) |  | ![features.png](/resources/features.png) |

## How to Use

1. **Open the Extension**: Click the new Activity Bar icon (checkmark document) titled **Awesome Copilot**. (Previously this view appeared under Explorer; it now has its own dedicated container with a proper icon.)
2. **Search Files**: Use the search bar at the top to filter files across all categories in real-time
3. **Browse Categories**: Expand Collections, Instructions, Prompts, Agents, or Skills sections
4. **Preview Content**: Click the preview icon on any file to see its content
5. **Download Files**: Click the download icon to save files to your workspace
6. **Refresh Data**: Click the refresh icon in the view title to update repository data

## Folder Structure

Downloaded files are organized in your workspace as follows:

- **Collections** → `.github/collections/`
- **Instructions** → `.github/instructions/`
- **Prompts** → `.github/prompts/`
- **Agents** → `.github/agents/`
- **Skills** → `.github/skills/` (entire folders with SKILL.md and supporting files)

These folders will be created automatically if they don't exist.

**Note:** Skills are unique in that each skill is a complete folder containing a `SKILL.md` file and potentially other supporting files. When you download a skill, the entire folder structure is preserved.

## Requirements

- VS Code version 1.103.0 or higher
- Internet connection to fetch repository data
- A workspace folder open in VS Code (for downloads)

## Extension Commands

- `Refresh`: Update repository data from GitHub
- `Download`: Save a file to your workspace
- `Preview`: View file content in VS Code

---

## Development

This extension was built with:

- TypeScript
- VS Code Extension API
- Axios for HTTP requests
- ESBuild for bundling

### Building

```bash
npm install
npm run compile
```

### Testing

```bash
npm run test
```

## UI Placement / Custom View Container

The extension contributes a custom Activity Bar view container named **Awesome Copilot**. If you prefer to move or hide it:

- Right-click the Activity Bar to toggle visibility.
- Drag the view into a different location if desired (VS Code will persist your layout).

If you previously dragged the old Explorer-based view into the Activity Bar and saw a generic label/icon, this update fixes that by supplying a dedicated container with themed icons (light/dark).

**Enjoy browsing and using awesome GitHub Copilot customizations!**

## License

MIT
