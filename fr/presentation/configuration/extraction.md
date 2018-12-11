# Configurer les extractions

## Exécution de l'extracteur {#config_exe}

La configuration de l'extracteur se fait via le fichier `*.Extract.proj`, écrit en XML (éditeur Notepad++ ou équivalent recommandé). Les numéros de ligne sont donnés à titre idnicatif et varient selon les configurations.

### Les données extraire

Pour configurer le catalogue Isogeo dans lequel se trouvent les données abonnées, il faut modifier les lignes 38 et 39  :

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

### Dossier de destination des extractions

Si l'extracteur est configuré pour extraire les données dans un dossier, le chemin est configurable à la ligne 8 :

```xml
<PropertyGroup>
  <IsogeoExtractorTasksPath Condition="'$(IsogeoExtractorTasksPath)'==''">$(MSBuildExtensionsPath)\Isogeo\Extractor</IsogeoExtractorTasksPath>

  <ExtractionDate>$(IsogeoExtractionDate)</ExtractionDate>
  <ExtractionTempPath>$(IsogeoExtractionTempPath)</ExtractionTempPath>
  <ExtractionPath>E:\Extract</ExtractionPath>
</PropertyGroup>
```

```

### Formats d'extraction

A partir de la ligne 16 :

```xml
<!-- Formats d'extraction -->
<ItemGroup>
  <ExtractFormat Include="geojson_2154">
    <Name>GeoJSON</Name>
    <CoordinateSystemName>RGF 93</CoordinateSystemName>
  </ExtractFormat>
  <ExtractFormat Include="shp_2154">
    <Name>Shapefile</Name>
    <CoordinateSystemName>RGF 93</CoordinateSystemName>
  </ExtractFormat>
</ItemGroup>
---

## Scripts FME {#config_fme}



