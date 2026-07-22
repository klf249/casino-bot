# Politique de sécurité

## Signaler une vulnérabilité

Merci de ne pas publier de token, secret, fichier `.env`, identifiant privé ou preuve exploitable dans une issue publique.

Pour un problème de sécurité, contactez le mainteneur depuis son profil GitHub et fournissez :

- une description claire du problème ;
- les étapes permettant de le reproduire ;
- l’impact potentiel ;
- une proposition de correction, si disponible.

Les signalements sérieux seront étudiés avant toute publication détaillée.

## Bonnes pratiques

- Utiliser uniquement des variables d’environnement pour les secrets.
- Régénérer immédiatement tout token exposé.
- Limiter les permissions du bot au strict nécessaire.
- Ne jamais versionner les bases de données ou fichiers contenant des données privées.
