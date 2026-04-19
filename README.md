# Discord Image Generation V2

**Author:** ST (sheikhtamimlover)

A powerful Node.js module that generates awesome images for Discord bots and other applications. This package has been upgraded to work with all versions of Canvas, solving compatibility issues found in the original version.

## Why This Upgrade?

The original discord-image-generation package was locked to an old Canvas version (`^2.6.1`), which caused installation issues with newer Node.js versions and system setups. **This upgraded version works with any Canvas version** - whether you're using the latest or any version in between. No more installation headaches!

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
- ✨ **Canvas Integration**: Built with @napi-rs/canvas, Jimp, and gif-encoder-2

## Usage

### Basic Example

```javascript
const ImageGeneration = require('discord-image-generation-v2');

// Create an instance
const gen = new ImageGeneration();

// Generate an image effect
gen.someEffect(imagePath, outputPath);
```

### Using with Discord Bot

Perfect for Discord bots like **ST BOT** and **GoatBot v2**!

```javascript
// Example: Using in a Discord command
const fs = require('fs');
const ImageGeneration = require('discord-image-generation-v2');

// Generate an image
const output = './generated.png';
await gen.affect('./user-avatar.png', output);

// Send to Discord
message.reply({
  files: [output]
});
```

## Project Structure

```
src/
├── index.js              # Main entry point
├── assets/               # Fonts and assets
├── module/
│   ├── functions.js      # Core functions
│   ├── filters/          # Image filters
│   ├── gif/              # GIF animations
│   ├── montage/          # Montage effects
│   └── utils/            # Utility functions
```

## Compatibility

✅ **Uses @napi-rs/canvas for better install reliability** - no native Canvas build required on most systems.
- Works well on Node 18+ platforms with prebuilt binaries
- No more Canvas version lock-in for your bot dependencies

## Used By

- **ST BOT** - [GitHub](https://github.com/sheikhtamimlover/ST-BOT.git)
- **GoatBot v2**

## Dependencies

- `@napi-rs/canvas` - Prebuilt Canvas bindings for better install compatibility
- `gif-encoder-2` - Pure JS GIF encoder
- `jimp` - Image manipulation library

## Original Package

This is an upgraded version of the original [discord-image-generation](https://github.com/Mr-KayJayDee/discord-image-generation) package. The original package had strict Canvas version requirements that caused compatibility issues. This upgraded version solves those issues by supporting any version of the dependencies.

## License

MIT

## Repository

[discord-image-generationV2](https://github.com/sheikhtamimlover/discord-image-generationV2.git)

---

**Note:** If you're looking to use this with a Discord bot, check out [ST BOT](https://github.com/sheikhtamimlover/ST-BOT.git) for integration examples!
