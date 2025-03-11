# MARP CI CSS Experiment Repository

Dieses Repository dient dazu, CSS-Dateien für ein konsistentes Corporate Design (CI) in [MARP](https://marp.app/) zu testen und zu entwickeln. MARP ist ein Markdown-basiertes Präsentationstool, das es ermöglicht, eigene Themes zu verwenden.

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
         "https://raw.githubusercontent.com/MeanDeanFWI/thws/refs/heads/main/thws.css"
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
  
6. **Folientypen**

   Folgende Arten von Folien können verwendet werden:

| **Sektion**            | **MARP-Klassenbefehl**          |
|------------------------|--------------------------------|
| Allgemeine Inhaltsfolie | &lt;!-- class: default --&gt;    |
| Titelseite             | &lt;!-- class: titlepage --&gt;  |
| Lernziele              | &lt;!-- class: lernziele --&gt;  |
| Diskussion             | &lt;!-- class: diskussion --&gt; |
| Zusammenfassung        | &lt;!-- class: summary --&gt;    |
| Zitat-Bereich         | &lt;!-- class: quote --&gt;      |
| Grafik-Bereich        | &lt;!-- class: grafik --&gt;     |
| Vollbild-Grafik       | &lt;!-- class: vollbild --&gt;   |
| Tabellen              | &lt;!-- class: table --&gt;      |
