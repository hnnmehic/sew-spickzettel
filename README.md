# SEW Spickzettel

Eine einzige statische Datei: `index.html`. Kein Build nötig.

## GitHub Pages

```bash
cd sew-spickzettel
git init && git add -A && git commit -m "SEW Spickzettel"
gh repo create sew-spickzettel --public --source=. --push
gh api repos/{owner}/sew-spickzettel/pages -X POST -f "source[branch]=main" -f "source[path]=/"
# -> https://<user>.github.io/sew-spickzettel/
```

## Eigene Subdomain

`index.html` in den Webroot der Subdomain hochladen (z.B. per SFTP). Fertig.

## Bedienung

- `/` oder `Strg/⌘+K` → Suche, `Enter` springt zum ersten Treffer, `Esc` leert die Suche
- Mehrere Wörter = alle müssen vorkommen (z.B. `native count`)
- Suche als Link teilbar: `index.html?q=having`
