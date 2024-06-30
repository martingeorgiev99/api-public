2nd year student here.
**I have not uploaded the API choice or design as it was accepted last school year.**
This submission is almost identical to the one I uploaded last year - only difference being that CORS is now not required to be disabled in your browser.
The feedback from last year's submission was that CORS should stay enabled and I should work around it.

The project is hosted at:

https://martingeorgiev99.github.io/api-public/

The API is used under Blog->Blog pages number 2, 3, 4, and 5. It pulls a random comic image and displays it once the blog text is finished.

The site has been adapted for mobile view first.

Thanks for reading, have a good day!

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
