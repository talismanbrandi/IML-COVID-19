##  Definitions of variables

__Census Data__
- _Population Density_: The population density data taken from 2019.
- _Non-White_: The fraction of non-white population in any county including Hispanics and Latinos.
- _Income_: The income per capita as defined by the US Census Bureau.
- _Poverty_: The fraction of the population deemed as being below the poverty line.
- _Unemployment_: The unemployment rate as defined by the US Census Bureau (fraction of population).
- _Uninsured_: The fraction of the population that does not have health insurance.
- _Employed_: The fraction of the population that is employed.
- _Labour_: The fraction of the population working in construction, service, delivery or production.
- _Transit_: The fraction of the population who take the public transportation system or carpool excluding those who drive or work from home.
- _Mean Commute_: The mean commute distance for a person livng in a county in minutes.
- _Senior Citizen_: The fraction of the population that is above 65 years of age. 
- _Gini Index_: Gini Index of income inequality

_sources_
```
# APIs from the US Census Bureau
census_key = ## The key from https://www.census.gov/data/developers.html "Request a key".
population_density_url = 'https://api.census.gov/data/2019/pep/population?get=DENSITY&in=state:*&for=county:*&key={}'.format(census_key)
above_65_url = 'https://api.census.gov/data/2019/acs/acs5/subject?get=GEO_ID,NAME,S0101_C02_030E&in=state:*&for=county:*&key={}'.format(census_key)
transport_url = 'https://api.census.gov/data/2019/acs/acs5?get=GEO_ID,NAME,B08006_001E,B08006_003E,B08006_017E&in=state:*&for=county:*&key={}'.format(census_key)
race_url = 'https://api.census.gov/data/2019/acs/acs5/profile?get=GEO_ID,NAME,DP05_0070E,DP05_0077E&in=state:*&for=county:*&key={}'.format(census_key)
poverty_url = 'https://api.census.gov/data/2019/acs/acs5/subject?get=GEO_ID,NAME,S1701_C03_001E&in=state:*&for=county:*&key={}'.format(census_key)
income_url = 'https://api.census.gov/data/2019/acs/acs5/subject?get=GEO_ID,NAME,S1902_C03_019E&in=state:*&for=county:*&key={}'.format(census_key)
employed_url = 'https://api.census.gov/data/2019/acs/acs5/subject?get=GEO_ID,NAME,S2301_C03_001E&in=state:*&for=county:*&key={}'.format(census_key)
unemployment_url = 'https://api.census.gov/data/2019/acs/acs5/subject?get=GEO_ID,NAME,S2301_C04_001E&in=state:*&for=county:*&key={}'.format(census_key)
mean_commute_url = 'https://api.census.gov/data/2019/acs/acs5/subject?get=GEO_ID,NAME,S0801_C01_046E&in=state:*&for=county:*&key={}'.format(census_key)
labour_url = 'https://api.census.gov/data/2019/acs/acs5/profile?get=GEO_ID,NAME,DP03_0028PE,DP03_0030PE,DP03_0031PE&in=state:*&for=county:*&key={}'.format(census_key)
insurance_url = 'https://api.census.gov/data/2019/acs/acs5/profile?get=GEO_ID,NAME,DP03_0099PE&in=state:*&for=county:*&key={}'.format(census_key)
gini_url = 'https://api.census.gov/data/2019/acs/acs5?get=GEO_ID,NAME,B19083_001E&in=state:*&for=county:*&key={}'.format(census_key)
```  

__Concentration of Chronic Conditions (CCC)__ (https://pubmed.ncbi.nlm.nih.gov/32233970/)
The definition of CCC is in the attached article. The numbers are on a scale of -16 -- 16 with 16 being high.

__Comorbidities__ (https://www.cdc.gov/mmwr/volumes/69/wr/mm6929a1.htm?s_cid=mm6929a1_w)
The numbers are the percentage of the population that have any of these chronic conditions: chronic obstructive pulmonary disease, emphysema, or chronic bronchitis; heart disease (angina or coronary heart disease, heart attack, or myocardial infarction); diabetes; chronic kidney disease; or obesity (body mass index ≥30 kg/m2)

__urban_code__ (https://pubmed.ncbi.nlm.nih.gov/32233970/)
This is the rural/urban classification that we are using. The deifintions are in the Results section in page 3 and Table 2 in page 4. 6_non_core and 5_micropolitan is rural, 4_small_metro and 3_mdedium_metro are mid-sized and 2_large_fringe and 1_large_central are urban.

__COVID-19 data__ (date 01-17-2021)
- _confirmed rate_: no. of confirmed cases per 100,000
- _death rate_: no. of deaths per 100,000
- _fatality rate_: no. of deaths / no. of confirmed. The no. of confirmed is from 01-07-2021. So it is adjusted by 10 days.
- _Population_: The population of the county

_source_
```
# links to the JHU GitHub
jhu_deaths = 'https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_deaths_US.csv'
jhu_confirmed = 'https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_time_series/time_series_covid19_confirmed_US.csv'
```

