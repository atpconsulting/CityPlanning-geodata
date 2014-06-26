# Land Use

### Summary  
 
City of Philadelphia land use as ascribed to individual parcel boundaries or units of land. Land use is the type of activity occurring on the land such as residential, commercial or industrial. Each unit of land is assigned one of nine major classifications of land use (2-digit code), and where possible a more narrowly defined sub-classification (3-digit code). The land use feature class has been field checked and corrected for the following Planning Districts. The year of the update is in parentheses:   
  
    Central (2012)   
    Central Northeast (2013)   
    Lower North (2013)   
    Lower Northeast (2012)   
    Lower Northwest (2013)  
    Lower South (2011)   
    West Park (2011)   
    University Southwest (2012)   
  
Field checks and updates are planned for the 11 remaining Planning Districts as part of the Philadelpia2035 comprehensive planning process.  
  
Feature updated:    9/6/2013   
Attribute updated:   9/6/2013   
Metadata updated: 6/10/2014  


### Description  

Citywide land use as determined by the City Philadelphia Planning Commission (PCPC). Prepared for Philadelphia2035, the Citys comprehensive development plan, to support the zoning reform remapping and the District Planning projects. For more information on the Philadelphia2035 comprehensive planning process, see www.phila2035.org 

Land use classifications are activity-based. Each land unit has only one land use designation interpreted by a 1, 2 or 3-digit code. Specificity of a land use description increases from the one to three digit code. Example: 1= Residential, 1.2 = Residential Medium Density, and 1.2.1 = Residential Rowhouse.

Land use features are derived from Philadelphia Water Department tax parcel boundaries (2009 to current release date) and from other GIS datasets prepared by City departments including: planimetric features, transportation right-of-ways (ROW), parks and open space, and water. Land use boundaries are typically coincident with PWD tax parcel boundaries, where tax parcel boundaries are available to define units of land. In some cases multiple land activities on a single parcel and been individual represented as individual polygons of land use. 

This land use feature class is under revision through 2014. Updates will be made to correct attributes and features and to populate 3-digit codes based upon field verifications made by PCPC staff. Land use field surveys will be conducted for each of the 18 Planning District beginning in 2011 as part of the Philadelphia2035 Compressive Planning process. For areas not yet updated by a Planning District field survey, land use designations are qualified estimates derived from the Office of Property Assessment data (see details under Development Process below). 

####Lineage
The land use feature class has been field checked and corrected for selected Planning Districts as follows. The year of the update is in parentheses: 
- Central (2012)
- Central Northeast (2013)
- Lower North (2013)
- Lower Northeast (2012)
- Lower Northwest (2013)
- Lower South (2011)
- West Park (2011)
- University Southwest (2012)

Also includes portions of Lower Schuylkill (2012) in Lower Southwest and portions of the North district along the Amtrak corridor (2013).

Field checks and updates are planned for the remaining Planning Districts as part of the Philadelpia2035 comprehensive planning process.

####Landuse Codes and Descriptions

Landuse codes are organized from the 1-digit to 3-digit level. Specificity of land use increases with each increasing digit. Coded numeric values are stored as integers. Full text descriptions are contained in separate string fields. Values in the 3-digit code and description fields may not be fully populated, indicating that these features have not been field verified, or that this level of specificity cannot be accurately assigned. All features are attributed at the 1- and 2-digit levels.

#####2-digit level

    1.0 Residential 
    1.1 Residential Low Density
    1.2 Residential Medium Density
    1.3 Residential High Density
    2.0 Commercial2.1 Commercial Consumer
    2.2 Commercial Business and Professional
    2.3 Commercial Mixed Residential 
    3.0 Industrial 
    4.0 Civic/Institution
    5.0 Transportation
    6.0 Culture/Recreation
    6.1 Culture/Amusement
    6.2 Active Recreation
    7.0 Park/Open Space
    7.1 Park/Open Space
    7.2 Cemetery
    8.0 Water
    9.0 Vacant or Other
    9.1 Vacant Land
    9.2 Other/Unknown

####Development Process
The PCPC acquired the Philadelphia Water Department's (PWD) tax parcel boundary feature class (2009) for use as base layer geometry. This parcel base does not contain transportation, park, or water features required for identification of land uses for every unit of land across the entire city. Separate feature classes were acquired by the PCPC to represent all other land features streets, highways and rail right of ways, rail yards, parks and open space, parking lots and sidewalks, and marine terminals. 

