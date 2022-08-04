# Autocomplete-API
Aviation Edge [Autocomplete API](https://aviation-edge.com/airport-autocomplete/) returns relevant airports and cities in the database based on the letters submitted. This allows users to pick the airport or city of their choice off the list after typing in the letters when the API is implemented. The airports the API returns include airports that have the submitted letters anywhere in them. For example, when the letters "ist" requested, the API returns both "**Ist**anbul Airport" and "Br**ist**ol Airport" (among other items).

The API is particularly useful for travel agency and flight booking websites, tools or apps to display the relevant airport and cities as a list for the user to choose from.

### Documentation
You may find input parameters, output examples with explanations for each item, filter list, and more in the [documentation](https://aviation-edge.com/developers/).

### Example Fields of Use
- Travel agency and flight booking/schedule tracking websites, tools, apps where users are expected to submit a departure or arrival city or airport
- Any autocomplete feature related to cities or airports

### Request 
Airports with the letters containing "xyz" in them:

**GET** `https://aviation-edge.com/v2/public/autocomplete?key=[API_KEY]&city=xyz`

### Response
```
[
{
"code": "AMS",
"name": "Amsterdam",
"cityCode": "AMS",
"cityName": "Amsterdam",
"countryCode": "NL",
"countryName": "Netherlands",
"lat": 52.3730556, "lng": 4.8922222,
"timezone": "Europe/Amsterdam",
"type": "city" } ],
"airports":
[
{
"code": "ZYA",
"name": "Amsterdam Centraal Railway Station",
"cityCode": "AMS",
"cityName": "Amsterdam",
"countryCode": "NL",
"countryName": "Netherlands",
"lat": 52.3730556,
"lng": 4.8922222,
"timezone": "Europe/Amsterdam",
"type": "rail_station",
"isRailRoad": 1,
"isBusStation": 0 },
{
"code": "AMS",
"name": "Schiphol",
"cityCode": "AMS",
"cityName": "Amsterdam",
"countryCode": "NL",
"countryName": "Netherlands",
"lat": 52.30907,
"lng": 4.763385,
"timezone": "Europe/Amsterdam",
"type": "airport",
"isRailRoad": 0,
"isBusStation": 0 } ],
"airportsByCities":
},
...
]
```

### Access & Support
[Contact us](https://aviation-edge.com/contact/) via email for any questions or support requests.

[Get your API key](https://aviation-edge.com/premium-api/) in a minute and start testing the data right away. The API is provided through API subscriptions. All plans grant access to the Future Schedules API and other APIs with a difference of the monthly API call limit. Choose the best plan for you and upgrade, downgrade or cancel your plan anytime without  commitments.

### License
The use of the API is subject to Aviation Edge [Terms and Conditions](https://aviation-edge.com/api-terms-of-service/).
