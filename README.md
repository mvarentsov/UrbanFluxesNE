# Urban Fluxes in Northern Eurasia (UrbanFluxesNE)

> [!CAUTION]
> **The dataset has moved to Zenodo. It will be made publicly available once the dataset is finalized and the accompanying article is published.**
>
> **Until then, please request access from the corresponding author, [Mikhail Varentsov](mailto:mikhail.varentsov@srcc.msu.ru).**

### Sites

| City | Site | Latitude | Longitude | Reference heights (m) | Observations | Site parameters | Map |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Moscow | MSU-MO | 55.707187 | 37.522814 | 2, 11, 19 | [L1](Moscow/timeseries/L1/) | [CSV](Moscow/site_data/RU-Moscow-MSU-MO/RU-Moscow-MSU-MO_sitedata.csv) | [PNG](Moscow/site_data/RU-Moscow-MSU-MO/RU-Moscow-MSU-MO_buffers_en.png) |
| Moscow | IAP-Zvenigorod | 55.696111 | 36.775278 | 10, 56 | [L1](Moscow/timeseries/L1/) | [CSV](Moscow/site_data/RU-Moscow-IAP-Zvenigorod/RU-Moscow-IAP-Zvenigorod_sitedata.csv) | [PNG](Moscow/site_data/RU-Moscow-IAP-Zvenigorod/RU-Moscow-IAP-Zvenigorod_buffers_en.png) |
| Moscow | LOD | 55.818050 | 37.556350 | 31 | - | - | - |
| Tomsk | TFN-IMCES | 56.474956 | 85.054185 | 30, 40 | [L1](Tomsk/timeseries/L1/) | [CSV](Tomsk/site_data/RU-Tomsk-TFN-IMCES/RU-Tomsk-TFN-IMCES_sitedata.csv) | [PNG](Tomsk/site_data/RU-Tomsk-TFN-IMCES/RU-Tomsk-TFN-IMCES_buffers_en.png) |
| Tomsk | TFN-Oblkom | 56.467183 | 84.957451 | 23, 30 | [L1](Tomsk/timeseries/L1/) | [CSV](Tomsk/site_data/RU-Tomsk-TFN-Oblkom/RU-Tomsk-TFN-Oblkom_sitedata.csv) | [PNG](Tomsk/site_data/RU-Tomsk-TFN-Oblkom/RU-Tomsk-TFN-Oblkom_buffers_en.png) |
| Tomsk | TFN-BEK | 56.480872 | 85.101526 | 30 | [L1](Tomsk/timeseries/L1/) | [CSV](Tomsk/site_data/RU-Tomsk-TFN-BEK/RU-Tomsk-TFN-BEK_sitedata.csv) | [PNG](Tomsk/site_data/RU-Tomsk-TFN-BEK/RU-Tomsk-TFN-BEK_buffers_en.png) |
| Tomsk | TFN-Voronino | 56.557778 | 85.256111 | 10 | [L1](Tomsk/timeseries/L1/) | [CSV](Tomsk/site_data/RU-Tomsk-TFN-Voronino/RU-Tomsk-TFN-Voronino_sitedata.csv) | [PNG](Tomsk/site_data/RU-Tomsk-TFN-Voronino/RU-Tomsk-TFN-Voronino_buffers_en.png) |
| Beijing | IAP-Beijing | 39.974304 | 116.371285 | 8, 16, 47, 80, 140, 200, 280 | [L1](Beijing/timeseries/L1/) | [CSV](Beijing/site_data/CN-Beijing-IAP-Beijing/CN-Beijing-IAP-Beijing_sitedata.csv) | [PNG](Beijing/site_data/CN-Beijing-IAP-Beijing/CN-Beijing-IAP-Beijing_buffers_en.png) |
| Beijing | IAP-Xianghe | 39.753441 | 116.960451 | 32, 80 | [L1](Beijing/timeseries/L1/) | [CSV](Beijing/site_data/CN-Beijing-IAP-Xianghe/CN-Beijing-IAP-Xianghe_sitedata.csv) | [PNG](Beijing/site_data/CN-Beijing-IAP-Xianghe/CN-Beijing-IAP-Xianghe_buffers_en.png) |

