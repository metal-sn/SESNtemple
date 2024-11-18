[![DOI](https://zenodo.org/badge/22593/nyusngroup/SESNtemple.svg)](https://zenodo.org/badge/latestdoi/22593/nyusngroup/SESNtemple)

### SNIDtemplates 
This release contains all new SuperNova IDentification (SNID; [Blondin & Tonry 2007](http://arxiv.org/abs/0709.4488)) spectral templates (compared to SNID database templates-2.0) of Stripped-Envelope SN (i.e., SNe IIb, Ib, Ic and Ic-bl) presented/included in [Liu & Modjaz 2014](http://adsabs.harvard.edu/abs/2014arXiv1405.1437L), [Liu et al. 2016](http://adsabs.harvard.edu/abs/2016ApJ...827...90L) and in [Modjaz et al. (2016)](http://adsabs.harvard.edu/abs/2016ApJ...832..108M), that are based on both CfA Data (initially released in Liu & Modjaz 2014) and the rest of literature data (included in Liu et al. 2016 for IIb and Ib, Modjaz et al. 2016 for Ic and Ic-bl). We also now include SNID templates of Superluminous SNe Ic (SLSNe Ic) produced in [Liu, Modjaz & Bianco (2017)](http://adsabs.harvard.edu/abs/2016arXiv161207321L), based on literature data. NOTE: if you want to include the SLSNe Ic in your SNID template library, you also need to modify the required SNID file so this new type of SLSN Ic is recognized (see SNID documentation on how to add new types). We have also now added SNID templates of young Type Ic and young Type Ib presented in [Williamson et al. (2023)](http://ui.adsabs.harvard.edu/abs/2023ApJ...944L..49W), [Yesmin et al. (2024)](https://ui.adsabs.harvard.edu/abs/2024arXiv240904522Y/abstract) respectively.

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

There are 4 subdirectories with that include the .lnw files for the SNID templates: 
- **/templates_adjusted**: These include SNe that had been included in Blondin's SNID library release (ie "templates-2.0") but for which we either added additional spectra, changed the SN type or the date of max
- **/templates_new**: These include SNe that had not been released in Blondin's SNID library release (ie "templates-2.0"), and thus are "new". The subdirectory SLSNIc_SNIDtemplates contains the SNID templates of SLSNe Ic from Liu, Modjaz & Bianco 2017.
-  **/templates_williamson**: This subdirectory SNID templates (.lnw files) of Young Ic.
-  **/templates_youngIb/templates_yesmin**: This subdirectory includes SNID templates of young SNe Ib with at least three premaximum spectra. Details about this template set is available on SNIDtemplates/templates_youngIb/README.md.

NOTES: 
- we included 2 new SN types:

    -"Ibn", of which we include 3 SNe (00er,02ao, 06jc)
    
    -"Ic-SL", of which we include 32 SNe (from Liu, Modjaz & Bianco 2017). Note that since the continuum-removed spectra of SLSNe Ic are similar to those of SN Ic-bl (as shown in Liu, Modjaz & Bianco 2017), including SLSNe templates may lead to dual IDs of one object as both Ic-bl and SLSN Ic.
- For comparison: there were 465 spectra of 36 SESNe in Blondin's release (templates-2.0). **In this release**, there are at total 631 spectral templates of 51 SNe Ib and its subtypes (including 1 SN that was already in templates-2.0), 429 of 45 SNe Ic and its Ic and Ic-bl subtypes (including 2 SNe that were already in templates-2.0), and 178 spectra of 32 SLSNe Ic.

### Acknowledgement:

If you use data products in this repository, please <b>acknowledge</b> this work by including in your paper:

	This work made use of the data products generated by the Modjaz METAL group (formerly NYU SN group), and 
	released under DOI:10.5281/zenodo.58766, 
	available at \url{https://github.com/metal-sn/SESNtemple/}.
	  
*and* <b>cite</b> the appropriate reference(s):

Liu & Modjaz (2014):

  	@ARTICLE{2014arXiv1405.1437L,
    	author = {{Liu}, Y. and {Modjaz}, M.},
     	title = "{SuperNova IDentification spectral templates of 70 stripped-envelope core-collapse supernovae}",
   	journal = {ArXiv e-prints},
  	archivePrefix = "arXiv",
     	eprint = {1405.1437},
   	primaryClass = "astro-ph.SR",
   	keywords = {Astrophysics - Solar and Stellar Astrophysics, Astrophysics - High Energy Astrophysical Phenomena},
       	year = 2014,
     	month = may,
    	adsurl = {http://adsabs.harvard.edu/abs/2014arXiv1405.1437L},
	  adsnote = {Provided by the SAO/NASA Astrophysics Data System}
  	}

Liu et al. (2016):

    @ARTICLE{2016ApJ...827...90L,
   	author = {{Liu}, Y.-Q. and {Modjaz}, M. and {Bianco}, F.~B. and {Graur}, O.
	},
    	title = "{Analyzing the Largest Spectroscopic Data Set of Stripped Supernovae to Improve Their Identifications and Constrain Their Progenitors}",
  	journal = {\apj},
	archivePrefix = "arXiv",
   	eprint = {1510.08049},
 	primaryClass = "astro-ph.HE",
 	keywords = {methods: data analysis, supernovae: general, supernovae: individual: SNe 1993J, 2005bf, 2005E, 2011dh},
     	year = 2016,
    	month = aug,
   	volume = 827,
      	eid = {90},
    	pages = {90},
      	doi = {10.3847/0004-637X/827/2/90},
   	adsurl = {http://adsabs.harvard.edu/abs/2016ApJ...827...90L},
  	adsnote = {Provided by the SAO/NASA Astrophysics Data System}
	}

Modjaz et al. (2016):
  
    @ARTICLE{2016ApJ...832..108M,
   	author = {{Modjaz}, M. and {Liu}, Y.~Q. and {Bianco}, F.~B. and {Graur}, O.
	},
    	title = "{The Spectral SN-GRB Connection: Systematic Spectral Comparisons between Type Ic Supernovae and Broad-lined Type Ic Supernovae with and without Gamma-Ray Bursts}",
 	journal = {\apj},
	archivePrefix = "arXiv",
	eprint = {1509.07124},
	primaryClass = "astro-ph.HE",
	keywords = {gamma-ray burst: general, gamma-ray burst: individual: GRB-980425, GRB-030329, GRB-060218, GRB-100316D, GRB-120422A, GRB-	130427A, GRB-130702A, GRB-130215A, supernovae: general, supernovae: individual: SN-1994I, SN-2004aw, SN-2007gr, SN-1998bw, SN-2003dh, SN-2006aj, SN-2009bb, SN-2010bh, SN-2012ap, SN-2012bz, SN-2013cq, SN-2013dx, SN-2013ez },
     	year = 2016,
    	month = dec,
   	volume = 832,
      	eid = {108},
    	pages = {108},
      	doi = {10.3847/0004-637X/832/2/108},
  	adsurl = {http://adsabs.harvard.edu/abs/2016ApJ...832..108M},
 	adsnote = {Provided by the SAO/NASA Astrophysics Data System}
	}


Liu, Modjaz & Bianco (2017):

    @ARTICLE{2017ApJ...845...85L,
    author = {{Liu}, Y.-Q. and {Modjaz}, M. and {Bianco}, F.~B.},
    title = "{Analyzing the Largest Spectroscopic Data Set of Hydrogen-poor Super-luminous Supernovae}",
	journal = {\apj},
	archivePrefix = "arXiv",
	eprint = {1612.07321},
	primaryClass = "astro-ph.HE",
	keywords = {methods: data analysis, supernovae: general, supernovae: individual: ASASSN-15lh, SN 2011kl, SN 2007bi},
	year = 2017,
	month = aug,
	volume = 845,
	eid = {85},
	pages = {85},
	doi = {10.3847/1538-4357/aa7f74},
	adsurl = {http://adsabs.harvard.edu/abs/2017ApJ...845...85L},
	adsnote = {Provided by the SAO/NASA Astrophysics Data System}
	}


 Williamson, Modjaz & Bianco (2019):

     @ARTICLE{2019ApJ...880L..22W,
         author = {{Williamson}, Marc and {Modjaz}, Maryam and {Bianco}, Federica B.},
         title = "{Optimal Classification and Outlier Detection for Stripped-envelope Core-collapse Supernovae}",
         journal = {\apjl},
         keywords = {methods: data analysis, supernovae: general, Astrophysics - Solar and Stellar Astrophysics, Astrophysics - High Energy Astrophysical Phenomena},
         year = 2019,
         month = aug,
         volume = {880},
         number = {2},
         eid = {L22},
         pages = {L22},
         doi = {10.3847/2041-8213/ab2edb},
         archivePrefix = {arXiv},
         eprint = {1903.06815},
         primaryClass = {astro-ph.SR},
         adsurl = {https://ui.adsabs.harvard.edu/abs/2019ApJ...880L..22W},
         adsnote = {Provided by the SAO/NASA Astrophysics Data System}
         }


Williamson et al. (2023):

    @ARTICLE{2023ApJ...944L..49W,
        author = {{Williamson}, Marc and {Vogl}, Christian and {Modjaz}, Maryam and {Kerzendorf}, Wolfgang and {Singhal}, Jaladh and {Boland}, Teresa and {Burke}, Jamison and {Chen}, Zhihao and {Hiramatsu}, Daichi and {Galbany}, Llu{\'\i}s and {Gonzalez}, Estefania Padilla and {Howell}, D. Andrew and {Jha}, Saurabh W. and {Kwok}, Lindsey A. and {McCully}, Curtis and {Newsome}, Megan and {Pellegrino}, Craig and {Rho}, Jeonghee and {Terreran}, Giacomo and {Wang}, Xiaofeng},
        title = "{SN 2019ewu: A Peculiar Supernova with Early Strong Carbon and Weak Oxygen Features from a New Sample of Young SN Ic Spectra}",
        journal = {\apjl},
        keywords = {Type Ic supernovae, Core-collapse supernovae, Radiative transfer simulations, Spectroscopy, Optical astronomy, 1730, 304, 1967, 1558, 1776, Astrophysics - High Energy Astrophysical Phenomena, Astrophysics - Solar and Stellar Astrophysics},
        year = 2023,
        month = feb,
        volume = {944},
        number = {2},
        eid = {L49},
        pages = {L49},
        doi = {10.3847/2041-8213/acb549},
        archivePrefix = {arXiv},
        eprint = {2211.04482},
        primaryClass = {astro-ph.HE},
        adsurl = {https://ui.adsabs.harvard.edu/abs/2023ApJ...944L..49W},
        adsnote = {Provided by the SAO/NASA Astrophysics Data System}
	}

Yesmin et al. (2024):

	@ARTICLE{2024arXiv240904522Y,
	       author = {{Yesmin}, N. and {Pellegrino}, C. and {Modjaz}, M. and {Baer-Way}, R. and {Howell}, D.~A. and {Arcavi}, I. and {Farah}, J. and {Hiramatsu}, D. and {Hosseinzadeh}, G. and {McCully}, C. and {Newsome}, M. and {Padilla Gonzalez}, E. and {Terreran}, G. and {Jha}, S.},
	        title = "{Spectral Dataset of Young Type Ib Supernovae and their Time-evolution}",
	      journal = {arXiv e-prints},
	     keywords = {Astrophysics - High Energy Astrophysical Phenomena, Astrophysics - Solar and Stellar Astrophysics},
	         year = 2024,
	        month = sep,
	          eid = {arXiv:2409.04522},
	        pages = {arXiv:2409.04522},
	          doi = {10.48550/arXiv.2409.04522},
	archivePrefix = {arXiv},
	       eprint = {2409.04522},
	 primaryClass = {astro-ph.HE},
	       adsurl = {https://ui.adsabs.harvard.edu/abs/2024arXiv240904522Y},
	      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
	}

