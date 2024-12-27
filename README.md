# Urban Fluxes in Northern Eurasia (UrbanFluxesNE)


### Structure of the files with meteorological variables:

### Current structure of the metadata file (sitedata.csv)
- City & site name: `city_name`, `site_name`
- Location: `longitude`,	`latitude` [degrees]
- Shift of the local time with respect to UTC: `time_belt` [hours]
- Vertical levels of observations: `obs_levels` [m]
- Imperveous area fraction within 250, 500 and 1000 m around towers according to ESA WorldCover data [(Zanaga et al, 2021)](10.5281/zenodo.7254220): `impervious_area_fraction_R*m` [unitless]
- Urban canopy area fraction within 250, 500 and 1000 m around towers according Copernicus Global Land Cover data [(Buchhorn et al, 2020)](https://doi.org/10.3390/rs12061044): `uc_area_fraction_R*m` [unitless]
- Modal type of the local climate zone (LCZ) among urban and natural types within 250, 500 and 1000 m around towers according to global LCZ map [(Demuzere et al., 2022)](https://doi.org/10.5194/essd-14-3835-2022): `LCZ_urb_R*m`, `LCZ_rur_R*m` [categorial]

### Contributors:
- Dr. Varentsov M.I. (data collection & processing)
- Dr. Telminov A.E. (organizing observations in Tomsk)
- Dr. Kobzev A.A. (organizing observations in Tomsk)
- Drozd I.D. (organizing observations in Moscow, MSU site)
- Pashkin A.D. (organizing observations in Tomsk and Moscow, MSU site)
- Dr. Gavrikov A.V. (organizing observations in Moscow, MSU site)
- Artamonov A.Y. (organizing observations in Moscow, MSU site)
- Dr. Stepanenko V.M. (organizing observations in Moscow, MSU site & project supervision)
- Dr. Repina I.A. (organizing observations in Tomsk, Moscow, MSU site & project supervision)

The development of this dataset was supported by the Russian Science Foundation, project no. 24-17-00155 under supervision of [Dr. Irina Repina](https://www.researchgate.net/profile/Irina-Repina)
