<div align="center">
  <img src="assets/legend17-editor.png" width="220" alt="Legend17 Editor" />

  # Legend17 Editor

  **Comfortable UI pipeline for teams building with PixiJS 8.**

  Prefabs for artists. Type-safe code for developers.

  [![Latest release](https://img.shields.io/github/v/release/harlamov/editor?display_name=tag&style=flat-square&color=E8C267)](https://github.com/harlamov/editor/releases/latest)
  ![Platform](https://img.shields.io/badge/platform-Windows-2F80ED?style=flat-square)
  ![PixiJS](https://img.shields.io/badge/PixiJS-8-E91E63?style=flat-square)

  <a href="https://github.com/harlamov/editor/releases/latest">
    <img src="https://img.shields.io/badge/Download-Latest_Release-E8C267?style=for-the-badge&logo=github&logoColor=111827" alt="Download latest release" />
  </a>
</div>

## Explore the tutorial

Learn the editor basics and walk through the complete prefab-to-runtime pipeline:

```shell
npm create @harlamov/editor-tutorial@latest
```

## Start a game

Create a new project from a carefully assembled PixiJS 8 template with the editor workflow already in place:

```shell
npm create @harlamov/game@latest
```

## Features

### Git-based production flow

- Edit `.prefab` files and commit them without friction — they are plain JSON
- Every prefab generates into a TypeScript class that mirrors its complete hierarchy. No JSON is shipped to the runtime
- Breaking prefab changes surface at compile time wherever the game still references the previous structure
- **CLI for CI/CD:** coming soon

### Hot-reload editing

- `run dev`, export changed prefabs and see the result in the browser immediately
- Source textures are packed into WebP atlases with content-hashed filenames for reliable cache invalidation and versioned delivery
- Only atlases whose source textures have changed are rebuilt
- Prefab code and graphics are loaded on demand at runtime instead of being included in the main bundle

### Automatic layouts

- **Landscape**, **portrait**, and **square** are logical layout modes, independent of the physical device orientation
- Every prefab layer can have unique properties in each logical layout mode

### Automatic updates

- Download the editor once — new versions are installed automatically

## Loading prefab is now this simple:

```ts
const mainMenu = await new MainMenu().prepare();

// yeah, that's it :)
```

## Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| `F10` | Switch to the next layout mode |
| `Ctrl + S` | Save prefab |
| `Ctrl + Shift + S` | Save and generate code/assets |
| `Ctrl + Z` / `Ctrl + Shift + Z` | Undo / redo |
| `Ctrl + C` / `Ctrl + V` | Copy / paste layers |
| `Ctrl + D` | Duplicate selection |
| `Arrow keys` / `Shift + Arrow keys` | Move by 1 / 10 pixels |
| `Ctrl + ↑` / `Ctrl + ↓` | Reorder selected layers |
| `Alt + ↑` / `Alt + ↓` | Select the previous / next visible layer |
| `F8` | Wrap selected layers in a container |
| `F9` | Copy selected layers to the other layout modes |

## Production status and feedback

Legend17 Editor is production-ready and already used in shipped projects. Development continues, and feedback, bug reports, and suggestions are welcome:

- [Open an issue](https://github.com/harlamov/editor/issues)
- [alexey@harlamov.games](mailto:alexey@harlamov.games)
- [Telegram — @harlamov_games](https://t.me/harlamov_games)

### P.S.

I've been working on web games for more than 15 years, and in that time i've been through pretty much everything: Flash (now Animate, now appx abandoned), exports from Flash to JSON, texture-packers, Haxe, OpenFL, Cocos, Tiled, several attempts to build different editors.. It was always hard and tricky to work with UI.

This is the tool that i genuinely enjoy using, fr. I hope some of you will find it useful and enjoy it too.