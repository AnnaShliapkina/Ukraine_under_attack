# ACLED Data Project

This project uses data from the Armed Conflict Location & Event Data Project (ACLED) to analyze various events related to political violence, demonstrations, and other significant non-violent political events.

## Data Description

The dataset includes the following columns:

- **event_id_cnty**: A unique alphanumeric event identifier by number and country acronym. This identifier remains constant even when the event details are updated.  
  Example: `ETH9766`

- **event_date**: The date on which the event took place. Recorded as Year-Month-Day.  
  Example: `2023-02-16`

- **year**: The year in which the event took place.  
  Example: `2018`

- **time_precision**: A numeric code between 1 and 3 indicating the level of precision of the date recorded for the event. The higher the number, the lower the precision.  
  Values: `1`, `2`, `3`

- **disorder_type**: The disorder category an event belongs to.  
  Values: `Political violence`, `Demonstrations`, `Strategic developments`

- **event_type**: The type of event; further specifies the nature of the event.  
  Example: `Battles`

- **sub_event_type**: A subcategory of the event type.  
  Example: `Armed clash`

- **actor1**: One of two main actors involved in the event (does not necessarily indicate the aggressor).  
  Example: `Rioters (Papua New Guinea)`

- **assoc_actor_1**: Actor(s) involved in the event alongside ‘Actor 1’ or actor designations that further identify ‘Actor 1’.  
  Example: `Labor Group (Spain); Women (Spain)`

- **inter1**: A numeric code between 0 and 8 indicating the type of ‘Actor 1’.  
  Values: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`

- **actor2**: One of two main actors involved in the event (does not necessarily indicate the target or victim).  
  Example: `Civilians (Kenya)`

- **assoc_actor_2**: Actor(s) involved in the event alongside ‘Actor 2’ or actor designation further identifying ‘Actor 2’.  
  Example: `Labor Group (Spain); Women (Spain)`

- **inter2**: A numeric code between 0 to 8 indicating the type of ‘Actor 2’.  
  Values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`

- **interaction**: A two-digit numeric code (combination of ‘Inter 1’ and ‘Inter 2’) indicating the two actor types interacting in the event.  
  Example: `13`, `58`

- **civilian_targeting**: This column indicates whether the event involved civilian targeting.  
  Values: `Civilians targeted`, blank

- **iso**: A unique three-digit numeric code assigned to each country or territory according to ISO 3166.  
  Example: `231` for Ethiopia

- **region**: The region of the world where the event took place.  
  Example: `Eastern Africa`

- **country**: The country or territory in which the event took place.  
  Example: `Ethiopia`

- **admin1**: The largest sub-national administrative region in which the event took place.  
  Example: `Oromia`

- **admin2**: The second largest sub-national administrative region in which the event took place.  
  Example: `Arsi` (Can be blank)

- **admin3**: The third largest sub-national administrative region in which the event took place.  
  Example: `Merti` (Can be blank)

- **location**: The name of the location at which the event took place.  
  Example: `Abomsa`

- **latitude**: The latitude of the location in four decimal degrees notation (EPSG:3857).  
  Example: `8.5907`

- **longitude**: The longitude of the location in four decimal degrees notation (EPSG:3857).  
  Example: `39.8588`

- **geo_precision**: A numeric code between 1 and 3 indicating the level of certainty of the location recorded for the event. The higher the number, the lower the precision.  
  Values: `1`, `2`, `3`

- **source**: The sources used to record the event. Separated by a semicolon.  
  Example: `Ansar Allah; Yemen Data Project`

- **source_scale**: An indication of the geographic closeness of the used sources to the event.  
  Example: `Local partner-National`

- **notes**: A short description of the event.  
  Example: `On 16 February 2023, OLF-Shane abducted an unidentified number of civilians after stopping a vehicle in an area near Abomsa (Merti, Arsi, Oromia). The abductees were traveling from Adama to Abomsa, Arsi.`

- **fatalities**: The number of reported fatalities arising from an event. When there are conflicting reports, the most conservative estimate is recorded.  
  Example: `3` (No information on fatalities is recorded as 0 reported fatalities)

- **tags**: Additional structured information about the event. Separated by a semicolon.  
  Example: `women targeted:politicians; sexual violence`

- **timestamp**: An automatically generated Unix timestamp that represents the exact date and time an event was uploaded to the ACLED API.  
  Example: `1676909320`

![Event Types](/charts/ACLED%20Event%20Types.jpg)

## About ACLED

ACLED collects and records reported information on political violence, demonstrations (rioting and protesting), and other select non-violent, politically important events. It aims to capture the modes, frequency, and intensity of political violence and demonstrations. Political violence is defined as the use of force by a group with a political purpose or motivation, or with distinct political effects. A political violence event is a single altercation where force is used by one or more groups toward a political end. A demonstration event is an in-person public gathering of three or more people advocating for a shared cause. Other select non-violent instances of politically significant developments are also included in the dataset to capture the potential precursors or critical junctures of a violent conflict.

ACLED's system defines political disorder by its constituent events, allowing users to compare trends across countries and time periods without predefining broader aggregate categories of events like wars, conflicts, operations, campaigns, or movements. These analytical decisions are left to the user.

For more information, visit [ACLED](https://www.acleddata.com) or contact via email at admin@acleddata.com.
