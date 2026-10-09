# Family Calendar Card Companion

Optionale Home-Assistant-Integration für die [Family Calendar Card](https://github.com/Baeka89/family-calendar-card). Die Karte funktioniert weiterhin alleine. Diese Integration speichert ausschließlich zusätzliche Anzeigezuordnungen von Terminen gemeinsam für alle Geräte und Benutzer derselben Home-Assistant-Instanz. Originaltermine werden nicht verändert.

## Installation

 In HACS `Baeka89/family-calendar-card-companion` als benutzerdefiniertes Repository vom Typ **Integration** hinzufügen, herunterladen und Home Assistant neu starten. Eine Aufnahme in den HACS-Standardkatalog muss separat beantragt werden.

Unter **Einstellungen → Geräte & Dienste → Integration hinzufügen** nach **Family Calendar Card Companion** suchen und bestätigen. Keine Zugangsdaten, Helfer oder YAML-Konfiguration erforderlich. In der Karte einen Termin öffnen und unter **Betrifft auch diese Kalender** die zusätzlichen Kalender speichern. Angeboten werden die in der jeweiligen Karte konfigurierten Kalender.

## Bestehende Installationen

Der Domain- und Speichername `family_calendar_card` bleibt unverändert. Bestehende gemeinsame Zuordnungen bleiben erhalten. Ein vorhandener YAML-Eintrag `family_calendar_card:` wird automatisch in einen UI-Eintrag übernommen. Nach erfolgreicher Übernahme den YAML-Eintrag entfernen. Rein lokale Browserzuordnungen werden nicht automatisch hochgeladen.

## Ohne Integration

Die Karte zeigt weiterhin Kalender und Termine, alle Ansichten, Farben und die vom Quellkalender unterstützten Bearbeitungsfunktionen. Nur das Speichern gemeinsamer zusätzlicher Anzeigezuordnungen benötigt diese Integration. Farben und Sichtbarkeitspräferenzen bleiben lokale Kartenfunktionen.

Alle authentifizierten Home-Assistant-Benutzer dürfen gemeinsame Anzeigezuordnungen bearbeiten. Die Daten liegen lokal in Home Assistant, es gibt keinen Cloud-Dienst. Änderungen innerhalb einer Karte erhalten Zuordnungen zu anderen Kalendern.

## Entwicklung

`python3 tests/test_shared_store.py` und `python3 tests/test_config_flow.py` prüfen die Verträge mit simulierten Home-Assistant-Adaptern. GitHub Actions prüft zusätzlich HACS und hassfest. Diese Integration stellt keine Sensoren bereit.

## Verbindung und Aktualisierung

Ohne bestätigte Verbindung zur Integration zeigt die Karte einen Einrichtungshinweis statt Zuordnungsschaltflächen. Schlägt eine laufende Speicherung fehl, wird kein erfolgreicher Speichervorgang gemeldet. Karte und Integration werden separat in HACS aktualisiert. Der Download der Karte installiert die Integration nicht automatisch.

## Deaktivieren oder Entfernen

Die Integration lässt sich unter Geräte & Dienste deaktivieren oder entfernen. Anschließend Home Assistant neu starten und das Dashboard neu laden. Die normalen Kartenfunktionen bleiben verfügbar. Ein noch vorhandener YAML-Eintrag muss vorher entfernt werden, sonst wird die Integration erneut importiert. Bereits angezeigte Zuordnungen können im Browsercache erhalten bleiben; das ist keine aktive geräteübergreifende Synchronisierung.

## Sprachen / Languages

Karte, Editor und Integration unterstützen Englisch, Deutsch, Französisch, Niederländisch, Spanisch, Estnisch, Katalanisch, Dänisch und Schwedisch. README und Changelog werden auf Deutsch und Englisch gepflegt.

Card, editor and integration support English, German, French, Dutch, Spanish, Estonian, Catalan, Danish and Swedish. README and changelog are maintained in English and German.

## English installation and usage

This optional integration adds shared, persistent, display-only calendar assignments to [Family Calendar Card](https://github.com/Baeka89/family-calendar-card). The card works independently; its normal views, colors and supported calendar editing do not require the companion. Source events are never changed by display assignments.

Add `Baeka89/family-calendar-card-companion` to HACS as a custom repository of type **Integration**, download it and restart Home Assistant. Inclusion in the HACS default catalog requires a separate application. Under **Settings → Devices & services → Add integration**, find **Family Calendar Card Companion** and confirm. New installations need no credentials, helpers or YAML. Open an event in the card and select additional configured calendars under **Also concerns these calendars**.

Existing YAML setups using `family_calendar_card:` are imported automatically. Remove the YAML entry after successful import. The domain and shared storage key stay unchanged, preserving existing shared assignments. Browser-only assignments are not uploaded automatically.

Assignments are shared across devices and users of the same Home Assistant instance. All authenticated users can change them. Data stays in Home Assistant with no cloud service. Changes preserve assignments to calendars outside the editing card. Colors and visibility preferences remain local card features.

Without a confirmed companion connection, the card displays setup information instead of assignment controls. A failed save does not report success. Update the card and integration separately through HACS; downloading the card never installs the companion automatically.

To disable or remove the integration, use Devices & services, then restart Home Assistant and reload the dashboard. Remove any remaining YAML entry first to prevent automatic reimport. Normal card features remain available. Cached assignments may still be displayed in a browser; this is not active synchronization.

Development checks: `python3 tests/test_shared_store.py` and `python3 tests/test_config_flow.py` use simulated Home Assistant adapters. CI additionally runs HACS and hassfest. The integration does not create sensors.

Gepflegt von / Maintained by [Baeka89](https://github.com/Baeka89). [MIT-Lizenz / MIT license](LICENSE).
