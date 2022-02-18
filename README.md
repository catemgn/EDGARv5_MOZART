## :globe_with_meridians: EDGAR v5.0 emissions inventory for the MOZART chemical mechanism: source code 
Here you can find the accompanying code used for processing the dataset at https://doi.org/10.5281/zenodo.6130621. The dataset provides [EDGAR v5.0](https://edgar.jrc.ec.europa.eu/index.php/dataset_ap50) monthly emissions for year 2015 speciated for [MOZART chemical mechanism](https://gmd.copernicus.org/articles/3/43/2010/) and ready to use in [WRF-Chem ](https://ruc.noaa.gov/wrf/wrf-chem/) atmospheric model with MOZART-MOSAIC options.


### :mag: Description

The dataset provides monthly EDGAR v5.0 global  air  pollutant  emissions  for  the  year  2015,  speciated  for  the  MOZART  chemical  mechanism.
Emission files are provided as individual NetCDF files for each pollutant containing anthropogenic sector emissions as individual variables. 
All the data processing summarised by the flowchart below:

<p align="center">
<img src="/images/flowchart.png" width="700" height="600">
</p>

Each step of the process is described in detail in the technical documention (technical_note_EDGARv5_MOZART.pdf) accompanying the [dataset](https://doi.org/10.5281/zenodo.6130621).
In this repository you can find the code for each step in the corresponding scripts in the [code](/code) folder:

* 1): `download_edgarv5.sh`
* 2): `edgarv5_format.ipynb`
* 3): `download_nmvoc_edgarv432.sh`
* 4): `nmvoc4.3.2_format.ipynb`
* 5): `CEDS_MOZART_VOCmap.xlsx`
* 6): `nmvoc4.3.2_map_mozart_mass.ipynb`
* 7), 8): `nmvoc4.3.2_map_mozart_fractions.ipynb`
* 9):  `edgarv5_NMVOC_map_sectors.xlsx`,`map_v5tov4.3.2_nmvoc_sectors.ipynb`
* 10): `edgarv5_nmvoc_speciate_to_mozart.ipynb4`
* 11): `add_total_emissions.ipynb`
* 12): `edgarv5_toWRFChemanthroemiss.ipynb`

For more details refer to the individual scripts.

### :envelope_with_arrow: Contacts 
If you have questions,comments, or suggestions please drop an email to **c.mogno@ed.ac.uk**. <br />
If you find bugs (and there will be!) feel free to [open an issue](https://github.com/catemgn/EDGARv5_MOZART/issues) in the repo.

### :speech_balloon: How to cite  
If you use the dataset produced by this code and/or part of the code for an academic publication or any other work, we would be grateful if you could cite the zenodo repository: https://doi.org/10.5281/zenodo.6130621

### :memo: License
All  the  material provided is distributed under [MIT License](https://choosealicense.com/licenses/mit/).

