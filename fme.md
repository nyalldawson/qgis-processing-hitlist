# Mapping of FME transformers to Processing algorithms or QGIS expressions

N/A means "not applicable" in this context

FME Transformer|QGIS Processing Alg|QGIS Expression|Notes
---|---|---|---
[2DArcReplacer](https://www.safe.com/transformers/2d-arc-replacer/)|N/A|Needs expression functions to create circular strings
[2DBoxReplacer](https://www.safe.com/transformers/2d-box-replacer/)|N/A|Needs expression functions to create circular strings
[2DEllipseReplacer](https://www.safe.com/transformers/2d-ellipse-replacer/)|N/A|Needs expression functions to create circular strings
[2DForcer](https://www.safe.com/transformers/2d-forcer/)|Drop Z Value|Missing
[2DGridAccumulator](https://www.safe.com/transformers/2d-grid-accumulator/)|Create grid (with extend option)|N/A
[2DGridCreator](https://www.safe.com/transformers/2d-grid-creator/)|Create grid|N/A
[3DAffiner](https://www.safe.com/transformers/3d-affiner/)|Affine transform|N/A
[3DArcReplacer](https://www.safe.com/transformers/3d-arc-replacer/)|Missing|N/A
[3DForcer](https://www.safe.com/transformers/3d-forcer/)|Set Z Value|Missing
[3DInterpolator](https://www.safe.com/transformers/3d-interpolator/)|Missing|N/A|Also desirable for m values|
[3DRotator](https://www.safe.com/transformers/3d-rotator/)|Rotate|N/A
[Affiner](https://www.safe.com/transformers/affiner/)|Affine transform|Missing
[AffineWarper](https://www.safe.com/transformers/affine-warper/)|Missing|N/A|Would use gdal to perform warp via gcps -- could expose more than just affine transformation. Possibly aided by Lutra's upcoming work improving the QGIS georeferencer.|
[AggregateFilter](https://www.safe.com/transformers/aggregate-filter/)|Missing|N/A
[Aggregator](https://www.safe.com/transformers/aggregator/) |Aggregate, Collect geometries|collect
[AmazonAthenaConnector](https://www.safe.com/transformers/amazon-athena-connector/)|Missing|N/A
[AnchoredSnapper](https://www.safe.com/transformers/anchored-snapper/)|Snap geometries to layer|Missing|Performance issues |
[AngleConverter](https://www.safe.com/transformers/angle-converter/)|Missing|Needs expression functions to create circular strings
[AngularityCalculator](https://www.safe.com/transformers/angularity-calculator/)|Missing|Needs expression functions to create circular strings
[AppearanceExtractor](https://www.safe.com/transformers/appearance-extractor/) |Missing|Needs expression functions to create circular strings|Doesn't apply in QGIS|
[AppearanceMerger](https://www.safe.com/transformers/appearance-merger/)|Missing|Needs expression functions to create circular strings|Doesn't apply in QGIS|
[AppearanceRemover](https://www.safe.com/transformers/appearance-remover/)|Missing|Needs expression functions to create circular strings|Doesn't apply in QGIS|
[AppearanceSetter](https://www.safe.com/transformers/appearance-setter/)|Missing|Needs expression functions to create circular strings|Doesn't apply in QGIS|
[AppearanceStyler](https://www.safe.com/transformers/appearance-styler/)|Missing|Needs expression functions to create circular strings|Doesn't apply in QGIS|
[ArcEstimator](https://www.safe.com/transformers/arc-estimator/)|Missing|N/A|Port from PostGIS? Partial work at https://github.com/nyalldawson/QGIS/tree/convert_to_curves|
[ArcGISGridSnapper](https://www.safe.com/transformers/arcgis-grid-snapper/)|Missing|N/A
[ArcGISOnlineConnector](https://www.safe.com/transformers/arcgis-online-connector/)|Missing|N/A
[ArcPropertyExtractor](https://www.safe.com/transformers/arc-property-extractor/)|Missing|Needs expression functions to create circular strings
[ArcPropertySetter](https://www.safe.com/transformers/arc-property-setter/)|Missing|Needs expression functions to create circular strings
[ArcStroker](https://www.safe.com/transformers/arc-stroker/)|Segmentize by ...|Missing
[AreaAmalgamator](https://www.safe.com/transformers/area-amalgamator/)|Missing|N/A
[AreaBuilder](https://www.safe.com/transformers/area-builder/)|Polygonize|Missing
[AreaCalculator](https://www.safe.com/transformers/area-calculator/)|Add geometry attributes|$area
[AreaGapAndOverlapCleaner](https://www.safe.com/transformers/area-gap-and-overlap-cleaner/)|Snap geometries to layer|Missing
[AreaOnAreaOverlayer](https://www.safe.com/transformers/area-on-area-overlayer/)|Union|N/A
[AttributeCompressor](https://www.safe.com/transformers/attribute-compressor/) |Missing|N/A
[AttributeCopier](https://www.safe.com/transformers/attribute-copier/)|Field calculator, Refactor fields|N/A
[AttributeCreator](https://www.safe.com/transformers/attribute-creator/)|Add field to attributes table|N/A
[AttributeDecompressor](https://www.safe.com/transformers/attribute-decompressor/)|Missing|N/A
[AttributeDereferencer](https://www.safe.com/transformers/attribute-dereferencer/)|N/A |Needs expression functions to create circular strings
[AttributeEncoder](https://www.safe.com/transformers/attribute-encoder/)|N/A |Needs expression functions to create circular strings
[AttributeExploder](https://www.safe.com/transformers/attribute-exploder/)|Missing|N/A
[AttributeExposer](https://www.safe.com/transformers/attribute-exposer/)|N/A |Needs expression functions to create circular strings|Doesn't apply in QGIS|
[AttributeFileReader](https://www.safe.com/transformers/attribute-file-reader/)|Missing|N/A
[AttributeFileWriter](https://www.safe.com/transformers/attribute-file-writer/)|Extract binary field |N/A
[AttributeFilter](https://www.safe.com/transformers/attribute-filter/)|Extract by attribute, Feature filter|N/A
[AttributeKeeper](https://www.safe.com/transformers/attribute-keeper/)|Missing|N/A|Not currently possible, but highly desirable for flexible models|
[AttributeManager](https://www.safe.com/transformers/attribute-manager/)|Refactor fields |N/A
[AttributePivoter](https://www.safe.com/transformers/attribute-pivoter/)|Statistics by categories|N/A
[AttributeRangeFilter](https://www.safe.com/transformers/attribute-range-filter/)|Missing|N/A
[AttributeRangeMapper](https://www.safe.com/transformers/attribute-range-mapper/)|Missing|N/A
[AttributeRemover](https://www.safe.com/transformers/attribute-remover/)|Delete fields|N/A
[AttributeRenamer](https://www.safe.com/transformers/attribute-renamer/)|Rename field|N/A
[AttributeReprojector](https://www.safe.com/transformers/attribute-reprojector/)|N/A |Needs expression functions to create circular strings
[AttributeRounder](https://www.safe.com/transformers/attribute-rounder/)|N/A |Needs expression functions to create circular strings
[AttributeSplitter](https://www.safe.com/transformers/attribute-splitter/)|Split features by character|string_to_array
[AttributeTrimmer](https://www.safe.com/transformers/attribute-trimmer/)|N/A |Needs expression functions to create circular strings
[AttributeValidator](https://www.safe.com/transformers/attribute-validator/)|Missing|N/A
[AttributeValueMapper](https://www.safe.com/transformers/attribute-value-mapper/)|Missing|N/A
[AutodeskBIM360DocsConnector](https://www.safe.com/transformers/autodeskbim360-docs-connector/) |N/A |N/A
[AutodeskDocsConnector](https://www.safe.com/transformers/autodesk-docs-connector/)|N/A |N/A
[AWSIoTConnector](https://www.safe.com/transformers/aws-iot-connector/)|N/A |N/A
[AzureBlobStorageConnector](https://www.safe.com/transformers/azure-blob-storage-connector/)|N/A |N/A
[AzureComputerVisionConnector](https://www.safe.com/transformers/azure-computer-vision-connector/)|N/A |N/A
[AzureEventHubsConnector](https://www.safe.com/transformers/azure-event-hubs-connector/)|N/A |N/A
[AzureFileStorageConnector](https://www.safe.com/transformers/azure-file-storage-connector/)|N/A |N/A
[AzureIoTConnector](https://www.safe.com/transformers/azure-iot-connector/)|N/A |N/A
[AzureQueueStorageConnector](https://www.safe.com/transformers/azure-queue-storage-connector/)|N/A |N/A
[AzureServiceBusConnector](https://www.safe.com/transformers/azure-service-bus-connector/) |N/A |N/A
[AzureTextAnalyticsConnector](https://www.safe.com/transformers/azure-text-analytics-connector/)|N/A |N/A
[BaseConverter](https://www.safe.com/transformers/base-converter/)|N/A |Needs expression functions to create circular strings
[BinaryDecoder](https://www.safe.com/transformers/binary-decoder/)|N/A |Needs expression functions to create circular strings
[BinaryEncoder](https://www.safe.com/transformers/binary-encoder/)|N/A |Needs expression functions to create circular strings
[BoundingBoxAccumulator](https://www.safe.com/transformers/bounding-box-accumulator/)|Extract layer extent |N/A
[BoundingBoxReplacer](https://www.safe.com/transformers/bounding-box-replacer/)|Bounding boxes|bounds
[BoundsExtractor](https://www.safe.com/transformers/bounds-extractor/)|N/A |Needs expression functions to create circular strings
[BoxConnector](https://www.safe.com/transformers/box-connector/)|Missing|N/A|3rd party plugin candidate |
[Bufferer](https://www.safe.com/transformers/bufferer/)|Buffer|buffer
[BulkAttributeRemover](https://www.safe.com/transformers/bulk-attribute-remover/)|Missing|N/A
[BulkAttributeRenamer](https://www.safe.com/transformers/bulk-attribute-renamer/)|Missing|N/A
[CenterlineReplacer](https://www.safe.com/transformers/centerline-replacer/)|Missing|N/A|No reliable algorithm publicly available, non trivial! |
[CenterPointExtractor](https://www.safe.com/transformers/center-point-extractor/)|centroid, point on surface, pole of inaccessibility|centroid, point_on_surface, pole_of_inaccessibility 
[CenterPointReplacer](https://www.safe.com/transformers/center-point-replacer/)|centroid, point on surface, pole of inaccessibility|centroid, point_on_surface, pole_of_inaccessibility 
[CesiumIonConnector](https://www.safe.com/transformers/cesium-ion-connector/)|Missing|N/A
[ChangeDetector](https://www.safe.com/transformers/change-detector/)|Detect dataset changes|N/A
[CharacterCodeExtractor](https://www.safe.com/transformers/character-code-extractor/)|Possible with Refactor field and expression|Needs expression functions to create circular strings
[CharacterCodeReplacer](https://www.safe.com/transformers/character-code-replacer/)|Possible with Refactor field and expression|Needs expression functions to create circular strings
[ChartGenerator](https://www.safe.com/transformers/chart-generator/)|Bar plot, box plot, etc|N/A|Better served by the 3rd party "DataPlotly" plugin|
[Chopper](https://www.safe.com/transformers/chopper/)|Subdivide, Explode Lines|segments_to_lines, Missing subdivide function 
[CircularityCalculator](https://www.safe.com/transformers/circularity-calculator/)|Missing|N/A
[CityEngineModelGenerator](https://www.safe.com/transformers/city-engine-model-generator/) |Missing|N/A
[CKANConnector](https://www.safe.com/transformers/ckan-connector/)|Missing|N/A
[Clipper](https://www.safe.com/transformers/clipper/)|clip|intersection 
[Cloner](https://www.safe.com/transformers/cloner/)|Array of translated features|N/A
[ClosedCurveFilter](https://www.safe.com/transformers/closed-curve-filter/)|N/A |Needs expression functions to create circular strings
[CommonLocalReprojector](https://www.safe.com/transformers/common-local-reprojector/)|Missing|N/A|would need a way to transform using a custom WKT or proj string|
[CommonSegmentFinder](https://www.safe.com/transformers/common-segment-finder/)|Missing|N/A|GEOS library exposes this functionality, but not exposed through QGIS|
[ComprehendConnector](https://www.safe.com/transformers/comprehend-connector/) |Missing|N/A
[ContourGenerator](https://www.safe.com/transformers/contour-generator/)|GDAL Contours|N/A
[ConvexityFilter](https://www.safe.com/transformers/convexity-filter/)|N/A |Needs expression functions to create circular strings
[CoordinateConcatenator](https://www.safe.com/transformers/coordinate-concatenator/) |Missing|N/A
[CoordinateExtractor](https://www.safe.com/transformers/coordinate-extractor/) |Add x/y fields to layer|x/y/etc
[CoordinateRounder](https://www.safe.com/transformers/coordinate-rounder/)|Snap points to grid|Missing
[CoordinateSwapper](https://www.safe.com/transformers/coordinate-swapper/)|Swap x and y coordinates|flip_coordinates
[CoordinateSystemDescriptionConverter](https://www.safe.com/transformers/coordinate-system-description-converter/)|Missing|N/A
[CoordinateSystemExtractor](https://www.safe.com/transformers/coordinate-system-extractor/)|Missing|N/A
[CoordinateSystemRemover](https://www.safe.com/transformers/coordinate-system-remover/)|Missing|N/A
[CoordinateSystemSetter](https://www.safe.com/transformers/coordinate-system-setter/)|Assign projection|N/A
[Counter](https://www.safe.com/transformers/counter/)|Add autoincremental field|N/A
[CRCCalculator](https://www.safe.com/transformers/crc-calculator/)|N/A |Needs expression functions to create circular strings
[Creator](https://www.safe.com/transformers/creator/)|Geometry by expression|N/A
[CSGBuilder](https://www.safe.com/transformers/csg-builder/)|Missing|N/A
[CSGEvaluator](https://www.safe.com/transformers/csg-evaluator/)|Missing|N/A
[CsmapAttributeReprojector](https://www.safe.com/transformers/csmap-attribute-reprojector/)|N/A |Needs expression functions to create circular strings|QGIS always uses the proj library|
[CsmapReprojector](https://www.safe.com/transformers/csmap-reprojector/)|N/A |Needs expression functions to create circular strings|QGIS always uses the proj libray |
[Curvefitter](https://www.safe.com/transformers/curvefitter/)|Missing|N/A|Port from PostGIS? Partial work at https://github.com/nyalldawson/QGIS/tree/convert_to_curves|
[DatabaseDeleter](https://www.safe.com/transformers/database-deleter/)|Missing|N/A
[DatabaseJoiner](https://www.safe.com/transformers/database-joiner/)|Join attributes by \*|N/A
[DatabaseUpdater](https://www.safe.com/transformers/database-updater/)|Missing|N/A
[DateTimeCalculator](https://www.safe.com/transformers/date-time-calculator/)|N/A |Needs expression functions to create circular strings
[DateTimeConverter](https://www.safe.com/transformers/date-time-converter/)|Missing|N/A
[DateTimeRounder](https://www.safe.com/transformers/date-time-rounder/)|Missing|N/A
[DateTimeStamper](https://www.safe.com/transformers/date-time-stamper/)|N/A |Needs expression functions to create circular strings
[Deaggregator](https://www.safe.com/transformers/deaggregator/)|Multipart to singleparts|Missing
[Decelerator](https://www.safe.com/transformers/decelerator/)|N/A |Needs expression functions to create circular strings
[DecimalDegreesCalculator](https://www.safe.com/transformers/decimal-degrees-calculator/)|N/A |Needs expression functions to create circular strings
[DEMDistanceCalculator](https://www.safe.com/transformers/dem-distance-calculator/)|Missing|N/A
[DEMGenerator](https://www.safe.com/transformers/dem-generator/)|TIN interpolation|N/A
[Densifier](https://www.safe.com/transformers/densifier/)|Densify by count/Densify by distance|Missing
[DensityCalculator](https://www.safe.com/transformers/density-calculator/)|Missing|N/A
[DGNStyler](https://www.safe.com/transformers/dgn-styler/)|Missing|N/A|3rd party plugin candidate |
[DimensionExtractor](https://www.safe.com/transformers/dimension-extractor/)|N/A |Needs expression functions to create circular strings
[DirectTweeter](https://www.safe.com/transformers/direct-tweeter/)|Missing|N/A|3rd party plugin candidate |
[Displacer](https://www.safe.com/transformers/displacer/)|Points diplacement is a partial match |N/A
[Dissolver](https://www.safe.com/transformers/dissolver/)|Dissolve|Union
[DMSCalculator](https://www.safe.com/transformers/dms-calculator/)|N/A |Needs expression functions to create circular strings
[DonutBridgeBuilder](https://www.safe.com/transformers/donut-bridge-builder/)|Missing|N/A
[DonutBuilder](https://www.safe.com/transformers/donut-builder/)|Difference|difference
[DonutHoleExtractor](https://www.safe.com/transformers/donut-hole-extractor/)|N/A |Needs expression functions to create circular strings
[DropboxConnector](https://www.safe.com/transformers/dropbox-connector/)|Missing|N/A|3rd party plugin candidate |
[DuplicateFilter](https://www.safe.com/transformers/duplicate-filter/)|Delete duplicate geometries, delete duplicates by attribute|N/A
[DWGStyler](https://www.safe.com/transformers/dwg-styler/)|Missing|N/A|DXF export is not exposed to Processing|
[ElevationExtractor](https://www.safe.com/transformers/elevation-extractor/)|Extract z values|z
[EllipsePropertyExtractor](https://www.safe.com/transformers/ellipse-property-extractor/)|N/A |Needs expression functions to create circular strings
[EllipsePropertySetter](https://www.safe.com/transformers/ellipse-property-setter/)|N/A |Needs expression functions to create circular strings
[Emailer](https://www.safe.com/transformers/emailer/)|Missing|N/A
[EnvironmentVariableFetcher](https://www.safe.com/transformers/environment-variable-fetcher/)|N/A |Needs expression functions to create circular strings
[EsriReprojector](https://www.safe.com/transformers/esri-reprojector/)|N/A |Needs expression functions to create circular strings|QGIS always uses the PROJ library for transforms|
[EthereumConnector](https://www.safe.com/transformers/ethereum-connector/)|Missing|Missing
[ExcelStyler](https://www.safe.com/transformers/excel-styler/)|Missing|N/A
[ExpressionEvaluator](https://www.safe.com/transformers/expression-evaluator/) |Many|Many 
[Extruder](https://www.safe.com/transformers/extruder/)|v.extrude |N/A
[FaceReplacer](https://www.safe.com/transformers/face-replacer/)|Missing|N/A
[FeatureColorSetter](https://www.safe.com/transformers/feature-color-setter/)|N/A |Needs expression functions to create circular strings|Possibly value in algorithms which create layer styles in place|
[FeatureHolder](https://www.safe.com/transformers/feature-holder/)|N/A |Needs expression functions to create circular strings
[FeatureJoiner](https://www.safe.com/transformers/feature-joiner/)|Join attributes by field value, Join attributes by location|N/A
[FeatureMerger](https://www.safe.com/transformers/feature-merger/)|Join attributes by field value|N/A
[FeatureReader](https://www.safe.com/transformers/feature-reader/)|N/A |Needs expression functions to create circular strings|Vector file handling|
[FeatureTypeExtractor](https://www.safe.com/transformers/feature-type-extractor/)|N/A |Needs expression functions to create circular strings
[FeatureTypeFilter](https://www.safe.com/transformers/feature-type-filter/)|Filter by geometry type|N/A
[FeatureWriter](https://www.safe.com/transformers/feature-writer/)|N/A |Needs expression functions to create circular strings|Vector file writer |
[FilenamePartExtractor](https://www.safe.com/transformers/filename-part-extractor/)|N/A |Needs expression functions to create circular strings
[FMEFlowJobSubmitter](https://www.safe.com/transformers/fme-flow-job-submitter/)|N/A |N/A
[FMEFlowJobWaiter](https://www.safe.com/transformers/fme-flow-job-waiter/)|N/A |N/A
[FMEFlowLogFileRetriever](https://www.safe.com/transformers/fme-flow-log-file-retriever/)|N/A |N/A
[FMEFlowNotifier](https://www.safe.com/transformers/fme-flow-notifier/)|N/A |N/A
[FMEFlowResourceConnector](https://www.safe.com/transformers/fme-flow-resource-connector/) |N/A |N/A
[FMEFunctionCaller](https://www.safe.com/transformers/fme-function-caller/)|N/A |Needs expression functions to create circular strings
[FTPCaller](https://www.safe.com/transformers/ftp-caller/)|Missing|N/A
[Generalizer](https://www.safe.com/transformers/generalizer/)|Simplify, smooth|simplify, smooth
[Geocoder](https://www.safe.com/transformers/geocoder/)|Missing|N/A|3rd party plugin candidate, exposing geocoding via different services|
[GeometryCoercer](https://www.safe.com/transformers/geometry-coercer/)|Convert geometry type|N/A
[GeometryColorSetter](https://www.safe.com/transformers/geometry-color-setter/)|N/A |Needs expression functions to create circular strings
[GeometryExtractor](https://www.safe.com/transformers/geometry-extractor/)|N/A |Needs expression functions to create circular strings
[GeometryFilter](https://www.safe.com/transformers/geometry-filter/)|Filter by geometry type|N/A
[GeometryInstantiator](https://www.safe.com/transformers/geometry-instantiator/)|Affine transform, Array of translated features|N/A
[GeometryPartExtractor](https://www.safe.com/transformers/geometry-part-extractor/)|Missing|N/A
[GeometryPropertyExtractor](https://www.safe.com/transformers/geometry-property-extractor/)|N/A |Needs expression functions to create circular strings
[GeometryPropertyRemover](https://www.safe.com/transformers/geometry-property-remover/)|Missing|N/A
[GeometryPropertyRenamer](https://www.safe.com/transformers/geometry-property-renamer/)|Missing|N/A
[GeometryPropertySetter](https://www.safe.com/transformers/geometry-property-setter/)|Missing|N/A
[GeometryRefiner](https://www.safe.com/transformers/geometry-refiner/)|N/A |Needs expression functions to create circular strings
[GeometryRemover](https://www.safe.com/transformers/geometry-remover/)|Drop geometries |N/A
[GeometryReplacer](https://www.safe.com/transformers/geometry-replacer/)|Geometry by expression|N/A
[GeometryValidator](https://www.safe.com/transformers/geometry-validator/)|Validate geometries|is_valid
[GeoRSSFeatureComposer](https://www.safe.com/transformers/georss-feature-composer/)|N/A |Needs expression functions to create circular strings
[GeoRSSFeatureReader](https://www.safe.com/transformers/georss-feature-reader/)|Inbuilt vector handling|Missing
[GMLFeatureComposer](https://www.safe.com/transformers/gml-feature-composer/)|N/A |Needs expression functions to create circular strings
[GOIDGenerator](https://www.safe.com/transformers/goid-generator/)|Missing|N/A
[GoogleBigQueryConnector](https://www.safe.com/transformers/google-big-query-connector/)|Missing|N/A
[GoogleCloudPubSubConnector](https://www.safe.com/transformers/google-cloud-pub-sub-connector/) |N/A |N/A
[GoogleCloudStorageConnector](https://www.safe.com/transformers/google-cloud-storage-connector/)|N/A |N/A
[GoogleDriveConnector](https://www.safe.com/transformers/google-drive-connector/)|Missing|N/A|3rd party plugin candidate |
[GoogleIoTConnector](https://www.safe.com/transformers/google-iot-connector/)|N/A |N/A
[GoogleLanguageConnector](https://www.safe.com/transformers/google-language-connector/)|N/A |N/A
[GoogleVisionConnector](https://www.safe.com/transformers/google-vision-connector/)|N/A |N/A
[GridInQuestIIReprojector](https://www.safe.com/transformers/grid-in-questii-reprojector/) |N/A |Needs expression functions to create circular strings|QGIS always uses the PROJ library for reprojection|
[GtransAttributeReprojector](https://www.safe.com/transformers/gtrans-attribute-reprojector/)|N/A |Needs expression functions to create circular strings|QGIS always uses the PROJ library for reprojection|
[GtransReprojector](https://www.safe.com/transformers/gtrans-reprojector/)|N/A |Needs expression functions to create circular strings|QGIS always uses the PROJ library for reprojection|
[H3HexagonalIndexer](https://www.safe.com/transformers/h3-hexagonal-indexer/)|Missing|N/A
[HDFSConnector](https://www.safe.com/transformers/hdfs-connector/)|N/A |Needs expression functions to create circular strings|Handled by the GDAL library|
[HoleCounter](https://www.safe.com/transformers/hole-counter/)|N/A |Needs expression functions to create circular strings
[HTMLExtractor](https://www.safe.com/transformers/html-extractor/)|Missing|N/A|3rd party plugin candidate |
[HTMLLayouter](https://www.safe.com/transformers/html-layouter/)|Missing|N/A
[HTMLReportGenerator](https://www.safe.com/transformers/html-report-generator/)|Missing|N/A
[HTMLToXHTMLConverter](https://www.safe.com/transformers/html-toxhtml-converter/)|Missing|N/A
[HTTPCaller](https://www.safe.com/transformers/http-caller/)|Missing|N/A
[HullAccumulator](https://www.safe.com/transformers/hull-accumulator/)|Convex hull, Concave hull|convex_hull
[HullReplacer](https://www.safe.com/transformers/hull-replacer/)|Convex hull, Concave hull|convex_hull
[IBMIoTConnector](https://www.safe.com/transformers/ibm-iot-connector/)|Missing|N/A
[IFCPropertySetDefinitionCreator](https://www.safe.com/transformers/ifc-property-set-definition-creator/)|N/A |N/A
[IFCQuantitySetDefinitionCreator](https://www.safe.com/transformers/ifc-quantity-set-definition-creator/)|N/A |N/A
[ImageFetcher](https://www.safe.com/transformers/image-fetcher/)|Missing|N/A
[ImageRasterizer](https://www.safe.com/transformers/image-rasterizer/)|Rasterize (GDAL), Convert map to raster, XYZ Tiles |N/A
[InlineQuerier](https://www.safe.com/transformers/inline-querier/)|Spatialite execute SQL, Execute SQL|N/A
[Inspector](https://www.safe.com/transformers/inspector/)|N/A |Needs expression functions to create circular strings
[Intersector](https://www.safe.com/transformers/intersector/)|Intersection|intersection 
[JMSReceiver](https://www.safe.com/transformers/jms-receiver/)|Missing|N/A|3rd party plugin candidate |
[JMSSender](https://www.safe.com/transformers/jms-sender/)|Missing|N/A|3rd party plugin candidate |
[JSONExtractor](https://www.safe.com/transformers/json-extractor/)|Explode hstore field |map and array functions 
[JSONFlattener](https://www.safe.com/transformers/json-flattener/)|Explode hstore field |map and array functions 
[JSONFormatter](https://www.safe.com/transformers/json-formatter/)|N/A |Needs expression functions to create circular strings
[JSONFragmenter](https://www.safe.com/transformers/json-fragmenter/)|N/A |Needs expression functions to create circular strings
[JSONTemplater](https://www.safe.com/transformers/json-templater/)|N/A |Needs expression functions to create circular strings
[JSONUpdater](https://www.safe.com/transformers/json-updater/)|N/A |Needs expression functions to create circular strings
[JSONValidator](https://www.safe.com/transformers/json-validator/)|Missing|N/A
[Junction](https://www.safe.com/transformers/junction/)|Merge vector layers|N/A
[KafkaConnector](https://www.safe.com/transformers/kafka-connector/)|Missing|N/A
[KinesisReceiver](https://www.safe.com/transformers/kinesis-receiver/)|Missing|N/A|3rd party plugin candidate |
[KinesisSender](https://www.safe.com/transformers/kinesis-sender/)|Missing|N/A|3rd party plugin candidate |
[KMLPropertySetter](https://www.safe.com/transformers/kml-property-setter/)|Missing|N/A
[KMLRegionSetter](https://www.safe.com/transformers/kml-region-setter/)|Missing|N/A
[KMLStyler](https://www.safe.com/transformers/kml-styler/)|Missing|N/A
[KMLTimeSetter](https://www.safe.com/transformers/kml-time-setter/)|Missing|N/A
[KMLTourBuilder](https://www.safe.com/transformers/kml-tour-builder/)|Missing|N/A|3rd party plugin candidate |
[KMLViewSetter](https://www.safe.com/transformers/kml-view-setter/)|Missing|N/A|3rd party plugin candidate |
[Labeller](https://www.safe.com/transformers/labeller/)|N/A |Needs expression functions to create circular strings
[LabelPointReplacer](https://www.safe.com/transformers/label-point-replacer/)|N/A |Needs expression functions to create circular strings
[LatLongToMGRSConverter](https://www.safe.com/transformers/lat-long-tomgrs-converter/)|Missing|N/A
[LeftRightSpatialCalculator](https://www.safe.com/transformers/left-right-spatial-calculator/)|Missing|N/A|Raw API already exists, but not exposed to QGIS Processing or Expressions |
[LengthCalculator](https://www.safe.com/transformers/length-calculator/)|Add geometry attributes|$area
[LengthToPointCalculator](https://www.safe.com/transformers/length-to-point-calculator/)|Missing|N/A
[LineBuilder](https://www.safe.com/transformers/line-builder/)|Points to paths |N/A
[LineCloser](https://www.safe.com/transformers/line-closer/)|Missing|N/A
[LineCombiner](https://www.safe.com/transformers/line-combiner/)|Merge lines|line_merge
[LineExtender](https://www.safe.com/transformers/line-extender/)|Extend lines|extend
[LineOnAreaOverlayer](https://www.safe.com/transformers/line-on-area-overlayer/)|Union|N/A
[LineOnLineOverlayer](https://www.safe.com/transformers/line-on-line-overlayer/)|Union|N/A
[ListBasedFeatureMerger](https://www.safe.com/transformers/list-based-feature-merger/)|N/A |Needs expression functions to create circular strings
[ListBuilder](https://www.safe.com/transformers/list-builder/)|N/A |Needs expression functions to create circular strings
[ListConcatenator](https://www.safe.com/transformers/list-concatenator/)|N/A |Needs expression functions to create circular strings
[ListCopier](https://www.safe.com/transformers/list-copier/)|N/A |Needs expression functions to create circular strings
[ListDuplicateRemover](https://www.safe.com/transformers/list-duplicate-remover/)|N/A |Needs expression functions to create circular strings
[ListElementCounter](https://www.safe.com/transformers/list-element-counter/)|N/A |Needs expression functions to create circular strings
[ListExploder](https://www.safe.com/transformers/list-exploder/)|Missing|N/A
[ListExpressionPopulator](https://www.safe.com/transformers/list-expression-populator/)|N/A |Needs expression functions to create circular strings
[ListHistogrammer](https://www.safe.com/transformers/list-histogrammer/)|N/A |Needs expression functions to create circular strings
[ListIndexer](https://www.safe.com/transformers/list-indexer/)|N/A |Needs expression functions to create circular strings
[ListPopulator](https://www.safe.com/transformers/list-populator/)|N/A |Needs expression functions to create circular strings
[ListRangeExtractor](https://www.safe.com/transformers/list-range-extractor/)|N/A |Needs expression functions to create circular strings
[ListRenamer](https://www.safe.com/transformers/list-renamer/)|N/A |Needs expression functions to create circular strings|Doesn't apply in QGIS|
[ListSearcher](https://www.safe.com/transformers/list-searcher/)|N/A |Needs expression functions to create circular strings
[ListSorter](https://www.safe.com/transformers/list-sorter/)|N/A |Needs expression functions to create circular strings
[ListSummer](https://www.safe.com/transformers/list-summer/)|N/A |Needs expression functions to create circular strings
[LocalCoordinateSystemSetter](https://www.safe.com/transformers/local-coordinate-system-setter/)|Assign projection|N/A
[Logger](https://www.safe.com/transformers/logger/)|Missing|N/A
[LogMessageStreamer](https://www.safe.com/transformers/log-message-streamer/)|Save log to file|N/A
[MapboxStyler](https://www.safe.com/transformers/mapbox-styler/)|Missing|N/A
[MapInfoStyler](https://www.safe.com/transformers/map-info-styler/)|Missing|N/A
[MapnikRasterizer](https://www.safe.com/transformers/mapnik-rasterizer/)|N/A |Needs expression functions to create circular strings
[MapTextLabeller](https://www.safe.com/transformers/map-text-labeller/)|N/A |Needs expression functions to create circular strings
[MapTextStyler](https://www.safe.com/transformers/map-text-styler/)|N/A |Needs expression functions to create circular strings
[Matcher](https://www.safe.com/transformers/matcher/)|Delete duplicate geometries, Delete duplicates by attribute|N/A
[MeasureExtractor](https://www.safe.com/transformers/measure-extractor/)|Line substring, Extract specific vertices, Interpolate point on line, Extract M values|line_substring, line_interpolate_point, m
[MeasureGenerator](https://www.safe.com/transformers/measure-generator/)|Set M value, Set M value from raster|line_locate_point 
[MeasureRemover](https://www.safe.com/transformers/measure-remover/)|Drop M/Z values, Filter vertices by M value|N/A
[MeasureSetter](https://www.safe.com/transformers/measure-setter/)|Set M value, Set M value from raster|line_locate_point 
[MeshMerger](https://www.safe.com/transformers/mesh-merger/)|Missing|N/A
[MeshSimplifier](https://www.safe.com/transformers/mesh-simplifier/)|Missing|N/A
[MGRSToLatLongConverter](https://www.safe.com/transformers/mgrs-to-lat-long-converter/)|Missing|N/A
[MinimumAreaForcer](https://www.safe.com/transformers/minimum-area-forcer/)|Missing|N/A
[MinimumSpanningCircleReplacer](https://www.safe.com/transformers/minimum-spanning-circle-replacer/)|Missing|N/A
[ModuloCounter](https://www.safe.com/transformers/modulo-counter/)|Missing|N/A
[MQTTConnector](https://www.safe.com/transformers/mqtt-connector/)|Missing|N/A
[MSWordStyler](https://www.safe.com/transformers/ms-word-styler/) |Missing|N/A|3rd party plugin candidate |
[MultipleGeometryFilter](https://www.safe.com/transformers/multiple-geometry-filter/)|Multiparts to singleparts|geometry_n
[MultipleGeometrySetter](https://www.safe.com/transformers/multiple-geometry-setter/)|Collect geometries, Promote to Multipart|collect_geometries
[NeighborFinder](https://www.safe.com/transformers/neighbor-finder/)|Join attributes by nearest |N/A
[NeighborhoodAggregator](https://www.safe.com/transformers/neighborhood-aggregator/) |DBSCAN clustering, K-means clustering, v.cluster|N/A
[NeighborPairFinder](https://www.safe.com/transformers/neighbor-pair-finder/)|Missing|N/A
[NetworkCostCalculator](https://www.safe.com/transformers/network-cost-calculator/)|Shortest Path algorithms|N/A
[NetworkFlowOrientor](https://www.safe.com/transformers/network-flow-orientor/)|Missing|N/A
[NetworkTopologyCalculator](https://www.safe.com/transformers/network-topology-calculator/)|Missing|N/A
[NLPClassifier](https://www.safe.com/transformers/nlp-classifier/)|Missing|N/A
[NLPTrainer](https://www.safe.com/transformers/nlp-trainer/)|Missing|N/A
[NullAttributeMapper](https://www.safe.com/transformers/null-attribute-mapper/)|Missing|N/A|Possible using field calculator with QGIS expressions|
[NumericRasterizer](https://www.safe.com/transformers/numeric-rasterizer/)|GDAL Rasterize|N/A
[OffsetCurveGeneratorOffsetter](https://www.safe.com/transformers/offset-curve-generator-offsetter/)|Missing|N/A
[Offsetter](https://www.safe.com/transformers/offsetter/)|Translate |translate
[OneDriveConnector](https://www.safe.com/transformers/one-drive-connector/)|Missing|N/A|3rd party plugin candidate |
[OrientationExtractor](https://www.safe.com/transformers/orientation-extractor/)|N/A |Needs expression functions to create circular strings
[Orientor](https://www.safe.com/transformers/orientor/)|Force right hand rule|force_rhr
[ParameterFetcher](https://www.safe.com/transformers/parameter-fetcher/)|Field calculator with input parameters|N/A
[PartCounter](https://www.safe.com/transformers/part-counter/)|N/A |Needs expression functions to create circular strings
[PathBuilder](https://www.safe.com/transformers/path-builder/)|Missing|N/A
[PathSplitter](https://www.safe.com/transformers/path-splitter/)|Explode lines|segments_to_lines 
[PDFPageFormatter](https://www.safe.com/transformers/pdf-page-formatter/) |Missing|N/A|Inbuilt algorithms for exporting layouts are desirable |
[PDFStyler](https://www.safe.com/transformers/pdf-styler/)|Missing|N/A|Requires inbuilt algorithm for exporting layout to GeoPDF with attributes |
[PipeEvaluator](https://www.safe.com/transformers/pipe-evaluator/)|Missing|N/A
[PipeReplacer](https://www.safe.com/transformers/pipe-replacer/)|Missing|N/A
[PlanarityFilter](https://www.safe.com/transformers/planarity-filter/)|N/A |Needs expression functions to create circular strings|Requires 'is_planar' expression function|
[Player](https://www.safe.com/transformers/player/)|N/A |Needs expression functions to create circular strings
[PointCloudCombiner](https://www.safe.com/transformers/point-cloud-combiner/)|Via pdal or lastools plugins|N/A
[PointCloudComponentAdder](https://www.safe.com/transformers/point-cloud-component-adder/) |Via pdal or lastools plugins|N/A
[PointCloudComponentCopier](https://www.safe.com/transformers/point-cloud-component-copier/)|Via pdal or lastools plugins|N/A
[PointCloudComponentKeeper](https://www.safe.com/transformers/point-cloud-component-keeper/)|Via pdal or lastools plugins|N/A
[PointCloudComponentRemover](https://www.safe.com/transformers/point-cloud-component-remover/)|Via pdal or lastools plugins|N/A
[PointCloudComponentRenamer](https://www.safe.com/transformers/point-cloud-component-renamer/)|Via pdal or lastools plugins|N/A
[PointCloudComponentTypeCoercer](https://www.safe.com/transformers/point-cloud-component-type-coercer/)|Via pdal or lastools plugins|N/A
[PointCloudConsumer](https://www.safe.com/transformers/point-cloud-consumer/)|Via pdal or lastools plugins|N/A
[PointCloudCreator](https://www.safe.com/transformers/point-cloud-creator/)|Via pdal or lastools plugins|N/A
[PointCloudExpressionEvaluator](https://www.safe.com/transformers/point-cloud-expression-evaluator/)|Via pdal or lastools plugins|N/A
[PointCloudExtractor](https://www.safe.com/transformers/point-cloud-extractor/)|Via pdal or lastools plugins|N/A
[PointCloudFilter](https://www.safe.com/transformers/point-cloud-filter/) |Via pdal or lastools plugins|N/A
[PointCloudMerger](https://www.safe.com/transformers/point-cloud-merger/) |Via pdal or lastools plugins|N/A
[PointCloudOnRasterComponentSetter](https://www.safe.com/transformers/point-cloud-on-raster-component-setter/)|Via pdal or lastools plugins|N/A
[PointCloudPropertyExtractor](https://www.safe.com/transformers/point-cloud-property-extractor/)|Via pdal or lastools plugins|N/A
[PointCloudReplacer](https://www.safe.com/transformers/point-cloud-replacer/)|Via pdal or lastools plugins|N/A
[PointCloudSimplifier](https://www.safe.com/transformers/point-cloud-simplifier/)|Via pdal or lastools plugins|N/A
[PointCloudSorter](https://www.safe.com/transformers/point-cloud-sorter/) |Via pdal or lastools plugins|N/A
[PointCloudSplitter](https://www.safe.com/transformers/point-cloud-splitter/)|Via pdal or lastools plugins|N/A
[PointCloudStatisticsCalculator](https://www.safe.com/transformers/point-cloud-statistics-calculator/)|Via pdal or lastools plugins|N/A
[PointCloudSurfaceBuilder](https://www.safe.com/transformers/point-cloud-surface-builder/) |Via pdal or lastools plugins|N/A
[PointCloudThinner](https://www.safe.com/transformers/point-cloud-thinner/)|Via pdal or lastools plugins|N/A
[PointCloudToPointCoercer](https://www.safe.com/transformers/point-cloud-to-point-coercer/)|Via pdal or lastools plugins|N/A
[PointCloudTransformationApplier](https://www.safe.com/transformers/point-cloud-transformation-applier/)|Via pdal or lastools plugins|N/A
[PointOnAreaOverlayer](https://www.safe.com/transformers/point-on-area-overlayer/)|Join attributes by location|N/A
[PointOnLineOverlayer](https://www.safe.com/transformers/point-on-line-overlayer/)|Join attributes by location|N/A
[PointOnPointOverlayer](https://www.safe.com/transformers/point-on-point-overlayer/) |Join attributes by location|N/A
[PointOnRasterValueExtractor](https://www.safe.com/transformers/point-on-raster-value-extractor/)|Sample raster values |raster_value 
[PointPropertyExtractor](https://www.safe.com/transformers/point-property-extractor/)|N/A |Needs expression functions to create circular strings|Rotation is treated just like normal attributes in QGIS|
[PointPropertySetter](https://www.safe.com/transformers/point-property-setter/)|Field calculator|Mixed expression functions, e.g. radians, degrees|Rotation is treated just like normal attributes in QGIS|
[PowerPointStyler](https://www.safe.com/transformers/power-point-styler/) |Missing|N/A|3rd party plugin candidate |
[PROJAttributeReprojector](https://www.safe.com/transformers/proj-attribute-reprojector/)|N/A |N/A
[ProjectWiseWSGConnector](https://www.safe.com/transformers/project-wisewsg-connector/)|N/A |N/A
[PROJReprojector](https://www.safe.com/transformers/proj-reprojector/)|Reproject layer |transform
[PythonCaller](https://www.safe.com/transformers/python-caller/)|QGIS processing use Python |N/A|Possible to create algorithms and expressions via Python. Desirable would be to allow Python scripts to be embedded inside a model. |
[PythonCreator](https://www.safe.com/transformers/python-creator/)|QGIS processing use Python |N/A|Possible to create algorithms and expressions via Python. Desirable would be to allow Python scripts to be embedded inside a model. |
[RabbitMQConnector](https://www.safe.com/transformers/rabbitmq-connector/)|Missing|Missing
[RandomNumberGenerator](https://www.safe.com/transformers/random-number-generator/)|N/A |Needs expression functions to create circular strings
[RasterAspectCalculator](https://www.safe.com/transformers/raster-aspect-calculator/)|Aspect|N/A
[RasterBandAdder](https://www.safe.com/transformers/raster-band-adder/)|Missing|N/A|Possible via Create Constant Raster Layer and GDAL Merge algorithms, but a direct algorithm is desirable|
[RasterBandCombiner](https://www.safe.com/transformers/raster-band-combiner/)|GDAL Merge|N/A
[RasterBandInterpretationCoercer](https://www.safe.com/transformers/raster-band-interpretation-coercer/)|GDAL Translate|N/A
[RasterBandKeeper](https://www.safe.com/transformers/raster-band-keeper/) |Rearrange Bands |N/A
[RasterBandMinMaxExtractor](https://www.safe.com/transformers/raster-band-min-max-extractor/)|Raster layer statistics|raster_statistic
[RasterBandNameSetter](https://www.safe.com/transformers/raster-band-name-setter/)|Missing|N/A
[RasterBandNodataRemover](https://www.safe.com/transformers/raster-band-nodata-remover/)|Fill NoData Cells|N/A
[RasterBandNodataSetter](https://www.safe.com/transformers/raster-band-nodata-setter/)|Missing|N/A
[RasterBandOrderer](https://www.safe.com/transformers/raster-band-orderer/)|Rearrange Bands |N/A
[RasterBandPropertyExtractor](https://www.safe.com/transformers/raster-band-property-extractor/)|Missing|N/A
[RasterBandRemover](https://www.safe.com/transformers/raster-band-remover/)|Rearrange Bands |N/A
[RasterBandSeparator](https://www.safe.com/transformers/raster-band-separator/)|Rearrange Bands |N/A
[RasterCellCoercer](https://www.safe.com/transformers/raster-cell-coercer/)|Raster pixels to points, Raster pixels to polygons |N/A
[RasterCellOriginSetter](https://www.safe.com/transformers/raster-cell-origin-setter/)|Missing|N/A
[RasterCellValueCalculator](https://www.safe.com/transformers/raster-cell-value-calculator/)|Raster calculator|N/A
[RasterCellValueReplacer](https://www.safe.com/transformers/raster-cell-value-replacer/)|Reclassify by layer, Reclassify by table|N/A
[RasterCellValueRounder](https://www.safe.com/transformers/raster-cell-value-rounder/)|Missing|N/A
[RasterCheckpointer](https://www.safe.com/transformers/raster-checkpointer/)|N/A |Needs expression functions to create circular strings
[RasterConsumer](https://www.safe.com/transformers/raster-consumer/)|N/A |Needs expression functions to create circular strings
[RasterConvolver](https://www.safe.com/transformers/raster-convolver/)|N/A |Needs expression functions to create circular strings
[RasterDEMGenerator](https://www.safe.com/transformers/rasterdem-generator/)|TIN Interpolation|N/A
[RasterExpressionEvaluator](https://www.safe.com/transformers/raster-expression-evaluator/)|Raster calculator|N/A
[RasterExtentsCoercer](https://www.safe.com/transformers/raster-extents-coercer/)|Extract layer extent |N/A
[RasterExtractor](https://www.safe.com/transformers/raster-extractor/)|Missing|N/A
[RasterGCPExtractor](https://www.safe.com/transformers/rastergcp-extractor/)|Missing|N/A
[RasterGCPSetter](https://www.safe.com/transformers/rastergcp-setter/)|Missing|N/A
[RasterGeoreferencer](https://www.safe.com/transformers/raster-georeferencer/) |Missing|N/A
[RasterHillshader](https://www.safe.com/transformers/raster-hillshader/)|Hillshade |N/A
[RasterInterpretationCoercer](https://www.safe.com/transformers/raster-interpretation-coercer/) |GDAL Translate|N/A
[RasterMosaicker](https://www.safe.com/transformers/raster-mosaicker/)|GDAL Merge|N/A
[RasterNumericCreator](https://www.safe.com/transformers/raster-numeric-creator/)|Create Constant Raster Layer|N/A
[RasterObjectDetectionModelTrainer](https://www.safe.com/transformers/raster-object-detection-model-trainer/)|Missing|N/A
[RasterObjectDetector](https://www.safe.com/transformers/raster-object-detector/)|Missing|N/A
[RasterObjectDetectorSampleGenerator](https://www.safe.com/transformers/raster-object-detector-sample-generator/)|Missing|N/A
[RasterObjectDetectorSamplePreparer](https://www.safe.com/transformers/raster-object-detector-sample-preparer/)|Missing|N/A
[RasterPaletteAdder](https://www.safe.com/transformers/raster-palette-adder/)|Missing|N/A
[RasterPaletteExtractor](https://www.safe.com/transformers/raster-palette-extractor/)|Missing|N/A
[RasterPaletteGenerator](https://www.safe.com/transformers/raster-palette-generator/)|Missing|N/A
[RasterPaletteInterpretationCoercer](https://www.safe.com/transformers/raster-palette-interpretation-coercer/)|Missing|N/A|A small subset of functionality avialable via GDAL Translate |
[RasterPaletteNodataSetter](https://www.safe.com/transformers/raster-palette-nodata-setter/)|Missing|N/A
[RasterPaletteRemover](https://www.safe.com/transformers/raster-palette-remover/)|Missing|N/A
[RasterPaletteResolver](https://www.safe.com/transformers/raster-palette-resolver/)|Missing|N/A
[RasterPropertyExtractor](https://www.safe.com/transformers/raster-property-extractor/)|Raster layer statistics|raster_statistic
[RasterPyramider](https://www.safe.com/transformers/raster-pyramider/)|Build overviews (pyramids) |N/A
[RasterRegisterer](https://www.safe.com/transformers/raster-registerer/)|Missing|N/A
[RasterReplacer](https://www.safe.com/transformers/raster-replacer/)|N/A |Needs expression functions to create circular strings
[RasterResampler](https://www.safe.com/transformers/raster-resampler/)|GDAL Translate, GDAL Warp|N/A
[RasterRGBCreator](https://www.safe.com/transformers/rasterrgb-creator/)|GDAL Rasterize|N/A
[RasterRotationApplier](https://www.safe.com/transformers/raster-rotation-applier/)|Missing|N/A
[RasterSegmenter](https://www.safe.com/transformers/raster-segmenter/)|Missing|N/A
[RasterSelector](https://www.safe.com/transformers/raster-selector/)|Missing|N/A
[RasterSharpener](https://www.safe.com/transformers/raster-sharpener/)|Missing|N/A
[RasterSingularCellValueCalculator](https://www.safe.com/transformers/raster-singular-cell-value-calculator/)|Missing|N/A
[RasterSlopeCalculator](https://www.safe.com/transformers/raster-slope-calculator/)|Slope|N/A
[RasterStatisticsCalculator](https://www.safe.com/transformers/raster-statistics-calculator/)|Raster layer statistics|raster_statistic
[RasterSubsetter](https://www.safe.com/transformers/raster-subsetter/)|Clip raster by extent, Clip raster by mask layer|N/A
[RasterTiler](https://www.safe.com/transformers/raster-tiler/)|Retile, gdal2tiles|N/A
[RasterToPolygonCoercer](https://www.safe.com/transformers/raster-to-polygon-coercer/)|Polygonize|Missing
[RCaller](https://www.safe.com/transformers/r-caller/) |Via Processing "R" Provider plugin|N/A
[Recorder](https://www.safe.com/transformers/recorder/)|N/A |Needs expression functions to create circular strings
[ReframeReprojector](https://www.safe.com/transformers/reframe-reprojector/)|N/A |Needs expression functions to create circular strings|QGIS always uses the Proj library for transformation|
[RekognitionConnector](https://www.safe.com/transformers/rekognition-connector/)|Missing|N/A
[ReprojectAngleCalculator](https://www.safe.com/transformers/reproject-angle-calculator/)|Missing|N/A
[ReprojectLengthCalculator](https://www.safe.com/transformers/reproject-length-calculator/)|Missing|N/A
[Reprojector](https://www.safe.com/transformers/reprojector/)|Reproject layer |transform
[Rotator](https://www.safe.com/transformers/rotator/)|Rotate|rotate
[RubberSheeter](https://www.safe.com/transformers/rubber-sheeter/)|Missing|N/A
[S3Connector](https://www.safe.com/transformers/s3-connector/)|Inbuilt from GDAL|N/A
[SalesforceConnector](https://www.safe.com/transformers/salesforce-connector/) |Missing|N/A|3rd party plugin candidate |
[Sampler](https://www.safe.com/transformers/sampler/)|Random extract, Random extract by subsets offer partial functionality|N/A|Missing "not sampled" outputs, non-randomized sampling |
[Scaler](https://www.safe.com/transformers/scaler/)|Affine transform|Missing|A dedicated algorithm (like the 'Rotation' algorithm) is desirable|
[SchemaMapper](https://www.safe.com/transformers/schema-mapper/)|Missing|N/A
[SchemaScanner](https://www.safe.com/transformers/schema-scanner/)|N/A |N/A
[SecondOrderConformer](https://www.safe.com/transformers/second-order-conformer/)|Missing|N/A
[SectorGenerator](https://www.safe.com/transformers/sector-generator/)|Create wedge buffers |wedge_buffer 
[SharedItemAdder](https://www.safe.com/transformers/shared-item-adder/)|Missing|N/A|QGIS equivalent would be "import to style database"|
[SharedItemIDExtractor](https://www.safe.com/transformers/shared-itemid-extractor/)|Missing|N/A
[SharedItemIDSetter](https://www.safe.com/transformers/shared-itemid-setter/)|Missing|N/A
[SharedItemRetriever](https://www.safe.com/transformers/shared-item-retriever/)|Create Categorized Renderer from Style|N/A|Missing other renderers|
[SharePointOnlineConnector](https://www.safe.com/transformers/share-point-online-connector/)|Missing|Missing
[SherbendGeneralizer](https://www.safe.com/transformers/sherbend-generalizer/) |Missing|N/A
[ShortestPathFinder](https://www.safe.com/transformers/shortest-path-finder/)|Shortest Path Point to Point, etc|N/A
[SlackConnector](https://www.safe.com/transformers/slack-connector/)|Missing|N/A|3rd party plugin candidate |
[Snapper](https://www.safe.com/transformers/snapper/)|Snap geometries to layer|Missing
[Snipper](https://www.safe.com/transformers/snipper/)|Line substring is partial replacement (missing node/m value options)|line_substring
[SNSSender](https://www.safe.com/transformers/sns-sender/)|Missing|N/A|3rd party plugin candidate |
[SolidBuilder](https://www.safe.com/transformers/solid-builder/)|Missing|N/A
[SolidDissolver](https://www.safe.com/transformers/solid-dissolver/)|Missing|N/A
[Sorter](https://www.safe.com/transformers/sorter/)|Order by expression|N/A
[SpatialFilter](https://www.safe.com/transformers/spatial-filter/)|Extract by location|N/A
[SpatialRelator](https://www.safe.com/transformers/spatial-relator/)|Join attributes by location|N/A
[SpatialSorter](https://www.safe.com/transformers/spatial-sorter/)|Missing|N/A
[SpikeRemover](https://www.safe.com/transformers/spike-remover/)|v.clean, Simplify with Visvaligam algorithm|simplify_vw
[SQLCreator](https://www.safe.com/transformers/sql-creator/)|Postgres execute and load SQL, Execute SQL|N/A
[SQLExecutor](https://www.safe.com/transformers/sql-executor/)|Execute SQL, Postgres Execute SQL, Spatialite Execute SQL|N/A
[SQSConnector](https://www.safe.com/transformers/sqs-connector/)|Missing|N/A
[StatisticsCalculator](https://www.safe.com/transformers/statistics-calculator/)|Basic statistics for fields, Statistics by Categories|N/A
[StreamOrderCalculator](https://www.safe.com/transformers/stream-order-calculator/)|Missing|N/A|Existing algorithms require a DEM, not destination node|
[StreamPriorityCalculator](https://www.safe.com/transformers/stream-priority-calculator/)|Missing|N/A
[StringCaseChanger](https://www.safe.com/transformers/string-case-changer/)|N/A |Needs expression functions to create circular strings
[StringConcatenator](https://www.safe.com/transformers/string-concatenator/)|String concatentation|concat,
[StringFormatter](https://www.safe.com/transformers/string-formatter/)|N/A |Needs expression functions to create circular strings
[StringLengthCalculator](https://www.safe.com/transformers/string-length-calculator/)|N/A |Needs expression functions to create circular strings
[StringPadder](https://www.safe.com/transformers/string-padder/)|N/A |Needs expression functions to create circular strings
[StringPairReplacer](https://www.safe.com/transformers/string-pair-replacer/)|N/A |Needs expression functions to create circular strings
[StringReplacer](https://www.safe.com/transformers/string-replacer/)|N/A |Needs expression functions to create circular strings
[StringSearcher](https://www.safe.com/transformers/string-searcher/)|N/A |Needs expression functions to create circular strings
[SubstringExtractor](https://www.safe.com/transformers/substring-extractor/)|N/A |Needs expression functions to create circular strings
[SummaryReporter](https://www.safe.com/transformers/summary-reporter/)|Missing|N/A
[SurfaceBuilder](https://www.safe.com/transformers/surface-builder/)|Missing|N/A
[SurfaceDissolver](https://www.safe.com/transformers/surface-dissolver/)|Missing|N/A
[SurfaceDraper](https://www.safe.com/transformers/surface-draper/)|Drape|N/A
[SurfaceFootprintReplacer](https://www.safe.com/transformers/surface-footprint-replacer/)|Missing|N/A
[SurfaceModeller](https://www.safe.com/transformers/surface-modeller/)|TIN Interpolation|N/A
[SurfaceOnSurfaceOverlayer](https://www.safe.com/transformers/surface-on-surface-overlayer/)|Missing|N/A
[SurfaceSplitter](https://www.safe.com/transformers/surface-splitter/)|Missing|N/A
[SystemCaller](https://www.safe.com/transformers/system-caller/)|Missing|N/A
[TclCaller](https://www.safe.com/transformers/tcl-caller/)|Missing|N/A
[TCPIPReceiver](https://www.safe.com/transformers/tcpip-receiver/)|Missing|N/A
[TCPIPSender](https://www.safe.com/transformers/tcpip-sender/)|Missing|N/A
[TempPathnameCreator](https://www.safe.com/transformers/temp-pathname-creator/)|N/A |Needs expression functions to create circular strings
[Terminator](https://www.safe.com/transformers/terminator/) |Raise exception |N/A
[Tester](https://www.safe.com/transformers/tester/)|Feature filter|N/A
[TestFilter](https://www.safe.com/transformers/test-filter/)|Feature filter|N/A
[TextAdder](https://www.safe.com/transformers/text-adder/)|N/A |Needs expression functions to create circular strings
[TextDecoder](https://www.safe.com/transformers/text-decoder/)|N/A |Needs expression functions to create circular strings
[TextEncoder](https://www.safe.com/transformers/text-encoder/)|N/A |Needs expression functions to create circular strings
[TextLocationExtractor](https://www.safe.com/transformers/text-location-extractor/)|N/A |Needs expression functions to create circular strings
[TextPropertyExtractor](https://www.safe.com/transformers/text-property-extractor/)|N/A |Needs expression functions to create circular strings
[TextPropertySetter](https://www.safe.com/transformers/text-property-setter/)|N/A |Needs expression functions to create circular strings
[TextStroker](https://www.safe.com/transformers/text-stroker/)|N/A |Needs expression functions to create circular strings
[TextureCoordinateSetter](https://www.safe.com/transformers/texture-coordinate-setter/)|Missing|N/A|No support for textures in QGIS 3d yet|
[Tiler](https://www.safe.com/transformers/tiler/)|Missing|N/A
[TimeWindower](https://www.safe.com/transformers/time-windower/)|N/A |N/A
[TINGenerator](https://www.safe.com/transformers/tin-generator/)|TIN interpolation|N/A
[TopferIndexCalculator](https://www.safe.com/transformers/topfer-index-calculator/)|Missing|N/A
[TopologyBuilder](https://www.safe.com/transformers/topology-builder/)|Missing|N/A
[TraitMerger](https://www.safe.com/transformers/trait-merger/)|Missing|N/A
[TransporterReceiver](https://www.safe.com/transformers/transporter-receiver/) |N/A |Needs expression functions to create circular strings
[TransporterSender](https://www.safe.com/transformers/transporter-sender/)|N/A |Needs expression functions to create circular strings
[TrelloConnector](https://www.safe.com/transformers/trello-connector/)|Missing|N/A
[Triangulator](https://www.safe.com/transformers/triangulator/)|Tesselate |N/A
[TrimbleConnectConnector](https://www.safe.com/transformers/trimble-connect-connector/)|Missing|N/A
[Tweeter](https://www.safe.com/transformers/tweeter/)|Missing|N/A|3rd party plugin candidate |
[TweetSearcher](https://www.safe.com/transformers/tweet-searcher/)|Missing|N/A|3rd party plugin candidate |
[TweetStreamer](https://www.safe.com/transformers/tweet-streamer/)|Missing|N/A|3rd party plugin candidate |
[TwitterStatusFetcher](https://www.safe.com/transformers/twitter-status-fetcher/)|Missing|N/A|3rd party plugin candidate |
[UniqueIdentifierGenerator](https://www.safe.com/transformers/unique-identifier-generator/)|Possible with Refactor field and expression|replace (replace(uuid(),'{',''), '}','') |replace (replace(uuid(),'{',''), '}','')|
[VariableRetriever](https://www.safe.com/transformers/variable-retriever/)|N/A |Needs expression functions to create circular strings
[VariableSetter](https://www.safe.com/transformers/variable-setter/)|Missing|N/A
[VectorOnRasterOverlayer](https://www.safe.com/transformers/vector-on-raster-overlayer/)|Rasterize (overwrite with ...)|N/A
[VertexCounter](https://www.safe.com/transformers/vertex-counter/)|N/A |Needs expression functions to create circular strings
[VertexCreator](https://www.safe.com/transformers/vertex-creator/)|N/A |Needs expression functions to create circular strings
[VertexNormalRemover](https://www.safe.com/transformers/vertex-normal-remover/)|N/A |Needs expression functions to create circular strings
[VertexRemover](https://www.safe.com/transformers/vertex-remover/)|N/A |Needs expression functions to create circular strings
[VolumeCalculator](https://www.safe.com/transformers/volume-calculator/)|N/A |Needs expression functions to create circular strings
[VoronoiCellGenerator](https://www.safe.com/transformers/voronoi-cell-generator/)|Missing|N/A
[VoronoiDiagrammer](https://www.safe.com/transformers/voronoi-diagrammer/)|Voronoi polygons|N/A
[WebMapTiler](https://www.safe.com/transformers/web-map-tiler/)|Generate XYZ tiles|N/A
[WebSocketReceiver](https://www.safe.com/transformers/web-socket-receiver/)|Missing|N/A
[WebSocketSender](https://www.safe.com/transformers/web-socket-sender/)|Missing|N/A
[WhiteStarLeaseBuilder](https://www.safe.com/transformers/white-star-lease-builder/) |N/A |N/A
[WorkspaceRunner](https://www.safe.com/transformers/workspace-runner/)|N/A |Needs expression functions to create circular strings
[XMLAppender](https://www.safe.com/transformers/xml-appender/)|Missing|N/A
[XMLFeatureMapper](https://www.safe.com/transformers/xml-feature-mapper/) |Missing|N/A
[XMLFlattener](https://www.safe.com/transformers/xml-flattener/)|Missing|N/A
[XMLFormatter](https://www.safe.com/transformers/xml-formatter/)|Missing|N/A
[XMLFragmenter](https://www.safe.com/transformers/xml-fragmenter/)|Missing|N/A
[XMLNamespaceDeclarer](https://www.safe.com/transformers/xml-namespace-declarer/)|Missing|N/A
[XMLSampleGenerator](https://www.safe.com/transformers/xml-sample-generator/)|Missing|N/A
[XMLTemplater](https://www.safe.com/transformers/xml-templater/)|Missing|N/A
[XMLUpdater](https://www.safe.com/transformers/xml-updater/)|Missing|N/A
[XMLValidator](https://www.safe.com/transformers/xml-validator/)|Missing|N/A
[XMLXQueryExploder](https://www.safe.com/transformers/xmlx-query-exploder/)|Missing|N/A
[XMLXQueryExtractor](https://www.safe.com/transformers/xmlx-query-extractor/)|Missing|N/A
[XMLXQueryUpdater](https://www.safe.com/transformers/xmlx-query-updater/) |Missing|N/A
[XSLTProcessor](https://www.safe.com/transformers/xslt-processor/)|Missing|N/A
[YAMLtoJSONConverter](https://www.safe.com/transformers/yam-ltojson-converter/)|Missing|N/A