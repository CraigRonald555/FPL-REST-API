# FPL Squad Selecting Algorithm Testing API

## Full Description

The idea of this API is to allow anyone who is developing an automated-managing system for the [Fantasy Premier League](http://fantasy.premierleague.com) (FPL) to run their squad selecting algorithm through an entire year's worth of data in order to see how it would have performed in a season.

The plan is to have an Express API which is connected to a MySQL database that holds data taken from JSON files on the FPL website. This data will likely be parsed via a middleware in Express.

Endpoints will allow users to send an array of players (the squad) along with the game week and season to see how that set of players would have performed for that week. The result will be the total amount of points those players would have earned. 

## Planning documentation

1. [Table Design](https://docs.google.com/document/d/1rSaNnp6NBy6kyY_6TPAzc1Bxj4aa-n7a-r1ryaYfv3I/edit?usp=sharing)
2. [Finding the relevant data](https://docs.google.com/document/d/1Kzbi1v0owFkDWXcQnaUPGRZUa-UaDPMfGyWIZsoLBk4/edit?usp=sharing)
3. Node.js & Express Server
