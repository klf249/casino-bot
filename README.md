<div align="center">

# 🎰 Casino Bot

**Un bot Discord casino complet construit avec Node.js, discord.js et SQLite.**

[![Node.js](https://img.shields.io/badge/Node.js-20%2B-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![discord.js](https://img.shields.io/badge/discord.js-v14-5865F2?logo=discord&logoColor=white)](https://discord.js.org/)
[![SQLite](https://img.shields.io/badge/SQLite-Database-003B57?logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![License](https://img.shields.io/badge/license-not%20specified-lightgrey)](#licence)
[![GitHub stars](https://img.shields.io/github/stars/klf249/casino-bot?style=social)](https://github.com/klf249/casino-bot/stargazers)

Économie • Jeux • Boutique • Inventaire • Succès • Administration • Logs

</div>

## ✨ Aperçu

Casino Bot propose une économie de serveur centrée sur les **NozCoins**, avec des jeux de casino, un système de progression, une boutique, des tirages, des outils de modération et un panneau de configuration interactif.

Le projet est développé et maintenu par **Walker** (`@klf249`).

## 🚀 Fonctionnalités

- Économie persistante par serveur avec SQLite : monnaie, XP, profils et transactions.
- Jeux de casino : roulette, blackjack, slots, coinflip, hilo, craps, jackpot, bingo et pierre-feuille-ciseaux.
- Boutique, inventaire, récompenses, tirages pondérés et succès.
- Panneau de configuration interactif pour administrer le bot.
- Giveaway intégré avec inscriptions et reroll.
- Gestion des rôles et synchronisation avec la configuration du serveur.
- Modération, blacklist temporaire ou permanente et permissions hiérarchisées.
- Journaux d’audit pour les commandes, gains, transactions et événements de sécurité.
- Historique des transactions et outils de rollback.

## 📋 Prérequis

- Node.js `>= 20.11.0`
- npm
- Un bot Discord configuré dans le Developer Portal
- ImageMagick pour le rendu des cartes de profil

Sous Debian ou Ubuntu :

```bash
sudo apt update
sudo apt install -y imagemagick
```

## ⚡ Installation rapide

```bash
git clone https://github.com/klf249/casino-bot.git
cd casino-bot
npm install
cp .env.example .env
npm start
```

Renseigne ensuite les variables nécessaires dans `.env` :

```env
DISCORD_TOKEN=your_bot_token_here
CLIENT_ID=your_client_id_here
GUILD_ID=
```

## ⚙️ Configuration

Les principaux réglages sont disponibles dans `config.json` :

- `prefix` : préfixe principal des commandes.
- `buyerId` : identifiant du compte disposant des permissions avancées.
- `currency.*` : nom et apparence de la monnaie et de l’XP.
- `cooldowns.*` : délais entre les commandes.
- `limits.*` : limites de mises, dons et transferts.
- `embedColor.*` : palette utilisée dans les embeds.

## ▶️ Lancement

```bash
# Production
npm start

# Développement avec surveillance
npm run dev

# Vérification de la syntaxe
npm run check
```

## 🎮 Commandes principales

Le listing complet est accessible depuis le panneau d’aide du bot.

| Catégorie | Exemples |
|---|---|
| Économie | `+bal`, `+profil`, `+daily`, `+collect`, `+don` |
| Casino | `+roulette`, `+blackjack`, `+slots`, `+coinflip`, `+hilo` |
| Configuration | `+setup`, `+shopadd`, `+drawadd`, `+setreward` |
| Modération | `+warn`, `+sanctions`, `+bl`, `+tempbl` |
| Administration | `+setcommandpanel`, `+setprofil`, `+autologs`, `+rollbacktx` |

## 🏗️ Architecture

```text
src/
├── commands/     # Commandes organisées par domaine
├── db/           # Schéma SQLite et accès aux données
├── events/       # Événements Discord
├── handlers/     # Chargement dynamique des modules
├── utils/        # Outils métier et helpers
└── index.js      # Initialisation du client

data/             # Données d’exécution et base locale
image/            # Ressources visuelles
```

## 🔐 Sécurité

- Contrôles d’accès selon les rôles et niveaux de permission.
- Blacklist temporaire ou permanente.
- Cooldowns sur les commandes sensibles.
- Journalisation des opérations importantes.
- Historique des transactions et restauration ciblée.
- Vérification des permissions Discord avant les opérations administratives.

> Ne publie jamais ton token Discord, tes secrets ou ton fichier `.env` dans le dépôt.

## 🗺️ Roadmap

- [ ] Approfondir le système de clans.
- [ ] Développer un système de pillage complet.
- [ ] Renforcer la couverture de tests.
- [ ] Améliorer le découpage interne des modules.
- [ ] Ajouter davantage de documentation visuelle.

## 🤝 Contribution

Les issues et Pull Requests constructives sont les bienvenues. Pour une modification importante, ouvre d’abord une issue afin de présenter ton idée.

## 📄 Licence

Aucune licence n’est actuellement déclarée. Par défaut, tous les droits restent réservés au propriétaire du dépôt jusqu’à l’ajout d’un fichier `LICENSE`.

---

<div align="center">
Développé avec ☕ et JavaScript par <a href="https://github.com/klf249">Walker</a>.
</div>
