# Family Calendar Card Companion for Home Assistant

[![HACS](https://img.shields.io/badge/HACS-Compatible-blue.svg)](https://github.com/hacs/integration)
[![Maintainer](https://img.shields.io/badge/Maintainer-Baeka89-blue.svg)](https://github.com/Baeka89)
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/misomazo)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

[Deutsch](#deutsch) | [English](#english) · [Changelog](CHANGELOG.md)

<a id="deutsch"></a>

## Deutsch 🇩🇪

### 1. Projekt und Kurzbeschreibung

Family Calendar Card Companion ist die optionale Home-Assistant-Begleitintegration zur [Family Calendar Card](https://github.com/Baeka89/family-calendar-card). Maintainer: Baeka89.

### 2. Projektzweck und Funktionsumfang

Zusätzliche Anzeigezuordnungen von Terminen werden zentral und dauerhaft in Home Assistant gespeichert und per WebSocket zwischen Geräten und Benutzern synchronisiert. Originaltermine bleiben unverändert. Die Karte funktioniert ohne die Integration; nur diese gemeinsame Zusatzfunktion benötigt sie. Kalenderfarben, Ansichten und unterstützte Terminbearbeitung bleiben unabhängige Kartenfunktionen.

### 3. Systeme und Voraussetzungen

Home Assistant und die separat installierte Family Calendar Card. HACS wird für die HACS-Installation benötigt. In den Projektmetadaten ist keine verbindliche Home-Assistant-Mindestversion angegeben; Kompatibilität mit jeder Version wird nicht zugesagt. Es werden keine Sensoren und keine zusätzlichen Geräte eingerichtet. Karte, Editor und Integration unterstützen Deutsch, Englisch, Französisch, Niederländisch, Spanisch, Estnisch, Katalanisch, Dänisch und Schwedisch.

### 4. Installation

1. In HACS nach **Family Calendar Card Companion** suchen und die Integration herunterladen. Die Integration wurde in den HACS-Standardkatalog aufgenommen.
2. Home Assistant neu starten.
3. Unter **Einstellungen → Geräte & Dienste → Integration hinzufügen** nach **Family Calendar Card Companion** suchen und bestätigen.

Die Dateien liegen nach der Installation unter `/config/custom_components/family_calendar_card/`. Bei manueller Installation den vollständigen Ordner `custom_components/family_calendar_card` des gewünschten Releases an diesen Zielort kopieren und Home Assistant neu starten. Die Karte separat installieren; ihr Download installiert die Integration nicht automatisch.

### 5. Einrichtung und Authentifizierung

Keine separaten Zugangsdaten, automatisch erstellten Helfer oder neue YAML-Konfiguration erforderlich. Die Integration verwendet die vorhandene Home-Assistant-Anmeldung. Es wird nur eine Instanz eingerichtet.

### 6. Konfiguration und Optionen

Neue Installationen werden über die Oberfläche eingerichtet; es gibt keine weiteren Benutzereinstellungen in der Integration. Beispiel der zugehörigen Kartenkonfiguration:

```yaml
type: custom:family-calendar-card
entities:
  - calendar.family
  - calendar.work
```

Die IDs sind Beispiele und durch eigene vorhandene Kalender zu ersetzen. Für die zusätzliche Anzeigezuordnung stehen die in der jeweiligen Karte konfigurierten Kalender zur Auswahl.

### 7. Verwendung

In der Karte einen Termin öffnen, unter **Betrifft auch diese Kalender** zusätzliche Kalender auswählen und speichern. Bei Serien gilt die Zuordnung für das ausgewählte Vorkommen. Sie verändert auch bei schreibgeschützten Einladungen nicht den Originaltermin. Alle authentifizierten Benutzer derselben Home-Assistant-Instanz dürfen die gemeinsamen Zuordnungen bearbeiten. Zuordnungen zu Kalendern außerhalb der bearbeitenden Karte bleiben erhalten.

Die Daten liegen lokal in Home Assistant, ohne Cloud-Dienst; sie sind nicht ausschließlich im Browser gespeichert. Farben und Sichtbarkeitspräferenzen bleiben lokale Kartenfunktionen. Beispiele und Bilder: [Family Calendar Card](https://github.com/Baeka89/family-calendar-card).

### 8. Aktualisierung und Migration

Karte und Integration separat über HACS aktualisieren. Nach einem Integrationsupdate Home Assistant neu starten; nach einem Kartenupdate das Dashboard neu laden. Domain und Speichername `family_calendar_card` bleiben unverändert, vorhandene gemeinsame Zuordnungen bleiben erhalten. Ein vorhandener YAML-Eintrag `family_calendar_card:` wird in einen UI-Eintrag übernommen; ihn nach erfolgreicher Übernahme entfernen. Frühere Browserzuordnungen werden nicht automatisch hochgeladen: gewünschte Kalender erneut auswählen und speichern.

### 9. Einschränkungen und Fehlerbehebung

Ohne bestätigte Verbindung zeigt die Karte einen Einrichtungshinweis statt Zuordnungsschaltflächen. Eine fehlgeschlagene Speicherung wird nicht als erfolgreich gemeldet. Ohne stabile Ereigniskennung kann nach einer Änderung von Titel oder Datum eine erneute Zuordnung nötig sein.

Deaktivieren oder Entfernen unter **Einstellungen → Geräte & Dienste**; vorher einen verbleibenden YAML-Eintrag entfernen, um einen erneuten Import zu vermeiden. Danach Home Assistant neu starten und das Dashboard neu laden. Normale Kartenfunktionen bleiben verfügbar. Im Browsercache können ältere Zuordnungen sichtbar bleiben; dies bedeutet keine aktive Synchronisierung.

### 10. Entwicklung und Tests

Lokale Vertragsprüfungen mit simulierten Home-Assistant-Adaptern:

```bash
python3 tests/test_shared_store.py
python3 tests/test_config_flow.py
```

GitHub Actions führt zusätzlich HACS und hassfest aus. Lokale Vertragsprüfungen belegen keine erfolgreichen GitHub-Prüfungen oder Tests in einer echten Home-Assistant-Installation.

### 11. Versionshistorie

[CHANGELOG.md](CHANGELOG.md) und [GitHub-Releases](https://github.com/Baeka89/family-calendar-card-companion/releases). Die aktuelle Dokumentations- und Symbolbereinigung ist noch nicht veröffentlicht; die Integrationsversion bleibt bis zur Release-Vorbereitung unverändert.

### 12. Unterstützung, Mitwirkung und Lizenz

Fehler und Fragen: [GitHub Issues](https://github.com/Baeka89/family-calendar-card-companion/issues). Integrations-, Karten- und Home-Assistant-Version sowie Schritte zum Nachstellen nennen; persönliche Termindaten entfernen. Mitwirkung ist über Pull Requests möglich. Danke an die Home-Assistant- und HACS-Community sowie an Beitragende und Prüfende.

Maintainer: [Baeka89](https://github.com/Baeka89). Unterstützung: [PayPal](https://paypal.me/misomazo). Lizenz: [MIT](LICENSE).

<a id="english"></a>

## English 🇺🇸

### 1. Project and summary

Family Calendar Card Companion is the optional Home Assistant integration for [Family Calendar Card](https://github.com/Baeka89/family-calendar-card). Maintainer: Baeka89.

### 2. Purpose and features

Additional event display assignments are stored centrally and persistently in Home Assistant and synchronized across devices and users through WebSocket. Source events remain unchanged. The card works without the integration; only this shared extra feature requires it. Calendar colors, views and supported event editing remain independent card features.

### 3. Systems and requirements

Home Assistant and a separately installed Family Calendar Card. HACS is required for installation through HACS. Project metadata does not declare a binding minimum Home Assistant version; compatibility with every version is not claimed. No sensors or additional devices are created. The card, editor and integration support German, English, French, Dutch, Spanish, Estonian, Catalan, Danish and Swedish.

### 4. Installation

1. Search HACS for **Family Calendar Card Companion** and download the integration. The integration has been included in the HACS default catalog.
2. Restart Home Assistant.
3. Under **Settings → Devices & services → Add integration**, search for **Family Calendar Card Companion** and confirm.

Installed files are located in `/config/custom_components/family_calendar_card/`. For manual installation, copy the complete `custom_components/family_calendar_card` directory from the desired release to that destination and restart Home Assistant. Install the card separately; downloading it does not automatically install the integration.

### 5. Setup and authentication

No separate credentials, automatically created helpers or new YAML configuration are required. The integration uses the existing Home Assistant login. Only one instance is set up.

### 6. Configuration and options

New installations are configured through the UI; the integration has no additional user settings. Example configuration for the associated card:

```yaml
type: custom:family-calendar-card
entities:
  - calendar.family
  - calendar.work
```

IDs are examples; replace them with your existing calendars. Additional display assignments offer the calendars configured in the individual card.

### 7. Usage

Open an event in the card, select additional calendars under **Also concerns these calendars** and save. Recurring assignments apply to the selected occurrence. The source event remains unchanged, including read-only invitations. All authenticated users of the same Home Assistant instance can edit shared assignments. Assignments to calendars outside the editing card are preserved.

Data stays locally in Home Assistant without a cloud service; it is not stored exclusively in the browser. Colors and visibility preferences remain local card features. Examples and screenshots: [Family Calendar Card](https://github.com/Baeka89/family-calendar-card).

### 8. Updates and migration

Update the card and integration separately through HACS. Restart Home Assistant after an integration update; reload the dashboard after a card update. The domain and storage name `family_calendar_card` remain unchanged, preserving existing shared assignments. An existing `family_calendar_card:` YAML entry is imported into a UI entry; remove it after successful import. Previous browser-only assignments are not uploaded automatically: select the desired calendars again and save.

### 9. Limitations and troubleshooting

Without a confirmed connection, the card displays setup information instead of assignment controls. A failed save is not reported as successful. Without a stable event identifier, changing the title or date may require assigning the event again.

Disable or remove the integration under **Settings → Devices & services**; first remove any remaining YAML entry to prevent reimport. Then restart Home Assistant and reload the dashboard. Normal card features remain available. Older assignments may remain visible in a browser cache; this does not mean synchronization is active.

### 10. Development and tests

Local contract checks with simulated Home Assistant adapters:

```bash
python3 tests/test_shared_store.py
python3 tests/test_config_flow.py
```

GitHub Actions additionally runs HACS and hassfest. Local contract checks do not establish successful GitHub checks or tests in a real Home Assistant installation.

### 11. Version history

[CHANGELOG.md](CHANGELOG.md) and [GitHub releases](https://github.com/Baeka89/family-calendar-card-companion/releases). The current documentation and icon cleanup has not been released; the integration version remains unchanged until release preparation.

### 12. Support, contributing and license

Bugs and questions: [GitHub Issues](https://github.com/Baeka89/family-calendar-card-companion/issues). Include integration, card and Home Assistant versions and reproduction steps; remove personal event data. Contributions through pull requests are welcome. Thanks to the Home Assistant and HACS communities, contributors and reviewers.

Maintainer: [Baeka89](https://github.com/Baeka89). Support: [PayPal](https://paypal.me/misomazo). License: [MIT](LICENSE).
