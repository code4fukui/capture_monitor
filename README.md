# capture_monitor

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A simple Electron application to display a live preview from a specific video capture device on your desktop or in a browser.

## Web Demo

A live web-based version is available for testing in your browser:

[https://code4fukui.github.io/capture_monitor/](https://code4fukui.github.io/capture_monitor/)

## How It Works

This utility is designed to act as a simple, no-frills monitor for a specific video source. It automatically searches for a connected video input device that has the word "capture" in its name (e.g., "USB Capture," "HDMI Capture"). It then displays the feed from that device, filling the entire window.

This makes it ideal for:
- Monitoring the output of a game console or another computer via an HDMI capture card.
- Using a DSLR or mirrorless camera as a high-quality webcam and needing a clean preview.
- Any scenario where you need a dedicated display for a specific video input without the clutter of a full media player.

## Features

- **Automatic Device Detection:** Automatically finds and displays video from a device with "capture" in its label.
- **Cross-Platform:** Runs as a standalone desktop application on Windows, macOS, and Linux using Electron.
- **Minimalist Interface:** The window displays only the video feed, with no borders or controls.
- **Web-Based Demo:** Can be run directly in a compatible browser.

## Getting Started (Desktop Application)

### Prerequisites

- [Node.js](https://nodejs.org/en/) (latest version recommended)

### Installation & Usage

1.  Clone the repository:
    ```sh
    git clone https://github.com/code4fukui/capture_monitor.git
    cd capture_monitor
    ```
2.  Install dependencies:
    ```sh
    npm install
    ```
3.  Run the application:
    ```sh
    npm start
    ```

## Build

To create a distributable, standalone application for your operating system, run the build script. This uses `electron-packager` to generate the application in a new folder (e.g., `capture_monitor-win32-x64`).

```sh
npm run build
```

## Customization

You can easily modify the application's behavior:

-   **Fullscreen/Kiosk Mode:** In `main.js`, uncomment the line for `kiosk: true` to launch the app in a borderless, fullscreen mode.
-   **Mirror Video (Horizontal Flip):** In `index.css`, uncomment the `-webkit-transform: scaleX(-1);` line to mirror the video feed.
-   **Change Target Resolution:** In `index.html`, modify the `width` and `height` values to request a different resolution from your device.

## Author

- megaya

## License

MIT License — see [LICENSE](LICENSE).