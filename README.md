# Family Calendar Card Companion for Home Assistant

[![HACS](https://img.shields.io/badge/HACS-Compatible-blue.svg)](https://github.com/hacs/integration)
[![Maintainer](https://img.shields.io/badge/Maintainer-Baeka89-blue.svg)](https://github.com/Baeka89)
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/misomazo)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

[Deutsch](#deutsch) | [English](#english) · [Changelog](CHANGELOG.md)

---

<a id="deutsch"></a>

## Deutsch 🇩🇪

### Über dieses Projekt

Optionale Begleitintegration für die [Family Calendar Card](https://github.com/Baeka89/family-calendar-card). Sie speichert zusätzliche Anzeigezuordnungen von Terminen zentral und dauerhaft in Home Assistant und synchronisiert sie zwischen allen Geräten und Benutzern derselben Instanz. Originaltermine werden dabei nicht verändert.

**Die Karte funktioniert auch ohne diese Integration.** Nur gemeinsame zusätzliche Anzeigezuordnungen benötigen die Begleitintegration. Kalenderansichten, Farben und die vom Quellkalender unterstützte Terminbearbeitung bleiben unabhängig nutzbar. Farben und Sichtbarkeitspräferenzen bleiben lokale Kartenfunktionen.

### Funktionen

- Zusätzliche Kalenderzuordnungen ausschließlich für die Anzeige in der Karte.
- Zentrale Speicherung in Home Assistant und Aktualisierung über WebSocket.
- Gemeinsame Nutzung durch alle authentifizierten Home-Assistant-Benutzer.
- Zuordnungen zu Kalendern außerhalb der bearbeitenden Karte bleiben erhalten.
- Einrichtung über die Oberfläche, ohne Zugangsdaten, Helfer oder neue YAML-Konfiguration.
- Lokale Verarbeitung ohne Cloud-Dienst; die Integration erstellt keine Sensoren.

### Voraussetzungen

Home Assistant, HACS für die Installation über HACS und die separat installierte Family Calendar Card für die Bedienung. Zur Auswahl stehen die Kalender, die in der jeweiligen Karte konfiguriert sind.

### Installation und Einrichtung

1. In HACS nach **Family Calendar Card Companion** suchen. Falls das Repository noch nicht im Standardkatalog gelistet ist, `https://github.com/Baeka89/family-calendar-card-companion` als benutzerdefiniertes Repository vom Typ **Integration** hinzufügen.
2. Die Integration herunterladen und Home Assistant neu starten.
3. Unter **Einstellungen → Geräte & Dienste → Integration hinzufügen** nach **Family Calendar Card Companion** suchen und die Einrichtung bestätigen.
4. In der Karte einen Termin öffnen, unter **Betrifft auch diese Kalender** zusätzliche Kalender auswählen und speichern.

**Karte und Integration sind zwei getrennte Installationen.** Der Download der Karte installiert die Begleitintegration nicht automatisch. Die Aufnahme in den HACS-Standardkatalog ist ein separater Vorgang.

### Bestehende Installationen

Domain und Speichername `family_calendar_card` bleiben unverändert; bestehende gemeinsame Zuordnungen bleiben erhalten. Ein vorhandener YAML-Eintrag `family_calendar_card:` wird automatisch in einen UI-Eintrag übernommen. Nach erfolgreicher Übernahme den YAML-Eintrag entfernen.

Frühere rein lokale Browserzuordnungen werden nicht automatisch hochgeladen. Die gewünschten Kalender einmal erneut auswählen und speichern, um gemeinsame Zuordnungen anzulegen.

### Speicherung und Berechtigungen

Die gemeinsamen Anzeigezuordnungen liegen in Home Assistant, nicht ausschließlich im Browser. Alle authentifizierten Benutzer dieser Instanz dürfen sie bearbeiten. Änderungen innerhalb einer Karte erhalten Zuordnungen zu anderen Kalendern. Die Quellkalender und ihre Termine bleiben unverändert, auch bei eingeladenen oder schreibgeschützten Terminen.

### Verbindung und Aktualisierung

Ohne bestätigte Verbindung zur Integration zeigt die Karte einen Einrichtungshinweis statt Zuordnungsschaltflächen. Eine fehlgeschlagene Speicherung wird nicht als erfolgreich gemeldet.

Karte und Integration separat in HACS aktualisieren. Nach Aktualisierung der Integration Home Assistant neu starten; nach Aktualisierung der Karte das Dashboard neu laden.

### Deaktivieren oder Entfernen

Die Integration unter **Einstellungen → Geräte & Dienste** deaktivieren oder entfernen. Einen noch vorhandenen YAML-Eintrag vorher entfernen, damit die Integration nicht erneut importiert wird. Anschließend Home Assistant neu starten und das Dashboard neu laden.

Die normalen Kartenfunktionen bleiben verfügbar. Bereits angezeigte Zuordnungen können im Browsercache erhalten bleiben; dies ist keine aktive geräteübergreifende Synchronisierung.

### Sprachen

Karte, Editor und Integration unterstützen Englisch, Deutsch, Französisch, Niederländisch, Spanisch, Estnisch, Katalanisch, Dänisch und Schwedisch. README und Changelog werden vollständig auf Deutsch und Englisch gepflegt.

### Entwicklung

Die folgenden Prüfungen verwenden simulierte Home-Assistant-Adapter:

```bash
python3 tests/test_shared_store.py
python3 tests/test_config_flow.py
```

GitHub Actions prüft zusätzlich HACS und hassfest.

### Hilfe und Unterstützung

Fehler und Fragen zur Integration: [Issues](https://github.com/Baeka89/family-calendar-card-companion/issues). Beispiele und Bilder zur Bedienung: [Family Calendar Card](https://github.com/Baeka89/family-calendar-card).

Gepflegt von [Baeka89](https://github.com/Baeka89), veröffentlicht unter der [MIT-Lizenz](LICENSE). Du kannst die Entwicklung über [PayPal](https://paypal.me/misomazo) unterstützen.

---

<a id="english"></a>

## English 🇺🇸

### About this project

Optional companion integration for [Family Calendar Card](https://github.com/Baeka89/family-calendar-card). It stores additional event display assignments centrally and persistently in Home Assistant and synchronizes them across all devices and users of the same instance. Source events are never changed by these assignments.

**The card also works without this integration.** Only shared additional display assignments require the companion. Calendar views, colors and event editing supported by the source calendar remain independently available. Colors and visibility preferences remain local card features.

### Features

- Additional calendar assignments used exclusively for display in the card.
- Central Home Assistant storage and updates through WebSocket.
- Shared access for all authenticated Home Assistant users.
- Preserve assignments to calendars outside the editing card.
- Setup through the UI without credentials, helpers or new YAML configuration.
- Local processing without a cloud service; the integration creates no sensors.

### Requirements

Home Assistant, HACS for installation through HACS, and a separately installed Family Calendar Card to manage assignments. Available choices are the calendars configured in the individual card.

### Installation and setup

1. Search HACS for **Family Calendar Card Companion**. If the repository is not yet listed in the default catalog, add `https://github.com/Baeka89/family-calendar-card-companion` as a custom repository of type **Integration**.
2. Download the integration and restart Home Assistant.
3. Under **Settings → Devices & services → Add integration**, search for **Family Calendar Card Companion** and confirm setup.
4. Open an event in the card, select additional calendars under **Also concerns these calendars** and save.

**The card and integration are two separate installations.** Downloading the card does not automatically install the companion. Inclusion in the HACS default catalog is a separate process.

### Existing installations

The domain and storage name `family_calendar_card` remain unchanged, preserving existing shared assignments. An existing YAML entry `family_calendar_card:` is automatically imported into a UI entry. Remove the YAML entry after successful import.

Previous browser-only assignments are not uploaded automatically. Select the desired calendars again and save to create shared assignments.

### Storage and permissions

Shared display assignments are stored in Home Assistant, rather than exclusively in the browser. All authenticated users of the instance can edit them. Changes within one card preserve assignments to other calendars. Source calendars and their events remain unchanged, including invited or read-only events.

### Connection and updates

Without a confirmed connection to the integration, the card displays setup information instead of assignment controls. A failed save is not reported as successful.

Update the card and integration separately in HACS. Restart Home Assistant after updating the integration; reload the dashboard after updating the card.

### Disabling or removing

Disable or remove the integration under **Settings → Devices & services**. Remove any remaining YAML entry first to prevent automatic reimport. Then restart Home Assistant and reload the dashboard.

Normal card features remain available. Previously displayed assignments may remain in a browser cache; this is not active synchronization across devices.

### Languages

The card, editor and integration support English, German, French, Dutch, Spanish, Estonian, Catalan, Danish and Swedish. README and changelog are maintained in full in German and English.

### Development

The following checks use simulated Home Assistant adapters:

```bash
python3 tests/test_shared_store.py
python3 tests/test_config_flow.py
```

GitHub Actions additionally runs HACS and hassfest.

### Help and support

Integration bugs and questions: [Issues](https://github.com/Baeka89/family-calendar-card-companion/issues). Usage examples and screenshots: [Family Calendar Card](https://github.com/Baeka89/family-calendar-card).

Maintained by [Baeka89](https://github.com/Baeka89), released under the [MIT license](LICENSE). You can support development through [PayPal](https://paypal.me/misomazo).
