# JR Labs — Logo assets

Brand marks for **JR LABS LLC**. Stored here for reference (business cards,
Instagram/TikTok, docs, decks). **Not used by the website** — the site header
stays as the plain "JR LABS LLC" wordmark for now.

Brand: Inter · Indigo `#4f46e5` · Slate `#0f172a` · Emerald accent `#059669`.

## Files
| File | What | Use for |
|---|---|---|
| `jrlabs-badge.svg` | Full badge — JR + LABS + beaker in an app tile | App icon, standalone badge |
| `jrlabs-icon.svg` | Text-free icon — JR + beaker (no "LABS"). **Single SVG favicon source.** | Favicon (SVG), or beside the wordmark in a lockup |
| `jrlabs-lockup.svg` | Icon + "JR LABS" wordmark (horizontal) | Letterhead, business-card header, email signature |
| `jrlabs-avatar-1080.png` | 1080×1080 badge | **Instagram / TikTok profile photo** |
| `jrlabs-og-1200x630.png` | 1200×630 branded share card | Social/link preview image |
| `jrlabs-icon-512.png` | 512×512 icon | General-purpose PNG icon |
| `apple-touch-icon-180.png` | 180×180 | iOS home-screen icon |
| `favicon-16.png` / `favicon-32.png` | Browser tab icon (PNG fallback) | If ever added to a site/app |

**Favicon = one source of truth.** The SVG favicon *is* `jrlabs-icon.svg` — there is
intentionally no separate `favicon.svg` (a copy would only risk drifting out of sync).
Reference `jrlabs-icon.svg` directly. If a host insists on that exact filename, generate
it at deploy time instead of committing a duplicate:

```sh
cp jrlabs-icon.svg favicon.svg
```

## Golden rule
The **badge already contains the words "JR LABS."** Never place the full badge
next to the "JR LABS" wordmark (that doubles the name). Use:
- **Badge alone** → favicon, social avatar, app icon.
- **Icon + wordmark lockup** → website header, business cards, signatures.

"LLC" is only for formal/legal spots (footer, cards, contracts) — not everyday branding.

## Editing / re-exporting
The `*.svg` files in this folder are the vector source of truth — self-contained,
infinitely scalable, and (text already outlined to paths) rendered with no font
dependency. Edit an SVG directly, then re-export any PNG size from it, e.g.:

```sh
qlmanage -t -s <px> -o . jrlabs-icon.svg   # macOS; or open the SVG in a browser and export
```
