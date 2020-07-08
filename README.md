# Health Intevention Tracking for COVID-19 (HIT-COVID) Data

The Health Intervention Tracking for COVID-19 (HIT-COVID) project tracks the implementation and relaxation of public health actions taken by governments to slow transmission of SARS-COV-2 globally. Hundreds of volunteer data contributors were trained, provided with standardized field definitions and access to an online forum for asking questions and sharing ideas. Each change in policy and corresponding date is documented at the first-level administrative unit (e.g., states, districts) and nationally for all countries with more detailed geographic resolution in some locations (e.g., counties in the US). Data are entered into a structured questionnaire with a source document(s) required for each record. Source documents from official government sources are prioritized, but other sources are permitted. For each intervention, HIT-COVID captures a suite of additional data including whether interventions are required or recommended and the particular subpopulation to which policies apply. To ensure data quality, contributors are asked to complete weekly self-audit reports, have the ability to submit corrections on past entries, and the management team performs geographic or intervention-specific audits as issues arise. 

This is the public repository for data and documentation from the [HIT-COVID project](https://akuko.io/post/covid-intervention-tracking). Code book and data are available here and more details can be found on the [website](https://akuko.io/post/covid-intervention-tracking). 


## Data  

### The Data Collection Process
We have developed our processes of data collection and entry to try to ensure high quality and reproducibility (e.g., through having source documents uploaded for all data points). Here is a brief overview of the process:

- Contributors assigned to admin1 unit(s)
- Contributors asked to construct historic timeline of policy changes starting from 1-Jan-2020
- Historical data entry through RedCap system
- Contributors asked to update policy changes weekly
- Weekly data audit reports generated and sent to contributors for verification
- Regular reviews of data by HIT-COVID management team

### Key Data Fields 

There are two main data files in our database, `hit-covid-longdata.csv` and `hit-covid-completeness.csv`. The primary data file, `hit-covid-longdata.csv` contains all intervention data logged (in long form) with `hit-covid-completeness.csv` providing an overview of the completeness of logged interventions for different PHSM domains and geographic areas. 

#### `hit-covid-longdata.csv`

- unique_id: unique id for the row combining the record_id and the intervention
- record_id: unique id of the REDCap record (note that a single record is generated each time a set of data are entered so these can be shared across interventions)
- entry_time: time and date when data were entered by the contributor
- national entry: flag for whether this is a national-level policy
- country: ISO 3166-1 alpha-3 country code  
- country_name: country name
- admin1: first administrative unit code (following GADM5 unless otherwise noted)
- admin1_name: level 1 administrative unit name
- locality: specified geographic areas below level 1
- usa_county: name of county for USA county-level data
- usa_county_code: FIPS code of the USA county
- intervention_group: code that groups interventions by type
- intervention: name of the specific intervention
- date_of_update: date of updated status to policy implementation for a particular intervention
- status: updated status of intervention policy
- status_simp: simplified updated status of policy (partially implemented, strongly implemented, implementation suspended)
- subpopulation: sub-population that the status of the specific intervention applies to
- required: is the specific intervention required or recommended?
- enforcement: are police/military enforcing the specific intervention?
- size: what is the size of groups allowed for social gatherings or in restaurants?
- duration: what is the duration of quarantine or self-isolation?
- testing_population: sub-populations of symptomatic or asymptomatic populations tested
- details: any specific details about the policy update
- source_document_url: URL for the source document(s) stored on Dropbox
- url: URL(s) provided by the contributors for the policy update
- entry_quality: have these interventions been confirmed by the contributors (Verified, Changes pending, or Unverified)


#### `hit-covid-completeness.csv`

- country: ISO 3166-1 alpha-3 country code  
- admin1: first administrative unit code (following GADM5 unless otherwise noted)
- usa_county_data: does this completeness information refer to USA county-level data
- intervention_group: code that groups interventions by type
- date: date the contributor logged this completeness information
- completeness: is this intervention information considered complete and up to date for level 1 administrative unit or country (Complete, Incomplete, Unsure)


## Mangement Team

* Qulu Zheng, Johns Hopkins Bloomberg School of Public Health
* Sarah V. Leavitt, Boston University School of Public Health
* Lawson Ung, Harvard Medical School
* Forrest K. Jones, Johns Hopkins Bloomberg School of Public Health
* Elizabeth C. Lee, Johns Hopkins Bloomberg School of Public Health
* Alain Labrique, Johns Hopkins Bloomberg School of Public Health
* David Peters, Johns Hopkins Bloomberg School of Public Health
* Andrew S. Azman, Johns Hopkins Bloomberg School of Public Health

See also the list of data [contributors](https://akuko.io/post/9862de6c-1b8b-4927-b939-3c2282397c31) who participated in this project.

## License

This dataset is licensed under the GNU General Public License v3.0 - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Our nifty website was designed by Matt Berg and Dan McCarey from [ona.io](https://ona.io/home/)

Contact: Andrew Azman (azman@jhu.edu) or hit-covid@jhu.edu
