# MCdocs

Diese Website wird mit [vuepress](https://vuepress.vuejs.org/) und [vuepress-theme-plume](https://github.com/pengzhanbo/vuepress-theme-plume) generiert.

## Installation

```sh
pnpm i
````

## Verwendung

```sh
# Entwicklungsserver starten
pnpm docs:dev

# Für Produktion bauen
pnpm docs:build

# Produktions-Build lokal vorschauen
pnpm docs:preview

# VuePress und Theme aktualisieren
pnpm vp-update
```

## Deployment auf GitHub Pages

Das Plume-Theme enthält bereits eine GitHub-Actions-Konfiguration: `.github/workflows/docs-deploy.yml`. Zusätzlich müssen folgende Einstellungen im GitHub-Repository vorgenommen werden:

* [ ] Öffne `Settings > Actions > General`, scrolle zum Seitenende, aktiviere unter `Workflow permissions` die Option **Read and write permissions** und speichere die Änderung.

* [ ] Öffne `Settings > Pages`, wähle unter `Build and deployment` bei `Source` die Option **Deploy from a branch**, setze `Branch` auf **gh-pages** und speichere.
  (Der Branch `gh-pages` existiert beim ersten Mal möglicherweise noch nicht. Du kannst zuerst die obigen Einstellungen vornehmen, den Code in den `main`-Branch pushen, warten bis GitHub Actions abgeschlossen ist und danach die Pages-Konfiguration setzen.)

* [ ] Passe die Option `base` in `docs/.vuepress/config.ts` an:

  * Wenn du unter `https://<USERNAME>.github.io/` deployen möchtest, kannst du diesen Schritt überspringen, da der Standardwert von `base` `"/"` ist.
  * Wenn du unter `https://<USERNAME>.github.io/<REPO>/` deployen möchtest (also dein Repository `https://github.com/<USERNAME>/<REPO>` ist), setze `base` auf `"/<REPO>/"`.

Für die Verwendung einer eigenen Domain siehe:
[GitHub Pages – Custom Domains](https://docs.github.com/zh/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)

## Dokumentation

* [vuepress](https://vuepress.vuejs.org/)
* [vuepress-theme-plume](https://theme-plume.vuejs.press/)