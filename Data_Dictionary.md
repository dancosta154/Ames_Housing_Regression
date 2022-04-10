### Data Dictionary

This data dictionary provides an overview of features/variables/columns, alongside data types and descriptions. 

|Feature|Type|Source|Description|
|---|---|---|---|
|**overall_qual**|*int*|modeleight_log.csv|Rates the overall material and finish of the house|
|**gr_liv_area**|*int*|modeleight_log.csv|Above grade (ground) living area square feet| 
|**year_remod/add**|*int*|modeleight_log.csv|Remodel date (same as construction date if no remodeling or additions)| 
|**total_bsmt_sf**|*float*|modeleight_log.csv|Total square feet of basement area| 
|**exter_qual_num**|*int*|modeleight_log.csv|Evaluates the quality of the material on the exterior, converted to a numeric range| 
|**kitchen_qual_num**|*int*|modeleight_log.csv|Kitchen quality, converted to a numeric range|
|**bsmt_qual_num**|*float*|modeleight_log.csv|Evaluates the height of the basement, converted to a numeric range|
|**garage_area**|*float*|modeleight_log.csv|Size of garage in square feet|
|**garage_cars**|*float*|modeleight_log.csv|Size of garage in car capacity|
|**total_bsmt_sf**|*float*|modeleight_log.csv|Total square feet of basement area|
|**garage_finish**|*int*|modeleight_log.csv|Interior finish of the garage, converted to a numeric range|
|**overall_qual_liv_area**|*float*|modeleight_log.csv|Interaction column, using **overall_qual * gr_liv_area** columns|
|**overall_qual_squared**|*int*|modeleight_log.csv|Engineered column, using the **square of the overall_qual** column|
|**quality_and_age**|*int*|modeleight_log.csv|Interaction column, using **overall_qual * year_remod/add** columns|
|**house_total_sq**|*float*|modeleight_log.csv|Engineered column, using **total_bsmt_sf + gr_liv_area/add** columns |
|**year_remod_or_built**|*int*|modeleight_log.csv|Interaction column, using **year_remod/add * year_built** columns|
|**year_remod_or_built_sq**|*int*|modeleight_log.csv|Engineered column, using the **square of the year_remod_or_built** column|
