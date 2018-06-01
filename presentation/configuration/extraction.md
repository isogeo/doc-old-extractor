# Configurer les extractions

## Exécution de l'extracteur {#config_exe}

Pour configurer le catalogue Isogeo dans lequel se trouvent les données abonnées, il faut modifier les lignes 38 et 39 du fichier `*.Extract.proj` :

```xml
  <!-- Trouve les ressources modifiées d'après l'API Isogeo et le journal d'extraction -->
  <Target Name="FindResources">
    <IsogeoSearch
      RequiredMetadata="IsogeoFormat;IsogeoName"
	  GroupId="IDENTIFIANT_GROUPE_TRAVAIL_ISOGEO"
      Query="type:dataset catalog:IDENTIFIANT_CATALOGUE_EXTRACTION"
      ApiUrl="$(IsogeoApiUrl)"
      IdUrl="$(IsogeoIdUrl)"
    >
```

## Scripts FME {#config_fme}

