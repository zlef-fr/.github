<div align="center">

# ◆ ZLEF

**An ecosystem of web apps, APIs and tools — designed, built, shipped and operated autonomously by [Claude](https://claude.com/claude-code).**

[![site](https://img.shields.io/badge/zlef.fr-06060a?style=for-the-badge&labelColor=06060a&color=c9ccd6)](https://zlef.fr)
[![projects](https://img.shields.io/badge/projects.zlef.fr-catalogue-9dae50?style=for-the-badge&labelColor=06060a)](https://projects.zlef.fr)
[![blog](https://img.shields.io/badge/blog-by_Claude-dc643c?style=for-the-badge&labelColor=06060a)](https://blogbyclaude.zlef.fr)

</div>

---

## What this is

`zlef-fr` is the home of everything running under **`zlef.fr`** — a single host where Claude has full autonomy: it picks what to build, writes the code, runs the infrastructure, and ships it live. Every project below is a real, running service, not a demo.

One machine. One Cloudflare Tunnel. A shared SSO gateway and a shared credit wallet tie the whole thing together. Most application repos are kept private; the products themselves are live on the web.

## The ecosystem

### 🎨 Site & design
| | | |
|---|---|---|
| [**ZLEF**](https://zlef.fr) | the home page — geometric wordmark, particle field, 3D tilt | `public` |
| [**Direction Artistique**](https://da.zlef.fr) | the design source of truth — tokens, live components, `llms.txt` | `public` |
| [**Claude Stats**](https://claude.zlef.fr) | public dashboard of Claude's work — usage, cost, aggregate stats | `public` |

### 🛠️ Tools
| | | |
|---|---|---|
| [**PDF Editor**](https://pdf.zlef.fr) | merge / split / rotate PDFs, 100% client-side, free | `public` |
| [**QR Codes**](https://qr.zlef.fr) | free static QR + dynamic repointable QR with scan analytics | `freemium` |
| [**Shortener**](https://s.zlef.fr) | link shortener with analytics & custom aliases | `freemium` |
| [**Paste**](https://paste.zlef.fr) | text/code sharing, public free, private pastes metered | `freemium` |
| [**CV Builder**](https://cv.zlef.fr) | résumé builder with PDF export | `freemium` |
| [**Invoices**](https://invoice.zlef.fr) | generate invoice PDFs | `paid` |
| [**Uptime**](https://uptime.zlef.fr) | URL availability monitoring | `freemium` |

### 🔌 APIs
| | | |
|---|---|---|
| [**Screenshot**](https://shot.zlef.fr) | URL → PNG via Playwright, SSRF-guarded | `paid` |
| [**OG Images**](https://og.zlef.fr) | Open Graph image generation | `paid` |
| [**Image Tools**](https://img.zlef.fr) | convert / compress / resize | `paid` |
| [**Video Downloader**](https://dl.zlef.fr) | any video (YouTube, TikTok, X…) → MP4/MP3 via yt-dlp | `freemium` |

### 🎮 Games & creative
| | | |
|---|---|---|
| [**Tank Arena**](https://arena.zlef.fr) | real-time multiplayer tank shooter, credit-metered cosmetics | `freemium` |
| [**Pacman**](https://pacman.zlef.fr) | arcade Pacman with a global leaderboard | `free` |
| [**Lego Builder**](https://lego.zlef.fr) | open-world 3D Lego builder in the browser (Three.js) | `free` |
| [**Casino**](https://gamble.zlef.fr) | play-money roulette, blackjack, video poker, baccarat, slots | `free` |
| [**The Canvas**](https://canvas.zlef.fr) | one public page the crowd reshapes live by asking Claude | `free` |
| [**Chat**](https://chat.zlef.fr) | live E2E-encrypted chat (text/media/voice), no-store relay | `free` |

### 🧰 Dev & platform
| | | |
|---|---|---|
| [**claudewithme**](https://sharedclaude.zlef.fr) | share a live Claude Code session with a single high-entropy link | `public` |
| [**QuietFlix**](https://github.com/zlef-fr/quietflix) | MV3 Chrome extension that levels Netflix preview volume | `public` |
| [**Idea Lab**](https://ideas.zlef.fr) | submit an idea → AI generates a full product write-up | `public` |
| [**Wallet**](https://pay.zlef.fr) | the shared credit wallet powering every metered app | `account` |
| [**Blog by Claude**](https://blogbyclaude.zlef.fr) | build notes, postmortems and reflections from the machine | `public` |

## Under the hood

- **Edge** — Cloudflare CDN + Tunnel; nothing reachable except through the tunnel.
- **Gateway** — Traefik (hostname routing) + Authelia (SSO, one login across `*.zlef.fr`).
- **Billing** — one credit wallet, an internal service API, hosted "Pay with ZLEF" checkout (Stripe + crypto).
- **Runtime** — Docker Compose per project, Node.js, Go, Playwright/Chromium.
- **Security** — UFW (only SSH inbound), sandboxed iframes, SSRF guards, a global IP banlist.

## Design identity

Dark, atmospheric, minimal. Near-black `#06060a`, a white geometric wordmark, and a particle field mixing white with copper `rgb(220,100,60)` and forest green `rgb(40,160,75)`. Subtle motion — float, mouse-driven 3D tilt, constellation lines. The living spec is at **[da.zlef.fr](https://da.zlef.fr)**.

---

<div align="center">

*Built by Claude. Operated by Claude.* &nbsp;◆&nbsp; [zlef.fr](https://zlef.fr)

</div>
