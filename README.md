# Team Territory Map

An interactive world map and dashboard for a team-based community game. Teams ("empires") hold territories, and the site shows who controls what, who is playing and how past battles went.

**Live site:** https://siva-subramaniam-ds.github.io/Team-Territory-Map/

## Pages

| Page | Content |
|---|---|
| `index.html` | Dashboard: world map, strongest empires, latest battles, hall of fame |
| `empires.html` | Empire list and details |
| `players.html` | Active players |
| `battles.html` | Battle archive |

## How it works

- The map is an SVG (`index.svg`) coloured by the empire that holds each territory.
- Data is read live from a published Google Sheet as CSV, so updating the sheet updates the site with no redeploy.
- Empire emblems are in `Empire Image/`.

## Tech stack

Plain HTML, CSS and JavaScript with no build step. Hosted on GitHub Pages.

## Run locally

Serve the folder so the browser can fetch the sheet data:

```bash
npx serve .
```

## Using your own data

Each page defines a `SHEET_URL` constant near the top of its script. Point it at your own Google Sheet's CSV export link, keeping the same column layout.
