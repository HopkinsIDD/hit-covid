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

There are two main data files in our database, the 

• record_id: unique id of record (note that a single record is generated each time a set of data are entered so these can be shared across interventions)

• entry_time: time that data were entered

• national entry: flag for whether this is a national-level policy

• country: ISO country code

• country_name: Name of Country

• admin1: Level 1 Administrative Unit Code

• admin1_name: Level 1 Administrative Unit Code

• locality: specified geographic areas below level 1

• intervention_specific_clean: Intervention type

• t: Date of updated status to policy implementation for a particular intervention

• status: Updated status of policy

• status_simp: Simplified updated status of policy (Not implemented, partially implemented, or strongly implemented)

• subpopulation: Sub-population that the status of the specific intervention applies to

• required: Is the specific intervention required or recommended?

• enforcement: Are police/military enforcing the specific intervention?

• size: What is the size of groups allowed for social gatherings or in restaurants?

• duration: What is the duration of quarantine or self-isolation?

• testing_population: Sub-populations of symptomatic or asymptomatic populations tested?

• source_url: URL for the intervention section

• entry_quality: Have these interventions gone through internal audit?

• details: Any specific comments left?


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

* Our nifty website was designed by Matt Berg and XX from [ona.io](https://ona.io/home/)

Contact: Andrew Azman (azman@jhu.edu) or hit-covid@jhu.edu
