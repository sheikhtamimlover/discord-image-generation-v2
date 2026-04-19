# Discord Image Generation V2

**Author:** ST (sheikhtamimlover)

A powerful Node.js module that generates awesome images for Discord bots and other applications. This package provides a wide range of image manipulation effects, filters, and GIF animations.

## Installation

```bash
npm install discord-image-generation-v2
```

Or with Yarn:

```bash
yarn add discord-image-generation-v2
```

## Features

- 🎨 **Multiple Image Filters**: Blur, Grayscale, Sepia, Invert, and more
- 🎬 **GIF Support**: Create animated GIFs with effects like blinking and triggered animations
- 📷 **Montage Effects**: Over 30 pre-built montage effects including:
  - Meme templates (Lisa presentation, Stonk, etc.)
  - Fun effects (Facepalm, Kiss, Spank, etc.)
  - Badges and overlays (Jail, Wanted, Trash, etc.)
- ✨ **Canvas Integration**: Built with canvas, Jimp, and gif-encoder-2

## Usage

### Basic Example

```javascript
const { Blur } = require('discord-image-generation-v2');

const blur = new Blur();
const imageBuffer = await blur.getImage('./input.png');
```

### Using with Discord Bot

Perfect for Discord bots! Here's an example:

```javascript
const { Affect } = require('discord-image-generation-v2');
const fs = require('fs');

// Generate an image
const affect = new Affect();
const output = await affect.getImage('./user-avatar.png');

// Save or send
fs.writeFileSync('./generated.png', output);
```

## Project Structure

```
src/
├── index.js              # Main entry point
├── assets/               # Fonts and assets
│   └── fonts/            # Font files
├── module/
│   ├── functions.js      # Core functions
│   ├── filters/          # Image filters
│   ├── gif/              # GIF animations
│   ├── montage/          # Montage effects
│   └── utils/            # Utility functions
typings/
└── index.d.ts            # TypeScript definitions
```

## Compatibility

- **Node.js**: 14+
- **Canvas**: ^3.2.3 (latest)
- Works on most systems with prebuilt binaries

## Used By

- **ST BOT** - [GitHub](https://github.com/sheikhtamimlover/ST-BOT.git)
- **GoatBot v2**

## Dependencies

- `canvas` - Canvas graphics library
- `gif-encoder-2` - Pure JS GIF encoder
- `jimp` - Image manipulation library

## License

MIT

## Repository

[discord-image-generationV2](https://github.com/sheikhtamimlover/discord-image-generationV2.git)

---

**Note:** If you're looking to use this with a Discord bot, check out [ST BOT](https://github.com/sheikhtamimlover/ST-BOT.git) for integration examples!
