# Enigma Blocker – GitHub Pages (AMO Website)

Öffentliche Website für **addons.mozilla.org** (Homepage + Privacy Policy).

## Dateien

| Datei | Zweck |
|-------|--------|
| `index.html` | Homepage (DE + EN) |
| `privacy.html` | Privacy Policy (AMO-Pflicht-URL) |
| `assets/` | Icons |

## Repo anlegen & veröffentlichen

1. Auf GitHub neues Repo: z. B. **`enigma-blocker`** (Account `NeoEnigma-arch` oder deiner)
2. Nur den Inhalt dieses Ordners `github-pages/` als Repo-Root hochladen:

```text
index.html
privacy.html
assets/
README.md
.nojekyll
```

3. **Settings → Pages → Source: Deploy from a branch → `main` / root**
4. Fertige URLs (Beispiel):

```text
Homepage:        https://neoenigma-arch.github.io/enigma-blocker/
Privacy Policy:  https://neoenigma-arch.github.io/enigma-blocker/privacy.html
```

Wenn dein GitHub-Username anders heißt, ersetze `neoenigma-arch` entsprechend.

## Bei AMO eintragen

Siehe **`AMO-FELDER.md`** in diesem Ordner.

Lokal testen: `index.html` doppelklicken oder:

```text
npx --yes serve .
```
