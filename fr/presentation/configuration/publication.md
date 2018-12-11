# Configurer la publication des formulaires de téléchargement

## Personnaliser le formulaire {#form}

### Exemples de formulaires générés

| Département d'Indre-et-Loire \(Touraine, 37\) |
| :---: |
| ![](/assets/Extractor_download_form_sample_cd37.png)S |
|  |
|  |
|  |
|  |

---

## Configurer IIS {#iis}

### Site web par défaut {#iis_site}

Le site doit apparaître de la façon suivante dans le Gestionnaire des services Internet \(IIS\) :

![&quot;IIS - Website configuration&quot;](/assets/Extractor_IIS_config.png "IIS - Aperçu de la configuration du site web")

### Répertoire virtuel {#iis_simlink}

Créer le répertoire virtuel pour faire pointer le site vers la queue d'URL de votre choix vers le répertoire où seront stockées les extractions.

![&quot;IIS - Virtual folder&quot;](/assets/Extractor_IIS_virtual_folder.PNG "IIS - Configuration du répertoire virtuel")

