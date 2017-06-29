[![DOI](https://zenodo.org/badge/22593/nyusngroup/SESNtemple.svg)](https://zenodo.org/badge/latestdoi/22593/nyusngroup/SESNtemple)

This directory contains all mean spectra and standard deviation spectra of Stripped-Envelope SNe (SESN) from [Liu et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv151008049L), and [Modjaz et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv150907124M), including those not shown in plots. Mean spectra and standard deviation spectra can be used to quantify SN diversity, determine if a new transient is a novel type of explosion, and so on. <b>Note</b>: In order to compare a spectrum of a transient to mean spectra, the spectrum needs to be flattened, which can be produced with snidflat.pro using the default values in snid_pro.tgz, downloadable at [Stephane Blondin's webpage](https://people.lam.fr/blondin.stephane/software/snid/index.html#Download).
Mean spectra of SNe Ic are used as SN Ic templates for our template fitting code called "Ic_conv_Icbl_MCMC.py" (https://github.com/nyusngroup/SESNspectraLib), which measures line velocities in SNe Ic-bl based on blended lines. They live under the SESNspectraLib repository, since we want the template fitting code to be self-contained, and since those mean spectra templates were constructed from SN Ic spectra using slightly different phase ranges than the ones released here.

This directory has 4 sub-directories, ordered by subtype: SN IIb, Ib, Ic and Ic-bl. In each of those subdirectories, there are 2 sub-subdirectories ordered by the spectral inclusion method (see below). 

#### Name Convention:

meanspec + <b>type</b> + <b>spectral inclusion method</b> + <b>phase</b> + <b>smoothing method</b>
- type: Ib (SN Ib), Ic (SN Ic), Icbroad (SN Ic-bl), Icbroad_nogrb (SN Ic-bl without GRB), Icbroad_withgrb (SN Ic-bl with GRB, or SN-GRB), cosmsngrb (high luminosity, cosmological SN-GRB), llsngrb (low luminosity SN-GRB)
- spectral inclusion method: presence of "1specperSN" means that only 1 spectrum per SN is included in an average spectrum for the required phase range, while absence of "1specperSN" means that all spectra of that SN within the required phase range are included in the average spectra.
- phase: in the rest-frame with respect to date of V band maximum light (includes spectra at +/- 2 days with respect to the target phase)
- smoothing method: presence of "ft" means that spectra are smoothed using FFT method from [Liu et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv151008049L) and [Modjaz et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv150907124M), while absence of "ft" means that spectra are smoothed using band-pass filter in [Blondin & Tonry 2007](http://adsabs.harvard.edu/abs/2007ApJ...666.1024B). The spectra of SNe Ic-bl and of SNe Ic (as presented in Modjaz et al. 2016) were smoothed by the FFT method.


These mean spectra were constructed using code from [Blondin & Tonry 2007](http://adsabs.harvard.edu/abs/2007ApJ...666.1024B) and from  [Liu et al. (2016)](http://adsabs.harvard.edu/abs/2015arXiv151008049L). They were constructed in 5-day intervals, starting at phase=-10 days, and going to phase=50 days, ie there are mean spectra at phases: -10, -5, 0, 5, ... etc.


#### Key Words:
- fmean: mean spectrum constructed using smoothed spectra
- fsdev: standard deviation of data
- fmed: median spectrum
- fmeanp: maximum positive excursion from mean
- fmeann: maximum negative excursion from mean
- fmedp: maximum positive excursion from median
- fmedn: maximum negative excursion from median
- wlog: rest wavelength
- nsn: number of spectra that were used to construct mean spectrum, at each wavelength bin
- smean: mean spline
- SNsave: SN names and phases of the spectra that were used to construct mean spectrum
- tmin: minimum phase
- tmax: maximum phase

#### Examples 

Plot flattened average spectra in IDL:
```
IDL> restore, 'meanspecIc_1specperSN_00.sav'
IDL> plot, wlog, fmean
IDL> oplot, wlog, fmean + fsdev
IDL> oplot, wlog, fmean - fsdev
```
Plot flattened average spectra in Python:
```
from scipy.io.idl import readsav
import pylab as pl
s = readsav('meanspecIc_1specperSN_00.sav')
pl.fill_between(s.wlog, s.fmean + s.fsdev, s.fmean - s.fsdev, color = 'k', alpha = 0.5)
pl.plot(s.wlog, s.fmean, label="flattened mean Ic phase = 0", color="DarkGreen", lw=2)
pl.ylabel(r"relative flux", fontsize = 18)
pl.xlabel(r"Rest Wavelength $\AA$", fontsize = 18)
pl.legend(fontsize = 18)
pl.savefig("AverageIcPhase0.png")
```

which will generate the following figure

![alt tag](https://raw.githubusercontent.com/nyusngroup/SESNtemple/master/MeanSpec/AverageIcPhase0.png)

Plot non-flattened average spectra in Python:
```
from scipy.io.idl import readsav
import pylab as pl
import numpy as np
s = readsav('meanspecIc_1specperSN_00.sav')
dwbin = s.wlog[1:1024]-s.wlog[0:1023] 
dwbin = np.append(dwbin[0], dwbin) # array of bin sizes
fnoflat = (s.fmean+1)*s.smean # flux per log lambda bin
fnoflat_perA = fnoflat/dwbin # flux per angstrom
pl.plot(s.wlog,fnoflat_perA, label="non-flattened mean Ic phase = 0", color="DarkGreen", lw=2)
pl.ylabel(r"relative flux", fontsize = 18)
pl.xlabel(r"Rest Wavelength $\AA$", fontsize = 18)
pl.legend(fontsize = 18)
pl.savefig("AverageIcPhase0Conti.png")
```

which will generate the following figure

![alt tag](https://raw.githubusercontent.com/nyusngroup/SESNtemple/master/MeanSpec/AverageIcPhase0Conti.png)
