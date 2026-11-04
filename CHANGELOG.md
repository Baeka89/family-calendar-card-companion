# Changelog

Veröffentlichte Änderungen werden hier dokumentiert. Noch nicht veröffentlichte Änderungen stehen getrennt davor. / Published changes are documented here, preceded by a separate section for unreleased changes.

<a id="release-0-1-2"></a>

## [0.1.2] – 2026-11-04

### Deutsch 🇩🇪

#### Hinzugefügt

Keine.

#### Geändert

- Vollständige deutsche und englische Dokumentation in der festgelegten Reihenfolge; Installation über den HACS-Standardkatalog erläutert.

#### Behoben

Keine.

#### Entfernt

- Doppelte Symbole im Hauptverzeichnis `brand/` entfernt. Die verwendeten Dateien unter `custom_components/family_calendar_card/brand/` bleiben unverändert.

#### Updatehinweise

- Integration auf v0.1.2 aktualisieren und Home Assistant neu starten. Bestehende Zuordnungen bleiben erhalten. Das ZIP enthält `custom_components/family_calendar_card/` für die Installation unter `/config/`.

#### Bekannte Einschränkungen

- Keine neue Liveprüfung in einer echten Home-Assistant-Installation. Eine verbindliche Home-Assistant-Mindestversion ist bisher nicht angegeben.

#### Prüfungen

- 12 Speicher-Vertragsprüfungen und 4 Konfigurationsprüfungen lokal erfolgreich; GitHub-Validierung einschließlich HACS und hassfest am exakten Release-Commit erforderlich und vor Veröffentlichung geprüft.
### English 🇺🇸

#### Added

None.

#### Changed

- Complete German and English documentation in the required order; installation through the HACS default catalog is explained.

#### Fixed

None.

#### Removed

- Removed duplicate icons from the root `brand/` directory. The used files under `custom_components/family_calendar_card/brand/` are unchanged.

#### Update notes

- Update the integration to v0.1.2 and restart Home Assistant. Existing assignments are preserved. The ZIP contains `custom_components/family_calendar_card/` for installation under `/config/`.

#### Known limitations

- No new live test in a real Home Assistant installation. A binding minimum Home Assistant version has not yet been declared.

#### Checks

- 12 storage contract checks and 4 configuration checks passed locally; GitHub validation including HACS and hassfest is required on the exact release commit and checked before publication.

---

## [v0.1.1]

### English 🇺🇸

- Optional setup through Home Assistant's Add integration UI.
- Import existing YAML configuration without changing the shared storage key.
- Central, persistent display-only calendar assignments with WebSocket synchronization.
- Preserve assignments to calendars outside the editing card's selection.
- Complete setup translations for all nine supported languages.

### Deutsch 🇩🇪

- Optionale Einrichtung über Integration hinzufügen in Home Assistant.
- Vorhandene YAML-Konfiguration übernehmen und den gemeinsamen Speicherpfad beibehalten.
- Zentrale dauerhafte Anzeigezuordnungen mit WebSocket-Synchronisierung.
- Zuordnungen zu Kalendern außerhalb der bearbeitenden Karte erhalten.
- Einrichtungstexte in allen neun unterstützten Sprachen vervollständigen.
