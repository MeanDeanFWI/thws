# 🧑‍🏫 THWS Online CSS – Marp Custom Theme

Willkommen zum **Custom Marp Theme "thws.css"**, speziell entwickelt für Präsentationen im Stil der Technischen Hochschule Würzburg-Schweinfurt.

Das Theem thws.css ist für online Präsentationen optimiert, für Veranstaltungen in Präsenz steht das Theme thws-pr zu Verfügung, das die volle Folienbreite nutzt. Einfach zu erkennen welches Theme genutzt wird ist durch die Titelfolie, bei online ist dieser in einem Petrolton, bei Präsenz in Dunkelblau.

Die PDF Datei zeigt, wie das Theme verwendet werden kann.

## 🌟 Überblick

Dieses Theme basiert auf dem Standard-Marp-Design, erweitert durch individuelle Farben, Layouts und Textstile. Es integriert das moderne Schriftbild der **Inter**-Fontfamilie und ist auf Lesbarkeit, Konsistenz und einfache Anwendung optimiert.

---

## 🎨 Klassenübersicht

| Klasse              | Beschreibung                                                                 |
|---------------------|-------------------------------------------------------------------------------|
| `.titlepage`        | Titelfolie mit dunklem Hintergrund, großem Titel (h1) und Untertitel (h2)     |
| `.structural`       | Inhaltsfolie mit grauem Hintergrund, hellem Text                             |
| `.fullscreen`       | Vollbildbild mit Text-Overlay (z. B. Zitat, Beschreibung)                     |
| `.img-right`        | Bild rechts neben dem Text (Text links, Bild rechts)                          |
| `.center`           | Zentriert Inhalte vertikal in der Mitte der Folie                            |
| `.end`              | Inhalte am unteren Rand der Folie ausgerichtet                               |
| `.tiny-text`        | Reduziert die Textgröße für Text, Listen, Links und Tabellen auf 18px        |
| `.small-text`       | Reduziert die Textgröße auf 22px                                             |
| `.large-text`       | Erhöht die Textgröße auf 28px (auch Überschriften auf 46px)                  |

---

## 🔠 Text & Überschriften

| HTML-Tag  | Größe     | Gewicht   | Farbe        |
|-----------|-----------|-----------|--------------|
| `h1`      | 28px      | 700       | schwarz      |
| `h2`      | 26px      | 500       | schwarz      |
| `h3`      | 24px      | 500       | orange       |
| `h4`      | 24px      | 500       | grau (#6d6d6d)|
| `h5`      | 18px      | 300       | schwarz      |
| `h6`      | 18px      | 300       | orange       |
| `p`       | 24px      | 300       | schwarz      |

**Hinweis**: `<strong>` innerhalb von Überschriften verstärkt zusätzlich die Farbe und das Gewicht.

---

## 📊 Tabellenformatierung

- Tabellen nutzen standardmäßig die Schriftgröße `--small` (22px)
- Tabellenkopf (`<th>`) ist **weiß auf orange**
- Zeilenhintergründe alternieren (weiß / hellgrau)
- Rahmenfarbe: **weiß**

### 📝 Tabellen-Textgröße anpassen

Um die Schriftgröße für Tabellen in MARP zu verändern, nutze die Klassen:

```markdown
<!-- Tabelle mit kleinerer Schrift -->
<section class="tiny-text">
  | Spalte 1 | Spalte 2 |
  |----------|----------|
  | Inhalt   | Inhalt   |
</section>
```

---

## 📄 Fließtextgröße ändern

Verwende eine der folgenden Klassen im `<section>`-Tag:

- `.tiny-text` → 18px
- `.small-text` → 22px
- `.large-text` → 28px

Beispiel:

```markdown
<section class="large-text">
  # Große Überschrift
  - Punkt 1
  - Punkt 2
</section>
```

---

## 💬 Zitate

```markdown
> Dies ist ein wichtiges Zitat.
```

Zitate werden **orange**, fett und in 32px dargestellt.

---

## 📌 Logo und Seitennummerierung

- Jede Folie zeigt automatisch das **THWS-Logo** oben links
- Die **Seitennummer** erscheint unten rechts in hellgrau (`#CDCDCD`)

---

## 🛠️ Verwendung

1. CSS-Datei in deinem Marp-Projekt einbinden:
```yaml
---
marp: true
theme: thws
---
```

2. Folienklassen nutzen mit `<section class="...">` oder HTML-Kommentaren in Markdown:

```markdown
<!-- _class: titlepage -->
# Meine Präsentation
## Untertitel
```

---


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
Mit 💛 gestaltet für akademische Exzellenz – Präsentieren auf THWS-Niveau!
