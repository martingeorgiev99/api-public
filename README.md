# **Showcase Website**
*First assignment of my study in HZ UAC - ICT Course*

# **script.js**
The provided script uses the AllOrigins service to handle CORS. AllOrigins is a proxy that allows you to fetch data from an external API without facing CORS issues.

Here is a breakdown of the script:

Using AllOrigins Proxy:

https://api.allorigins.win/get?url=${encodeURIComponent('https://xkcd.com/' + (Math.floor(Math.random() * 2783) + 1) + '/info.0.json')}: This URL calls the AllOrigins proxy, passing the URL of the XKCD API as a query parameter. AllOrigins will fetch the data on your behalf and return it to you.
Fetch and Parse Data:

fetch(...).then(response => response.json()): Fetches the data from the AllOrigins API and parses it as JSON.
const parsedData = JSON.parse(data.contents): Parses the contents property of the returned JSON to get the actual data from the XKCD API.
Create and Append Image Element:

Creates an img element using the data from the XKCD API and appends it to the comicContainer div.
