Original read me file is barebones at best. Here is how I replicated the results.

1.) Data set

	Download the cps dataset from the replication package located in .../src/cps_00013.dta
		To get original data: https://cps.ipums.org/cps-action/variables/group, select variables located in 		the .dta with harmonized variables 
 	
	In order to prepare data, copy past the code from ..../do/fragment-prepare-cps-data.do into your own do file. Make sure to change directories of the 3 data files (dd,ddd,micro) to relevant directory (DataClean in my case).

	Run your do file.
