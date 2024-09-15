# Young SNe Ib
This repository contains the data products of the spectral data set of young Type Ib from Yesmin et al. 2024.
This release contains new spectral templates of SNe Ib used for the SuperNova IDentification (SNID; Blondin & Tonry 2007) presented in Yesmin et al. 2024, which are mainly based on Las Cumbres Observatory (LCO) data. SN 2019odp and SN 2016bau have additional data that were presented in Schweyer et al. 2023 and Aryan et al. 2021 respectively and are also included in the SNID templates that we created.

Adding these templates to the default library of SESN spectra of SNID (https://people.lam.fr/blondin.stephane/software/snid/) and the extended SESNe Modjaz Group Sample (MGS; Modjaz et al. 2014; Liu et al. 2016, 2017; Williamson et al. 2019) will increase the number of SNID templates of premaximum spectra of SNe Ib by ∼54%. Templates in the database will help SN classification via SNID. These templates are compliant with SNID version SNID-5.0.

The text file SNIDtemplate-youngIb-info.txt includes detailed information about the SNe in the sample and their spectra that were used to construct the templates. Its columns list for each SN:
- SN name
- IAU name
- the redshift (which was used to de-redshift the spectra)
- the date of maxium light, according to which the spectra are referenced for their phase
- filter in which the date of max is reported in
- method with which the date of maximum was determined

The subdirectory called "templates_yesmin" includes the .lnw files for the SNID templates.

For comparison: there were 235 spectra (with 91 premaximum spectra) of 22 SNe Ib in Blondin's release (templates-2.0) + MGS. In our data release, there are at total 91 photospheric spectral templates of 8 SNe Ib with 38 premaximum spectra. Furthermore, we add SNID templates for 19 photospheric spectra (8 premaximum spectra) of SN 2019odp published in Schweyer et al. 2023 and 6 photospheric spectra (2 premaximum spectra) of SN 2016bau published in Aryan et al. 2023. Thus, this data set significantly enhances the number of premaximum spectral templates of SNe Ib. 

# References
Blondin, S. & Tonry, J. L. 2007, ApJ, 666, 1024
Aryan, A., Pandey, S. B., Zheng, W., et al. 2021, MNRAS, 505, 2530
Schweyer, T., Sollerman, J., Jerkstrand, A., et al. 2023, arXiv e-prints, arXiv:2303.14146
Modjaz, M., Blondin, S., Kirshner, R. P., et al. 2014, The Astronomical Journal, 147, 99
Liu, Y.-Q., Modjaz, M., Bianco, F. B., & Graur, O. 2016, ApJ, 827, 90
Liu, Y.-Q., Modjaz, M., & Bianco, F. B. 2017, ApJ, 845, 85
Williamson, M., Modjaz, M., & Bianco, F. B. 2019, ApJ, 880, L22
