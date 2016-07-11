# SESNtemple

This repository contains data products from [Liu & Modjaz (2014)](http://adsabs.harvard.edu/abs/2014arXiv1405.1437L), [Liu et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv151008049L), and [Modjaz et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv150907124M) on Stripped Envelope SNe (SESN), ie SNe of types IIb, Ib, Ic and Ic-bl. There are three different types of SN templates we produced and used in our research, which are stored in three different folders:

- <b>/AverageSpec</b> contains all average spectra and standard deviation spectra in [Liu et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv151008049L), and [Modjaz et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv150907124M). Average spectra and standard deviation spectra can be used to quantify SN diversity, determine if a new transient is a novel type of explosion, and so on. See the README file in the folder for details of average spectra.
- <b>/SNIDtemplates</b> contains all SuperNova IDentification (SNID; [Blondin & Tonry 2007](http://adsabs.harvard.edu/abs/2007ApJ...666.1024B)) templates that were released in [Liu & Modjaz (2014)](http://adsabs.harvard.edu/abs/2014arXiv1405.1437L), and used in [Liu et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv151008049L), and [Modjaz et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv150907124M). Adding these templates to the spectra library database of SNID will increase the number of SESN templates in the database, which will help SN classification via SNID. See the README file in the folder for details of SN spectra that are used to construct SNID templates.
- <b>/TempleSpec_for_Ic_conv_Icbl_MCMC</b> contains SN Ic average spectra used as templates for the code [Ic_conv_Icbl_MCMC.py](https://github.com/nyusngroup/SESNspectraLib), a Python module to measure the absorption velocity of SN Ic-bl from the Fe II 5169 spectral feature in [Modjaz et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv150907124M). See the README file in the folder <b>AverageSpec</b> for details of average spectra.

If you use data products in this repository, please <b>cite</b> related references listed above.

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

	 @ARTICLE{2015arXiv151008049L,
     	author = {{Liu}, Y.-Q. and {Modjaz}, M. and {Bianco}, F.~B. and {Graur}, O.
		  },
      	title = "{Analyzing the Largest Spectroscopic Dataset of Stripped Supernovae to Improve Their Identifications and   Constrain Their Progenitors}",
    	journal = {ArXiv e-prints},
  	archivePrefix = "arXiv",
     	eprint = {1510.08049},
  	primaryClass = "astro-ph.HE",
   	keywords = {Astrophysics - High Energy Astrophysical Phenomena, Astrophysics - Solar and Stellar Astrophysics},
	 year = 2016,
      	month = oct,
    	adsurl = {http://adsabs.harvard.edu/abs/2015arXiv151008049L},
    	adsnote = {Provided by the SAO/NASA Astrophysics Data System} 
	 }

Modjaz et al. (2016):
  
	  @ARTICLE{2015arXiv150907124M,
     	author = {{Modjaz}, M. and {Liu}, Y.~Q. and {Bianco}, F.~B. and {Graur}, O.
		  },
      	title = "{The Spectral SN-GRB Connection: Systematic Spectral Comparisons between Type Ic Supernovae, and broad-lined 	Type Ic Supernovae with and without Gamma-Ray Bursts}",
    	journal = {ArXiv e-prints},
  	archivePrefix = "arXiv",
     	eprint = {1509.07124},
  	primaryClass = "astro-ph.HE",
   	keywords = {Astrophysics - High Energy Astrophysical Phenomena, Astrophysics - Solar and Stellar Astrophysics},
       	year = 2016,
      	month = sep,
    	adsurl = {http://adsabs.harvard.edu/abs/2015arXiv150907124M},
    	adsnote = {Provided by the SAO/NASA Astrophysics Data System}
	 }
  
  
