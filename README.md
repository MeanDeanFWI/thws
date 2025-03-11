# MARP CI CSS Experiment Repository

Dieses Repository dient dazu, CSS-Dateien für ein konsistentes Corporate Design (CI) in [MARP](https://marp.app/) zu testen und zu entwickeln. MARP ist ein Markdown-basiertes Präsentationstool, das es ermöglicht, eigene Themes zu verwenden.

## Installation

Um eine der CSS-Dateien aus diesem Repository zu verwenden, kann sie direkt per RAW-Link eingebunden werden. Beispiel:

```yaml
---
theme: 'https://raw.githubusercontent.com/<USERNAME>/<REPO-NAME>/main/<THEME-FILE>.css'
---
```

**Hinweis:** Ersetze `<USERNAME>`, `<REPO-NAME>` und `<THEME-FILE>.css` mit den entsprechenden Werten aus deinem Repository.

## Anleitung zur Installation eines Custom Themes in MARP für VS Code

1. **MARP for VS Code installieren**
   - Installiere die [MARP-Erweiterung für VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode).

2. **Theme-Datei per RAW-Link einbinden**
   - Anstatt das Theme lokal zu speichern, kann es direkt per RAW-Link in der MARP-Konfiguration genutzt werden.

3. **MARP-Konfiguration anpassen**
   - Erstelle oder editiere die Datei `.vscode/settings.json` in deinem Projekt und füge folgende Konfiguration hinzu:

     ```json
     {
       "markdown.marp.themes": [
         "https://raw.githubusercontent.com/<USERNAME>/<REPO-NAME>/main/<THEME-FILE>.css"
       ]
     }
     ```

4. **Theme in einer MARP-Datei nutzen**
   - In der jeweiligen Markdown-Datei mit MARP kannst du das Theme wie folgt aktivieren:

     ```yaml
     ---
     theme: '<THEME-FILE>'
     ---
     ```

5. **Vorschau aktivieren**
   - Öffne die MARP-Datei in VS Code und nutze die Vorschau (`Strg + Shift + V` oder `Cmd + Shift + V` auf macOS), um dein Theme zu testen.

