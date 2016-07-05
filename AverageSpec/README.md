The average spectra are constructed using code in [Blondin & Tonry 2007](http://arxiv.org/abs/0709.4488). 

#### Name Convention:

meanspec + <b>type</b> + <b>spectra inclusion method</b> + <b>phase</b> + <b>smooth method</b>
- type: Ib (SN Ib), Ic (SN Ic), Icbroad (SN Ic-bl), Icbroad_nogrb (SN Ic-bl without GRB), Icbroad_withgrb (SN Ic-bl with GRB, or SN-GRB), cosmsngrb (high luminosity SN-GRB), llsngrb (low luminosity SN-GRB)
- spectra inclusion method: presence of "1specperSN" means that only 1 spectrum per SN is included in an average spectrum, while absence of "1specperSN" means that all spectra within the required phase range are included in the average spectra.
- phase: in the rest-fram with respect to date of V band maximum light
- smooth method: presence of "ft" means that spectra are smoothed using FFT method in [Liu et al. (2016)](http://arxiv.org/abs/1510.08049) and [Modjaz et al. (2016)](http://arxiv.org/abs/1509.07124), while absence of "ft" means that spectra are smoothed using band-pass filter in [Blondin & Tonry 2007](http://arxiv.org/abs/0709.4488).

#### Key Words:
- fmean: mean spectrum constructed using smoothed spectra
- fsdev: standard deviation of data
- fmed: median spectrum
- fmeanp: maximum positive excursion from mean
- fmeann: maximum negative excursion from mean
- fmedp: maximum positive excursion from median
- fmedn: maximum negative excursion from median
- wlog: wavelength
- nsn: number of spectra at each wavelength bin
- smean: mean spline
- SNsave: information of SN names and phases that go into the mean spectra
- tmin: minimum phase
- tmax: maximum phase

#### Examples 

In IDL:
```
IDL> restore, 'meanspecIc_1specperSN_0.sav'
IDL> plot, wlog, fmean
IDL> oplot, wlog, fmean + fsdev
IDL> oplot, wlog, fmean - fsdev
```
In Python:
```
from scipy.io.idl import readsav
import pylab as pl
s = readsav('meanspecIc_1specperSN_0.sav')
pl.fill_between(s.wlog, s.fmean + s.fsdev, s.fmean - s.fsdev, color = 'k', alpha = 0.5)
pl.plot(s.wlog, s.fmean, label="mean Ic phase = 0", color="DarkGreen", lw=2)
pl.ylabel(r"relative flux", fontsize = 18)
pl.xlabel(r"Rest Wavelength $\AA$", fontsize = 18)
pl.legend(fontsize = 18)
pl.savefig("AverageIcPhase0.png")
```

which will generate the following figure

![alt tag](https://raw.githubusercontent.com/nyusngroup/SESNtemple/master/AverageSpec/AverageIcPhase0.png)