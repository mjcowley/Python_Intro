# Data Files

Real survey data used in the training notebooks. The notebooks download these automatically, so you don't need to fetch them yourself.

| File | Format | Contents | Used in |
|------|--------|----------|---------|
| `zfourge_cdfs.csv` | CSV | ZFOURGE CDFS photometric catalogue: positions, FourStar $K_s$ flux, flags and spectroscopic redshifts (30,911 objects) | Parts 3, 4 |
| `zfourge_cdfs_eazy.fits` | FITS binary table | EAZY photometric redshifts and rest-frame U, V and J fluxes for the same objects | Parts 3, 4 |
| `zfourge_cdfs.fout` | Whitespace-delimited text | FAST stellar population fits (stellar mass, star formation rate, age, dust) for the same objects | Parts 3, 4 |
| `gaia_dr3_cdfs.csv` | CSV | Gaia DR3 sources within 12 arcmin of the CDFS centre (440 sources) | Parts 3, 4 |
| `legacy_cdfs_r.fits` | FITS image | 700 × 700 pixel (3 × 3 arcmin) r-band cutout of CDFS at 0.262 arcsec per pixel, in nanomaggies | Parts 3, 4 |
| `swire_s0_template.sed` | Whitespace-delimited text | SWIRE S0 (lenticular) galaxy template: wavelength in Å and normalised $F_\lambda$, from 0.1 µm to 5 mm | Part 4 |
| `pantheon_plus.csv` | CSV | Pantheon+ type Ia supernovae: redshift, distance modulus (SH0ES calibration) and its diagonal uncertainty, calibrator flag and host mass (1,701 light curves of 1,543 supernovae) | Part 5 |

## Notes

- **Missing values** are `-99` in the ZFOURGE files, as in the original ZFOURGE release. In the Gaia file they're blank.
- **ZFOURGE fluxes** (`f_Ks`, `e_Ks`) are on an AB zero point of 25, so $m_\mathrm{AB} = 25 - 2.5\log_{10}(f)$, and one flux unit is 0.3631 µJy. Only ratios of the rest-frame fluxes are used, so their units cancel.
- **Pantheon+** distance moduli `mu` use the SH0ES Cepheid calibration, so they imply $H_0 \approx 73$ km/s/Mpc. Some supernovae were observed by more than one survey and appear more than once. The full release, including the covariance matrix, is on [GitHub](https://github.com/PantheonPlusSH0ES/DataRelease).
- The ZFOURGE files contain a selection of columns from the full catalogues. Download everything from [VizieR](https://vizier.cds.unistra.fr/viz-bin/VizieR?-source=J/ApJ/830/51) or the [ZFOURGE website](https://zfourge.tamu.edu/).

## Sources and Acknowledgements

If you use these data in your own work, cite the original sources:

- **ZFOURGE**: Straatman, C. M. S., et al. 2016, ApJ, 830, 51 ([ADS](https://ui.adsabs.harvard.edu/abs/2016ApJ...830...51S)), retrieved from VizieR catalogue J/ApJ/830/51.
- **Gaia DR3**: Gaia Collaboration, Vallenari, A., et al. 2023, A&A, 674, A1 ([ADS](https://ui.adsabs.harvard.edu/abs/2023A%26A...674A...1G)), retrieved from VizieR catalogue I/355/gaiadr3.
- **Pantheon+**: Scolnic, D., et al. 2022, ApJ, 938, 113 ([ADS](https://ui.adsabs.harvard.edu/abs/2022ApJ...938..113S)) and Brout, D., et al. 2022, ApJ, 938, 110 ([ADS](https://ui.adsabs.harvard.edu/abs/2022ApJ...938..110B)), from the [Pantheon+ data release](https://github.com/PantheonPlusSH0ES/DataRelease).
- **SWIRE templates**: Polletta, M., et al. 2007, ApJ, 663, 81 ([ADS](https://ui.adsabs.harvard.edu/abs/2007ApJ...663...81P)), from the [SWIRE Template Library](http://www.iasf-milano.inaf.it/~polletta/templates/swire_templates.html).
- **DESI Legacy Imaging Surveys**: Dey, A., et al. 2019, AJ, 157, 168 ([ADS](https://ui.adsabs.harvard.edu/abs/2019AJ....157..168D)). Cutout from DR10 via the [Legacy Survey viewer](https://www.legacysurvey.org/viewer).