Multiple feature classes were merged into a single feature class in ArcGIS 9x to produce a seamless fabric of land and water features citywide. Gaps in the spatial fabric persisted where feature classes did not topologically align. Gaps, slivers and overlaps between features, resulting from the merge process, were identified and edited using ArcGIS geodatabase topology rules.

The resulting draft Land Use 2010 feature class was joined with the Office of Property Assessment (OPA), formerly BRT, real estate database (2009). The PCPC used OPA building description values from the real estate table as the basis for land use categorization. All features were attributed to the 2-digit level. PCPC staff checked and corrected these categorizations using the following resources: PhilaShops retail properties database (2003); Philadelphia Industrial Development Corporations Industrial Market and Landuse Strategy report (2009), and Philadelphia Parks and Recreation (PPR) parks land and facilities database (2010). 

Under the Philadelphia2035 District Planning process, this feature class will undergo field verification as each Planning District project is completed. A total of 18 Planning Districts will be surveyed from 2011 to 2016. Field verification results in corrections to land use attributes and population of the 3-digit land use codes, which cannot otherwise cannot be determined without field inspection. Revisions to this land use feature class will be posted as survey work and evaluation for each Planning District is fully completed.

####Thematic Mapping
For thematic mapping, use the c_dig2 or c_Dig2Desc fields. The c_Dig2Desc field maintains the full text description of the 2-digit land use codes (e.g., 11 = Residential Low Density). An ESRI ArcGIS layer file (.lyr) with pre-set symbology is available from the PCPC.

Symbol RGB Values

    11 - Residential Low : 255, 255, 204
    12 - Residential Medium : 245, 255, 18
    13 - Residential High : 255, 170, 0
    21 - Commercial Consumer : 230, 0, 0
    22 - Commercial Business/Professional : 168, 0, 0
    23 - Mixed Commercial/Residential : 232, 149, 121
    31 - Industrial : 140, 0, 255
    41 - Civic/Institution: 0, 112, 255
    51 - Transportation : 204, 204, 204
    61 - Culture/Recreation : 0, 255, 230
    62 - Active Recreation: 155,204,179; 99, 204, 0
    71 - Park/Open Space : 99, 204, 0
    72 - Cemetery : 99, 204, 0; 107, 126, 147
    81 - Water : 191, 232, 255
    91 - Vacant: 168, 112, 0
    92 - Other/Unknown: 107, 126, 174; 210, 210, 210

####Coordinate System:
State Plane Pennsylvania South US Survey Feet, NAD83  

### Data Dictionary

| Field | Description  
| ----- | :----------:  
| C_DIG1 |  1-digit level land use coding, numeric code.
| C_DIG1DESC |  1-digit level land use text description.
| C_DIG2 |  2-digit level land use coding, numeric code.
| C_DIG2DESC |  2-digit level land use text description.
| C_DIG3 |  3-digit level land use coding, numeric code.
| C_DIG3DESC |  3-digit level land use text description.
| VACBLDG |  
| YEAR |  the year to which the land use codes are current. If year 2010, this reflects land use codes that have NOT been field surveyed and the codes were assigned as described in the "Development Process" below.

### Credits  

Mark Wheeler, GISP  
City Planner  
City Philadelphia Planning Commission  
1515 Arch Street, 13th Floor  
Philadelphia PA 19102  
mark.wheeler@phila.gov  
215-683-4686  


### Use Limitations  

Landuse is not a substitute for, or an equivalency to, zoning and is not a legal determination of property use or property boundaries. Site specific verification may be required. Calculations of land use by category are approximations. Gaps and misalignments between features are due to the import of spatial features produced by different City departments, and topological integrity among features is not present.The City of Philadelphia reserves all rights in the GIS database and any data contained therein, and the end users use of the data does not constitute a transfer of, nor does the end user receive, any title or interest in the database or any other City data. The City of Philadelphia makes no representation about the accuracy of any specific information in this GIS data and is provided as is and without Warranty of any kind. The user of this data will assume complete responsibility for any and all occurrences resulting from its use or display and will hold the City of Philadelphia harmless from any and all claims, demands, liabilities, obligations, damages, suits, judgments or settlements, including reasonable costs and attorneys' fees that arise from use of this data.