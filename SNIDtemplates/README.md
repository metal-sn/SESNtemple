[![DOI](https://zenodo.org/badge/22593/nyusngroup/SESNtemple.svg)](https://zenodo.org/badge/latestdoi/22593/nyusngroup/SESNtemple)

### SNIDtemplates 
This release contains all new SuperNova IDentification (SNID; [Blondin & Tonry 2007](http://arxiv.org/abs/0709.4488)) spectral templates (compared to SNID database templates-2.0) of Stripped-Envelope SN (i.e., SNe IIb, Ib, Ic and Ic-bl) presented/included in [Liu & Modjaz 2014](http://adsabs.harvard.edu/abs/2014arXiv1405.1437L), [Liu et al. 2016](http://adsabs.harvard.edu/abs/2016ApJ...827...90L) and in [Modjaz et al. (2016)](http://adsabs.harvard.edu/abs/2016ApJ...832..108M), that are based on both CfA Data (initially released in Liu & Modjaz 2014) and the rest of literature data (included in Liu et al. 2016 for IIb and Ib, Modjaz et al. 2016 for Ic and Ic-bl). We also now include SNID templates of Superluminous SNe Ic (SLSNe Ic) produced in [Liu, Modjaz & Bianco (2017)](http://adsabs.harvard.edu/abs/2016arXiv161207321L), based on literature data. NOTE: if you want to include the SLSNe Ic in your SNID template library, you also need to modify the required SNID file so this new type of SLSN Ic is recognized (see SNID documentation on how to add new types).

Adding these templates to the default library of SESN spectra of SNID (https://people.lam.fr/blondin.stephane/software/snid/) will increase the number of Stripped-Envelope templates in the database, which in turn will help SN classification via SNID. We have more than doubled the number of SNe in the SNID spectral library. These are templates compliant with SNID version SNID-5.0.

The text file **SNIDtemplate-SESNe-info.txt** includes detailed information about the SESNe and their spectra that were used to construct the templates. Its columns list for each SN:
- the subtype
- the redshift (which was used to de-redshift the spectra) 
- the date of maxium light, according to which the spectra are referenced for their phase (we note that SN-GRBs and SNe Ibn have the largest uncertainties in their date of max). This release also contains spectra of SNe without maximum light measurements (see info).
- in which (rest) filter the date of max is referring to (note that, in order to be consistent, we use always V-band values, and if there is no V-band measurement, we use the conversion of Bianco et al. (2014) for SESNe, to convert between the given filter and the V-band)
- method with which the date of maximum was determined and the reference for photometry (if a number is listed, see the bottom of the file for explanations for individual SNe)
- literature references for the spectra

We also include SNe that have no measured date of max - in the SNID library, their listed "phases" are computed with respect to the first spectrum. 

For the SLSNe Ic, **SLSNIc-LiuModjazBianco17-infolist.txt**  contains information about the SLSNe Ic and their spectra in a similar format (see also Table 1 in Liu, Modjaz & Bianco 2017 for more information on the spectra).

There are 2 subdirectories with that include the .lnw files for the SNID templates: 
- **/templates_adjusted**: These include SNe that had been included in Blondin's SNID library release (ie "templates-2.0") but for which we either added additional spectra, changed the SN type or the date of max
- **/templates_new**: These include SNe that had not been released in Blondin's SNID library release (ie "templates-2.0"), and thus are "new". The subdirectory SLSNIc_SNIDtemplates contains the SNID templates of SLSNe Ic from Liu, Modjaz & Bianco 2017.

NOTES: 
- we included 2 new SN types:

    -"Ibn", of which we include 3 SNe (00er,02ao, 06jc)
    
    -"Ic-SL", of which we include 32 SNe (from Liu, Modjaz & Bianco 2017). Note that since the continuum-removed spectra of SLSNe Ic are similar to those of SN Ic-bl (as shown in Liu, Modjaz & Bianco 2017), including SLSNe templates may lead to dual IDs of one object as both Ic-bl and SLSN Ic.
- For comparison: there were 465 spectra of 36 SESNe in Blondin's release (templates-2.0). **In this release**, there are at total 631 spectral templates of 51 SNe Ib and its subtypes (including 1 SN that was already in templates-2.0), 429 of 45 SNe Ic and its Ic and Ic-bl subtypes (including 2 SNe that were already in templates-2.0), and 178 spectra of 32 SLSNe Ic.

