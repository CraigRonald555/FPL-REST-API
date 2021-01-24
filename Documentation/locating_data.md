## Locating relevant data from FPL website

By storing the data from https://fantasy.premierleague.com/api/event/${gameweek}/live/ for each game week, the REST API can retrieve the total points scored for each player that game week.

The returned JSON file breaks down the peformance of each player in a game week in a way which should make it fairly simple to retieve key information, as you can see below:

<img src="json example.JPG" height=500 width=250 />

Each for each game week in a season, an object will be stored in a Firebase backend. The REST endpoints can then retrieve the appropriate data based on the purpose of the endpoint, and the parameters sent to it.

The format of the backend will be:
```
{

	"2021": {
		"gameweek 1": {
		"url": "https://fantasy.premierleague.com/api/event/1/live/",
		"elements": *THE RESPECTIVE JSON OBJECT RETURNED FROM URL ABOVE*
     		},
		"gameweek 2": {
		"url": "https://fantasy.premierleague.com/api/event/2/live/",
    		"elements": *THE RESPECTIVE JSON OBJECT RETURNED FROM URL ABOVE*
     		},
    		...
    		...
  	},
  
  	"2122": {
    		...
   	}
   
}
```

An endpoint only accessible to admins will be added to update the database with any game week objects which have not yet been imported into the database. 

Edit:

I realised users won't have access to the players' FPL ids therefore an object for players will be added so users can request the playerid using the player name. By extracting data from https://fantasy.premierleague.com/api/bootstrap-static/, player data will be stored with this format:

```
{
	"$player_id": {
		"first_name": *first name*,
		"surname": *surname*,
		"web_name": *web_name*
}
```

