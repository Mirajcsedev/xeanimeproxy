# 🌀 HiAnime Proxy — Cloudflare Worker

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/Mirajcsedev/hianime-proxy)
![Platform](https://img.shields.io/badge/Platform-Cloudflare%20Workers-orange)
![Streaming](https://img.shields.io/badge/Type-HLS%20Proxy-blue)

A **high-performance HLS (M3U8) proxy** built with **Cloudflare Workers**.  
Designed to bypass CORS, rewrite manifests, and stream video efficiently using **raw TCP/TLS sockets**.

---

## ✨ What This Proxy Does

✔️ Proxies HLS / M3U8 streams  
✔️ Fixes CORS issues automatically  
✔️ Rewrites playlists, segments, and keys  
✔️ Supports non-standard ports via sockets  
✔️ Streams directly from source → client (low memory)

---

## 🚀 One-Click Cloudflare Deployment

Click the button below to deploy instantly:

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/Mirajcsedev/hianime-proxy)

**Steps:**
1. Login to Cloudflare
2. Authorize Workers
3. Deploy 🚀

_No local setup required._

---

## 📦 Features

- 🎥 **HLS Streaming Proxy**
- 🔄 **Automatic M3U8 Rewriting**
- 🧠 **ReadableStream / TransformStream**
- 🔐 **Raw TCP & TLS Socket Support**
- 🕵️ **Stealth Browser Headers**
- 🌍 **Edge-Deployed for Low Latency**

---

## ⚙️ Environment Variables

You can configure these in **Cloudflare Dashboard → Workers → Settings → Variables**

| Variable Name | Required | Default Value | Description |
|---------------|----------|---------------|-------------|
| `DEFAULT_REFERER` | ❌ | `https://megacloud.tv` | Spoofed referer if none is provided |
| `DEBUG` | ❌ | `false` | Enable debug logging |

### Example Configuration

```env
DEFAULT_REFERER=https://megacloud.tv
DEBUG=true
## Usage

```http
GET https://your-worker.workers.dev/?url=ENCODED_URL&referer=ENCODED_REFERER
```

### Parameters

* `url`: The video/m3u8 URL to proxy (fully URL-encoded).
* `referer`: The referer header to spoof (optional, defaults to `https://megacloud.tv`).

## Development

To run locally in development mode:

```bash
npm run dev
```

## Author

**RY4N**
* GitHub: [@ryanwtf88](https://github.com/ryanwtf88)
