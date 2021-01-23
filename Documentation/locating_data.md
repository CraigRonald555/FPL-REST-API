## Locating relevant data from FPL website

By storing the data from https://fantasy.premierleague.com/api/event/${gameweek}/live/ for each game week, the REST API can retrieve the total points scored for each player that game week.

The returned JSON file breaks down the peformance of each player in a game week in a way which should make it fairly simple to retieve key information, as you can see below:

<img src="json example.JPG" height=500 width=250 />

Each for each game week in a season, an object will be stored in a Firebase backend. The REST endpoints can then retrieve the appropriate data based on the purpose of the endpoint, and the parameters sent to it.

The format of the backend will be:
```
{

	"20/21": {
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
  
  	"21/22": {
    		...
   	}
   
}
```

An Admin endpoint will be added to update the database with any game week objects which have not yet been imported into the database.

