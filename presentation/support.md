# Support

L'extracteur étant installé dans une infrastrcuture autonome, il s'agit d'envoyer le maximum d'informations avant 


## Fichier de journalisation {#log}

L'extracteur journalise ses opérations (_log_) afin de pouvoir diagnostiquer plus facilement les problèmes.

### Journaux IIS {#log_iis}

Les requêtes envoyées via les pages web de téléchargement sont directement suivies par le serveur IIS. joindre les derniers fichiers de logs permettre d'isoler les soucis liés à l'accès aux formulaires de téléchargement :

!["IIS - Log files"](/assets/Extractor_IIS_logs.png "IIS - Où récupérer les fichiers de journalisation \(logs\)")

### Journal d'extraction {#log_extraction}

Le fichier `Isogeo.Extractor.log` se trouve dans le dossier de l'utilisateur configuré pour lancé l'extracteur :

```
C:\Users\%USERNAME%\AppData\Local\Temp\Isogeo.Extractor.log
```

