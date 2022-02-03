# EDGARv5_MOZART
EDGAR v5.0 emissions inventory for year 2015 speciated for MOZART chemistry and ready to use in WRF-Chem MOZART_MOSAIC options.

![header_image](/images/edgar.jpg) ![header_image2](/images/wrfchem_logo.png) 

##### Table of Contents  
* [Description](#Description)  
* [Acknowledgements](#Acknowledgements)
* [Contacts](#Contacts)
* [How to cite](#How-to-cite)
* [License](#License)


    
<a name="Description"/>
<a name="Acknowledgements"/>
<a name="Contacts"/>
<a name="How-to-cite"/>
<a name="License"/>


## Description
Emissions inventories need to be prepared to be used in chemical transport models (CTMs). They usually need ad-hoc preprocessing based on the chemical mechanism used in the CTM, including speciation of non-methane volatile organic compounds (NMVOCs). 

Here we provide **monthly [EDGAR v5.0](https://edgar.jrc.ec.europa.eu/index.php/dataset_ap50) global  air  pollutant  emissions  for  the  year  2015,  speciated  for  the  MOZART  chemical  mechanism.** 

Emission files are provided as individual NetCDF files for each pollutant containing anthropogenic sector emissions as individual variables in the following form:
<p align="center">
<img src="/images/dataset_structure.PNG" width="600" height="600">
</p>

These files are also ready-to be used in WRF-Chem [anthro-emiss preprocessing  tool](https://www2.acom.ucar.edu/wrf-chem/wrf-chem-tools-community)  with the MOZART-MOSAIC options.

In the folder you will find:
* *edgarv5MOZARTdata.tar.gz*:  EDGAR  v5.0  monthly  emissions  for  the  year  2015  (NetCDFformat), speciated for MOZART chemical mechanism.  Both total and individual sector emissionsare included in each file.
* *edgarv5MOZARTMOSAIC.inp*:  Input file for anthroemiss preprocessing tool for MOZART-MOSAIC options in WRF-Chem.
* *code* (folder):  scripts used to prepare 1).  
* *technicalnoteEDGARv5MOZART.pdf*: documentation.


For extensive infromation, please refer to the technical documentation technicalnoteEDGARv5MOZART.pdf.


## Contacts
If you find a bug (and there will be!)

## How to cite
If you use this ready-to-use EDGAR v5.0 inventory and/or part of the code for an academic publication or any other work, we ask you to include the following acknowledgment: “We acknowledge the use of the EDGAR v5.0 emissions inventory as prepared by **Mogno and Marvin (2022)**  [[1]](#1)”

or directly cite the zenodo repository:
TO DO: ADD FINAL ZENODO REP.

## License
All  the  material  provided  (the  dataset,  the  input  file  for  anthroemiss,  the  code  and  the  presenttechnical documentation) is distributed under [MIT License](https://choosealicense.com/licenses/mit/).

## References
<a id="1">[1]</a>
 Caterina Mogno and Margaret R. Marvin. EDGAR v5.0 Global Air Pollutant Emissions for MOZART chemicalmechanism. ZENODO TO BE ADDED, 2022
