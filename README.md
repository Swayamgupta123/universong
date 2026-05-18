# 🎵 Universong

> **One song, every platform.** Paste any music link — get it on Spotify, Apple Music, YouTube Music, Deezer, Tidal, and more instantly.

![Universong Preview](https://api.song.link/favicon.ico)

## ✨ Features

- 🔗 Paste any song link from Spotify, Apple Music, or YouTube Music
- 🌍 Matches songs across **9 platforms** using ISRC codes
- 📋 Generates a shareable `song.link` URL anyone can open
- ⚡ Zero backend — runs entirely in the browser
- 🎨 Dark-mode UI with smooth animations
- 📱 Fully responsive on mobile

## 🚀 Live Demo

Deploy in 60 seconds — see **Deploy** section below.

## 🛠️ Tech Stack

| Layer | Tech |
|-------|------|
| Frontend | Vanilla HTML, CSS, JavaScript |
| API | [Odesli / song.link](https://odesli.co) (free, no key needed) |
| Hosting | Any static host (GitHub Pages, Netlify, Vercel) |

## 📦 Project Structure

```
universong/
├── index.html       # The entire app (single file)
├── README.md        # This file
└── .gitignore       # Git ignore rules
```

## 🔧 How It Works

1. User pastes a song URL (Spotify / Apple Music / YouTube Music)
2. App calls the **Odesli API** (`api.song.link/v1-alpha.1/links`)
3. Odesli matches the song using its **ISRC code** (music industry's universal song ID)
4. Returns deep links for every platform that has the song
5. User gets a beautiful results page + a shareable `song.link/...` URL

```
User pastes URL
      ↓
Odesli API (song.link)
      ↓
ISRC code matching
      ↓
Links for all platforms
      ↓
Shareable page URL
```

## 🌐 Deploy

### GitHub Pages (recommended)
```bash
git clone https://github.com/YOUR_USERNAME/universong.git
cd universong
# Push to GitHub, then go to:
# Settings → Pages → Source: main branch → / (root)
```

### Netlify Drop
Just drag and drop `index.html` at [netlify.com/drop](https://netlify.com/drop) — live in 10 seconds.

### Vercel
```bash
npm i -g vercel
vercel
```

### Cloudflare Pages
Connect your GitHub repo at [pages.cloudflare.com](https://pages.cloudflare.com) — auto-deploys on every push.

## 🎯 Supported Platforms

| Platform | Key |
|----------|-----|
| Spotify | `spotify` |
| Apple Music | `appleMusic` |
| YouTube Music | `youtubeMusic` |
| YouTube | `youtube` |
| Deezer | `deezer` |
| Tidal | `tidal` |
| Amazon Music | `amazonMusic` |
| Pandora | `pandora` |
| SoundCloud | `soundcloud` |

## 📡 API Reference

This project uses the [Odesli API](https://odesli.co) — completely free, no API key required.

```
GET https://api.song.link/v1-alpha.1/links?url=SONG_URL&userCountry=US
```

## 🤝 Contributing

Pull requests welcome! Ideas:
- [ ] Add more platforms (Napster, Boomplay, Gaana)
- [ ] History of recently searched songs (localStorage)
- [ ] OG preview cards for the shareable link
- [ ] Dark/light mode toggle

## 📄 License

MIT — free to use, fork, and deploy.

---

Built with ❤️ using the [Odesli API](https://odesli.co)
