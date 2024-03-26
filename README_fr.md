# WordPressテーマ開発環境

![docker-wordpress](https://github.com/khalednigrou/docker-wordpress/assets/4309858/70c4ec01-8498-4c7f-94ff-a85f6bf40ce0)

[Read in English](./README.md) | [日本語で読む](./README_ja.md)


Ce projet fournit un environnement basé sur Docker pour simplifier le processus de développement de thèmes pour les projets WordPress. Il utilise un fichier `docker-compose.yml` préconfiguré pour mettre en place une instance WordPress, une base de données MySQL et phpMyAdmin pour la gestion de la base de données, le tout fonctionnant dans des conteneurs isolés.

## Pour Commencer

Pour commencer avec cet environnement de développement, suivez ces étapes :

1. **Clonez le dépôt** sur votre machine locale.

2. **Naviguez vers le répertoire du projet** où le fichier `docker-compose.yml` est situé.

3. **Ajoutez vos fichiers de thème** au dossier `wp-projects`. Ce dossier est monté dans le conteneur WordPress, permettant à WordPress de reconnaître et d'utiliser votre thème.

4. **Copiez le fichier `.env.example`** en `.env` et modifiez les variables d'environnement selon vos besoins.

   ```sh
   cp .env.exemple .env  
   ```

5. **Démarrez les conteneurs** en exécutant la commande suivante dans votre terminal :

   ```sh
   docker-compose up -d
   ```

6. **Accédez à WordPress** en naviguant vers `http://localhost:8080` dans votre navigateur web. Ici, vous pouvez activer votre thème et commencer à développer.

7. **Accédez à phpMyAdmin** en naviguant vers `http://localhost:8081`. Utilisez cette interface pour gérer votre base de données WordPress.

## Notes Importantes

- Les identifiants de la base de données MySQL et les autres variables d'environnement sont définis dans le fichier `.env`. Vous pouvez modifier ces valeurs selon vos besoins.

- Le dossier `wp-projects` est ignoré par Git comme spécifié dans le fichier `.gitignore`, assurant que vos fichiers de thème ne sont pas accidentellement commités au contrôle de version.

- Pour arrêter les conteneurs, exécutez `docker-compose down` dans votre terminal.

Cet environnement simplifie le processus de développement de thèmes WordPress en fournissant une configuration WordPress prête à l'emploi. Ajoutez simplement votre thème au dossier `wp-projects` et commencez à construire votre thème dans un environnement conteneurisé.