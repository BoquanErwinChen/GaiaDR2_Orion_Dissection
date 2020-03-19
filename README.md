# Gaia DR2 Orion Dissection
Jupyter notebook for dissecting the Orion Star Forming Complex in Gaia data

Data are obtained from http://gaia.ari.uni-heidelberg.de/tap.html by running the following code

```
SELECT ra,  ra_error,  dec,  dec_error,  source_id,  parallax,  parallax_error,
pmra,  pmra_error,  pmdec,  pmdec_error,  dec_parallax_corr, dec_pmdec_corr, dec_pmra_corr, parallax_pmdec_corr, parallax_pmra_corr, pmra_pmdec_corr, ra_dec_corr,  
ra_parallax_corr, ra_pmra_corr, ra_pmdec_corr,
duplicated_source,  phot_g_mean_flux,  phot_g_mean_flux_error,  phot_g_mean_mag,  phot_bp_mean_flux,  phot_bp_mean_flux_error,  phot_bp_mean_mag,  phot_rp_mean_flux,  phot_rp_mean_flux_error,  phot_rp_mean_mag,  
bp_rp,  radial_velocity,  radial_velocity_error,  teff_val,  a_g_val,  e_bp_min_rp_val,  radius_val, lum_val, ruwe
FROM gaiadr2.gaia_source
WHERE ra between 75 and 90
AND dec between -15 and 15
AND parallax between 2 and 5
AND pmra between -4 and 4
AND pmdec between -4 and 4
AND parallax_over_error > 5
AND ruwe < 1.4
```
