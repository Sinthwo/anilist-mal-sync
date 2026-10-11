# Obsidian Anime Sync

**Sprachen:** [English](README.md) | [Français](README.fr.md) | Deutsch | [日本語](README.ja.md)

**Ein Synchronisierungsprojekt auf Basis von Python für Obsidian, AniList und MyAnimeList.**

> **Status:** Bisher steht nur das Grundgerüst des Projekts. Es wurde noch keine Anwendungslogik implementiert.

## Ziel

Verwalte deine Anime-Sammlung in Obsidian als Markdown-Dateien und synchronisiere künftig den Wiedergabestatus, den Episodenfortschritt, Bewertungen und weitere kompatible Felder über die APIs mit AniList und MyAnimeList.

## Geplante Funktionen

- Erstimport von AniList und MyAnimeList in Obsidian-Notizen
- Synchronisierung zwischen allen drei Anwendungen mit Konflikterkennung und Vorschaumodus
- Anime-Metadaten, Coverbilder und Markdown-Vorlagen
- Lokale SQLite-Snapshots des Synchronisierungszustands und Backups
- Terminalbefehle, Statistiken und Obsidian-Dashboards
- Unit-, Integrations- und Ende-zu-Ende-Tests

## Aufbau des Repositorys

| Pfad | Geplante Aufgabe |
| --- | --- |
| `src/anime_sync/providers/` | API-Clients für AniList und MyAnimeList |
| `src/anime_sync/obsidian/` | Lesen und Schreiben im Obsidian-Vault sowie Erstellen von Notizen |
| `src/anime_sync/sync/` | Datenabgleich und Konfliktbehandlung |
| `src/anime_sync/storage/` | Lokaler Synchronisierungszustand und Cache |
| `src/anime_sync/metadata/` | Ergänzen der Anime-Metadaten |
| `src/anime_sync/statistics/` | Berechnen von Zusammenfassungen |
| `src/anime_sync/automation/` | Geplante Synchronisierung und Dateiüberwachung |
| `templates/obsidian/` | Künftige Markdown-Vorlagen |
| `tests/` | Automatisierte Tests |
| `docs/` | Projektdokumentation |

## Erste Schritte

Das Repository enthält derzeit **leere Implementierungsdateien**. Die Anwendung ist noch nicht lauffähig. Implementiere zuerst die Konfiguration und API-Authentifizierung, anschließend reine Leseimporte und danach eine sichere bidirektionale Synchronisierung.

## Sicherheit

Committe niemals API-Tokens, OAuth-Geheimnisse, lokale Datenbanken oder deinen persönlichen Obsidian-Vault. Nutze `.env` lokal und prüfe Änderungen mit einem Probelauf, bevor du Schreibzugriffe auf die entfernten Dienste aktivierst.

## Geplante Technologien

Python · GraphQL · REST · SQLite · Obsidian Markdown · OAuth2

## Entwicklungsplan

1. Grundlagen und Konfiguration
2. AniList- und MyAnimeList-Authentifizierung sowie reine Lesezugriffe auf die APIs
3. Import und Export von Obsidian-Markdown-Dateien
4. Zuordnung von Einträgen anhand ihrer Identität und Migration
5. Synchronisierung mit Konfliktbehandlung
6. Dashboards und Automatisierung

## Dokumentation

Diese Seiten sind Platzhalter. Ihre Inhalte wurden noch nicht verfasst. Jede Seite verlinkt ihre Übersetzungen.

- [Architektur](docs/de/architecture.de.md)
- [Authentifizierung](docs/de/authentication.de.md)
- [CLI-Referenz](docs/de/cli-reference.de.md)
- [Konfiguration](docs/de/configuration.de.md)
- [Konfliktlösung](docs/de/conflict-resolution.de.md)
- [Datenbankschema](docs/de/database-schema.de.md)
- [Installation](docs/de/installation.de.md)
- [Obsidian-Integration](docs/de/obsidian-integration.de.md)
- [Synchronisierungsalgorithmus](docs/de/sync-algorithm.de.md)
- [Fehlerbehebung](docs/de/troubleshooting.de.md)

## Lizenz
