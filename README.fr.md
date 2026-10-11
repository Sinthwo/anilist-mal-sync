# Obsidian Anime Sync

**Langues :** [English](README.md) | Français | [Deutsch](README.de.md) | [日本語](README.ja.md)

> **Note personnelle :** J’apprends actuellement le français et le japonais.

**Un projet de synchronisation en Python pour Obsidian, AniList et MyAnimeList.**

> **État :** Le projet ne contient pour l’instant que sa structure initiale ; aucune logique applicative n’a encore été implémentée.

## Objectif

Gérer votre bibliothèque d’animes en Markdown dans Obsidian et, à terme, synchroniser les statuts de visionnage, la progression des épisodes, les notes et les autres champs compatibles avec AniList et MyAnimeList à l’aide de leurs API.

## Fonctionnalités prévues

- Import initial depuis AniList et MyAnimeList vers des notes Obsidian
- Synchronisation entre les trois outils, avec détection des conflits et mode de prévisualisation
- Métadonnées des animes, images de couverture et modèles Markdown
- Instantanés de synchronisation et sauvegardes dans une base SQLite locale
- Commandes dans le terminal, statistiques et tableaux de bord Obsidian
- Tests unitaires, d’intégration et de bout en bout

## Structure du dépôt

| Chemin | Rôle prévu |
| --- | --- |
| `src/anime_sync/providers/` | Clients API pour AniList et MyAnimeList |
| `src/anime_sync/obsidian/` | Lecture et écriture dans le coffre Obsidian et génération de notes |
| `src/anime_sync/sync/` | Réconciliation et gestion des conflits |
| `src/anime_sync/storage/` | État de synchronisation local et cache |
| `src/anime_sync/metadata/` | Enrichissement des métadonnées des animes |
| `src/anime_sync/statistics/` | Calcul des statistiques récapitulatives |
| `src/anime_sync/automation/` | Synchronisation planifiée et surveillance des fichiers |
| `templates/obsidian/` | Futurs modèles Markdown |
| `tests/` | Tests automatisés |
| `docs/` | Documentation du projet |

## Premiers pas

Le dépôt contient actuellement des **fichiers d’implémentation vides**. L’application ne peut pas encore être exécutée. Commencez par implémenter la configuration et l’authentification auprès des API, puis les imports en lecture seule, avant de mettre en place une synchronisation bidirectionnelle sécurisée.

## Sécurité

Ne commitez jamais de jetons API, de secrets OAuth, de bases de données locales ou votre coffre Obsidian personnel. Utilisez `.env` localement et vérifiez les changements avec une simulation avant d’activer les écritures sur les services distants.

## Technologies prévues

Python · GraphQL · REST · SQLite · Obsidian Markdown · OAuth2

## Feuille de route

1. Fondations et configuration
2. Authentification AniList et MyAnimeList et accès aux API en lecture seule
3. Import et export de fichiers Markdown pour Obsidian
4. Correspondance des identifiants et migration
5. Synchronisation avec gestion des conflits
6. Tableaux de bord et automatisation

## Documentation

Ces pages sont des espaces réservés ; leur contenu n’a pas encore été rédigé. Chaque page contient des liens vers ses traductions.

- [Architecture](docs/fr/architecture.fr.md)
- [Authentification](docs/fr/authentication.fr.md)
- [Référence de l’interface en ligne de commande](docs/fr/cli-reference.fr.md)
- [Configuration](docs/fr/configuration.fr.md)
- [Résolution des conflits](docs/fr/conflict-resolution.fr.md)
- [Schéma de la base de données](docs/fr/database-schema.fr.md)
- [Installation](docs/fr/installation.fr.md)
- [Intégration avec Obsidian](docs/fr/obsidian-integration.fr.md)
- [Algorithme de synchronisation](docs/fr/sync-algorithm.fr.md)
- [Dépannage](docs/fr/troubleshooting.fr.md)

## Licence
