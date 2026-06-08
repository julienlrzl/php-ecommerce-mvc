# E-Boutique · Site e-commerce en PHP/Twig

> Site e-commerce développé en PHP vanilla avec Twig, PDO et MySQL, architecture MVC implémentée à la main (sans framework).

**Stack** : PHP 8 · Twig 3 · PDO · MySQL · Composer

## Aperçu

Application e-commerce construite from-scratch en PHP sans utiliser de framework comme Symfony ou Laravel. L'objectif pédagogique était de comprendre les fondations du patron MVC en PHP et l'organisation d'un projet Composer.

## Démarrage

### 1. Base de données

```bash
mysql -u root -p < web4shop-8.sql
```

### 2. Dépendances PHP

```bash
cd ECommerce
composer install
```

### 3. Serveur

Pointer un Apache (ou le serveur de dev PHP) sur `ECommerce/public/` :

```bash
cd ECommerce
php -S localhost:8000 -t public
```

Puis ouvrir [http://localhost:8000](http://localhost:8000).

## Structure

```
ECommerce/
├── composer.json · composer.lock
├── .htaccess
├── app/
│   ├── Controller/      # Contrôleurs MVC
│   ├── Model/           # Accès données via PDO
│   └── View/            # Templates Twig
├── libraries/           # Code partagé (router, autoload, helpers)
└── public/              # Web root (DocumentRoot Apache)
    ├── index.php        # Front controller
    ├── css/ · js/ · image/
```

> `vendor/` (dépendances Composer) n'est pas versionné, il se reconstruit avec `composer install`.

## Équipe

- Julien Larzul
- Salim Lazrak
- Albin Martin

## Contexte

Projet réalisé dans le cadre du cours **PHP à Polytech Lyon**. Le rapport complet est dans `RapportPHP_LARZUL_LAZRAK_MARTIN.pdf`.
