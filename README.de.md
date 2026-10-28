# DockSpark

[English](README.md) · [简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Español](README.es.md)

Mit DockSpark wechselst du Browserprofile direkt über das macOS-Dock. Bewege den Mauszeiger über das Symbol eines unterstützten Browsers und wähle das gewünschte Profil aus, ohne das Profilmenü des Browsers öffnen zu müssen.

[Neueste Version herunterladen](https://github.com/DockSpark/DockSpark/releases/latest)
· [Website](https://dockspark.app)
· [Änderungsprotokoll (Englisch)](CHANGELOG.md)
· [Problem melden](https://github.com/DockSpark/DockSpark/issues)

## Funktionen

- Profile über ein Popover am Dock-Symbol des Browsers wechseln
- Browserprofile in einer nativen macOS-App verwalten
- Profile durch eigene Namen und Farben schnell erkennen
- Festlegen, welche benannten Profile im Menü beim Bewegen des Mauszeigers über das Dock-Symbol erscheinen
- DockSpark Free nutzen oder mit Pro eine unbegrenzte Anzahl von Browsern und Profilen freischalten
- Symbole in der Menüleiste und im Dock ein- oder ausblenden
- In der App nach Updates suchen
- Über das Hilfemenü die Dokumentation öffnen oder strukturiertes Feedback senden
- Die App auf Englisch, vereinfachtem Chinesisch, traditionellem Chinesisch, Japanisch, Koreanisch, Deutsch, Französisch oder Spanisch nutzen
- Popover an die Größe der Dock-Symbole anpassen, einschließlich Dock-Vergrößerung
- Anonyme Nutzungsanalyse in den allgemeinen Einstellungen ausschalten

## Voraussetzungen

- macOS 14.0 oder neuer
- Mac mit Apple Chip oder Intel-Prozessor
- Ein unterstützter Browser, der im Dock verbleibt

### Unterstützte Browser

| Browser | Profilwechsel über das Dock |
| --- | --- |
| Safari | Unterstützt |
| Firefox | Unterstützt |
| Google Chrome | Unterstützt |
| Chromium | Unterstützt |
| Microsoft Edge | Unterstützt |
| Brave Browser | Unterstützt |
| Vivaldi | Unterstützt |
| Opera | Unterstützt |
| Opera GX | Unterstützt |
| Arc | Unterstützt |

Safari, Google Chrome und Firefox sind standardmäßig aktiviert, wenn sie installiert sind. Der Free-Tarif erlaubt einen aktivierten Browser und drei benannte Profile pro Browser. Einträge für privates Surfen und den Inkognitomodus zählen nicht zum Profillimit. Pro hebt diese Grenzen auf. Weitere installierte Browser kannst du über die App-Liste hinzufügen.

## Installation

### Homebrew

```sh
brew trust --cask dockspark/tap/dockspark && \
  brew install --cask dockspark/tap/dockspark
```

### Manueller Download

1. Öffne die [neueste Veröffentlichung](https://github.com/DockSpark/DockSpark/releases/latest).
2. Lade `DockSpark-0.5.0.dmg` herunter. Lade nicht die von GitHub automatisch erzeugten Quellcodearchive herunter.
3. Öffne das Disk-Image und ziehe `DockSpark.app` in den Ordner „Programme“.
4. Starte DockSpark und erteile die angeforderten macOS-Berechtigungen.

Für die manuelle Installation steht auch `DockSpark-0.5.0.zip` zur Verfügung.

DockSpark ist mit einem Developer-ID-Zertifikat signiert und von Apple notarisiert.

## Berechtigungen

DockSpark fordert nur die Systemberechtigungen an, die für den Profilwechsel benötigt werden:

- **Bedienungshilfen** erkennen Zeigerinteraktionen mit den Symbolen unterstützter Browser im Dock.
- **Automation** erlaubt DockSpark, den ausgewählten Browser zum Profilwechsel aufzufordern.
- **Festplattenvollzugriff** ist optional. DockSpark verwendet ihn ausschließlich, um Profilmetadaten von Chromium und Firefox zu finden.

Du kannst diese Berechtigungen jederzeit unter **Systemeinstellungen > Datenschutz & Sicherheit** prüfen oder widerrufen.

## Verwendung

1. Füge einen unterstützten Browser zum Dock hinzu.
2. Richte den Browser und seine Profile in DockSpark ein.
3. Bewege den Mauszeiger über das Dock-Symbol des Browsers.
4. Wähle ein Profil im Popover aus.

## Skill für KI-Assistenten

Der [DockSpark-Skill](skills/dockspark/SKILL.md) hilft KI-Assistenten, DockSpark und seine Einsatzmöglichkeiten zu erklären, durch Installation und alltägliche Nutzung zu führen, offizielle Dokumentation zu finden und häufige Probleme zu beheben. Die Skill-Version **0.5.0** folgt der App-Version; die mitgelieferten Anleitungen wurden anhand von DockSpark 0.5.0 geprüft. Der Assistent antwortet in deiner Sprache.

Installation mit der [Skills CLI](https://github.com/vercel-labs/skills) (Node.js erforderlich; aktuelle Voraussetzungen findest du in ihrer Dokumentation):

```sh
npx skills add DockSpark/DockSpark --skill dockspark
```

Wähle deinen KI-Assistenten aus, wenn du dazu aufgefordert wirst. Standardmäßig erfolgt die Installation für das aktuelle Projekt. Für eine globale Installation füge `-g` hinzu. Der GitHub-Befehl setzt voraus, dass der Skill in diesem Repository veröffentlicht wurde. Aus einem lokalen Checkout verwendest du:

```sh
npx skills add . --skill dockspark
```

Für die [manuelle Installation in Codex](https://developers.openai.com/codex/skills/) kopiere das gesamte Verzeichnis `skills/dockspark`, einschließlich `references/` und `agents/`, nach `~/.agents/skills/dockspark` oder nach `.agents/skills/dockspark` in deinem Projekt. Andere Assistenten verwenden möglicherweise andere Skill-Verzeichnisse. Lade die Skills deines Assistenten neu oder starte eine neue Sitzung, falls der Skill nicht angezeigt wird.

Beispielanfragen:

- `Erkläre mir mit $dockspark, wobei DockSpark mir helfen kann.`
- `Hilf mir mit $dockspark, Chrome-Profile einzurichten.`
- `Untersuche mit $dockspark, warum beim Bewegen des Mauszeigers über ein Dock-Symbol nichts passiert.`

Du kannst dieselben Fragen auch auf Englisch oder in einer anderen Sprache stellen. Der Skill bietet Anleitungen; um die App zu nutzen, musst du DockSpark separat installieren. Prüfe bei jeder neuen App-Version die Anleitungen und offiziellen Links des Skills und aktualisiere seine Version zusammen mit der geprüften App-Version.

## Screenshot

![DockSpark-Fenster zur Profilverwaltung](Assets/img_dockspark.jpg)

> Der Screenshot zeigt die Oberfläche von DockSpark. Version 0.5.0 unterstützt den Profilwechsel über das Dock für Safari, Firefox, Chrome und die weiteren oben aufgeführten Chromium-basierten Browser.

## Updates

DockSpark verwendet Sparkle für Updates innerhalb der App. Du kannst Versionen auch manuell von der [Releases-Seite](https://github.com/DockSpark/DockSpark/releases) herunterladen.

## Integrität der Veröffentlichungen

Die SHA-256-Prüfsummen lauten:

```text
DockSpark-0.5.0.dmg  90c0f9369d67eb33e6939b1cac008ec70277f7c176c0f2a1aa0e50fb08e85eff
DockSpark-0.5.0.zip  1d7eb10b9ce7736f2a1e5f1fd790eebb399675fadb95702a6032f329f65db129
```

Prüfe sie nach dem Herunterladen:

```sh
shasum -a 256 DockSpark-0.5.0.dmg DockSpark-0.5.0.zip
```

## Feedback

Nutze [GitHub Issues](https://github.com/DockSpark/DockSpark/issues), um Fehler zu melden oder Verbesserungen vorzuschlagen. Gib bei Fehlermeldungen deine macOS-Version, die Browserversion und die Schritte zum Reproduzieren des Problems an.

Dieses Repository enthält die öffentlichen Veröffentlichungsmaterialien von DockSpark. Der Quellcode der App ist nicht enthalten.
