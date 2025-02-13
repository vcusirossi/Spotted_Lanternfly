# Spotted_Lanternfly
<br>
<br>
##Overview:
<br>
Observational data was retrieved from www.iNaturalist.com. iNaturalist is a 501c3 non profit organization that creates a citizen science platform where users contribute biodiversity observations by photograph or sound recording. Observations may include the complete linnaean classification, GPS locations, and dates. Additional parameters include life stages and type of evidence of life. The website and app contains crowd-sourced data to receive help with species identifications, collaborate with other citizen scientists for a common purpose, or access additional observational data collected by iNaturalist users for ecological or biological research Data Collection The data was subsetted for only Spotted lanternfly (Lycorma delicatula) observations. Data was downloaded as a comma separated values file (CSV file).
<br>
<br>
##Method:
<br>
Python with pandas was used to clean the data.<br>
  -The dataset was cleaned to remove observations not within the United States. Observations were filtered for “Research Grade” observations which are observations that are confirmed by an identifier or subject matter expert. <br>
  -The .drop function from pandas removed the columns uuid, private_latitude, and private_longtitude. <br>
  -The Following column names were adjusted to the following using the rename function: <br>
    -'place_town_name' to 'town', <br>
    -'place_county_name' to 'county', <br>
    -'place_state_name' to 'state', <br>
    -'place_country_name' to 'country' <br>
  -a new data frame was created and named lanternfly1 the cleaned data was then saved to an updated CSV file named ‘cleaned_lanternfly.csv’. <br>
<br>
<br>
##Terminology:
<br>
**id** – observation identification number observed_on_string – time and date of observation not standardized <br>
**observed_on**- date of observation with standardized date<br>
**time_observed_at** - date, time, and time zone of observation standardized<br>
**time_zone** – observation time zone<br>
**user_id** – user identification number<br>
**user_login** – user login name on inaturalist platform that recorded observation user_name – user first and last name of who conducted observation<br>
**created_at** – date, time, and time zone the observation was uploaded to iNaturalist updated_at – date, time, and time zone the observation was updated quality_grade – quality grade of the observation based on iNaturlaist’s standards<br>
**tag_list** – additional information user can input when documenting observation such as life cycle stage description – user can add a description of the observation<br>
**num_identification_agreements** – number of other users who agree with the identification of the species num_identification_disagreements - number of users who disagree with the identification of the species captive_cultivated - if the species is captive or cultivated<br>
**oauth_application_id** - identification if observation was uploaded via website our though the app place_guess – a field the user is able to input the location they found the observation
**latitude** – geographical location in decimal degrees<br>
**longitude** – geographical locationin decimal degrees<br>
**positional_accuracy** - positional accuracy of location of observation<br>
**public_positional_accuracy** - positional accuracy of location of observation not obscured<br>
**geoprivacy** - disclosure of observations location<br>
**taxon_geoprivacy** - if taxon location is restricted for threated taxa<br>
**coordinates_obscured** - location on visible to inaturalist staff or researchers<br>
**positioning_method** - how coordinates were obtained for observation positioning_device - device coordinates were obtained for observation town – town that the observation was located<br>
**county** – county where observation was located<br>
**state** - state where observation was located<br>
**country** – country where the observation was located<br>
**species_guess** – species guess by the user of what the observation is<br>
**scientific_name** – scientific name of the observation<br>
**common_name** – common name of the observation<br>
**iconic_taxon_name** – taxon name of the observation<br>
**taxon_id** - taxon identification of the observation<br>
<br>
<br>
##Source:
<br>
iNaturalist community. Observations of Lycorma delicatula from United States, Exported from https://www.inaturalist.org on 2/8/2025
