# Sakura Aesthetic Browser

A small desktop browser built with C# and Microsoft WebView2 (Chromium), with a Japanese/anime-inspired interface and a few built-in tools that I wanted to have in one place.

The project started as an experiment in building a browser UI from scratch and gradually grew into a more complete browser with tabs, bookmarks, history, ad blocking, a Japanese dictionary, and a custom new-tab experience.

![Sakura Aesthetic Browser](https://github.com/ronak200416/sakura-web-browser/releases/tag/exe)

## What it includes

### New Tab Page

The browser opens with a custom Tokyo-inspired rain scene instead of a standard blank new tab.

- 240-frame rain animation rendered on a canvas
- Smooth looping background
- Live clock and Japanese date
- Location-based weather
- Search bar with URL detection
- Japanese vertical text/calligraphy
- Dark, glass-style interface

### Sakura Shield

A built-in ad and tracker blocking system.

- URL-based filtering
- Tracker and ad domain blocking
- Cosmetic filtering for common ad containers
- YouTube ad skipping
- Live blocked-request counter

The filtering system is intentionally kept simple and lightweight rather than trying to replicate a full browser extension ecosystem.

### Japanese Dictionary

A small Japanese dictionary built directly into the browser.

You can select or look up Japanese words while browsing and get their meanings without installing a separate dictionary extension.

The feature can also be enabled or disabled from the browser settings.

### Browser Features

The browser currently supports:

- Multiple tabs
- Tab switching and closing
- Back / forward navigation
- Reload and hard reload
- Bookmarks
- Browsing history
- Zoom controls
- Custom search engines
- Force HTTPS
- Hardware-accelerated WebView2 rendering
- Browser settings

## Tech Stack

- **C#**
- **.NET**
- **Windows Forms**
- **Microsoft WebView2**
- **HTML / CSS / JavaScript**
- **Open-Meteo API** for weather data

The browser itself is written in C#, while the custom new-tab interface is built with HTML, CSS and JavaScript.

## Project Structure

```text
SakuraBrowser/
│
├── assets/
│   ├── home.html
│   ├── home.css
│   └── home.js
│
├── frames/
│   ├── ezgif-frame-001.jpg
│   ├── ezgif-frame-002.jpg
│   └── ...
│
├── src/
│   ├── Program.cs
│   ├── BrowserForm.cs
│   ├── BrowserSettings.cs
│   ├── AdBlockEngine.cs
│   ├── HistoryManager.cs
│   ├── SettingsForm.cs
│   └── JapaneseDictionary.cs
│
├── build.ps1
├── app.ico
└── README.md
```

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl + T` | New tab |
| `Ctrl + W` | Close tab |
| `Ctrl + Tab` | Next tab |
| `Ctrl + Shift + Tab` | Previous tab |
| `Ctrl + R` / `F5` | Reload |
| `Ctrl + Shift + R` | Hard reload |
| `Ctrl + L` / `Alt + D` | Focus address bar |
| `Ctrl + H` | History |
| `Ctrl + D` | Bookmark page |
| `Ctrl + B` | Bookmarks |
| `Ctrl + +` | Zoom in |
| `Ctrl + -` | Zoom out |
| `Ctrl + 0` | Reset zoom |
| `Alt + Left` | Back |
| `Alt + Right` | Forward |

## Building

### Requirements

- Windows 10 or Windows 11 (64-bit)
- .NET Framework 4.8 or compatible .NET SDK
- Microsoft Edge WebView2 Runtime

WebView2 is already included on most modern Windows installations, but you may need to install the runtime separately on some systems.

### Build

Clone the repository:

```bash
git clone https://github.com/yourusername/sakura-browser.git
cd sakura-browser
```

Then run:

```powershell
.\build.ps1
```

Or compile the project using your preferred C# build setup.

After building, run:

```powershell
.\SakuraBrowser.exe
```

## Why I Built This

I wanted to understand what actually goes into making a browser instead of only using one.

This project gave me a chance to work with WebView2, browser navigation, tabs, browser state, web requests, JavaScript/C# communication, custom UI, and a few browser-related features.

The visual design is heavily inspired by Japanese anime, Tokyo at night, and the kind of minimal interfaces I personally like using.

## Current Status

This is a personal project and is still being developed.

Some browser features are intentionally simplified compared with browsers such as Chrome, Edge, or Firefox. The goal is mainly to learn, experiment, and keep improving the project.

## Future Plans

Some things I would like to work on:

- Better tab management
- More complete ad-blocking rules
- Download manager
- Better privacy controls
- Session restore
- More browser customization
- Improved Japanese dictionary support
- Performance and memory improvements

## License

This project is licensed under the MIT License.

---

Built with C#, WebView2, HTML, CSS and JavaScript.

Made for learning, experimenting, and a little bit of 🌸.
