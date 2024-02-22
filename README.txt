Original read me file is barebones at best. Here is how I replicated the results. Fi

1.) Data set

	Download the cps dataset from the replication package located in .../src/cps_00013.dta as well 	as .../dta/cps_yngch. I created .../DataRaw to store them.
		To get original data: https://cps.ipums.org/cps-action/variables/group, select variables located 		in the .dta with harmonized variables 
 	
	In order to prepare data, copy past the code from ..../do/fragment-prepare-cps-data.do into your own do 	file. Make sure to change directories of the 3 data files (dd,ddd,micro) to relevant directory (DataClean 	in my case). Do this for both the use and save functions.

	Run your do file in stata console with attached macro command 13 for the micro data file.
		Ex: do fragment-prepare-cps-data.do 13
	
	Run your do file in stata console with attached macro command 0 for the DDD and DD data file.
		Ex: do fragment-prepare-cps-data.do 0

2.) Tables

	Copy code from .../do/run-cps-main-tables.do up until table 3. Change directory file paths.
	Copy paste the .../do/fragment-run-our-bbs-procedure.do file into the same directory

	Create a .../log file where you will save your stata output into. Change the directory path in to go to 	that path.

	Run your relevant table do file in stata with attached macro command all.
		Ex: do replicate_tables_all.do all

	Relevant results found in log file.

3.) Figures

	Create a file in your directory .../gph to store figures. Copy code from .../do/create-cps-figures.do. 	Change directories for save, use, and log functions to your relevant directories. 	(.../gph, .../DataClean/... for example).
	
	Relevant results found in gph file.