### Level 1 observation files

The `Beijing/timeseries/L1`, `Moscow/timeseries/L1` and `Tomsk/timeseries/L1` directories contain one CSV per observation type, site and height for the full available period. Tower files are named `Site-XXm_fluxes.csv`, `Site-XXm_meteo.csv` or `Site-XXm_radiation.csv`. The standalone AMIIS files are `TFN-IMCES-meteo.csv` and `TFN-IMCES-radiation.csv`.

`datetime_utc` gives the observation timestamp in UTC. The flux timestamps define the time grid. Meteorological data are placed on exact matching timestamps. Each radiation value is the mean over the preceding grid interval, including the timestamp at the end and excluding the one at the start. Radiation files contain the available shortwave and longwave components `SWdown`, `SWup`, `LWdown` and `LWup`. Empty cells represent missing values. Available columns vary by site, height and observation type.

### Variables

| Column | Description | Unit |
| --- | --- | --- |
| `Qh` | Sensible heat flux | W/m² |
| `Qle` | Latent heat flux | W/m² |
| `Qtau` | Momentum flux (shear stress) | N/m² |
| `Qco2` | Carbon dioxide flux | µmol/(m² s) |
| `Ustar` | Friction velocity | m/s |
| `Cd` | Drag coefficient, calculated as `(Ustar/Wind)²` | 1 |
| `Tair` | Air temperature | K |
| `RHair` | Relative humidity | % |
| `Pair` | Atmospheric pressure at sensor height | Pa |
| `RHOair` | Air density | kg/m³ |
| `Wind` | Wind speed | m/s |
| `Wind_U`, `Wind_V` | Eastward and northward wind components | m/s |
| `Wind_W` | Mean vertical wind component | m/s |
| `Wind_U_rot`, `Wind_V_rot`, `Wind_W_rot` | Mean wind components in the rotated processing frame | m/s |
| `Wind_U_rot_std`, `Wind_V_rot_std`, `Wind_W_rot_std` | Standard deviations of wind components in the rotated processing frame | m/s |
| `Wind_dir` | Wind direction | degrees |
| `Wind_alpha` | Wind attack angle | degrees |
| `Wind_nw`, `Wind_se` | Wind speeds from the northwest and southeast sensors at IAP-Beijing | m/s |
| `Wind_ne`, `Wind_sw` | Wind speeds from the northeast and southwest sensors at IAP-Xianghe | m/s |
| `SWdown`, `SWup` | Downward and upward shortwave radiation | W/m² |
| `LWdown`, `LWup` | Downward and upward longwave radiation | W/m² |

The IAP-Xianghe meteorological files preserve the wind direction values supplied by the instrument data. Their angular scale differs from the co-located flux series.

### Flux quality flags

| Column | Checks included |
| --- | --- |
| `qc_tot` | Physical range and outlier checks on available flux variables and `Cd` |
| `qc_tot_noCd` | Physical range and outlier checks on available flux variables |
| `qc_tot_ext` | `qc_tot` with rejected periods extended using a centered one-hour window |
| `qc_tot_noCd_ext` | `qc_tot_noCd` with rejected periods extended using a centered one-hour window |

A flag of `0` indicates rejection. A flag of `1` indicates that the applicable checks raised no rejection. Missing values by themselves receive `1`. The CSVs retain the observed values and the corresponding flags.

### Site reference

The site inventory gives `city_name`, `site_name`, `longitude` and `latitude` in degrees, `time_belt` as the local offset from UTC in hours, and reference observation heights `obs_levels` in metres. The L1 filenames identify the available heights for each observation type. `TFN-IMCESmezo` belongs to the `TFN-IMCES` site. [Site reference table](site_data_basic.csv)

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
- Dr. Irina Repina (organizing observations in Tomsk, Moscow, MSU site & project supervision)
- Dr. Zhou Libo (organizing observations and data curation for Beijing sites)

Source codes used for data processing are availible in [pyUrbanFluxes repository](https://github.com/mvarentsov/pyUrbanFluxes).

The development of this dataset was supported by the Russian Science Foundation, project no. 24-17-00155 under supervision of [Dr. Irina Repina](https://www.researchgate.net/profile/Irina-Repina)
