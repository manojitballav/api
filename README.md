# India COVID-19 Tracker

## Interfaces for pulling data into your dashboard
This is meant only for developer who has the knowledge and required skills to use this data
### Data Interface
https://api.covid19india.org/data.json

#### Contains time series data of confirmed nCov-19 citizens starting from 30 January 2020
Example format:
```
{
	"cases_time_series": [
		{
			"dailyconfirmed": "1",
			"dailydeceased": "0",
			"dailyrecovered": "0",
			"date": "30 January ",
			"totalconfirmed": "1",
			"totaldeceased": "0",
			"totalrecovered": "0"
		},
		{
			"dailyconfirmed": "0",
			"dailydeceased": "0",
			"dailyrecovered": "0",
			"date": "31 January ",
			"totalconfirmed": "1",
			"totaldeceased": "0",
			"totalrecovered": "0"
		}

```

#### State wise number of cases
Example format:
```
"statewise": [
		{
			"active": "371",
			"confirmed": "401",
			"deaths": "7",
			"lastupdatedtime": "March 22, 2020 at 10:27 pm",
			"recovered": "23",
			"state": "Total"
		},
		{
			"active": "72",
			"confirmed": "74",
			"deaths": "2",
			"lastupdatedtime": "",
			"recovered": "0",
			"state": "Maharashtra"
		}
```

### Travel History of Patients with Confirmed infection
https://api.covid19india.org/travel_history.json

#### Travel history data of individual patients
Use pid to get individual patient travel data.
Example format: 
```
{
	"travel_history": [
		{
			"address": "Hotel Aryas, Kuthattukulam, Muvattupuzha road",
			"datasource": "https://drive.google.com/drive/folders/1yAgt3IN1u8jX8g8jEasC4KNR26HUqeKi",
			"entryid": "1",
			"latlong": "9.8614231,76.5900643",
			"modeoftravel": "",
			"pid": "P35",
			"placename": "",
			"timefrom": "29/02/2020 10:30:00",
			"timeto": "29/02/2020 11:30:00",
			"type": "placeVisit"
		},
		{
			"address": "Suresh Hotel Ranni",
			"datasource": "https://drive.google.com/drive/folders/1yAgt3IN1u8jX8g8jEasC4KNR26HUqeKi",
			"entryid": "2",
			"latlong": "9.3823686,76.779199",
			"modeoftravel": "",
			"pid": "P35",
			"placename": "",
			"timefrom": "01/03/2020 21:30:00",
			"timeto": "01/03/2020 23:00:00",
			"type": "placeVisit"
		}
```
### RAW Data

https://api.covid19india.org/raw_data.json

Contains complete data related to infected person along with data sources from Social Media Site
Please use this data judiciously so that infected people are not targeted. 

Example format:
```
{
	"raw_data": [
		{
			"agebracket": "20",
			"backupnotes": "Student from Wuhan",
			"contractedfromwhichpatientsuspected": "",
			"currentstatus": "Recovered",
			"dateannounced": "30/01/2020",
			"detectedcity": "Thrissur",
			"detecteddistrict": "Thrissur",
			"detectedstate": "Kerala",
			"estimatedonsetdate": "",
			"gender": "F",
			"nationality": "India",
			"notes": "Travelled from Wuhan",
			"patientnumber": "1",
			"source1": "https://twitter.com/vijayanpinarayi/status/1222819465143832577",
			"source2": "https://weather.com/en-IN/india/news/news/2020-02-14-kerala-defeats-coronavirus-indias-three-covid-19-patients-successfully",
			"source3": "",
			"statepatientnumber": "KL-TS-P1",
			"statuschangedate": "14/02/2020"
		},
		{
			"agebracket": "",
			"backupnotes": "Student from Wuhan",
			"contractedfromwhichpatientsuspected": "",
			"currentstatus": "Recovered",
			"dateannounced": "02/02/2020",
			"detectedcity": "Alappuzha",
			"detecteddistrict": "Alappuzha",
			"detectedstate": "Kerala",
			"estimatedonsetdate": "",
			"gender": "",
			"nationality": "India",
			"notes": "Travelled from Wuhan",
			"patientnumber": "2",
			"source1": "https://www.indiatoday.in/india/story/kerala-reports-second-case-of-coronavirus-1642494-2020-02-02",
			"source2": "https://weather.com/en-IN/india/news/news/2020-02-14-kerala-defeats-coronavirus-indias-three-covid-19-patients-successfully",
			"source3": "",
			"statepatientnumber": "KL-AL-P1",
			"statuschangedate": "14/02/2020"
		}
```
