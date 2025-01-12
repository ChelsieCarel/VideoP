# VideoP:Pipeline hybride de traitement vidéo
Description du projet

VidP est un pipeline de traitement vidéo conçu pour automatiser le traitement, l'analyse et la gestion de vidéos à l'aide de conteneurs. Ce pipeline traite les vidéos en local pour générer des métadonnées, qui sont ensuite consolidées avec les vidéos originales dans le cloud. Les résultats sont accessibles publiquement via une page web.

Le pipeline est modulaire et repose sur plusieurs Pods (conteneurs) interconnectés pour exécuter différentes étapes du traitement vidéo.
Fonctionnalités principales


Architecture
Composants principaux

    Pipeline de traitement vidéo (en local) :
        Downscale Pod : Compression et redimensionnement des vidéos.
        LangIdent Pod : Détection de la langue parlée.
        Subtitle Pod : Génération de sous-titres.
        Animal Detect Pod : Détection et identification des animaux.

    Cloud :
        Les données sont traitées sur des instances EC2 avec un équilibreur de charge pour répartir les requêtes.
        Stockage des résultats dans Amazon S3 et DynamoDB.

    Interface utilisateur :
        Une page web (hébergée sur Apache2) permet d'afficher les vidéos et métadonnées.

Résultats attendus

    Les vidéos compressées, leurs métadonnées (langues, sous-titres, animaux détectés) et les originaux sont centralisés dans un espace de stockage sécurisé.
    Une interface web conviviale permet d'accéder aux données traitées et de visualiser les vidéos.
