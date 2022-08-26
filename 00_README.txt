#############################################
## INSTRUCTIONS FOR GTUNE DATA REPOSITORY: ##
#############################################
Header information included for all catalogs and datasets
--------------------------------------------------------------
#############################################
################# CATALOGS ##################
#############################################

- GTUNE_Catalog.txt >  Catalog of all the Underground Nuclear explosions used in the GTUNE labeled waveform prepared dataset, and input for IRIS_query script

- Combined_SIPRI_DOE.txt > SIPRI catalog of declassified nuclear blasts with the DOE source time and location information for the tests the United States is responsible for 

- SIPRI_Catalog.txt > Digital SIPRI catalog of declassified nuclear blasts

- DOE_Catalog.txt > DOE catalog of US nuclear test blasts

- EQ_Catalog.txt > Catalog of Earthquakes used for the Earthquake training labels and input for the IRIS_query.py scripts

#############################################
############ PREPARED DATASETS ##############
#############################################
___________ filename + .pkl/.h5 _____________

- GTUNE_unes > One minute, 10-second P-wave arrival fixed, labeled raw seismograms of underground nuclear blasts and corresponding meta data.

- EQs > One minute, 10-second P-wave arrival fixed, labeled raw seismograms of earthquakes and corresponding meta data.

- Noise > One-minute noise labeled seismograms and meta data.

- FSU > Un-cut Former Soviet Union dataset of underground nuclear blast waveforms and corresponding meta-data.

- LASA > Un-cut Large Aperature Seismic Array of underground nuclear blast waveforms and corresponding meta-data.

- LLNL > Un-cut Lawrence Livermore National Laboratory dataset of underground nuclear blast waveforms and corresponding meta-data.

All dataframes have the following column structures:

origin_time    |  trace_start_time  |	p_arrival   |	sampling_rate |	station_dist  |	 stla	  |  stlo      |  station |  evid     |	net	| chn	   | waveform
(epoch time (s)|   epoch (s)        |     (seconds) |       (hz)      |    (degrees)  |  latitude |  longitude |   name   | event id  | network | channel  | times series array                   

#############################################
########### DATA QUERY SCRIPTS ##############
#############################################
____________ Python 3.8 scripts ____________

 - Hinet_query.py > Script to query NIED Hi-Net array network of data.  *Note: you must first aquire a permission and username to access NIED data: https://hinetwww11.bosai.go.jp/nied/registration/?LANG=en 

 - IRIS_query.py > Script using ObsPy massdownloader for downloading all available fdsn web servers waveforms for nuclear blasts and earthquakes

 - Noise_EQ_filter.py > Script to filter out time periods without regional and global earthquakes occuring within a 30 minute time period.

