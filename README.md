# cringe-guard 📵

Control your LinkedIn and Instagram feeds with an LLM of your choice. A browser extension that filters out cringe content (engagement click-bait, promotional content, and low-value off-topic posts etc) on your social media feeds. It uses AI to analyse posts in real time and hides cringe worthy content.

This prototype demonstrates how AI can empower us to have more control over the content we consume.

> [!TIP]
> 🎉 New: Mute Words feature added - automatically filter posts containing specific words!

## Demo

![Cringe Guard Demo Video](./images/demo.gif)

## How it works?

The cringe-guard browser extension filters out cringe content from your LinkedIn and Instagram feeds using an AI model. When you browse these platforms:

1. **Detects New Posts**: As new posts appear in your feed, the extension detects them in real time.
2. **Sends for Analysis**: The post content is sent to an AI model (via an API) that classifies it based on predefined "cringe" criteria (e.g., engagement bait, overly promotional content, etc.).
3. **Filters Content**: Posts identified as cringe are filtered according to your preferred mode:
   - Blur Mode: Blurs cringe until you decide (with a "Click to View" option)
   - Vanish Mode: Vanish cringe completely from your feed
4. **User Control**: Users can customize the types of posts they want to see and hide, and control their settings (like
   API keys) via modifying `content.js`.

## Installation

### Firefox (Default)

1. Clone or download this repository
2. Open Firefox and navigate to `about:debugging`
3. Click "This Firefox" in the left sidebar
4. Click "Load Temporary Add-on"
5. Select the `manifest.json` file from the extension folder
6. Configure your Groq API key in the extension settings

### Chrome

1. Clone or download this repository
2. Replace `manifest.json` with `manifest-chrome.json` (rename it to `manifest.json`)
3. Open Chrome and navigate to `chrome://extensions/`
4. Enable "Developer mode" in the top-right corner
5. Click "Load unpacked" and select the extension folder
6. Configure your Groq API key in the extension settings

For detailed installation instructions, see [INSTALLATION.md](./INSTALLATION.md).

## TODO

- [x] Refactor the codebase a bit
- [x] Allow users to input API key through a simple interface in popup.html.
- [x] Provide users with the option to either blur or completely remove content from the DOM.
- [x] In addition to analyzing the text content of posts, automatically detect and remove posts with "Promoted" tags by default.
- [x] Add support for Instagram to filter cringe content on Instagram feeds.
- [ ] Enable custom post filters, letting users choose which posts to show or hide via UI
- [x] Persist user settings (API key and filters) using Chrome Storage API.
- [x] Test cross-browser compatibility (Chrome & Firefox)
- [ ] Bug: The extension is unexpectedly logging `GET chrome-extension://invalid/ net::ERR_FAILED` in the console for some reason.
- [ ] Redesign the logo to better reflect the purpose of the extension

## Built with ❤️ by

[Abhishek Tripathi](https://www.linkedin.com/in/abhishek-tripathi-a714ab30b/), check out more projects on [GitHub](https://github.com/Abhishekhack2909)

## Contributing

I welcome contributions to the `cringe-guard` project! Whether it's a bug fix, a feature request, or improving documentation, your contributions are appreciated.

> Thanks to [Unbaited](https://github.com/danielpetho/unbaited) for the inspiration.
