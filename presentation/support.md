# Support

L'extracteur étant installé dans une infrastructure autonome, il s'agit d'envoyer le maximum d'informations à notre support afin de faciliter le diagnostic et accélérer la résolution.

## Fichier de journalisation {#log}

L'extracteur journalise ses opérations (_log_) afin de pouvoir diagnostiquer plus facilement les problèmes.

### Journaux IIS {#log_iis}

Les requêtes envoyées via les pages web de téléchargement sont directement suivies par le serveur IIS. joindre les derniers fichiers de logs permettre d'isoler les soucis liés à l'accès aux formulaires de téléchargement :

!["IIS - Log files"](/assets/Extractor_IIS_logs.png "IIS - Où récupérer les fichiers de journalisation \(logs\)")

### Journal d'extraction {#log_extraction}

Chaque exécution de l'extracteur crée son propre fichier journal. Le dernier fichier journal  (log) correspondant à l'exécution la plus récente est nommé `Isogeo.Extractor.log`. Les précédents fichiers journaux sont renommés avec un incrément du plus récent au plus ancien.

Les fichiers journaux sont stockés dans le dossier temporaire de l'utilisateur configuré pour lancé l'extracteur :

```
C:\Users\%USERNAME%\AppData\Local\Temp\Isogeo.Extractor.log
```

