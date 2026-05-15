# DeskMate

DeskMate is a customizable Windows desktop widget canvas built with Tauri, React, and TypeScript. It sits behind your normal windows as a desktop overlay and lets you build a personal dashboard with clocks, notes, system stats, shortcuts, folders, app launchers, timers, feeds, and more.

DeskMate is designed for people who want their desktop to be useful without turning it into a heavy launcher or a browser tab.

## Features

- Desktop overlay window that stays behind normal apps
- Drag, resize, and arrange widgets on a configurable grid
- Multiple useful widgets, including:
  - Clock, world clock, timer, Pomodoro
  - CPU, RAM, disk, network, battery, Bluetooth, and task manager widgets
  - Notes, todo list, calculator, converter, bookmarks, RSS reader
  - Folder browser, gallery, app launcher, dock, shortcuts, and app folders
  - Weather, stocks, calendar, translate, currency, Gmail, Google Photos, Jira, and custom code widgets
- Per-widget settings and appearance customization
- Import and export configuration backups
- Optional launch at Windows startup
- Priority startup support using Windows Task Scheduler
- Local-first settings using persisted app storage

## Download

Go to the [Releases](../../releases) page and download the latest Windows installer.

Recommended:

- `deskmate_*_x64-setup.exe` for the normal installer experience
- `deskmate_*_x64_en-US.msi` if you prefer Windows Installer packages

After installation, open DeskMate from the Start menu. If Windows SmartScreen appears for an unsigned community build, choose **More info** and then **Run anyway** only if you downloaded the installer from this repository's official release page.

## System Requirements

- Windows 10 or Windows 11
- 64-bit system recommended
- WebView2 Runtime, usually already installed on modern Windows

## Quick Start

1. Install DeskMate from the latest GitHub release.
2. Launch DeskMate.
3. Right-click the desktop canvas to add widgets.
4. Use edit mode to move and resize widgets.
5. Open settings to customize appearance, grid layout, AI providers, data backup, and startup behavior.

## Startup Behavior

DeskMate can start automatically when Windows starts. When enabled, it creates a Windows Task Scheduler entry with high startup priority so DeskMate starts as early as Windows reasonably allows.

Windows does not guarantee that any user app can start before every other startup item, but DeskMate uses the strongest practical approach available for a normal desktop app:

- logon trigger
- no startup delay
- highest available run level
- highest task priority
- high process priority after launch

## Privacy

DeskMate stores its settings locally on your machine. Some widgets or integrations may contact external services when you configure them, such as weather, AI providers, Gmail, Google Photos, Jira, RSS feeds, translation, currency, or stocks.

API keys and provider settings should be treated as private. Do not commit personal configuration exports that contain secrets.

## Uninstall

Use Windows Settings:

```text
Settings > Apps > Installed apps > DeskMate > Uninstall
```

If you enabled launch at startup, DeskMate removes its startup task when the setting is turned off. Uninstalling the app should also remove normal application files created by the installer.

## License

MIT License

Copyright (c) 2026 Vikram

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

