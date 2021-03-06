# Mapping of FME transformers to Processing algorithms or QGIS expressions

N/A means "not applicable" in this context

FME Transformer|QGIS Processing Alg|QGIS Expression|Notes
---|---|---|---
[2DArcReplacer](https://www.safe.com/transformers/2d-arc-replacer/)|N/A|Needs expression functions to create circular strings|
[2DBoxReplacer](https://www.safe.com/transformers/2d-box-replacer/)|N/A|Needs expression function to create rectangles|
[2DEllipseReplacer](https://www.safe.com/transformers/2d-ellipse-replacer/)|N/A|Missing|
[2DForcer](https://www.safe.com/transformers/2d-forcer/)|Drop Z Value|Missing|
[2DGridAccumulator](https://www.safe.com/transformers/2d-grid-accumulator/)|Missing|N/A|
[2DGridCreator](https://www.safe.com/transformers/2d-grid-creator/)|Create grid|N/A|
[3DAffiner](https://www.safe.com/transformers/3d-affiner/)|Missing|Missing|
[3DArcReplacer](https://www.safe.com/transformers/3d-arc-replacer/)|Missing|Missing|
[3DForcer](https://www.safe.com/transformers/3d-forcer/)|Set Z Value|Missing|
[3DInterpolator](https://www.safe.com/transformers/3d-interpolator/)|Missing|N/A|Also desirable for m values
[3DRotator](https://www.safe.com/transformers/3d-rotator/)|Missing|Missing|
[Affiner](https://www.safe.com/transformers/affiner/)|Affine transform|Missing|
[AffineWarper](https://www.safe.com/transformers/affine-warper/)|Missing|N/A|Would use gdal to perform warp via gcps -- could expose more than just affine transformation. Possibly aided by Lutra's upcoming work improving the QGIS georeferencer.
[AggregateFilter](https://www.safe.com/transformers/aggregate-filter/)|Missing|is_multipart (3.14)|
[Aggregator](https://www.safe.com/transformers/aggregator/)|Aggregate, Collect geometries|collect|
[AnchoredSnapper](https://www.safe.com/transformers/anchored-snapper/)|Snap geometries to layer|Missing|Performance issues
[AngleConverter](https://www.safe.com/transformers/angle-converter/)|N/A|radians/degrees|
[AngularityCalculator](https://www.safe.com/transformers/angularity-calculator/)|N/A|Missing|
[AppearanceExtractor](https://www.safe.com/transformers/appearance-extractor/)|N/A|N/A|Doesn't apply in QGIS
[AppearanceMerger](https://www.safe.com/transformers/appearance-merger/)|N/A|N/A|Doesn't apply in QGIS
[AppearanceRemover](https://www.safe.com/transformers/appearance-remover/)|N/A|N/A|Doesn't apply in QGIS
[AppearanceSetter](https://www.safe.com/transformers/appearance-setter/)|N/A|N/A|Doesn't apply in QGIS
[AppearanceStyler](https://www.safe.com/transformers/appearance-styler/)|N/A|N/A|Doesn't apply in QGIS
[ArcEstimator](https://www.safe.com/transformers/arc-estimator/)|Missing|Missing|Port from PostGIS? Partial work at https://github.com/nyalldawson/QGIS/tree/convert_to_curves
[ArcPropertyExtractor](https://www.safe.com/transformers/arc-property-extractor/)|N/A|Missing|
[ArcPropertySetter](https://www.safe.com/transformers/arc-property-setter/)|N/A|Missing|
[ArcSDEGridSnapper](https://www.safe.com/transformers/arc-sdegrid-snapper/)|N/A|N/A|Doesn't apply in QGIS - no support for SDE
[ArcSDEQuerier](https://www.safe.com/transformers/arc-sdequerier/)|N/A|N/A|Doesn't apply in QGIS - no support for SDE
[ArcStroker](https://www.safe.com/transformers/arc-stroker/)|Segmentize by ...|Missing|
[AreaAmalgamator](https://www.safe.com/transformers/area-amalgamator/)|Missing|Missing|
[AreaBuilder](https://www.safe.com/transformers/area-builder/)|Polygonize|Missing|
[AreaCalculator](https://www.safe.com/transformers/area-calculator/)|Add geometry attributes|$area|
[AreaGapAndOverlapCleaner](https://www.safe.com/transformers/area-gap-and-overlap-cleaner/)|Snap geometries to layer|N/A|
[AreaOnAreaOverlayer](https://www.safe.com/transformers/area-on-area-overlayer/)|Union|N/A|
[AttributeCompressor](https://www.safe.com/transformers/attribute-compressor/)|Missing|Missing|
[AttributeCopier](https://www.safe.com/transformers/attribute-copier/)|Field calculator, Refactor fields|N/A|
[AttributeCreator](https://www.safe.com/transformers/attribute-creator/)|Add field to attributes table|N/A|
[AttributeDecompressor](https://www.safe.com/transformers/attribute-decompressor/)|Missing|Missing|
[AttributeDereferencer](https://www.safe.com/transformers/attribute-dereferencer/)|N/A|attribute()|
[AttributeEncoder](https://www.safe.com/transformers/attribute-encoder/)|N/A|Missing|
[AttributeExploder](https://www.safe.com/transformers/attribute-exploder/)|Missing|N/A|
[AttributeExposer](https://www.safe.com/transformers/attribute-exposer/)|N/A|N/A|Doesn't apply in QGIS
[AttributeFileReader](https://www.safe.com/transformers/attribute-file-reader/)|Missing|Missing|
[AttributeFileWriter](https://www.safe.com/transformers/attribute-file-writer/)|Extract binary field|N/A|
[AttributeFilter](https://www.safe.com/transformers/attribute-filter/)|Extract by attribute, Feature filter|N/A|
[AttributeKeeper](https://www.safe.com/transformers/attribute-keeper/)|Missing|N/A|Not currently possible, but highly desirable for flexible models
[AttributeManager](https://www.safe.com/transformers/attribute-manager/)|Refactor fields|N/A|
[AttributePivoter](https://www.safe.com/transformers/attribute-pivoter/)|Statistics by categories|N/A|
[AttributeRangeFilter](https://www.safe.com/transformers/attribute-range-filter/)|Missing|N/A|
[AttributeRangeMapper](https://www.safe.com/transformers/attribute-range-mapper/)|Missing|N/A|
[AttributeRemover](https://www.safe.com/transformers/attribute-remover/)|Delete fields|N/A|
[AttributeRenamer](https://www.safe.com/transformers/attribute-renamer/)|Rename field|N/A|
[AttributeReprojector](https://www.safe.com/transformers/attribute-reprojector/)|N/A|transform|
[AttributeRounder](https://www.safe.com/transformers/attribute-rounder/)|N/A|round|
[AttributeSplitter](https://www.safe.com/transformers/attribute-splitter/)|Split features by character|string_to_array|
[AttributeTrimmer](https://www.safe.com/transformers/attribute-trimmer/)|N/A|trim|
[AttributeValidator](https://www.safe.com/transformers/attribute-validator/)|Missing|N/A|
[AttributeValueMapper](https://www.safe.com/transformers/attribute-value-mapper/)|Missing|'map' functions|
[AutodeskA360Connector](https://www.safe.com/transformers/autodesk-a360-connector/)|Missing|N/A|3rd party plugin candidate
[BaseConverter](https://www.safe.com/transformers/base-converter/)|N/A|Missing|
[BinaryDecoder](https://www.safe.com/transformers/binary-decoder/)|N/A|Missing|
[BinaryEncoder](https://www.safe.com/transformers/binary-encoder/)|N/A|Missing|
[BMGReprojector](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_Transformers/Transformers/bmgreprojector.htm)|N/A|N/A|Reprojection always uses the proj library
[BoundingBoxAccumulator](https://www.safe.com/transformers/bounding-box-accumulator/)|Extract layer extent|N/A|
[BoundingBoxReplacer](https://www.safe.com/transformers/bounding-box-replacer/)|Bounding boxes|bounds|
[BoundsExtractor](https://www.safe.com/transformers/bounds-extractor/)|N/A|x_min, x_max, y_min, y_max (z_min, z_max, m_min, m_max added in 3.14)|
[BoxConnector](https://www.safe.com/transformers/box-connector/)|Missing|N/A|3rd party plugin candidate
[Bufferer](https://www.safe.com/transformers/bufferer/)|Buffer|buffer|
[BulkAttributeRemover](https://www.safe.com/transformers/bulk-attribute-remover/)|Missing|N/A|
[BulkAttributeRenamer](https://www.safe.com/transformers/bulk-attribute-renamer/)|Missing|N/A|
[CenterLineReplacer](https://www.safe.com/transformers/center-line-replacer/)|Missing|Missing|No reliable algorithm publicly available, non trivial!
[CenterPointExtractor](https://www.safe.com/transformers/center-point-extractor/)|centroid, point on surface, pole of inaccessibility|centroid, point_on_surface, pole_of_inaccessibility|
[CenterPointReplacer](https://www.safe.com/transformers/center-point-replacer/)|centroid, point on surface, pole of inaccessibility|centroid, point_on_surface, pole_of_inaccessibility|
[ChangeDetector](https://www.safe.com/transformers/change-detector/)|Detect dataset changes|N/A|
[CharacterCodeExtractor](https://www.safe.com/transformers/character-code-extractor/)|N/A|ascii (QGIS 3.14)|
[CharacterCodeReplacer](https://www.safe.com/transformers/character-code-replacer/)|N/A|char|
[ChartGenerator](https://www.safe.com/transformers/chart-generator/)|Bar plot, box plot, etc|N/A|Better served by the 3rd party "DataPlotly" plugin
[Chopper](https://www.safe.com/transformers/chopper/)|Subdivide, Explode Lines|segments_to_lines, Missing subdivide function|
[CircularityCalculator](https://www.safe.com/transformers/circularity-calculator/)|Missing|Missing|
[Clipper](https://www.safe.com/transformers/clipper/)|clip|intersection|
[Cloner](https://www.safe.com/transformers/cloner/)|Array of translated features|N/A|
[ClosedCurveFilter](https://www.safe.com/transformers/closed-curve-filter/)|N/A|is_closed|
[CommonLocalReprojector](https://www.safe.com/transformers/common-local-reprojector/)|Missing|Missing|would need a way to transform using a custom WKT or proj string
[CommonSegmentFinder](https://www.safe.com/transformers/common-segment-finder/)|Missing|Missing|GEOS library exposes this functionality, but not exposed through QGIS
[ContourGenerator](https://www.safe.com/transformers/contour-generator/)|GDAL Contours|N/A|
[ConvexityFilter](https://www.safe.com/transformers/convexity-filter/)|N/A|Needs "is_convex"/"is_concave" expression functions|
[CoordinateConcatenator](https://www.safe.com/transformers/coordinate-concatenator/)|Missing|Possible via array iteration functions, but not easily|
[CoordinateExtractor](https://www.safe.com/transformers/coordinate-extractor/)|Add x/y fields to layer|x/y/etc|
[CoordinateReplacer](http://docs.safe.com/fme/2018.0/html/FME_Desktop_Documentation/FME_Transformers/Transformers/coordinatereplacer.htm)|N/A|Missing|
[CoordinateRounder](https://www.safe.com/transformers/coordinate-rounder/)|Snap points to grid|Missing|
[CoordinateSwapper](https://www.safe.com/transformers/coordinate-swapper/)|Swap x and y coordinates|flip_coordinates|
[CoordinateSystemDescriptionConverter](https://www.safe.com/transformers/coordinate-system-description-converter/)|Missing|Missing|
[CoordinateSystemExtractor](https://www.safe.com/transformers/coordinate-system-extractor/)|Missing|Missing|
[CoordinateSystemRemover](https://www.safe.com/transformers/coordinate-system-remover/)|Missing|Missing|
[CoordinateSystemSetter](https://www.safe.com/transformers/coordinate-system-setter/)|Assign projection|N/A|
[Counter](https://www.safe.com/transformers/counter/)|Add autoincremental field|N/A|
[CRCCalculator](https://www.safe.com/transformers/crccalculator/)|N/A|Missing|
[Creator](https://www.safe.com/transformers/creator/)|Geometry by expression|N/A|
[CSGBuilder](https://www.safe.com/transformers/csg-builder/)|Missing|Missing|
[CSGEvaluator](https://www.safe.com/transformers/csg-evaluator/)|Missing|Missing|
[CsmapAttributeReprojector](https://www.safe.com/transformers/csmap-attribute-reprojector/)|N/A|N/A|QGIS always uses the proj library
[CsmapReprojector](https://www.safe.com/transformers/csmap-reprojector/)|N/A|N/A|QGIS always uses the proj libray
[Curvefitter](https://www.safe.com/transformers/curvefitter/)|Missing|Missing|Port from PostGIS? Partial work at https://github.com/nyalldawson/QGIS/tree/convert_to_curves
[DatabaseDeleter](https://www.safe.com/transformers/database-deleter/)|Missing|N/A|
[DatabaseJoiner](https://www.safe.com/transformers/database-joiner/)|Join attributes by \*|N/A|
[DatabaseUpdater](https://www.safe.com/transformers/database-updater/)|Missing|N/A|
[DateTimeCalculator](https://www.safe.com/transformers/date-time-calculator/)|N/A|Misc functions|
[DateTimeConverter](https://www.safe.com/transformers/date-time-converter/)|Missing|Missing|
[DateTimeStamper](https://www.safe.com/transformers/date-time-stamper/)|N/A|epoch(), now()|
[Deaggregator](https://www.safe.com/transformers/deaggregator/)|Multipart to singleparts|Missing|
[Decelerator](https://www.safe.com/transformers/decelerator/)|N/A|N/A|
[DecimalDegreesCalculator](https://www.safe.com/transformers/decimal-degrees-calculator/)|N/A|Needs from_dms function|
[DEMDistanceCalculator](https://www.safe.com/transformers/demdistance-calculator/)|Missing|N/A|
[DEMGenerator](https://www.safe.com/transformers/demgenerator/)|TIN interpolation|N/A|
[Densifier](https://www.safe.com/transformers/densifier/)|Densify by count/Densify by distance|Missing|
[DensityCalculator](https://www.safe.com/transformers/density-calculator/)|Missing|N/A|
[DGNStyler](https://www.safe.com/transformers/dgn-styler/)|Missing|N/A|3rd party plugin candidate
[DimensionExtractor](https://www.safe.com/transformers/dimension-extractor/)|N/A|Missing|
[DirectTweeter](https://www.safe.com/transformers/direct-tweeter/)|Missing|N/A|3rd party plugin candidate
[Displacer](https://www.safe.com/transformers/displacer/)|Points diplacement is a partial match|N/A|
[Dissolver](https://www.safe.com/transformers/dissolver/)|Dissolve|Union|
[DMSCalculator](https://www.safe.com/transformers/dmscalculator/)|N/A|to_dm, to_dms|
[DonutBridgeBuilder](https://www.safe.com/transformers/donut-bridge-builder/)|Missing|N/A|
[DonutBuilder](https://www.safe.com/transformers/donut-builder/)|Difference|difference|
[DonutHoleExtractor](https://www.safe.com/transformers/donut-hole-extractor/)|N/A|exterior_ring, interior_ring_n|
[DropboxConnector](https://www.safe.com/transformers/dropbox-connector/)|Missing|N/A|3rd party plugin candidate
[DuplicateFilter](https://www.safe.com/transformers/duplicate-filter/)|Delete duplicate geometries, delete duplicates by attribute|N/A|
[DWGStyler](https://www.safe.com/transformers/dwg-styler/)|Missing|N/A|DXF export is not exposed to Processing
[ElevationExtractor](https://www.safe.com/transformers/elevation-extractor/)|Extract z values|z|
[EllipsePropertyExtractor](https://www.safe.com/transformers/ellipse-property-extractor/)|N/A|Missing|
[EllipsePropertySetter](https://www.safe.com/transformers/ellipse-property-setter/)|N/A|Missing|
[Emailer](https://www.safe.com/transformers/emailer/)|Missing|N/A|
[EnvironmentVariableFetcher](https://www.safe.com/transformers/environment-variable-fetcher/)|N/A|env|
[EsriReprojector](https://www.safe.com/transformers/esri-reprojector/)|N/A|N/A|QGIS always uses the PROJ library for transforms
[ExcelStyler](https://www.safe.com/transformers/excel-styler/)|Missing|N/A|
[ExpressionEvaluator](https://www.safe.com/transformers/expression-evaluator/)|Many|Many|
[Extruder](https://www.safe.com/transformers/extruder/)|v.extrude|N/A|
[FaceReplacer](https://www.safe.com/transformers/face-replacer/)|Missing|N/A|
[FeatureColorSetter](https://www.safe.com/transformers/feature-color-setter/)|N/A|N/A|Possibly value in algorithms which create layer styles in place
[FeatureHolder](https://www.safe.com/transformers/feature-holder/)|N/A|N/A|
[FeatureJoiner](https://www.safe.com/transformers/feature-joiner/)|Join attributes by field value, Join attributes by location|N/A|
[FeatureMerger](https://www.safe.com/transformers/feature-merger/)|Join attributes by field value|N/A|
[FeatureReader](https://www.safe.com/transformers/feature-reader/)|N/A|N/A|Vector file handling
[FeatureTypeExtractor](https://www.safe.com/transformers/feature-type-extractor/)|N/A|Missing|
[FeatureTypeFilter](https://www.safe.com/transformers/feature-type-filter/)|Filter by geometry type|N/A|
[FeatureWriter](https://www.safe.com/transformers/feature-writer/)|N/A|N/A|Vector file writer
[FilenamePartExtractor](https://www.safe.com/transformers/filename-part-extractor/)|N/A|base_file_name, file_name, file_path|
[FMEFunctionCaller](https://www.safe.com/transformers/fmefunction-caller/)|N/A|N/A|
[FMEServerJobSubmitter](https://www.safe.com/transformers/fmeserver-job-submitter/)|N/A|N/A|
[FMEServerJobWaiter](https://www.safe.com/transformers/fmeserver-job-waiter/)|N/A|N/A|
[FMEServerLogFileRetriever](https://www.safe.com/transformers/fmeserver-log-file-retriever/)|N/A|N/A|
[FMEServerNotifier](https://www.safe.com/transformers/fmeserver-notifier/)|N/A|N/A|
[FMEServerResource](https://www.safe.com/transformers/fmeserver-resource/)|N/A|N/A|
[FTPCaller](https://www.safe.com/transformers/ftpcaller/)|Missing|N/A|
[GCMMessenger](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_Transformers/Transformers/gcmmessenger.htm)|Missing|N/A|3rd party plugin candidate
[Generalizer](https://www.safe.com/transformers/generalizer/)|Simplify, smooth|simplify, smooth|
[Geocoder](https://www.safe.com/transformers/geocoder/)|Missing|Missing|3rd party plugin candidate, exposing geocoding via different services
[GeographicBufferer](https://www.safe.com/transformers/geographic-bufferer/)|Missing|Missing|
[GeometryCoercer](https://www.safe.com/transformers/geometry-coercer/)|Convert geometry type|N/A|
[GeometryColorSetter](https://www.safe.com/transformers/geometry-color-setter/)|N/A|N/A|
[GeometryExtractor](https://www.safe.com/transformers/geometry-extractor/)|N/A|geom_to_wkt|
[GeometryFilter](https://www.safe.com/transformers/geometry-filter/)|Filter by geometry type|N/A|
[GeometryInstantiator](https://www.safe.com/transformers/geometry-instantiator/)|Affine transform, Array of translated features|N/A|
[GeometryPartExtractor](https://www.safe.com/transformers/geometry-part-extractor/)|Missing|geometry_n|
[GeometryPropertyExtractor](https://www.safe.com/transformers/geometry-property-extractor/)|N/A|Many|
[GeometryPropertyRemover](https://www.safe.com/transformers/geometry-property-remover/)|Missing|Missing|
[GeometryPropertyRenamer](https://www.safe.com/transformers/geometry-property-renamer/)|Missing|Missing|
[GeometryPropertySetter](https://www.safe.com/transformers/geometry-property-setter/)|Missing|Missing|
[GeometryRefiner](https://www.safe.com/transformers/geometry-refiner/)|N/A|N/A|
[GeometryRemover](https://www.safe.com/transformers/geometry-remover/)|Drop geometries|N/A|
[GeometryReplacer](https://www.safe.com/transformers/geometry-replacer/)|Geometry by expression|geom_from_wkt, etc|
[GeometryValidator](https://www.safe.com/transformers/geometry-validator/)|Validate geometries|is_valid|
[GeoRSSFeatureComposer](https://www.safe.com/transformers/geo-rss-feature-composer/)|N/A|Missing|
[GeoRSSFeatureReader](https://www.safe.com/transformers/geo-rss-feature-reader/)|Inbuilt vector handling|Missing|
[GMLFeatureComposer](https://www.safe.com/transformers/gmlfeature-composer/)|N/A|geom_from_gml|
[GOIDGenerator](https://www.safe.com/transformers/goid-generator/)|Missing|Missing|
[GoogleDriveConnector](https://www.safe.com/transformers/google-drive-connector/)|Missing|N/A|3rd party plugin candidate
[GridInquestIIReprojector](https://www.safe.com/transformers/grid-in-quest-ii-reprojector/)|N/A|N/A|QGIS always uses the PROJ library for reprojection
[GridInquestReprojector](https://www.safe.com/transformers/grid-in-quest-ii-reprojector/)|N/A|N/A|QGIS always uses the PROJ library for reprojection
[GtransAttributeReprojector](https://www.safe.com/transformers/gtrans-attribute-reprojector/)|N/A|N/A|QGIS always uses the PROJ library for reprojection
[GtransReprojector](https://www.safe.com/transformers/gtrans-reprojector/)|N/A|N/A|QGIS always uses the PROJ library for reprojection
[HDFSConnector](https://www.safe.com/transformers/hdfsconnector/)|N/A|N/A|Handled by the GDAL library
[HoleCounter](https://www.safe.com/transformers/hole-counter/)|N/A|num_interior_rings|
[HTMLExtractor](https://www.safe.com/transformers/html-extractor/)|Missing|N/A|3rd party plugin candidate
[HTMLLayouter](https://www.safe.com/transformers/html-layouter/)|Missing|N/A|
[HTMLReportGenerator](https://www.safe.com/transformers/html-report-generator/)|Missing|N/A|
[HTMLToXHTMLConverter](https://www.safe.com/transformers/html-to-xhtml-converter/)|Missing|N/A|
[HTTPCaller](https://www.safe.com/transformers/httpcaller/)|Missing|N/A|
[HullAccumulator](https://www.safe.com/transformers/hull-accumulator/)|Convex hull, Concave hull|convex_hull|
[HullReplacer](https://www.safe.com/transformers/hull-replacer/)|Convex hull, Concave hull|convex_hull|
[IFCPropertySetDefinition](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_Transformers/Transformers/ifcpropertysetdefinitioncreator.htm)|Missing|N/A|
[IFCQuantitySetDefinition](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_Transformers/Transformers/ifcquantitysetdefinitioncreator.htm)|Missing|N/A|
[ImageFetcher](https://www.safe.com/transformers/image-fetcher/)|Missing|N/A|
[ImageRasterizer](https://www.safe.com/transformers/image-rasterizer/)|Rasterize (GDAL), Convert map to raster, XYZ Tiles|N/A|
[InlineQuerier](https://www.safe.com/transformers/inline-querier/)|Spatialite execute SQL, Execute SQL|N/A|
[Inspector](https://www.safe.com/transformers/inspector/)|N/A|N/A|
[Intersector](https://www.safe.com/transformers/intersector/)|Intersection|intersection|
[JavaScriptCaller](https://docs.safe.com/fme/2018.0/html/FME_Desktop_Documentation/FME_Transformers/Transformers/javascriptcaller.htm)|Via plugin|N/A|Possible via the 3rd party "Processing JS" Plugin
[JMSReceiver](https://www.safe.com/transformers/jms-receiver/)|Missing|N/A|3rd party plugin candidate
[JMSSender](https://www.safe.com/transformers/jms-sender/)|Missing|N/A|3rd party plugin candidate
[JSONExtractor](https://www.safe.com/transformers/json-extractor/)|Explode hstore field|map and array functions|
[JSONFlattener](https://www.safe.com/transformers/json-flattener/)|Explode hstore field|map and array functions|
[JSONFormatter](https://www.safe.com/transformers/json-formatter/)|N/A|Missing|
[JSONFragmenter](https://www.safe.com/transformers/json-fragmenter/)|N/A|map and array functions|
[JSONTemplater](https://www.safe.com/transformers/json-templater/)|N/A|map and array functions|
[JSONUpdater](https://www.safe.com/transformers/json-updater/)|N/A|map and array functions|
[JSONValidator](https://www.safe.com/transformers/json-validator/)|Missing|N/A|
[KinesisReceiver](https://www.safe.com/transformers/kinesis-receiver/)|Missing|N/A|3rd party plugin candidate
[KinesisSender](https://www.safe.com/transformers/kinesis-sender/)|Missing|N/A|3rd party plugin candidate
[KMLPropertySetter](https://www.safe.com/transformers/kml-property-setter/)|Missing|N/A|
[KMLRegionSetter](https://www.safe.com/transformers/kml-region-setter/)|Missing|N/A|
[KMLStyler](https://www.safe.com/transformers/kml-styler/)|Missing|N/A|
[KMLTimeSetter](https://www.safe.com/transformers/kml-time-setter/)|Missing|N/A|
[KMLTourBuilder](https://www.safe.com/transformers/kml-tour-builder/)|Missing|N/A|3rd party plugin candidate
[KMLViewSetter](https://www.safe.com/transformers/kml-view-setter/)|Missing|N/A|3rd party plugin candidate
[Labeller](https://www.safe.com/transformers/labeller/)|N/A|N/A|
[LabelPointReplacer](https://www.safe.com/transformers/label-point-replacer/)|N/A|N/A|
[LatLongToMGRSConverter](https://www.safe.com/transformers/lat-long-to-mgrs-converter/)|Missing|Missing|
[LeftRightSpatialCalculator](https://www.safe.com/transformers/left-right-spatial-calculator/)|Missing|Missing|Raw API already exists, but not exposed to QGIS Processing or Expressions
[LengthCalculator](https://www.safe.com/transformers/length-calculator/)|Add geometry attributes|$length|
[LengthToPointCalculator](https://www.safe.com/transformers/length-to-point-calculator/)|Missing|line_locate_point|
[LicenseChecker](https://www.safe.com/transformers/license-checker/)|N/A|N/A|Definitely not required!
[LineBuilder](https://www.safe.com/transformers/line-builder/)|Points to paths|N/A|
[LineCloser](https://www.safe.com/transformers/line-closer/)|Missing|Missing|
[LineCombiner](https://www.safe.com/transformers/line-combiner/)|Merge lines|line_merge|
[LineExtender](https://www.safe.com/transformers/line-extender/)|Extend lines|extend|
[LineOnAreaOverlayer](https://www.safe.com/transformers/line-on-area-overlayer/)|Union|N/A|
[LineOnLineOverlayer](https://www.safe.com/transformers/line-on-line-overlayer/)|Union|N/A|
[ListBasedFeatureMerger](https://www.safe.com/transformers/list-based-feature-merger/)|N/A|array and aggregate functions|
[ListBuilder](https://www.safe.com/transformers/list-builder/)|N/A|array and aggregate functions|
[ListConcatenator](https://www.safe.com/transformers/list-concatenator/)|N/A|array_to_string|
[ListCopier](https://www.safe.com/transformers/list-copier/)|N/A|attributes|
[ListDuplicateRemover](https://www.safe.com/transformers/list-duplicate-remover/)|N/A|array_distinct|
[ListElementCounter](https://www.safe.com/transformers/list-element-counter/)|N/A|array_length|
[ListExploder](https://www.safe.com/transformers/list-exploder/)|Missing|N/A|
[ListExpressionPopulator](https://www.safe.com/transformers/list-expression-populator/)|N/A|array_foreach|
[ListHistogrammer](https://www.safe.com/transformers/list-histogrammer/)|N/A|Missing|
[ListIndexer](https://www.safe.com/transformers/list-indexer/)|N/A|array_get|
[ListPopulator](https://www.safe.com/transformers/list-populator/)|N/A|array|
[ListRangeExtractor](https://www.safe.com/transformers/list-range-extractor/)|N/A|Achievable via array_sort, but direct min/max functions desirable|
[ListRenamer](https://www.safe.com/transformers/list-renamer/)|N/A|N/A|Doesn't apply in QGIS
[ListSearcher](https://www.safe.com/transformers/list-searcher/)|N/A|array_find|
[ListSorter](https://www.safe.com/transformers/list-sorter/)|N/A|array_sort|
[ListSummer](https://www.safe.com/transformers/list-summer/)|N/A|Missing|
[LocalCoordinateSystemSetter](https://www.safe.com/transformers/local-coordinate-system-setter/)|Assign projection|N/A|
[Logger](https://www.safe.com/transformers/logger/)|Missing|N/A|
[LogMessageStreamer](https://www.safe.com/transformers/log-message-streamer/)|Save log to file|N/A|
[MapboxStyler](https://www.safe.com/transformers/mapbox-styler/)|Missing|N/A|
[MapInfoStyler](https://www.safe.com/transformers/map-info-styler/)|Missing|N/A|
[MapnikRasterizer](https://www.safe.com/transformers/mapnik-rasterizer/)|N/A|N/A|
[MapTextLabeller](https://www.safe.com/transformers/map-text-labeller/)|N/A|N/A|
[MapTextStyler](https://www.safe.com/transformers/map-text-styler/)|N/A|N/A|
[Matcher](https://www.safe.com/transformers/matcher/)|Delete duplicate geometries, Delete duplicates by attribute|N/A|
[MeasureExtractor](https://www.safe.com/transformers/measure-extractor/)|Line substring, Extract specific vertices, Interpolate point on line, Extract M values|line_substring, line_interpolate_point, m|
[MeasureGenerator](https://www.safe.com/transformers/measure-generator/)|Set M value, Set M value from raster|line_locate_point|
[MeasureRemover](https://www.safe.com/transformers/measure-remover/)|Drop M/Z values, Filter vertices by M value|N/A|
[MeasureSetter](https://www.safe.com/transformers/measure-setter/)|Set M value, Set M value from raster|Missing|
[MeshMerger](https://www.safe.com/transformers/mesh-merger/)|Missing|N/A|
[MeshSimplifier](https://www.safe.com/transformers/mesh-simplifier/)|Missing|N/A|
[MGRSToLatLongConverter](https://www.safe.com/transformers/mgrsto-lat-long-converter/)|Missing|Missing|
[MinimumAreaForcer](https://www.safe.com/transformers/minimum-area-forcer/)|Missing|Missing|
[MinimumSpanningCircle](https://www.safe.com/transformers/minimum-spanning-circle-replacer/)|Minimum enclosing circles|minimal_circle|
[ModuloCounter](https://www.safe.com/transformers/modulo-counter/)|Missing|Missing|
[MRF2DCleaner](https://www.safe.com/transformers/mrf2d-cleaner/)|Missing, partially covered by "Fix geometries"|N/A|3rd party plugin candidate
[MRF2DConflator](https://www.safe.com/transformers/mrf2d-conflator/)|Missing|N/A|
[MRF2DDangleRemover](https://www.safe.com/transformers/mrf2d-dangle-remover/)|v.clean using rmdangle works, but a native tool is desirable|N/A|
[MRF2DDuplicateRemover](https://www.safe.com/transformers/mrf2d-duplicate-remover/)|Delete duplicate geometries|N/A|
[MRF2DExtender](https://www.safe.com/transformers/mrf2d-extender/)|Snap geometries to layer using Move End Points Only mode|N/A|
[MRF2DGeneralizer](https://www.safe.com/transformers/mrf2d-generalizer/)|Simplify is a partial match|simplify|
[MRF2DIntersector](https://www.safe.com/transformers/mrf2d-intersector/)|Intersection, Line intersections|intersection|
[MRF2DJoiner](https://www.safe.com/transformers/mrf2d-joiner/)|Merge lines|line_merge|
[MRF2DShortGeometryRemover](https://www.safe.com/transformers/mrf2d-short-geometry-remover/)|Missing|N/A|
[MRF3DCleaner](https://www.safe.com/transformers/mrf3d-cleaner/)|Missing|N/A|3rd party plugin candidate
[MSWordStyler](https://www.safe.com/transformers/ms-word-styler/)|Missing|Missing|3rd party plugin candidate
[MultipleGeometryFilter](https://www.safe.com/transformers/multiple-geometry-filter/)|Multiparts to singleparts|geometry_n|
[MultipleGeometrySetter](https://www.safe.com/transformers/multiple-geometry-setter/)|Collect geometries, Promote to Multipart|collect_geometries|
[NeighborFinder](https://www.safe.com/transformers/neighbor-finder/)|Join attributes by nearest|N/A|
[NeighborhoodAggregator](https://www.safe.com/transformers/neighborhood-aggregator/)|DBSCAN clustering, K-means clustering, v.cluster|N/A|
[NeighborPairFinder](https://www.safe.com/transformers/neighbor-pair-finder/)|Missing|N/A|
[NetworkCostCalculator](https://www.safe.com/transformers/network-cost-calculator/)|Shortest Path algorithms|N/A|
[NetworkFlowOrientor](https://www.safe.com/transformers/network-flow-orientor/)|Missing|N/A|
[NetworkTopologyCalculator](https://www.safe.com/transformers/network-topology-calculator/)|Missing|N/A|
[NullAttributeMapper](https://www.safe.com/transformers/null-attribute-mapper/)|Missing|N/A|Possible using field calculator with QGIS expressions
[NumericRasterizer](https://www.safe.com/transformers/numeric-rasterizer/)|GDAL Rasterize|N/A|
[OffsetCurveGenerator](https://www.safe.com/transformers/offset-curve-generator/)|Offset lines|offset_curve|
[Offsetter](https://www.safe.com/transformers/offsetter/)|Translate|translate|
[OneDriveConnector](https://www.safe.com/transformers/one-drive-connector/)|Missing|N/A|3rd party plugin candidate
[OrientationExtractor](https://www.safe.com/transformers/orientation-extractor/)|N/A|Missing|
[Orientor](https://www.safe.com/transformers/orientor/)|Force right hand rule|force_rhr|
[ParameterFetcher](https://www.safe.com/transformers/parameter-fetcher/)|Field calculator with input parameters|N/A|
[PartCounter](https://www.safe.com/transformers/part-counter/)|N/A|num_geometries|
[PathBuilder](https://www.safe.com/transformers/path-builder/)|Missing|N/A|
[PathSplitter](https://www.safe.com/transformers/path-splitter/)|Explode lines|segments_to_lines|
[PDFPageFormatter](https://www.safe.com/transformers/pdf-page-formatter/)|Missing|N/A|Inbuilt algorithms for exporting layouts are desirable
[PDFStyler](https://www.safe.com/transformers/pdf-styler/)|Missing|N/A|Requires inbuilt algorithm for exporting layout to GeoPDF with attributes
[PinterestConnector](https://docs.safe.com/fme/2018.1/html/FME_Desktop_Documentation/FME_Transformers/Transformers/pinterestconnector.htm)|Missing|N/A|3rd party plugin candidate
[PlanarityFilter](https://www.safe.com/transformers/planarity-filter/)|N/A|Missing|Requires 'is_planar' expression function
[Player](https://www.safe.com/transformers/player/)|N/A|N/A|
[PointCloudCoercer](https://www.safe.com/transformers/point-cloud-coercer/)|Via pdal or lastools plugins|N/A|
[PointCloudCombiner](https://www.safe.com/transformers/point-cloud-combiner/)|Via pdal or lastools plugins|N/A|
[PointCloudComponentAdder](https://www.safe.com/transformers/point-cloud-component-adder/)|Via pdal or lastools plugins|N/A|
[PointCloudComponentCopier](https://www.safe.com/transformers/point-cloud-component-copier/)|Via pdal or lastools plugins|N/A|
[PointCloudComponentKeeper](https://www.safe.com/transformers/point-cloud-component-keeper/)|Via pdal or lastools plugins|N/A|
[PointCloudComponentRemover](https://www.safe.com/transformers/point-cloud-component-remover/)|Via pdal or lastools plugins|N/A|
[PointCloudComponentRenamer](https://www.safe.com/transformers/point-cloud-component-renamer/)|Via pdal or lastools plugins|N/A|
[PointCloudComponentTypeCoercer](https://www.safe.com/transformers/point-cloud-component-type-coercer/)|Via pdal or lastools plugins|N/A|
[PointCloudConsumer](https://www.safe.com/transformers/point-cloud-consumer/)|Via pdal or lastools plugins|N/A|
[PointCloudCreator](https://www.safe.com/transformers/point-cloud-creator/)|Via pdal or lastools plugins|N/A|
[PointCloudExpressionEvaluator](https://www.safe.com/transformers/point-cloud-expression-evaluator/)|Via pdal or lastools plugins|N/A|
[PointCloudExtractor](https://www.safe.com/transformers/point-cloud-extractor/)|Via pdal or lastools plugins|N/A|
[PointCloudFilter](https://www.safe.com/transformers/point-cloud-filter/)|Via pdal or lastools plugins|N/A|
[PointCloudMerger](https://www.safe.com/transformers/point-cloud-merger/)|Via pdal or lastools plugins|N/A|
[PointCloudOnRasterComponentSetter](https://www.safe.com/transformers/point-cloud-on-raster-component-setter/)|Via pdal or lastools plugins|N/A|
[PointCloudPropertyExtractor](https://www.safe.com/transformers/point-cloud-property-extractor/)|Via pdal or lastools plugins|N/A|
[PointCloudReplacer](https://www.safe.com/transformers/point-cloud-replacer/)|Via pdal or lastools plugins|N/A|
[PointCloudSimplifier](https://www.safe.com/transformers/point-cloud-simplifier/)|Via pdal or lastools plugins|N/A|
[PointCloudSorter](https://www.safe.com/transformers/point-cloud-sorter/)|Via pdal or lastools plugins|N/A|
[PointCloudSplitter](https://www.safe.com/transformers/point-cloud-splitter/)|Via pdal or lastools plugins|N/A|
[PointCloudStatisticsCalculator](https://www.safe.com/transformers/point-cloud-statistics-calculator/)|Via pdal or lastools plugins|N/A|
[PointCloudSurfaceBuilder](https://www.safe.com/transformers/point-cloud-surface-builder/)|Via pdal or lastools plugins|N/A|
[PointCloudThinner](https://www.safe.com/transformers/point-cloud-thinner/)|Via pdal or lastools plugins|N/A|
[PointCloudTransformationApplier](https://www.safe.com/transformers/point-cloud-transformation-applier/)|Via pdal or lastools plugins|N/A|
[PointOnAreaOverlayer](https://www.safe.com/transformers/point-on-area-overlayer/)|Join attributes by location|N/A|
[PointOnLineOverlayer](https://www.safe.com/transformers/point-on-line-overlayer/)|Join attributes by location|N/A|
[PointOnPointOverlayer](https://www.safe.com/transformers/point-on-point-overlayer/)|Join attributes by location|N/A|
[PointOnRasterValueExtractor](https://www.safe.com/transformers/point-on-raster-value-extractor/)|Sample raster values|raster_value|
[PointPropertyExtractor](https://www.safe.com/transformers/point-property-extractor/)|N/A|Mixed expression functions, e.g. radians, degrees|Rotation is treated just like normal attributes in QGIS
[PointPropertySetter](https://www.safe.com/transformers/point-property-setter/)|Field calculator|Mixed expression functions, e.g. radians, degrees|Rotation is treated just like normal attributes in QGIS
[PowerPointStyler](https://www.safe.com/transformers/power-point-styler/)|Missing|N/A|3rd party plugin candidate
[PythonCaller](https://www.safe.com/transformers/python-caller/)|||Possible to create algorithms and expressions via Python. Desirable would be to allow Python scripts to be embedded inside a model.
[PythonCreator](https://www.safe.com/transformers/python-creator/)|||Possible to create algorithms and expressions via Python. Desirable would be to allow Python scripts to be embedded inside a model.
[RandomNumberGenerator](https://www.safe.com/transformers/random-number-generator/)|N/A|rand, randf|
[RasterAspectCalculator](https://www.safe.com/transformers/raster-aspect-calculator/)|Aspect|N/A|
[RasterBandAdder](https://www.safe.com/transformers/raster-band-adder/)|Missing|N/A|Possible via Create Constant Raster Layer and GDAL Merge algorithms, but a direct algorithm is desirable
[RasterBandCombiner](https://www.safe.com/transformers/raster-band-combiner/)|GDAL Merge|N/A|
[RasterBandInterpretationCoercer](https://www.safe.com/transformers/raster-band-interpretation-coercer/)|GDAL Translate|N/A|
[RasterBandKeeper](https://www.safe.com/transformers/raster-band-keeper/)|Rearrange Bands|N/A|
[RasterBandMinMaxExtractor](https://www.safe.com/transformers/raster-band-min-max-extractor/)|Raster layer statistics|raster_statistic|
[RasterBandNameSetter](https://www.safe.com/transformers/raster-band-name-setter/)|Missing|N/A|
[RasterBandNodataRemover](https://www.safe.com/transformers/raster-band-nodata-remover/)|Fill NoData Cells|N/A|
[RasterBandNodataSetter](https://www.safe.com/transformers/raster-band-nodata-setter/)|Missing|N/A|
[RasterBandOrderer](https://www.safe.com/transformers/raster-band-orderer/)|Rearrange Bands|N/A|
[RasterBandPropertyExtractor](https://www.safe.com/transformers/raster-band-property-extractor/)|Missing|N/A|
[RasterBandRemover](https://www.safe.com/transformers/raster-band-remover/)|Rearrange Bands|N/A|
[RasterBandSeparator](https://www.safe.com/transformers/raster-band-separator/)|Rearrange Bands|N/A|
[RasterCellCoercer](https://www.safe.com/transformers/raster-cell-coercer/)|Raster pixels to points, Raster pixels to polygons|N/A|
[RasterCellOriginSetter](https://www.safe.com/transformers/raster-cell-origin-setter/)|Missing|N/A|
[RasterCellValueCalculator](https://www.safe.com/transformers/raster-cell-value-calculator/)|Raster calculator|N/A|
[RasterCellValueReplacer](https://www.safe.com/transformers/raster-cell-value-replacer/)|Reclassify by layer, Reclassify by table|N/A|
[RasterCellValueRounder](https://www.safe.com/transformers/raster-cell-value-rounder/)|Missing|Round raster (QGIS 3.14)|
[RasterCheckpointer](https://www.safe.com/transformers/raster-checkpointer/)|N/A|N/A|
[RasterConsumer](https://www.safe.com/transformers/raster-consumer/)|N/A|N/A|
[RasterDEMGenerator](https://www.safe.com/transformers/raster-dem-generator/)|TIN Interpolation|N/A|
[RasterExpressionEvaluator](https://www.safe.com/transformers/raster-expression-evaluator/)|Raster calculator|N/A|
[RasterExtentsCoercer](https://www.safe.com/transformers/raster-extents-coercer/)|Extract layer extent|layer_property using 'extent' property|
[RasterExtractor](https://www.safe.com/transformers/raster-extractor/)|Missing|N/A|
[RasterGCPExtractor](https://www.safe.com/transformers/raster-gcpextractor/)|Missing|N/A|
[RasterGCPSetter](https://www.safe.com/transformers/raster-gcpsetter/)|Missing|N/A|
[RasterGeoreferencer](https://www.safe.com/transformers/raster-georeferencer/)|Missing|N/A|
[RasterHillshader](https://www.safe.com/transformers/raster-hillshader/)|Hillshade|N/A|
[RasterInterpretationCoercer](https://www.safe.com/transformers/raster-interpretation-coercer/)|GDAL Translate|N/A|
[RasterMosaicker](https://www.safe.com/transformers/raster-mosaicker/)|GDAL Merge|N/A|
[RasterNumericCreator](https://www.safe.com/transformers/raster-numeric-creator/)|Create Constant Raster Layer|N/A|
[RasterPaletteAdder](https://www.safe.com/transformers/raster-palette-adder/)|Missing|N/A|
[RasterPaletteExtractor](https://www.safe.com/transformers/raster-palette-extractor/)|Missing|N/A|
[RasterPaletteGenerator](https://www.safe.com/transformers/raster-palette-generator/)|Missing|N/A|
[RasterPaletteInterpretationCoercer](https://www.safe.com/transformers/raster-palette-interpretation-coercer/)|Missing|N/A|A small subset of functionality avialable via GDAL Translate
[RasterPaletteNodataSetter](https://www.safe.com/transformers/raster-palette-nodata-setter/)|Missing|N/A|
[RasterPaletteRemover](https://www.safe.com/transformers/raster-palette-remover/)|Missing|N/A|
[RasterPaletteResolver](https://www.safe.com/transformers/raster-palette-resolver/)|Missing|N/A|
[RasterPropertyExtractor](https://www.safe.com/transformers/raster-property-extractor/)|Raster layer statistics|layer_property|
[RasterPyramider](https://www.safe.com/transformers/raster-pyramider/)|Build overviews (pyramids)|N/A|
[RasterReplacer](https://www.safe.com/transformers/raster-replacer/)|N/A|N/A|
[RasterResampler](https://www.safe.com/transformers/raster-resampler/)|GDAL Translate, GDAL Warp|N/A|
[RasterRGBCreator](https://www.safe.com/transformers/raster-rgb-creator/)|GDAL Rasterize|N/A|
[RasterRotationApplier](https://www.safe.com/transformers/raster-rotation-applier/)|Missing|N/A|
[RasterSelector](https://www.safe.com/transformers/raster-selector/)|Missing|N/A|
[RasterSingularCellValue](https://www.safe.com/transformers/raster-singular-cell-value-calculator/)|Raster calculator|N/A|
[RasterSlopeCalculator](https://www.safe.com/transformers/raster-slope-calculator/)|Slope|N/A|
[RasterSubsetter](https://www.safe.com/transformers/raster-subsetter/)|Clip raster by extent, Clip raster by mask layer|N/A|
[RasterTiler](https://www.safe.com/transformers/raster-tiler/)|Retile, gdal2tiles|N/A|
[RasterToPolygonCoercer](https://www.safe.com/transformers/raster-to-polygon-coercer/)|Polygonize|N/A|
[RCaller](https://www.safe.com/transformers/rcaller/)|Via Processing "R" Provider plugin|N/A|
[Recorder](https://www.safe.com/transformers/recorder/)|N/A|N/A|
[ReframeReprojector](https://www.safe.com/transformers/reframe-reprojector/)|N/A|N/A|QGIS always uses the Proj library for transformation
[ReprojectAngleCalculator](https://www.safe.com/transformers/reproject-angle-calculator/)|Missing|Missing|
[ReprojectLengthCalculator](https://www.safe.com/transformers/reproject-length-calculator/)|Missing|Missing|
[Reprojector](https://www.safe.com/transformers/reprojector/)|Reproject layer|transform|
[Rotator](https://www.safe.com/transformers/rotator/)|Rotate|rotate|
[RubberSheeter](https://www.safe.com/transformers/rubber-sheeter/)|Missing|N/A|
S3Connector|Inbuilt from GDAL|N/A|
[SalesforceConnector](https://www.safe.com/transformers/salesforce-connector/)|Missing|N/A|3rd party plugin candidate
[Sampler](https://www.safe.com/transformers/sampler/)|Random extract, Random extract by subsets offer partial functionality|N/A|Missing "not sampled" outputs, non-randomized sampling
[Scaler](https://www.safe.com/transformers/scaler/)|Affine transform|Missing|A dedicated algorithm (like the 'Rotation' algorithm) is desirable
[SchemaMapper](https://www.safe.com/transformers/schema-mapper/)|Missing|N/A|
[SecondOrderConformer](https://www.safe.com/transformers/second-order-conformer/)|Missing|Missing|
[SectorGenerator](https://www.safe.com/transformers/sector-generator/)|Create wedge buffers|wedge_buffer|
[SharedItemAdder](https://www.safe.com/transformers/shared-item-adder/)|Missing|N/A|QGIS equivalent would be "import to style database"
[SharedItemIDExtractor](https://www.safe.com/transformers/shared-item-id-extractor/)|Missing|N/A|
[SharedItemIDSetter](https://www.safe.com/transformers/shared-item-id-setter/)|Missing|N/A|
[SharedItemRetriever](https://www.safe.com/transformers/shared-item-retriever/)|Create Categorized Renderer from Style|N/A|Missing other renderers
[SherbendGeneralizer](https://www.safe.com/transformers/sherbend-generalizer/)|Missing|Missing|
[ShortestPathFinder](https://www.safe.com/transformers/shortest-path-finder/)|Shortest Path Point to Point, etc|N/A|
[SlackConnector](https://www.safe.com/transformers/slack-connector/)|Missing|N/A|3rd party plugin candidate
[Snapper](https://www.safe.com/transformers/snapper/)|Snap geometries to layer|N/A|
[Snipper](https://www.safe.com/transformers/snipper/)|Line substring is partial replacement (missing node/m value options)|line_substring|
[SNSSender](https://www.safe.com/transformers/sns-sender/)|Missing|N/A|3rd party plugin candidate
[SolidBuilder](https://www.safe.com/transformers/solid-builder/)|Missing|N/A|
[Sorter](https://www.safe.com/transformers/sorter/)|Order by expression|N/A|
[SpatialFilter](https://www.safe.com/transformers/spatial-filter/)|Extract by location|N/A|
[SpatialRelator](https://www.safe.com/transformers/spatial-relator/)|Join attributes by location|relate|
[SpikeRemover](https://www.safe.com/transformers/spike-remover/)|v.clean, Simplify with Visvaligam algorithm|simplify_vw|
[SQLCreator](https://www.safe.com/transformers/sql-creator/)|Postgres execute and load SQL, Execute SQL|N/A|
[SQLExecutor](https://www.safe.com/transformers/sql-executor/)|Execute SQL, Postgres Execute SQL, Spatialite Execute SQL|N/A|
[SQSDeleter](https://www.safe.com/transformers/sqs-deleter/)|Missing|N/A|3rd party plugin candidate
[SQSMessageCounter](https://www.safe.com/transformers/sqs-message-counter/)|Missing|N/A|3rd party plugin candidate
[SQSReceiver](https://www.safe.com/transformers/sqs-receiver/)|Missing|N/A|3rd party plugin candidate
[SQSSender](https://www.safe.com/transformers/sqs-sender/)|Missing|N/A|3rd party plugin candidate
[StatisticsCalculator](https://www.safe.com/transformers/statistics-calculator/)|Basic statistics for fields, Statistics by Categories|N/A|
[StreamOrderCalculator](https://www.safe.com/transformers/stream-order-calculator/)|Missing|N/A|Existing algorithms require a DEM, not destination node
[StreamPriorityCalculator](https://www.safe.com/transformers/stream-priority-calculator/)|Missing|N/A|
[StringCaseChanger](https://www.safe.com/transformers/string-case-changer/)|N/A|upper, lower, title|
[StringConcatenator](https://www.safe.com/transformers/string-concatenator/)|String concatentation|concat, \|\||
[StringFormatter](https://www.safe.com/transformers/string-formatter/)|N/A|format|
[StringLengthCalculator](https://www.safe.com/transformers/string-length-calculator/)|N/A|length|
[StringPadder](https://www.safe.com/transformers/string-padder/)|N/A|lpad, rpad|
[StringPairReplacer](https://www.safe.com/transformers/string-pair-replacer/)|N/A|missing|
[StringReplacer](https://www.safe.com/transformers/string-replacer/)|N/A|replace, regex_replace|
[StringSearcher](https://www.safe.com/transformers/string-searcher/)|N/A|regex_match, regex_substr|
[SubstringExtractor](https://www.safe.com/transformers/substring-extractor/)|N/A|substr, left, right|
[SummaryReporter](https://www.safe.com/transformers/summary-reporter/)|Missing|N/A|
[SurfaceBuilder](https://www.safe.com/transformers/surface-builder/)|Missing|Missing|
[SurfaceDissolver](https://www.safe.com/transformers/surface-dissolver/)|Missing|N/A|
[SurfaceDraper](https://www.safe.com/transformers/surface-draper/)|Drape|N/A|
[SurfaceFootprintReplacer](https://www.safe.com/transformers/surface-footprint-replacer/)|Missing|N/A|
[SurfaceModeller](https://www.safe.com/transformers/surface-modeller/)|TIN Interpolation|N/A|
[SurfaceOnSurfaceOverlayer](https://www.safe.com/transformers/surface-on-surface-overlayer/)|Missing|N/A|
[SurfaceSplitter](https://www.safe.com/transformers/surface-splitter/)|Missing|N/A|
[SystemCaller](https://www.safe.com/transformers/system-caller/)|Missing|N/A|
[TclCaller](https://www.safe.com/transformers/tcl-caller/)|Missing|N/A|
[TCPIPReceiver](https://www.safe.com/transformers/tcpip-receiver/)|Missing|N/A|
[TCPIPSender](https://www.safe.com/transformers/tcpip-sender/)|Missing|N/A|
[TempPathnameCreator](https://www.safe.com/transformers/temp-pathname-creator/)|N/A|Missing|
[Terminator](https://www.safe.com/transformers/terminator/)|Raise exception|N/A|
[Tester](https://www.safe.com/transformers/tester/)|Feature filter|N/A|
[TestFilter](https://www.safe.com/transformers/test-filter/)|Feature filter|N/A|
[TextAdder](https://www.safe.com/transformers/text-adder/)|N/A|N/A|
[TextDecoder](https://www.safe.com/transformers/text-decoder/)|N/A|Missing|
[TextEncoder](https://www.safe.com/transformers/text-encoder/)|N/A|Missing|
[TextLocationExtractor](https://www.safe.com/transformers/text-location-extractor/)|N/A|N/A|
[TextPropertyExtractor](https://www.safe.com/transformers/text-property-extractor/)|N/A|N/A|
[TextPropertySetter](https://www.safe.com/transformers/text-property-setter/)|N/A|N/A|
[TextStroker](https://www.safe.com/transformers/text-stroker/)|N/A|N/A|
[TextureCoordinateSetter](https://www.safe.com/transformers/texture-coordinate-setter/)|Missing|N/A|No support for textures in QGIS 3d yet
[Tiler](https://www.safe.com/transformers/tiler/)|Missing|N/A|
[TINGenerator](https://www.safe.com/transformers/tin-generator/)|TIN interpolation|N/A|
[TopologyBuilder](https://www.safe.com/transformers/topology-builder/)|Missing|N/A|
[TraitMerger](https://www.safe.com/transformers/trait-merger/)|Missing|N/A|
[TransporterReceiver](https://www.safe.com/transformers/transporter-receiver/)|N/A|N/A|
[TransporterSender](https://www.safe.com/transformers/transporter-sender/)|N/A|N/A|
[Triangulator](https://www.safe.com/transformers/triangulator/)|Tesselate|N/A|
[Tweeter](https://www.safe.com/transformers/tweeter/)|Missing|N/A|3rd party plugin candidate
[TweetSearcher](https://www.safe.com/transformers/tweet-searcher/)|Missing|N/A|3rd party plugin candidate
[TweetStreamer](https://www.safe.com/transformers/tweet-streamer/)|Missing|N/A|3rd party plugin candidate
[TwitterStatusFetcher](https://www.safe.com/transformers/twitter-status-fetcher/)|Missing|N/A|3rd party plugin candidate
[UUIDGenerator](https://www.safe.com/transformers/uuidgenerator/)|N/A|uuid|
[VariableRetriever](https://www.safe.com/transformers/variable-retriever/)|N/A|@...|
[VariableSetter](https://www.safe.com/transformers/variable-setter/)|Missing|N/A|
[VectorOnRasterOverlayer](https://www.safe.com/transformers/vector-on-raster-overlayer/)|Rasterize (overwrite with ...)|N/A|
[VertexCounter](https://www.safe.com/transformers/vertex-counter/)|N/A|num_points|
[VertexCreator](https://www.safe.com/transformers/vertex-creator/)|N/A|missing|
[VertexRemover](https://www.safe.com/transformers/vertex-remover/)|N/A|missing|
[VolumeCalculator](https://www.safe.com/transformers/volume-calculator/)|N/A|missing|
[VoronoiCellGenerator](https://www.safe.com/transformers/voronoi-cell-generator/)|Missing|N/A|
[VoronoiDiagrammer](https://www.safe.com/transformers/voronoi-diagrammer/)|Voronoi polygons|N/A|
[WebMapTiler](https://www.safe.com/transformers/web-map-tiler/)|Generate XYZ tiles|N/A|
[WebSocketReceiver](https://www.safe.com/transformers/web-socket-receiver/)|Missing|N/A|
[WebSocketSender](https://www.safe.com/transformers/web-socket-sender/)|Missing|N/A|
[WorkspaceRunner](https://www.safe.com/transformers/workspace-runner/)|N/A|N/A|
[XMLAppender](https://www.safe.com/transformers/xml-appender/)|Missing|N/A|
[XMLFeatureMapper](https://www.safe.com/transformers/xml-feature-mapper/)|Missing|N/A|
[XMLFlattener](https://www.safe.com/transformers/xml-flattener/)|Missing|N/A|
[XMLFormatter](https://www.safe.com/transformers/xml-formatter/)|Missing|N/A|
[XMLFragmenter](https://www.safe.com/transformers/xml-fragmenter/)|Missing|N/A|
[XMLNamespaceDeclarer](https://www.safe.com/transformers/xml-namespace-declarer/)|Missing|N/A|
[XMLSampleGenerator](https://www.safe.com/transformers/xml-sample-generator/)|Missing|N/A|
[XMLTemplater](https://www.safe.com/transformers/xml-templater/)|Missing|N/A|
[XMLUpdater](https://www.safe.com/transformers/xml-updater/)|Missing|N/A|
[XMLValidator](https://www.safe.com/transformers/xml-validator/)|Missing|N/A|
[XMLXQueryExploder](https://www.safe.com/transformers/xmlx-query-exploder/)|Missing|N/A|
[XMLXQueryExtractor](https://www.safe.com/transformers/xmlx-query-extractor/)|Missing|N/A|
[XMLXQueryUpdater](https://www.safe.com/transformers/xmlx-query-updater/)|Missing|N/A|
