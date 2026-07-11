# 🎁 Wunschliste

Eine einfache, statische Wunschliste — eine einzige `index.html`, ohne Build-Schritt.
Zum Verschicken einfach den GitHub-Pages-Link teilen.

## Bearbeiten

Alle Wünsche stehen im `data`-Array oben im `<script>`-Block in [`index.html`](index.html).
Einfach dort Einträge ändern, hinzufügen oder entfernen und committen:

```js
{
  category: "Tau",
  items: [
    { name: "Pathfinder", qty: "2x" },   // qty ist optional
    { name: "Stormsurge" },
    { name: "Etwas mit Link", url: "https://..." },
  ],
},
```

Felder pro Eintrag:

| Feld       | Pflicht | Beschreibung                          |
|------------|---------|---------------------------------------|
| `name`     | ja      | Anzeigetext                           |
| `qty`      | nein    | Anzahl, z. B. `"2x"`                   |
| `url`      | nein    | Link (Name wird klickbar)             |
| `optional` | nein    | `true` → zeigt einen „optional"-Tag   |

Eine ganze Kategorie als optional markieren: den Namen in `optionalCategories` eintragen.

## GitHub Pages aktivieren

1. Auf GitHub: **Settings → Pages**
2. Unter **Build and deployment → Source**: `Deploy from a branch`
3. Branch auf den gewünschten Branch (z. B. `main`) und Ordner `/ (root)` setzen, **Save**
4. Nach ein paar Minuten ist die Liste unter `https://<user>.github.io/<repo>/` erreichbar
