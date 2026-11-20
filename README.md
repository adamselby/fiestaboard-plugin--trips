# Trips, a FiestaBoard plugin

Count down to the next trip, with a daily updating countdown. No calendar needed, all details are stored in plugin settings.

## Configure

| Setting | Notes |
|---|---|
| Trips | One row per trip: destination, depart date, optional return date (`YYYY-MM-DD`). |
| Timezone | Defaults to America/Chicago. |
| Upcoming Window | How far ahead `trips.upcoming` looks. Default 90 days. |
| Take Over the Board | Takes over on departure and return days. Off by default. |
| Takeover Priority | Higher number wins. Default 30. |

### Page recipes

Next trip countdown, or nothing:

```text
{{= IFERROR(IF(trips.next_name = "", "", "NEXT TRIP: " & trips.next_formatted), "") }}
```

Supports Vestaboard and Vestaboard Note
