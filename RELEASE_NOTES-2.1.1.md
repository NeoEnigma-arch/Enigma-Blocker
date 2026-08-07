# Enigma Blocker – Release 2.1.1

## Highlights

- Werbe- und Tracker-Blocker im Enigma-Stil
- YouTube: Ads überspringen, Feed-Ads entfernen, leere Ad-Flächen kollabieren
- Filterlisten (Ads, Trackers, Malware, Annoyances, DE, YouTube)
- Whitelist, Custom-Filter, Element-Picker, Statistik
- AMO-ready: i18n (DE/EN), `data_collection_permissions: none`

## Technical

- Manifest V2, Addon-ID: `enigma-blocker@krayzen.gmx.de`
- Autor / Support: krayzen@gmx.de
- Alles lokal, keine Telemetrie

## Notes for reviewers

- `webRequest` + `webRequestBlocking` only to cancel ad/tracker requests
- No remote code, no developer servers
- `data_collection`: none
