# SESNtemple

This repository contains data products in [Liu & Modjaz (2014)](http://arxiv.org/abs/1405.1437), [Liu et al. (2016)](http://arxiv.org/abs/1510.08049), and [Modjaz et al. (2016)](http://arxiv.org/abs/1509.07124). There are three different types of SNe templates we produces and used in our research, which are stored in three different folders. 

- <b>AverageSpec</b> contains all average spectra and standard deviation spectra in [Liu et al. (2016)](http://arxiv.org/abs/1510.08049), and [Modjaz et al. (2016)](http://arxiv.org/abs/1509.07124). Average spectra and standard deviation spectra can be used to quantify SN diversity, determine if a new transient is a novel type of explosion, and so on. See the README file in the folder for details of average spectra.
- <b>SNIDtemplates</b> contains all SuperNova IDentification (SNID; [Blondin & Tonry 2007](http://arxiv.org/abs/0709.4488)) templates in [Liu & Modjaz (2014)](http://arxiv.org/abs/1405.1437), [Liu et al. (2016)](http://arxiv.org/abs/1510.08049), and [Modjaz et al. (2016)](http://arxiv.org/abs/1509.07124). Adding these templates to the database of SNID will increase the number of SN Ib/c templates in the database, which will help SN classification via SNID. See the README file in the folder for details of spectra that are used to construct SNID templates.
- <b>TempleSpec_for_Ic_conv_Icbl_MCMC</b> contains SN Ic average spectra (or templates) used for [Ic_conv_Icbl_MCMC.py](https://github.com/nyusngroup/SESNspectraLib), a Python module to measure the absorption velocity of SN Ic-bl from the Fe II 5169 spectral feature in [Modjaz et al. (2016)](http://arxiv.org/abs/1509.07124). See the README file in the folder <b>AverageSpec</b> for details of average spectra.

If you use data products in this repository, please <b>cite</b> related references listed above.


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


	 @ARTICLE{2015arXiv151008049L,
     	author = {{Liu}, Y.-Q. and {Modjaz}, M. and {Bianco}, F.~B. and {Graur}, O.
		  },
      	title = "{Analyzing the Largest Spectroscopic Dataset of Stripped Supernovae to Improve Their Identifications and   Constrain Their Progenitors}",
    	journal = {ArXiv e-prints},
  	archivePrefix = "arXiv",
     	eprint = {1510.08049},
  	primaryClass = "astro-ph.HE",
   	keywords = {Astrophysics - High Energy Astrophysical Phenomena, Astrophysics - Solar and Stellar Astrophysics},
	 year = 2015,
      	month = oct,
    	adsurl = {http://adsabs.harvard.edu/abs/2015arXiv151008049L},
    	adsnote = {Provided by the SAO/NASA Astrophysics Data System} 
	 }
  
	  @ARTICLE{2015arXiv150907124M,
     	author = {{Modjaz}, M. and {Liu}, Y.~Q. and {Bianco}, F.~B. and {Graur}, O.
		  },
      	title = "{The Spectral SN-GRB Connection: Systematic Spectral Comparisons between Type Ic Supernovae, and broad-lined 	Type Ic Supernovae with and without Gamma-Ray Bursts}",
    	journal = {ArXiv e-prints},
  	archivePrefix = "arXiv",
     	eprint = {1509.07124},
  	primaryClass = "astro-ph.HE",
   	keywords = {Astrophysics - High Energy Astrophysical Phenomena, Astrophysics - Solar and Stellar Astrophysics},
       	year = 2015,
      	month = sep,
    	adsurl = {http://adsabs.harvard.edu/abs/2015arXiv150907124M},
    	adsnote = {Provided by the SAO/NASA Astrophysics Data System}
	 }
  
  
