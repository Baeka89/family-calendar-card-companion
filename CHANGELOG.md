# Changelog

Veröffentlichte Änderungen werden hier dokumentiert. Noch nicht veröffentlichte Änderungen stehen getrennt davor. / Published changes are documented here, preceded by a separate section for unreleased changes.

## Noch nicht veröffentlicht / Unreleased

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

- Noch nicht veröffentlicht. Integrationsversion unverändert; bestehende Speicherung und Konfiguration bleiben erhalten.

#### Bekannte Einschränkungen

- Keine neue Liveprüfung in Home Assistant. Mindestversion bisher nicht verbindlich angegeben.

#### Prüfungen

- Identität der doppelten Symboldateien vor dem Entfernen geprüft. 12 lokale Speicher-Vertragsprüfungen und 4 Konfigurationsprüfungen erfolgreich; HACS und hassfest auf GitHub sind für diesen Arbeitsstand noch nicht ausgeführt.

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

- Not released yet. Integration version is unchanged; existing storage and configuration are preserved.

#### Known limitations

- No new live Home Assistant test. A binding minimum version has not yet been declared.

#### Checks

- Verified the duplicate icon files were identical before removal. 12 local storage contract checks and 4 configuration checks passed; GitHub HACS and hassfest have not yet run for this work state.

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
