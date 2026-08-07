# Enigma Blocker → AMO (addons.mozilla.org)

Ziel: **Listed** Veröffentlichung auf [addons.mozilla.org](https://addons.mozilla.org).

## 1. Vor dem Upload

1. Mozilla-Account: https://addons.mozilla.org/developers/
2. Developer Agreement akzeptieren
3. **Addon-ID** im Manifest (aktuell):  
   `enigma-blocker@krayzen.gmx.de`  
   Entwickler / Support: **krayzen@gmx.de**  
   (Addon-ID nach dem ersten AMO-Submit nicht mehr ändern.)
4. **Privacy Policy öffentlich hosten**  
   Datei: `amo/privacy-policy.html`  
   z. B. GitHub Pages / eigene Domain → URL notieren
5. Screenshots (empfohlen): Popup, Optionen, Badge auf einer Demo-Seite  
   Größe typisch 1280×800 oder laut AMO-Vorgabe

## 2. Paket

Fertig gebaut:

```text
.\package-release.ps1
→ release/enigma-blocker-2.1.1.zip
```

**Eine ZIP** – wie Enigma 2.0 / Text-Chiffrierer. Das ist der AMO-Upload.

## 3. Submit (Developer Hub)

1. https://addons.mozilla.org/developers/addon/submit/  
2. **On this site** (listed) wählen  
3. ZIP hochladen  
4. Listing ausfüllen mit Texten aus:
   - `amo/listing-de.md`
   - `amo/listing-en.md`
5. Kategorie: **Privacy & Security**
6. Privacy Policy URL eintragen
7. Bei „Notes to reviewer“ Text aus `amo/reviewer-notes.md` (Kurzfassung)
8. Absenden → automatische + ggf. manuelle Review

## 4. Nach Freigabe

- Addon ist signiert und für alle Firefox-Nutzer installierbar
- Updates: Version im `manifest.json` erhöhen → neues ZIP → neue Version im Hub

## 5. API-Signierung (optional, CLI)

Falls du später `web-ext` nutzt:

```bash
# API-Keys: https://addons.mozilla.org/developers/addon/api/key/
web-ext sign --channel listed --api-key=... --api-secret=...
```

## 6. Policies (wichtig)

- [Add-on Policies](https://extensionworkshop.com/documentation/publish/add-on-policies/)
- Keine Remote-Code-Ausführung
- Keine irreführende Beschreibung
- Daten: Manifest hat `"required": ["none"]` – stimmt mit Privacy Policy überein

## Version

**2.1.1** – AMO-ready (Autor/ID: krayzen@gmx.de)
