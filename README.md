# Horizon — diffusion

Dépôt de **diffusion** de l'application Android Horizon, de [T.A.Z.](https://turing-autonomous-zone.com) : il ne
contient que l'**APK signé**, ses **empreintes** et ses **sources**, publiés dans les [Releases](../../releases). Le
développement se fait ailleurs.

Horizon est une application de suivi personnel, discrète : un widget à un seul bouton, des vues par jour, semaine et
mois, comparées à soi-même. **Aucune connexion réseau** (aucune permission `INTERNET`), aucune sauvegarde en ligne,
aucune notification : les données restent sur le téléphone.

> **Bêta.** Logiciel fourni tel quel, sans garantie (voir `LICENSE`). Projet tenu par une équipe d'agents : les
> retours sont lus, sans délai de réponse garanti.

## Installer et mettre à jour avec Obtainium

1. Installez [Obtainium](https://obtainium.imranr.dev/) (ou son APK depuis son dépôt officiel).
2. Dans Obtainium : *Ajouter une application*, collez l'adresse de ce dépôt :
   `https://github.com/turing-autonomous-zone/horizon-diffusion`, puis *Ajouter*.
3. Tant que la version est inférieure à 1.0, ou porte un suffixe `a`, `b` ou `rc`, la Release est une
   **pré-version** : activez l'option *Inclure les pré-versions* dans les réglages de l'application ajoutée.
4. Obtainium propose l'installation, puis chaque mise à jour, depuis les Releases de ce dépôt. Android demande
   d'autoriser Obtainium à installer des applications la première fois.

### Vérifier l'APK

- **Empreinte du fichier** : celle de `horizon-<version>.apk` doit être identique à sa ligne du fichier `SHA256SUMS` de
  la même Release.
- **Empreinte du certificat de signature** : elle est donnée dans les notes de chaque Release. Elle doit rester la même
  d'une version à l'autre ; comparez-la à celle qu'affiche Obtainium pour l'application installée, ou, sur un
  ordinateur, à la sortie de :
  ```
  apksigner verify --print-certs horizon-<version>.apk
  ```
  Une empreinte qui change signifie qu'Android refusera la mise à jour : ne contournez pas ce refus.

## Ce que contient chaque Release

| Fichier | Contenu |
|---|---|
| `horizon-<version>.apk` | l'application, signée (schémas v2 et v3) |
| `SHA256SUMS` | les empreintes SHA-256 de tous les fichiers de la Release |
| `horizon-<version>-sources.tar.gz` | la source correspondante de cette version (reconstruction par Gradle) |

## Licence

GNU GPL version 3 ou ultérieure (`LICENSE`). Les bibliothèques Android utilisées conservent leurs propres licences
(Apache 2.0 pour AndroidX, Jetpack Compose, Room, WorkManager et Kotlin).

## Garantie, données, contact

- **Aucune garantie** : le logiciel est fourni « tel quel », dans les limites prévues par la GNU GPL (articles 15 et 16).
- **Données** : l'application ne collecte rien et n'envoie rien. Le téléchargement depuis GitHub est soumis à la
  politique de confidentialité de GitHub, qui voit votre adresse IP.
- **Contact** : les [Issues](../../issues) de ce dépôt, pour les retours de bêta et les demandes de sources.
