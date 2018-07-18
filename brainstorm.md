# Package Management in dunkelgrün

(cartoon pizza)

## ]init[ Package Management - Status / Herausforderungen

* `vendors` > `npm install`
* Library aufbohren: vendors: Bspw. BUNDP / npm instal github:// -> Beispiel: Jens

```json
"dependencies": {
    "@init/brick-bpa-forms": "^1.0.0",
    "@init/brick-bpa-matomo": "^1.0.0",
    "a11y-dialog": "^4.0.1",
    "react-dom": "^16.2.0",
    "react-highlight-words": "^0.11.0",
    "react-md-spinner": "^0.2.5",
    "react-paginate": "^5.1.0",
    "react-select": "github:jnachtigall/react-select#b5401e7e90ed5ad0552dd947cde38730df3f8319",
    "react-slidedown": "^1.3.0",
    "react-url-query": "^1.4.0",
    "react-window-size-listener": "^1.0.10",
    "scrollbar-width": "^3.1.1",
    "slick-carousel": "^1.8.1",
    "stickybits": "^2.1.2",
    "tooltip.js": "^1.2.0",
    "whatwg-fetch": "^2.0.3"
  },
```

* Wiederverwendbare Software-Komponenten aus eigenem Hause: Bsp.: action-outside
* npmjs.org down: Bspw.: Bilder

## Die Lösung: Verdaccio

Private NPM-Registry

* Privates Hosting von Software-Komponenten (Neuentwicklung oder Forks)
* Ausfallsichheit?
  * Caching-Funktion von npmjs.org
  * Uplinks

### Installation

```bash
npm install --global verdaccio
verdaccio
```

(NPM)(Docker)(others)

### Benutzung

#### Upload

* Write good, resusable code
* ```bash
  git init
  npm init
  npm set registry http://localhost:4873
  npm publish
    ```

#### Download

Browser: [http://localhost:4873](http://localhost:4873)

* React-Anwendung

```bash
npm set registry http://localhost:4873
npm install <some-dependency>
```

## Semantic Versioning

major.minor.patch
[semver.org](semver.org)

```bash
npm version major|minor|patch -m "<tag annotation>"
```

## Umfeld / Vertrauenswürdigkeit

* Grafiken / Metriken von GitHub
* Grafik von packagehealth
* Prominente Nutzer

## Weitere Fragen

* Tauglichkeit für ]init[ / Meinungen?
* Wie git repos zusammenhalten? -> GitLab-Gruppe?
* Rechte-/Rollen: `login`, `add-user`
* Workflow / Standard-Struktur für Pakete?
* Evtl. sinnvol f. Auslieferung CMS? -> Loslösung von Dev-Repo
* Scoped Pakete für @init?
* Scoped Pakete für Projekte?
* ....

