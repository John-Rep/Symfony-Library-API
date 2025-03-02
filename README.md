# Bienvenue à l'API du projet React Native

## Avant de Commencer

Vérifiez que vous disposez de PHP, Composer, Symfony, et ngrok:
- ```php -v```
  - si vous ne disposez pas de PHP, vous pouvez l'installer ici:
  - https://windows.php.net/download/
- ```composer -v```
  - si vous ne disposez pas de Composer, vous pouvez l'installer ici:
  - https://getcomposer.org/download/
- ```symfony -v```
  - si vous ne disposez pas de Symfony, vous pouvez l'installer ici:
  - https://symfony.com/download
- ```ngrok -v```
  - si vous ne disposez pas de ngrok, vous pouvez créer un compte et l'installer ici:
  - https://dashboard.ngrok.com/get-started/setup/windows
 


## Préparer et Lancer l'API

Après avoir fait un clone du repository :
- Installez les dépendances :
  - ```composer install```
- Connecter une base de données :
  - Changer la ligne 27 du fichier .env pour connecter votre base de données.
  - Le format est le suivant :
    - DATABASE_URL="mysql://utilisateur:motdepasse@127.0.0.1:3306/nom_de_la_base?serverVersion=8.0"
- Configurer la base de données :
  - Si vous n'avez pas encore créé la base :
    - ```symfony console doctrine:database:create```
  - Une fois la base de données connectée :
    - ```symfony console doctrine:migrations:migrate```


Maintenant vous pouvez lancer l'application API avec la commande :
- ```symfony server:start```


Une fois l'application Symfony lancée, créez un tunnel avec ngrok :
- ngrok http http://localhost:8000
- cette commande génère un lien pour copier et coller dans l'autre projet
