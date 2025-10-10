# Urban Fluxes in Northern Eurasia (UrbanFluxesNE)

### Current structure of the files with meteorological variables:
- 'Qh', sensible heat flux [W/m2]
- 'Qtau', Momentum flux $\\tau, [kg·m^{-2}·s^{-1}$]
- 'Ustar', friction velocity [m/s]
- 'T_air', air temperature [degrees C]
- 'RH_air', relative humidity [%]
- 'P_air', atmospheric pressure [hPa]
- 'Rho_air', air density [kg/m3]
- 'Wind_U', zonal wind speed component [m/s]*
- 'Wind_V', meridional wind speed component [m/s]*
- 'Wind_W', vertical wind speed component before axis rotation [m/s]
- 'Wind_vel', wind speed [m/s]
- 'Wind_dir', wind direction [m/s]*
- 'Wind_alpha', wind attack angle before axis correction [degrees]

*for MSU site wind components needs additional rotation, will be corrected soon

### Current structure of the [metadata file](https://github.com/mvarentsov/UrbanFluxesNE/blob/main/site_data.csv):
- City & site name: `city_name`, `site_name`
- Location: `longitude`,	`latitude` [degrees]
- Shift of the local time with respect to UTC: `time_belt` [hours]
- Vertical levels of observations: `obs_levels` [m]
- Imperveous area fraction within 250, 500 and 1000 m around towers according to ESA WorldCover data [(Zanaga et al, 2021)](10.5281/zenodo.7254220): `impervious_area_fraction_R*m` [unitless]
- Urban canopy area fraction within 250, 500 and 1000 m around towers according Copernicus Global Land Cover data [(Buchhorn et al, 2020)](https://doi.org/10.3390/rs12061044): `uc_area_fraction_R*m` [unitless]
- Modal type of the local climate zone (LCZ) among urban and natural types within 250, 500 and 1000 m around towers according to global LCZ map [(Demuzere et al., 2022)](https://doi.org/10.5194/essd-14-3835-2022): `LCZ_urb_R*m`, `LCZ_rur_R*m` [categorial]

### Contributors:
- Dr. Varentsov M.I. (data collection & processing)
- Dr. Telminov A.E. (organizing observations & data processing in Tomsk)
- Dr. Kobzev A.A. (organizing observations in Tomsk)
- Drozd I.D. (organizing observations & data processing in Moscow, MSU urban site)
- Pashkin A.D. (organizing observations in Tomsk and Moscow, MSU urban site)
- Dr. Gavrikov A.V. (organizing observations in Moscow, MSU urban site)
- Artamonov A.Y. (organizing observations in Moscow, MSU surban ite)
- Dr. Liuliukin V.S. (organizing observations & data processing for Moscow region, ZNS rural site)
- Dr. Stepanenko V.M. (organizing observations in Moscow, MSU site & project supervision)
- Dr. Repina I.A. (organizing observations in Tomsk, Moscow, MSU site & project supervision)

The development of this dataset was supported by the Russian Science Foundation, project no. 24-17-00155 under supervision of [Dr. Irina Repina](https://www.researchgate.net/profile/Irina-Repina)
