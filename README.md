# Obsidian Anime Sync

**A Python-based synchronization project for Obsidian, AniList and MyAnimeList.**

> **Status:** Project scaffold only — no application logic is implemented yet.

## Vision

Manage your anime library in Markdown inside Obsidian and eventually synchronize watch statuses, episode progress, scores and other compatible fields with AniList and MyAnimeList using their APIs.

## Planned features

- Initial imports from AniList and MyAnimeList into Obsidian notes
- Three-way synchronization with conflict detection and preview mode
- Anime metadata, covers and Markdown templates
- Local SQLite sync snapshots and backups
- Terminal commands, statistics and Obsidian dashboards
- Unit, integration and end-to-end tests

## Repository layout

| Path | Planned responsibility |
| --- | --- |
| `src/anime_sync/providers/` | AniList and MyAnimeList API clients |
| `src/anime_sync/obsidian/` | Obsidian vault read/write and note generation |
| `src/anime_sync/sync/` | Reconciliation and conflict handling |
| `src/anime_sync/storage/` | Local sync state and cache |
| `src/anime_sync/metadata/` | Anime metadata enrichment |
| `src/anime_sync/statistics/` | Summary calculations |
| `src/anime_sync/automation/` | Scheduled sync and file watching |
| `templates/obsidian/` | Future Markdown templates |
| `tests/` | Automated tests |
| `docs/` | Project documentation |

## Getting started

The repository currently contains **empty implementation files**. It is not runnable yet. Implement configuration and API authentication first, followed by read-only imports, then safe bidirectional synchronization.

## Security

Never commit API tokens, OAuth secrets, local databases or your personal Obsidian vault. Use `.env` locally and review changes with a dry run before enabling remote writes.

## Planned technology

Python · GraphQL · REST · SQLite · Obsidian Markdown · OAuth2

## Roadmap

1. Foundation and configuration
2. AniList and MyAnimeList authentication and read-only APIs
3. Obsidian Markdown import/export
4. Identity matching and migration
5. Conflict-aware synchronization
6. Dashboards and automation

## License

No license has been selected yet. Add a license before inviting external contributions.
