Sequencial runs of the Python code:

1) edgarv5_format.ipynb: 
Reorgnaise the raw edgarv5 monthly data by sector for year 2015 as nc files by species. 
This notebook reorganises raw edgarv5 2015 monthly emissions gridmaps and save them to nc files by species. 
Outputs are nc files for each species containing montlhy contributions of all the sectors specified in https://edgar.jrc.ec.europa.eu/overview.php?v=50_AP (total: 27) minus the supersonic aviation (no monthly data available).
Each .nc produce file has the structure:

SPECIES_NAME:
	sector1_name(lat, lon,months)
	sector2_name(lat, lon,months)
	...
	sectorN_name(lat, lon,months)

The species taken into account from edgarv5 are all: PM10,PM25,OC,BC,NH3,NOx,SO2,NMVOC (total 8).
The sectors taken into account are all the ones in the edgarv5 except from supersonic aviation (total 27-1)

2)nmvoc4.3.2_format.ipynb:
This notebook reorganises raw Edgar4.3.2 monthly speciated VOCs emissions gridmaps for 2010 and save them to nc files by species.
NC file output structure is the same as output in 1):

VOC SPECIES_NAME:
	sector1_name(lat, lon,months)
	sector2_name(lat, lon,months)
	...
	sectorN_name(lat, lon,months)

NOTE: on the 17 sectors available as described in: https://edgar.jrc.ec.europa.eu/dataset_ap432_VOC_spec we used 16 (17 minus aviation supersonic which has no monthly data).

3) nmvoc4.3.2_map_mozart_mass.ipynb:
This code maps EDGARv4.3.2 speciated VOCs emissions from GEIA/CEDS to MOZART chemical mechanism VOCs emissions using the mapping in the CEDS_MOZART_VOCmap.xlsx.
The final output mapping is between mass and not molar contribution.

4)nmvoc4.3.2_map_MOZART_fractions.ipynb:
This notebook calculates gridded maps with mass fractional contribution of each VOCs MOZART species to total NMVOCs . 

5)map_v5_to_v4.3.2_nmvoc_sectors.ipynb:
There is no 1:1 correspondence of NMOVCs sectors between Edgar v5.0 and Edgarv4.3.2. This notebook maps the edgar v5.0 NMVOCs to match edgar v4.3.2 sectors, so it will be possible to perform speciation by consitent sector types. The mapping is provided in the 'edgarv5_NMVOC_map_sectors.xlsx' file.
All edgar v5.0 NMVOCs sectors are mapped, except manure management (ippc2006:3A2,ippc1996:4B, MNM) that is no correspondend in speciated edgar v4.3.2 NMVOCs.

6)edgarv5_nmvoc_speciate_to_mozart.ipynb:
This notebook speciate total edgar v5.0 nmvoc to MOZART mechanism using the fractional VOCs gridmaps calculated in step 4). 
NOTE: speciation is provided for all sectors having NMVOC in edgarv5 using lumped sectors to match edgarv4.3.2 sectors. 

7)  add_total_emissions.ipynb
This notebook add to each species the total emissions coming from the sum of emissions of all sectors.

8) edgarv5_to_WRFChem_anthroemiss.ipynb
This notebook prepares the edgarv5 emissions to be used in WRF-Chem preprocessing tool anthro-emiss by adding date and datetime variables and units attribute needed.


