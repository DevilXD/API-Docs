`GET` `/getplayer[ResponseFormat]/{devId}/{signature}/{session}/{timestamp}/{player}`

#### Description
Returns information on the requested `player`.

#### URL Parameters
`devId`: Your developer Id

`signature`: Generated method signature

`session`: Session Id

`timestamp`: UTC timestamp

`player`: Player name or player id of the player you want to get info on

#### Response Examples
```json
[
    {
       "Created_Datetime":"11/17/2015 11:11:19 PM",
       "HoursPlayed":1201,
       "Id":255669,
       "Last_Login_Datetime":"12/5/2018 6:39:36 AM",
       "Leaves":36,
       "Level":409,
       "Losses":1956,
       "MasteryLevel":39,
       "Name":"iDropBodies",
       "Personal_Status_Message":"",
       "Platform":"Steam",
       "RankedConquest":{
          "Leaves":4,
          "Losses":24,
          "Name":"Conquest",
          "Points":48,
          "PrevRank":311,
          "Rank":311,
          "Rank_Stat_Conquest":null,
          "Rank_Stat_Duel":null,
          "Rank_Stat_Joust":null,
          "Season":2,
          "Tier":26,
          "Trend":0,
          "Wins":46,
          "player_id":null,
          "ret_msg":null
       },
       "Region":"North America",
       "TeamId":0,
       "Team_Name":"",
       "Tier_Conquest":26,
       "Total_Achievements":56,
       "Total_Worshippers":459885773,
       "Wins":4134,
       "ret_msg":null
    }
 ]
```

#### Response Details
`Created_Datetime`: The date that the user registered

`Hours_Played`: The amount of hours played

`Id`: Player Id, used for the other API endpoints

`Last_Login_Datetime`: Last time the user logged in

`Leaves`: When the user gets deserter or disconnects/exits game and leaves a bot in place

`Level`: Account level of the user

`Loses`: Games lost

`MasteryLevel`: Champions unlocked/bought

`Name`: The player name

`Personal_Status_Message`: Unused

`Platform`: The platform the user plays on

`Region`: Region the user plays in

`TeamId`: Unused, references clans

`Team_Name`: Unused, references clans

`Tier_Conquest`: References ranked tier

`Total_Achievements`: Achievements earned by the user

`Total_Worshippers`: Total experience earned

`Wins`: Total game wins
