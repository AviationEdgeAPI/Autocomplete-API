# Autocomplete-API
Aviation Edge [Autocomplete API](https://aviation-edge.com/airport-autocomplete/) returns relevant airports and cities in the database based on the letters submitted. This allows users to pick the airport or city of their choice off the list after typing in the letters when the API is implemented. The airports the API returns include airports that have the submitted letters anywhere in them. For example, when the letters "ist" requested, the API returns both "**Ist**anbul Airport" and "Br**ist**ol Airport" (among other items).

The API is particularly useful for travel agency and flight booking websites, tools or apps to display the relevant airport and cities as a list for the user to choose from.

### Documentation
You may find input parameters, output examples with explanations for each item, filter list, and more in the [documentation](https://aviation-edge.com/developers/).

### Example Fields of Use
- Travel agency and flight booking/schedule tracking websites, tools, apps where users are expected to submit a departure or arrival city or airport
- Any autocomplete feature related to cities or airports

### Request 

**GET** `https://aviation-edge.com/v2/public/autocomplete?key=[API_KEY]&city=berlin`

### Response

```
{
    "GMT": "1",
    "codeIataAirport": "SXF",
    "codeIataCity": "BER",
    "codeIcaoAirport": "EDDB",
    "codeIso2Country": "DE",
    "latitudeAirport": 52.370277,
    "longitudeAirport": 13.521388,
    "nameAirport": "Berlin-Schoenefeld",
    "nameCountry": "Germany",
    "phone": "",
    "timezone": "Europe/Berlin"
}
…
```

### Useful Example Codes
1.	Fetching the data (axiom library used)

```
const axios = require('axios');

const API_KEY = 'api-key'; // Replace with your actual API key
const BASE_URL = 'https://aviation-edge.com/v2/public/autocomplete';

async function getAirportsByCity(city) {
    try {
        const response = await axios.get(BASE_URL, {
            params: {
                key: API_KEY,
                city: city
            }
        });

        if (response.status === 200 && response.data) {
            return response.data;
        } else {
            throw new Error(`Failed to retrieve data. Status code: ${response.status}`);
        }
    } catch (error) {
        console.error(`Error fetching airports for city ${city}:`, error);
    }
}

// Example usage:
getAirportsByCity('berlin').then(data => {
    console.log(data);
});
```

### Access & Support
[Contact us](https://aviation-edge.com/contact/) via email for any questions or support requests.

[Get your API key](https://aviation-edge.com/premium-api/) in a minute and start testing the data right away. The API is provided through API subscriptions. All plans grant access to the Future Schedules API and other APIs with a difference of the monthly API call limit. Choose the best plan for you and upgrade, downgrade or cancel your plan anytime without commitments.

### License
The use of the API is subject to Aviation Edge [Terms and Conditions](https://aviation-edge.com/api-terms-of-service/).
