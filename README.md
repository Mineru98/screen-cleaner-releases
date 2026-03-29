<p align="center">
  <img src="assets/thumbnail.svg" alt="ScreenCleaner" width="100%"/>
</p>

<p align="center">
  <b>English</b> &nbsp;|&nbsp; <a href="README.ko.md">한국어</a> &nbsp;|&nbsp; <a href="README.ja.md">日本語</a> &nbsp;|&nbsp; <a href="README.zh.md">简体中文</a>
</p>

<br/>

# ScreenCleaner

## Why I Built This

Okay, real talk — MacBook screens get *disgusting*.

You finally decide to do something about it. Grab a cloth, lean in, start wiping — and suddenly a tab disappears, Spotify starts blasting at full volume, and somehow a file got renamed to "ggggggg".

Now you're spending the next 5 minutes fixing things instead of cleaning.

The screen? Still dirty.

macOS has no built-in cleaning mode. So I made one.

---

## What It Does

**ScreenCleaner** is a tiny macOS menu bar app with one job: give you a safe window to clean your screen without anything going wrong.

Hit **Start Cleaning**, and it:

- **Blocks all keyboard input** at the system level — no accidental keypresses, no matter how hard you lean on the keyboard
- **Dims the screen to black** so you can see every smudge and streak clearly
- **Counts down a timer** (1, 3, 5, 10 min — or custom) so you know when you're done

When the timer ends, everything comes back exactly as you left it. Clean screen, no chaos.

---

## Installation

### Homebrew (recommended)

```bash
brew tap Mineru98/tap
brew install --cask screen-cleaner
```

### Manual

1. Download the latest `.dmg` from [Releases](https://github.com/Mineru98/screen-cleaner-releases/releases)
2. Open the `.dmg` and drag **ScreenCleaner.app** to `/Applications`
3. Launch the app and grant **Accessibility** permission when prompted

---

## Requirements

| | |
|---|---|
| **macOS** | 14 Sonoma or later |
| **Permission** | Accessibility (for keyboard blocking) |
| **Architecture** | Apple Silicon & Intel |

---

## Usage

1. Launch **ScreenCleaner** from your Applications or menu bar
2. Grant **Accessibility** permission on first launch
3. Select a timer preset — **1 / 3 / 5 / 10 min** — or enter a custom duration
4. Click **Start Cleaning**
5. Wipe your screen freely
6. The app automatically restores everything when the timer ends

### Keys During Cleaning

All keyboard input is blocked except for these three:

| Key | Action |
|-----|--------|
| `F1` | Decrease brightness |
| `F2` | Increase brightness |
| `ESC` (hold 5 sec) | Cancel cleaning and restore everything |

> Tap ESC once and nothing happens. Hold it for 5 full seconds to exit.

---

## Features

- System-level keyboard blocking via `CGEventTap` — nothing gets through
- Screen dims to black overlay for better visibility while cleaning
- Crash-safe: brightness is automatically restored even if the app quits unexpectedly
- Minimal UI — no clutter, just the timer and a button
- Lives in the menu bar, out of your way until you need it
