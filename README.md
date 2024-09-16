# brouter-mtb
a Brouter Mountainbike Profile

This profile tries to find routes suitable for mountainbikes. It tries to avoid major roads and focuses on tracks for uphills and paths/tracks for downhills where possible.

There are two major parameters to modify the behaviour: 

* is_wet 
 * false: normal behaviour (default)
 * true: try to avoid ways which are potentially unpleasant to ride when they are wet (for example ways with grass/earth surface)
* mtb_hard_factor (range 0 - 4)
 * 0: normal behaviour (default in mtb-zossebart.brf), generate routes for XC/AM
 * 2: generate harder routes (for example All Mountain, default in mtb-zossebart-hard.brf)
 * 4: highest setting (for example Enduro)
 
Also, there are some additional switches for special features:
* allow_ferries: switch on and off the usage of ferries (default off)
* allow_steps: wether the route can go over steps (default on)
* use_uncertain_gates: wether passing of gates with unknown access restrictions is allowed or not. The default behaviour is to do not pass such gates. However, in some poorly mapped areas, it might be beneficial to enable this switch to avoid lots of big detours in the routing. Be aware that you could end up at a closed or restricted gate then!

**CAUTION:** Locus ignores the default settings of the parameters when the profile is first configured! This means the _avoid_unpaved_ parameter is set to _false_, which leads to the creation of harder routes in profile versions prior to v1.1.0!
Please enable _avoid_unpaved_ at the first setup if you want the default behaviour! This setting is global for all profiles configured in Locus.
This is not a problem with other apps or brouter-web, as they are not aware of these parameters and thus use the default settings.
Beginning from v1.1.0, the profile is split into two separate variants (normal/hard), so this is not a problem any more.

## Changelog ##
### v1.0.0 ###
* initial version

### v1.0.1 ###
* refactor to syntax alternatives (should improve the readability)

### v1.0.2 ###
* correction to make Locus parameter switches work again

### v1.1.0 ###
* split into normal/hard versions of the profile, removed avoid_unpaved parameter

### v1.1.1 ###
* fix for wrong turninstructions bug

### v1.1.2 ###
* add profile parameter comments, fix ferry route avoidance

### v1.1.3 ###
* add missing turninstructionmode parameters

### v1.1.4 ###
* add oruxmaps turninstructionmode parameter

### v1.2.0 ###
* avoid oneways on cycleways
* kinematic model parameters for more precise ETA

### v1.2.1 ###
* add parameter to switch access on uncertain gates (without access-tags)
