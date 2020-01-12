# Mapping of FME transformers to Processing algorithms or QGIS expressions


FME Transformer|QGIS Processing Alg|QGIS Expression|Notes
---|---|---|---
2DArcReplacer|N/A| |Needs expression functions to create circular strings
2DBoxReplacer|N/A| |Needs expression function to create rectangle
2DEllipseReplacer| | |Needs expression function
2DForcer|Drop Z Value| |Needs expression function
2DGridAccumulator| | |
2DGridCreator|Create grid|N/A|
3DAffiner|||
3DArcReplacer|||
3DForcer|Set Z Value| |needs expression function
3DInterpolator| |N/A|needs an algorithm, also for m values
3DRotator|||
Affiner|Affine transform| |Needs expression function
AffineWarper|||
AggregateFilter| | |Needs algorithm + "is_multipart" function
Aggregator|Aggregate, Collect geometries|collect|
AnchoredSnapper|Snap geometries to layer| |Needs expression function, (performance issue with small tolerance)
AngleConverter|N/A|radians/degrees|
AngularityCalculator|N/A| |Needs expression function
AppearanceExtractor|N/A|N/A|Doesn't apply in QGIS
AppearanceMerger|N/A|N/A|Doesn't apply in QGIS
AppearanceRemover|N/A|N/A|Doesn't apply in QGIS
AppearanceSetter|N/A|N/A|Doesn't apply in QGIS
AppearanceStyler|N/A|N/A|Doesn't apply in QGIS
ArcEstimator| | |Port from PostGIS? Partial work at https://github.com/nyalldawson/QGIS/tree/convert_to_curves
ArcPropertyExtractor|N/A| |Needs expression function
ArcPropertySetter|||
ArcSDEGridSnapper|N/A|N/A|Doesn't apply in QGIS
ArcSDEQuerier|N/A|N/A|Doesn't apply in QGIS
ArcStroker|Segmentize by ...| |Needs expression function
AreaAmalgamator|||
AreaBuilder|Polygonize| |Needs expression function
AreaCalculator|N/A|$area|
AreaGapAndOverlap|||
AreaOnAreaOverlayer|||
AttributeCompressor|||
AttributeCopier|Field calculator, Refactor fields|N/A|
AttributeCreator|Add field to attributes table|N/A|
AttributeDecompressor|||
AttributeDereferencer|N/A|attribute()|
AttributeEncoder|N/A| |Needs expression function
AttributeExploder| | |
AttributeExposer|N/A|N/A|Doesn't apply in QGIS
AttributeFileReader|||Needs expression function, algorithm
AttributeFileWriter|Extract binary field||
AttributeFilter|Extract by attribute, Feature filter||
AttributeKeeper|||Not currently possible, but desirable for flexible models
AttributeManager|Refactor fields||
AttributePivoter|||possibly covered by "statistics by categories"
AttributeRangeFilter|||
AttributeRangeMapper|||
AttributeRemover|Delete fields||
AttributeRenamer|||only possible using refactor fields, but that approach is not flexible
AttributeReprojector||transform|
AttributeRounder||round|
AttributeSplitter||string_to_array|
AttributeTrimmer||trim|
AttributeValidator|||
AttributeValueMapper|||
AutodeskA360Connector|||
BaseConverter|||Needs expression function
BinaryDecoder|||Needs expression function
BinaryEncoder|||Needs expression function
BMGReprojector|||
BoundingBoxAccumulator|Extract layer extent||
BoundingBoxReplacer|Bounding boxes|bounds|
BoundsExtractor||x_min, x_max, y_min, y_max|Should add z/m min/max too
BoxConnector|||
Bufferer|Buffer|buffer|
BulkAttributeRemover|||
BulkAttributeRenamer|||
CenterLineReplacer|||needs algorithm, non trivial!
CenterPointExtractor|centroid, point on surface, pole of inaccessibility|centroid, point_on_surface, pole_of_inaccessibility|
CenterPointReplacer|||
ChangeDetector|||needs algorithm
CharacterCodeExtractor|||needs expression function
CharacterCodeReplacer||char|
ChartGenerator|||
Chopper|||
CircularityCalculator|||Needs expression function
Clipper|clip|intersection|
Cloner|||
ClosedCurveFilter||is_closed|
CommonLocalReprojector|||
CommonSegmentFinder|||
ContourGenerator|GDAL Contours||
ConvexityFilter|||Needs "is_convex"/"is_concave" expression functions
CoordinateConcatenator|||
CoordinateExtractor||x/y/etc|
CoordinateReplacer|||
CoordinateRounder|Snap points to grid||
CoordinateSwapper|Swap x and y coordinates|flip_coordinates|
CoordinateSystemDescription|||
CoordinateSystemExtractor|||
CoordinateSystemRemover|||
CoordinateSystemSetter|||
Counter|Add autoincremental field||
CRCCalculator|||Needs expression function
Creator|||
CSGBuilder|||
CSGEvaluator|||
CsmapAttributeReprojector|||
CsmapReprojector|||
Curvefitter ⊛|||
DatabaseDeleter|||
DatabaseJoiner|||
DatabaseUpdater|||
DateTimeCalculator||Misc functions|
DateTimeConverter|||
DateTimeStamper||epoch(), now()|
Deaggregator|Multipart to singleparts||
Decelerator|||
DecimalDegreesCalculator|||Needs from_dms function
DEMDistanceCalculator|||
DEMGenerator|||
Densifier|Densify by count/Densify by distance||Add expression functions?
DensityCalculator|||
DGNStyler|||
DimensionExtractor|||
DirectTweeter|||
Displacer|||
Dissolver|Dissolve|Union|
DMSCalculator||to_dm, to_dms|
DonutBridgeBuilder|||
DonutBuilder|||
DonutHoleExtractor||exterior_ring, interior_ring_n|Needs algorithm
DropboxConnector|||
DuplicateFilter|Delete duplicate geometries, delete duplicates by attribute||
DWGStyler|||
ElevationExtractor|Extract z values|z|
EllipsePropertyExtractor|||
EllipsePropertySetter|||
Emailer|||
EnvironmentVariableFetcher||env|
EsriReprojector|||
ExcelStyler|||
ExpressionEvaluator||Many|
Extruder|||
FaceReplacer|||
FeatureColorSetter|||
FeatureHolder|||
FeatureJoiner|Join attributes by field value, Join attributes by location||
FeatureMerger|||
FeatureReader|||Vector file handling
FeatureTypeExtractor|||
FeatureTypeFilter|||
FeatureWriter|||Vector file writer
FilenamePartExtractor|||Needs expression functions dealing with file path operations, i.e. expose QFileInfo methods
FMEFunctionCaller|||
FMEServerJobSubmitter|||
FMEServerJobWaiter|||
FMEServerLogFileRetriever|||
FMEServerNotifier|||
FMEServerResource|||
FTPCaller|||Needs algorithm
GCMMessenger|||
Generalizer|Simplify, smooth|simplify, smooth|
Geocoder|||
GeographicBufferer|||
GeometryCoercer|Convert geometry type||
GeometryColorSetter|||
GeometryExtractor||geom_to_wkt|
GeometryFilter|||Needs algorithm
GeometryInstantiator|||
GeometryPartExtractor|||
GeometryPropertyExtractor|||
GeometryPropertyRemover|||
GeometryPropertyRenamer|||
GeometryPropertySetter|||
GeometryRefiner|||
GeometryRemover|Drop geometries||
GeometryReplacer|Geometry by expression|geom_from_wkt, etc|
GeometryValidator|Validate geometries||Needs "is_valid" expression function
GeoRSSFeatureComposer|||
GeoRSSFeatureReader|||
GMLFeatureComposer|||
GOIDGenerator|||
GoogleDriveConnector|||
GridInquestIIReprojector|||
GridInquestReprojector|||
GtransAttributeReprojector|||
GtransReprojector|||
HDFSConnector|||
HoleCounter||num_interior_rings|
HTMLExtractor|||
HTMLLayouter|||
HTMLReportGenerator|||
HTMLToXHTMLConverter|||
HTTPCaller|||Needs algorithm
HullAccumulator|Convex hull, concave hull|convex_hull|
HullReplacer|||
IFCPropertySetDefinition|||
IFCQuantitySetDefinition|||
ImageFetcher|||
ImageRasterizer|Rasterize (GDAL), Convert map to raster||
InlineQuerier|||
Inspector|||
Intersector|||
JavaScriptCaller|||
JMSReceiver|||
JMSSender|||
JSONExtractor|||
JSONFlattener|||
JSONFormatter|||
JSONFragmenter|||
JSONTemplater|||
JSONUpdater|||
JSONValidator|||
KinesisReceiver|||
KinesisSender|||
KMLPropertySetter|||
KMLRegionSetter|||
KMLStyler|||
KMLTimeSetter|||
KMLTourBuilder|||
KMLViewSetter|||
Labeller|||
LabelPointReplacer|||
LatLongToMGRSConverter|||
LeftRightSpatialCalculator|||
LengthCalculator|||
LengthToPointCalculator|||
LicenseChecker|||
LineBuilder|||
LineCloser|||
LineCombiner|||
LineExtender|||
LineOnAreaOverlayer|||
LineOnLineOverlayer|||
ListBasedFeatureMerger|||
ListBuilder|||
ListConcatenator|||
ListCopier|||
ListDuplicateRemover|||
ListElementCounter|||
ListExploder|||
ListExpressionPopulator|||
ListHistogrammer|||
ListIndexer|||
ListPopulator|||
ListRangeExtractor|||
ListRenamer|||
ListSearcher|||
ListSorter|||
ListSummer|||
LocalCoordinateSystemSetter|||
Logger|||
LogMessageStreamer|||
MapboxStyler|||
MapInfoStyler|||
MapnikRasterizer|||
MapTextLabeller ⊛|||
MapTextStyler|||
Matcher|||
MeasureExtractor|||
MeasureGenerator|||
MeasureRemover|||
MeasureSetter|||
MeshMerger|||
MeshSimplifier|||
MGRSToLatLongConverter|||
MinimumAreaForcer|||
MinimumSpanningCircle|||
Replacer|||
ModuloCounter|||
MRF2DCleaner ⊛|||
MRF2DConflator ⊛|||
MRF2DDangleRemover ⊛|||
MRF2DDuplicateRemover ⊛|||
MRF2DExtender ⊛|||
MRF2DGeneralizer ⊛|||
MRF2DIntersector ⊛|||
MRF2DJoiner ⊛|||
MRF2DShortGeometry ⊛|||
MRF3DCleaner ⊛|||
MSWordStyler|||
MultipleGeometryFilter|||
MultipleGeometrySetter|||
NeighborFinder|||
NeighborhoodAggregator|||
NeighborPairFinder|||
NetworkCostCalculator|||
NetworkFlowOrientor|||
NetworkTopologyCalculator|||
NullAttributeMapper|||
NumericRasterizer|||
OffsetCurveGenerator|||
Offsetter|||
OneDriveConnector|||
OrientationExtractor|||
Orientor|||
ParameterFetcher|||
PartCounter|||
PathBuilder|||
PathSplitter|||
PDFPageFormatter|||
PDFStyler|||
PinterestConnector|||
PlanarityFilter|||
Player|||
PointCloudCoercer|||
PointCloudCombiner|||
PointCloudComponent|||
PointCloudComponent|||
PointCloudComponent|||
PointCloudComponent|||
PointCloudComponent|||
PointCloudComponent|||
PointCloudConsumer|||
PointCloudCreator|||
PointCloudExpression|||
PointCloudExtractor|||
PointCloudFilter|||
PointCloudMerger|||
PointCloudOnRaster|||
ComponentSetter|||
PointCloudPropertyExtractor|||
PointCloudReplacer|||
PointCloudSimplifier|||
PointCloudSorter|||
PointCloudSplitter|||
PointCloudStatistics|||
PointCloudSurfaceBuilder|||
PointCloudThinner|||
PointCloudTransformation|||
PointOnAreaOverlayer|||
PointOnLineOverlayer|||
PointOnPointOverlayer|||
PointOnRasterValueExtractor|||
PointPropertyExtractor|||
PointPropertySetter|||
PowerPointStyler|||
PythonCaller|||
PythonCreator|||
RandomNumberGenerator|||
RasterAspectCalculator|||
RasterBandAdder|||
RasterBandCombiner|||
RasterBandInterpretation|||
RasterBandKeeper|||
RasterBandMinMaxExtractor|||
RasterBandNameSetter|||
RasterBandNodataRemover|||
RasterBandNodataSetter|||
RasterBandOrderer|||
RasterBandPropertyExtractor|||
RasterBandRemover|||
RasterBandSeparator|||
RasterCellCoercer|||
RasterCellOriginSetter|||
RasterCellValueCalculator|||
RasterCellValueReplacer|||
RasterCellValueRounder|||
RasterCheckpointer|||
RasterConsumer|||
RasterDEMGenerator|||
RasterExpressionEvaluator|||
RasterExtentsCoercer|||
RasterExtractor|||
RasterGCPExtractor|||
RasterGCPSetter|||
RasterGeoreferencer|||
RasterHillshader|||
RasterInterpretationCoercer|||
RasterMosaicker|||
RasterNumericCreator|||
RasterPaletteAdder|||
RasterPaletteExtractor|||
RasterPaletteGenerator|||
RasterPaletteInterpretation|||
RasterPaletteNodataSetter|||
RasterPaletteRemover|||
RasterPaletteResolver|||
RasterPropertyExtractor|||
RasterPyramider|||
RasterReplacer|||
RasterResampler|||
RasterRGBCreator|||
RasterRotationApplier|||
RasterSelector|||
RasterSingularCellValue|||
RasterSlopeCalculator|||
RasterSubsetter|||
RasterTiler|||
RasterToPolygonCoercer|||
RCaller|||
Recorder|||
ReframeReprojector|||
ReprojectAngleCalculator|||
ReprojectLengthCalculator|||
Reprojector|||
Rotator|||
RubberSheeter|||
S3Connector|||
S3Deleter|||
S3Downloader|||
S3ObjectLister|||
S3Uploader|||
SalesforceConnector|||
Sampler|||
Scaler|||
SchemaMapper|||
SecondOrderConformer|||
SectorGenerator|||
SharedItemAdder|||
SharedItemIDExtractor|||
SharedItemIDSetter|||
SharedItemRetriever|||
SherbendGeneralizer|||
ShortestPathFinder|||
SlackConnector|||
Snapper|||
Snipper|||
SNSSender|||
SolidBuilder|||
Sorter|||
SpatialFilter|||
SpatialRelator|||
SpikeRemover|||
SQLCreator|||
SQLExecutor|||
SQSDeleter|||
SQSMessageCounter|||
SQSReceiver|||
SQSSender|||
StatisticsCalculator|||
StreamOrderCalculator|||
StreamPriorityCalculator|||
StringCaseChanger|||
StringConcatenator|||
StringFormatter|||
StringLengthCalculator|||
StringPadder|||
StringPairReplacer|||
StringReplacer|||
StringSearcher|||
SubstringExtractor|||
SummaryReporter|||
SurfaceBuilder|||
SurfaceDissolver|||
SurfaceDraper|||
SurfaceFootprintReplacer|||
SurfaceModeller|||
SurfaceOnSurfaceOverlayer|||
SurfaceSplitter|||
SystemCaller|||
TclCaller|||
TCPIPReceiver|||
TCPIPSender|||
TempPathnameCreator|||
Terminator|||
Tester|||
TestFilter|||
TextAdder|||
TextDecoder|||
TextEncoder|||
TextLocationExtractor|||
TextPropertyExtractor|||
TextPropertySetter|||
TextStroker|||
TextureCoordinateSetter|||
Tiler|||
TINGenerator|||
TopologyBuilder|||
TraitMerger|||
TransporterReceiver|||
TransporterSender|||
Triangulator|||
Tweeter|||
TweetSearcher|||
TweetStreamer|||
TwitterStatusFetcher|||
UUIDGenerator|||
VariableRetriever|||
VariableSetter|||
VectorOnRasterOverlayer|||
VertexCounter|||
VertexCreator|||
VertexRemover|||
VolumeCalculator|||
VoronoiCellGenerator|||
VoronoiDiagrammer|||
WebMapTiler|||
WebSocketReceiver|||
WebSocketSender|||
WhiteStarLeaseBuilder|||
WorkspaceRunner|||
XMLAppender|||
XMLFeatureMapper|||
XMLFlattener|||
XMLFormatter|||
XMLFragmenter|||
XMLNamespaceDeclarer|||
XMLSampleGenerator|||
XMLTemplater|||
XMLUpdater|||
XMLValidator|||
XMLXQueryExploder|||
XMLXQueryExtractor|||
XMLXQueryUpdater|||
XSLTProcessor