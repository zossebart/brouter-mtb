# brouter-mtb
a Brouter Mountainbike Profile

This profile tries to find routes suitable for mountainbikes. It tries to avoid major roads and focuses on tracks for uphills and paths/tracks for downhills where possible.

There are two major switches to modify the behaviour: 

* is_wet 
 * false: normal behaviour (default)
 * true: try to avoid ways which are potentially unpleasant to ride when they are wet (for example ways with grass/earth surface)
* avoid_unpaved
 * true: normal behaviour (default), generate routes for XC/AM
 * false: generate harder routes (for example Enduro)
 
These parameters are configurable from within the Locus UI when used with Locus version 3.19 and up. 

**CAUTION:** Locus ignores the default settings of the parameters when the profile is first configured! This means the _avoid_unpaved_ parameter is set to _false_, which leads to the creation of harder routes!
Please enable _avoid_unpaved_ at the first setup if you want the default behaviour!
This is not a problem with other apps or brouter-web, as they are not aware of these parameters and thus use the default settings.

## Changelog ##
### v1.0.0 ###
* initial version
### v1.0.1 ###
* refactor to syntax alternatives (should improve the readability)
