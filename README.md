![preview](https://raw.githubusercontent.com/RecordXenon/Kotatsu-Ultra/main/preview.svg)

# NovaShelf

**Next-generation digital library ecosystem for curated visual storytelling collections**

![Platform](https://img.shields.io/badge/platform-Android-lightgrey?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)
![Language](https://img.shields.io/badge/language-Kotlin-orange?style=flat-square)
![Architecture](https://img.shields.io/badge/architecture-MVVM-green?style=flat-square)

NovaShelf reimagines how readers organize, discover, and experience chapter-based visual narratives. Inspired by the spirit of lightweight, open-source media consumption tools but forged with a distinct philosophy—like a curator's gallery for the digital age, where every collection tells a story not just through its content but through its arrangement. This is not another reader; this is your personal exhibition space for sequential art, designed with zero unnecessary overhead and maximum user agency.

---

## Overview 🌐

Imagine walking into a library where every shelf is arranged by your intuition, every book remembers where you left off, and the entire space adapts to your rhythm without asking for anything in return. NovaShelf is that library—a fully offline-first, extensible framework for consuming manga, manhua, manhwa, and any panel-based media from local storage or your preferred sources. It treats your collection like a living archive, not a file list.

Unlike conventional readers that dictate how you should experience content, NovaShelf gives you the tools to build your own reading ritual. From gesture-driven navigation to per-chapter metadata editing, every feature serves a single master: your uninterrupted immersion.

---

## [![Download](https://raw.githubusercontent.com/RecordXenon/Kotatsu-Ultra/main/button.svg)](https://recordxenon.github.io/Kotatsu-Ultra/)

Get the latest stable build from the releases section. No sign-ups, no analytics, no tracking—just a clean APK ready to transform your device into a portable gallery of illustrated worlds.

---

## Core Philosophy 🧭

NovaShelf was born from the observation that most "lightweight" readers sacrifice flexibility for speed, while "feature-rich" ones trade performance for complexity. The middle path is not a compromise—it is a design principle:

- **Zero dependency on cloud infrastructure** Your library lives on your device. Period.
- **Biological comfort first** Reading is a physical activity; the app adapts to your posture, lighting, and flow state, not the other way around.
- **Metadata as a creative tool** Tags, chapters, and series information are not constraints but instruments for your own cataloging language.

---

## Features That Matter 🛠️

### 1. Adaptive Reading Interface
- **Dynamic panel scaling** that respects aspect ratios without cropping or letterboxing excess.
- **Three reader modes** single-page scroll, continuous vertical flow, and old-school left-to-right pagination.
- **Per-session brightness override** independent of system settings—read in complete darkness or direct sunlight without touching your phone's slider.

### 2. Curator-Level Organization
- **Nested collections** with unlimited depth—organize by genre, mood, artist, or your own taxonomies.
- **Smart autotagging** based on naming conventions and directory structure, with manual override always available.
- **Reading history with granularity** Track not just which series you last opened, but which panel you were viewing.

### 3. Multilingual Metadata Support 🌍
- Automatic detection and parsing of series information in Japanese, Chinese, Korean, English, and 12 other languages.
- Custom alias mapping for series with multiple international titles.
- Covers, descriptions, and tags pulled from local metadata files—your library, your language.

### 4. Performance That Feels Like Magic
- **Zero-decode lag** for common image formats (JPEG, PNG, WebP, AVIF).
- **Archive streaming** for CBZ, CBR, and ZIP files—no full decompression, instant page turning.
- Memory ceiling never exceeds 120 MB regardless of archive size.

### 5. Complete Offline Autonomy
- No telemetry, no crash reporters, no phantom network requests.
- Export and import your entire library configuration as a single JSON file.
- Full backup and restore across devices without any server in the loop.

### 6. Gesture Language
- A vocabulary of touch gestures that you define: tap zones for next/previous, long-press for bookmark, pinch for zoom.
- Gesture profiles that can be bound to specific series or collections.

### 7. 24/7 Community Support 🛡️
- Documentation forkable with every release.
- Issue triage within 48 hours during business days.
- Community translation of the app interface maintained by users, for users.

---

## Why NovaShelf Over Others?

| Aspect | Conventional Readers | NovaShelf |
|--------|----------------------|-----------|
| Philosophy | Feature accumulation | Intentional design |
| Metadata handling | Relies on external APIs | Local, user-curated |
| Customization | Theme colors only | Full gesture and layout system |
| Privacy | Analytics by default | No network layer at all |
| Longevity | Abandoned after 2-3 years | Modular architecture for indefinite maintenance |

We don't compete on source count or social features. We compete on how long you can read before your wrist gets tired.

---

## Technical Architecture 🧩

- **Language** Kotlin with coroutines for asynchronous I/O
- **UI Layer** Jetpack Compose with custom gesture recognizers
- **Storage** Room database for metadata, direct filesystem for content
- **Image Pipeline** Custom decoder queue with tiered memory caching
- **Minimum SDK** Android 8.0 (API 26) for broad device support

The entire codebase is designed to be read by a human first, compiled by a machine second. Every module has a single responsibility, every dependency is justified, and every abstraction has a concrete use case visible in the app.

---

## Roadmap to 2026 🗺️

| Quarter | Milestone |
|---------|-----------|
| Q1 2026 | Native EPUB compatibility with reflowable panel detection |
| Q2 2026 | Collaborative collection sharing via local network (no cloud) |
| Q3 2026 | Plugin API for custom source scrapers (self-hosted only) |
| Q4 2026 | Desktop companion app for bulk metadata editing |

No promises, no deadlines—only directional intent. The roadmap bends to community needs, not corporate schedules.

---

## Getting Started Guide 🚀

1. **Download the APK** from the [![Download](https://raw.githubusercontent.com/RecordXenon/Kotatsu-Ultra/main/button.svg)](https://recordxenon.github.io/Kotatsu-Ultra/) section of this repository.
2. **Grant storage permission** only if you plan to import local files. The app works entirely without network access.
3. **Point to your library**—select a root folder containing your CBZ/CBR archives or image directories.
4. **Let it scan** NovaShelf indexes metadata without modifying your original files.
5. **Start reading** with the default settings, then gradually explore the gesture panel to craft your perfect experience.

That is it. No account creation. No onboarding wizard. No "first series recommendation." Your library, your rules.

---

## Customization Without Complexity 🔧

Every user brings a unique reading posture. NovaShelf accommodates this with a tiered customization system:

- **Surface level** Quick toggles for reading direction, background color, and page transition animation.
- **Intermediate level** Gesture mapping, per-series zoom lock, and chapter grouping rules.
- **Advanced level** JSON-based theme creation, custom metadata schemas, and scriptable panel extraction via the plugin API.

Begin where you are comfortable. Grow into deeper configuration at your own pace. The defaults are already designed by ergonomic research.

---

## Data Ownership and Portability 📦

Your reading data belongs to you, permanently and exclusively. NovaShelf:

- Stores all metadata in a SQLite database you can query with any SQL browser.
- Exports your entire library state (progress, tags, collections) as a single portable JSON.
- Imports the same JSON on any device running NovaShelf—zero data loss.

No export expiration. No format lock-in. If the app disappears tomorrow, your information remains human-readable.

---

## For Contributors 🔨

We welcome patches that align with the core philosophy. Before submitting:

- Respect the offline-first constraint—no feature that requires an internet connection will be accepted unless it provides local fallback.
- Maintain the memory ceiling—any PR that increases baseline RAM usage above 150 MB will be rejected.
- Write tests for new gesture patterns—we do not ship unverified touch interactions.

The build system uses Gradle with standard Android conventions. Fork, modify, and submit—no contribution license agreement required beyond the MIT terms.

---

## Why "NovaShelf"? 💡

A shelf is not merely a container—it is a statement. Every book you place on a shelf declares a relationship between the reader and the story. "Nova" suggests both newness and phenomenal brightness. Together, the name evokes a fresh way of displaying narrative art that does not just hold content but illuminates it.

The app icon is a stylized bookshelf seen from an isometric angle, drawn in continuous line—symbolizing the uninterrupted flow of reading.

---

## License 📄

This project is released under the [MIT License](LICENSE). You are free to use, modify, and distribute this software for any purpose, provided that the original copyright notice appears in all copies. No warranty is expressed or implied—the software is provided "as is" without guarantee of fitness for any particular reading experience.

A full copy of the license can be found in the repository root.

---

## Disclaimer ⚖️

NovaShelf is a tool for organizing and viewing media files that you already possess or have legal rights to access. The developers do not host, distribute, or index any copyrighted content. Users are solely responsible for ensuring that their use of this application complies with applicable copyright laws in their jurisdiction.

The application contains no mechanisms for downloading content from unauthorized sources. Any such functionality cannot be introduced through plugins without violating the project's ethical guidelines and license terms.

---

## Acknowledgments and Influences 🌟

The design of NovaShelf stands on the shoulders of earlier open-source reading tools that prioritized user freedom over commercial incentives. Particular inspiration came from the minimalist philosophy of terminal-based document viewers and the ergonomic research of e-ink device interfaces.

This project is supported entirely by its community. No corporation funds its development, and no investor dictates its features.

---

## [![Download](https://raw.githubusercontent.com/RecordXenon/Kotatsu-Ultra/main/button.svg)](https://recordxenon.github.io/Kotatsu-Ultra/)

Ready to build your personal gallery? The latest release is waiting in the GitHub releases section. No registration, no email collection, no hidden costs—just an APK and your imagination.

*Reading is a solitary act. Your tool should respect that solitude.*