### SNIDtemplates 
This release contains all SuperNova IDentification (SNID; [Blondin & Tonry 2007](http://arxiv.org/abs/0709.4488)) templates of Stripped-Envelope SN (i.e., SNe IIb, Ib, Ic and Ic-bl) spectra presented/included in [Liu & Modjaz 2014] (http://adsabs.harvard.edu/abs/2014arXiv1405.1437L), [Liu et al. 2016] (http://adsabs.harvard.edu/abs/2015arXiv151008049L), and [Modjaz et al. 2016] (http://adsabs.harvard.edu/abs/2015arXiv150907124M), based on both CfA Data (initially released in Liu & Modjaz 2014) and the rest of literature data (included in Liu et al. 2016 for IIb and Ib, Modjaz et al. 2016 for Ic and Ic-bl). Adding these templates to the default library of SESN spectra of SNID (https://people.lam.fr/blondin.stephane/software/snid/) will increase the number of Stripped-Envelope templates in the database, which in turn will help SN classification via SNID. 

The text file "SNIDtemplate-SESNe-info.txt" includes detailed information about the SNe and their spectra that were used to construct the templates. Its columns list for each SN:
- the subtype
- the redshift (which was used to de-redshift the spectra) 
- the date of maxium light, according to which the spectra are referenced for their phase, though the release also contains spectra of SNe without maximum light measurements (see info).
- in which (rest) filter the date of max is referring to (note that, in order to be consistent, we use always V-band values, and if there is no V-band measurement, we use the conversion of Bianco et al. (2014) for SESNe, to convert between the given filter and the V-band)
- method with which the date of maximum was determined and the reference for photometry (if a number is listed, see the bottom of the file for explanations for individual SNe)
- references for the spectra

We also include SNe that have no measured date of max - in the SNID library, their listed "phases" are computed with respec to the first spectrum. These are templates compliant with SNID version SNID-5.0.

There are 2 subdirectories with that include the .lnw files for the SNID templates: 
- /templates_new
- /templates_adjusted 

NEED TO MODIFY THE REST:
add new subtype: Ibn.
there are 465 spectra of 36 SNe Ib/c in templates-2.0.
there are 403 spectral templates out of 44 SNe Ib (including 1 SN that is already in templates-2.0) and 341 out of 39 SNe Ic (including 2 SNe that is already in templates-2.0) in this templates.

