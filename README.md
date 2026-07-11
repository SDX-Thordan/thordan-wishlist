# 🎁 Wunschliste

Eine einfache, statische Wunschliste — eine einzige `index.html`, ohne Build-Schritt.
Zum Verschicken einfach den GitHub-Pages-Link teilen.

## Bearbeiten

Alle Wünsche stehen im `data`-Array oben im `<script>`-Block in [`index.html`](index.html).
Einfach dort Einträge ändern, hinzufügen oder entfernen und committen:

```js
{
  category: "Tau",
  accent: "#e0664e",   // Farbe für Punkt + Rand
  optional: true,       // (nein) ganze Kategorie als "optional" markieren
  items: [
    { name: "Pathfinder", qty: "2x", url: "https://..." },
    { name: "Stormsurge" },
  ],
},
```

Felder pro Eintrag:

| Feld       | Pflicht | Beschreibung                          |
|------------|---------|---------------------------------------|
| `name`     | ja      | Anzeigetext                           |
| `qty`      | nein    | Anzahl, z. B. `"2x"`                   |
| `url`      | nein    | Link (Name wird klickbar)             |
| `optional` | nein    | `true` → zeigt einen „optional"-Hinweis |

Felder pro Kategorie: `category` (Name), `accent` (Akzentfarbe), `optional` (ganze
Kategorie), `items` (die Wünsche).

## GitHub Pages aktivieren

1. Auf GitHub: **Settings → Pages**
2. Unter **Build and deployment → Source**: `Deploy from a branch`
3. Branch auf den gewünschten Branch (z. B. `main`) und Ordner `/ (root)` setzen, **Save**
4. Nach ein paar Minuten ist die Liste unter `https://<user>.github.io/<repo>/` erreichbar
