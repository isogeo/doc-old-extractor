# Questions/réponses fréquentes

## Comment l'extracteur détermine t-il qu'une donnée est nouvelle ou modifiée ? {#understandDatesProcessing}

L'un des avantages de l'extracteur Isogeo est qu'il ne déclecnhe les scripts d'extraction et de publication uniquement lorsqu'une nouvelle donnée a été abonnée à son service ou bien qu'une donnée déjà abonnée a été modifée. Cela permet des économies de temps réseau et de connexion.

Pour ce faire, l'extracteur se fie aux informations contenues dans les métadonnées :

* la date de la première exécution de l'extracteur dans laquelle se trouvait la donnée ;
* la date de dernière mise à jour de la donnée. Celle-ci est modifiable dans [l'onglet **Histoire** de l'éditeur de métadonnée](http://help.isogeo.com/fr/features/documentation/md_history.html#ev%C3%A9nements).

---

## Forcer la mise à jour des données extraites {#forceUpdate}

![](/assets/Extractor_app_force_dataset_update.png "Ajouter une date de mise 	&agrave; jour pour forcer l&apos;extraction")

