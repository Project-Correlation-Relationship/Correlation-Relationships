# Property Extents

__Datasets:__ MasterMap Topographic Area and HM Land Registry INSPIRE Polygon
<br> __Linked IDs:__ TOID and INSPIRE-ID
<br> __Correlation Operator:__ Spatial Overlap

 <a href="http://www.google.com/">
    <button>Download</button>
</a>

## Description
Land Registry freehold polygons represent land ownership, whereas Ordnance Survey MasterMap (OSMM) topographic areas generally represent the physical features of the landscape.

Easily identifying the physical features owned by a particular party is of value to a wide range of users, such as utility companies and estate agents. Often ownership boundaries do not perfectly align with physical features, either because of differences in their capture processes, or because no feature actually exists on the ground.   

## Examples
Figure 1 shows the overlap between OSMM Topographic Area Polygons (green lines) and HM Land Registry INSPIRE Polygons (red lines) in an area in Leicester. Image includes Copyrighted from Ordnance Survey and Aerial Photography of Great Britain.

![Overlaps](/_media/Overlap.png)
<br>__Figure 1:__ Overlap between OSMM Topographic Area Polygons and HM Land Registry INSPIRE Polygons

![Overlaps](/_media/Overlap2.png)
<br>__Figure 2:__ ....
 
Figure 2 shows a Land Registry boundary line (red) and an OSMM Topographic Area boundary (dark grey). The two lines diverge. It is questionable that this overlap exists in reality.
 
 
## Correlation Methodology and Confidence Metric

Spatial relation based on overlap, excluding touching boundaries

![Overlap excluding touching boundaries](/_media/method1.PNG)

__Stage 1__
![Stage 2](/_media/method2.PNG =250x)
- Take into account the potential error in captured location.
- Buffer all features OUT by this error quantity.
- The intersection between these buffered LR and OS features is then tested.
- If the intersection is true, then a confidence metric of 3 is applied.

__Stage 2__
![Stage 2](/_media/method3.PNG)
<img src="/_media/method3.PNG" width="100" height="100">
- Ignore potential error in captured location.
- Leave all features in their captured positions.
- The intersection between these features is tested.
- If the intersection is true, then a confidence metric of 2 is applied.

__Stage 3__
![Stage3](/_media/method4.PNG)
- Again, take into account the potential error in captured location.
- Buffer all features IN by this error quantity.
- The intersection between these buffered LR and OS features is then tested.
- If the intersection is true, then a confidence metric of 1 is applied.

This will ensure that overlaps which are within capture tolerance and hence may not be real, are given a lower confidence metric than intersections between the main bodies of features.

## Correlation Lookup Volume
There are approximately 265 million OSMM topographic areas in England and Wales. There are approximately 23 million HM Land Registry INSPIRE polygons. Therefore, the correlation contains up to 5.9x10<sup>15</sup> relationships.

 <a href="http://www.google.com/">
    <button>Downlaod</button>
</a>

## Practical Applications
### Utilities
A gas utility company may wish to replace the pipes in an area. Plotting the paths of these pipes against OSMM will identify the polygons intersected along with their identifiers (TOIDs). It would then be a simple process to query the linked identifiers to find the Inspire polygons related to these OSMM features and from there the landowners who would need to be contacted.

### Estate agents
If a homeowner approaches an estate agent with a view to selling their property, an application could be built to link the property address to the main building TOID (using OS Address Base Premium). From there, the intersecting the HM Land Registry Inspire ID can be quickly found from the linked identifiers table. The owner of the parcel can then be identified and compared to the proposed seller to verify they are one and the same. This will help mitigate the risk of fraudulent activities.

Alternatively, once the Inspire ID has been found, other OSMM Topographic Area features linked to the same Inspire ID can be looked up to give an instant view of garden area, outbuildings, main building footprint area, building height and other attributes of the property.

