# Notes for AMO reviewers – Enigma Blocker 2.1.0

## Purpose
Local ad/tracker blocker. No remote code, no telemetry, no accounts.

## Permissions rationale

| Permission | Why |
|------------|-----|
| `webRequest` + `webRequestBlocking` | Cancel requests to ad/tracker URLs (core function) |
| `<all_urls>` | Ads appear on arbitrary sites; content scripts apply cosmetic filters |
| `storage` | Settings, whitelist, stats (local only) |
| `tabs` | Badge counts, reload after whitelist toggle |
| `contextMenus` | Quick actions (whitelist, element picker) |
| `notifications` | Optional user feedback (off by default in settings path if unused aggressively) |

## Data collection
Manifest declares `data_collection_permissions.required: ["none"]`.  
No data leaves the browser via this extension.

## Source
Plain JS/CSS/HTML, not minified. Filter lists are plain text under `rules/`.

## YouTube scripts
`youtube.js` (content) + `youtube-page.js` (page-injected via `web_accessible_resources`) only strip ad payloads / UI. Comment/post APIs are intentionally left alone.

## Test plan
1. Install temporary / listed build.
2. Open a page with known ad network requests → requests canceled / badge increases.
3. Open YouTube home → ad tiles removed without breaking playback.
4. Whitelist a host → no blocking on that host.
5. Options page: toggle lists, export settings.
