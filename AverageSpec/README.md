The average spectra are constructed using code in [Blondin & Tonry 2007](http://arxiv.org/abs/0709.4488). 

Name Convention:

meanspec + <b>type</b> + spectra inclusion method + phase + smooth method
- type: Ib (SN Ib), Ic (SN Ic), Icbroad (SN Ic-bl), Icbroad_nogrb (SN Ic-bl without GRB), Icbroad_withgrb (SN Ic-bl with GRB, or SN-GRB), cosmsngrb (high luminosity SN-GRB), llsngrb (low luminosity SN-GRB)
- spectra inclusion method: presence of "1specperSN" means that only 1 spectrum per SN is included in an average spectrum, while absence of "1specperSN" means that all spectra within the required phase range are included in the average spectra.
- phase: with respect to date of V band maximum light
- smooth method: presence of "ft" means that spectra are smoothed using FFT method in [Liu et al. (2016)](http://arxiv.org/abs/1510.08049) and [Modjaz et al. (2016)](http://arxiv.org/abs/1509.07124), while absence of "ft" means that spectra are smoothed using band-pass filter in [Blondin & Tonry 2007](http://arxiv.org/abs/0709.4488).

Key Words:
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

Example in IDL:
```
IDl> restore, 'meanspecIcbroad_1specperSN_0_ft.sav'
IDL> plot, wlog, fmean
IDL> oplot, wlog, fmean + fsdev
IDL> oplot, wlog, fmean - fsdev
```

