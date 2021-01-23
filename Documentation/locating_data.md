## Locating relevant data from FPL website

By parsing the data stored at https://fantasy.premierleague.com/api/event/${gameweek}/live/, the necessary data to make the API work can be stored in the SQL backend. The returned JSON file breaks down the peformance of each player in a game week in a way which should make it fairly simple to retieve key information, as you can see below.

<img src="json example.JPG" height=500 width=250 />

An endpoint which can be called to update the database 
