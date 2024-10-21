# All-Star Team Selector

Build an application to create an all-star teams based on coach's stat preferences.

- The input will be two coaches selection criteria. Example: fn(coach1_pref[], coach2_pref[]) where coach1_pref = `['points', 'rebound', 'block']` and coach2_pref = `['points', 'assist', 'rebound']`.
- A coach can pick up to three stats to use as selection criteria.
- The application will ingest and analyze provided player season level statistics.
- The application will determine the top players based on the coach's criteria. If the criteria is `['points', 'rebound', 'block']`, then players should be selected based on those three statistics and assigned accordingly. However it is important to keep in mind that the order of the coach's statistic preference matters. The 0 index stat criteria should take precedence over subsequent criteria, but all should impact the selection.
- Teams should be assigned in alternating fashion. Team 0 gets 1st pick, Team 1 2nd pick, Team 0 3rd pick, etc.
- A player can only be on one team.
- Rosters are limited to 10 player per team
- The output will be json with a two dimensional array with the two teams, including the stats.

Example Out, two teams with 10 players on each.
```json
[
  [
    {
      // TEAM A
      "player_id": "sr:player:XYZ",
      "player_name": "Player A",
      "points": 398,
      "rebound": 154,
      "assist": 100,
      "block": 8,
      "steal": 35,
      "field_goal_made": 149,
      "three_point_made": 33,
      "offensive_rebound": 25,
      "seconds_played": 58860
    } 
  ],
  [
    {
      // TEAM B
      "player_id": "sr:player:852022",
      "player_name": "Player B",
      "points": 398,
      "rebound": 154,
      "assist": 100,
      "block": 8,
      "steal": 35,
      "field_goal_made": 149,
      "three_point_made": 33,
      "offensive_rebound": 25,
      "seconds_played": 58860
    }
  ]
]
```
