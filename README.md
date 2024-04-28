# Amazon Scraper API

This project is a simple API built with Node.js and Express. It uses the ScraperAPI service to scrape data from Amazon.

## index.js

The `index.js` file is the entry point to the application. Here's a breakdown of what it does:

1. **Imports**: At the top of the file, we import the necessary modules. We're using `express` to create our server and `request-promise` to make HTTP requests.

2. **Server Setup**: We create an Express application and set the port to either the environment variable `PORT` or 5001.

3. **ScraperAPI URL Generator**: We define a function `generateScraperUrl` that takes an API key and returns a URL for the ScraperAPI service.

4. **Middleware**: We use the `express.json()` middleware to parse JSON request bodies.

5. **Routes**: We define two routes:
   - `GET /`: This route just returns a welcome message.
   - `GET /products/:productId`: This route takes a product ID as a URL parameter and an API key as a query parameter. It makes a request to the ScraperAPI service to get data for the specified product and returns this data as a JSON response.

To run the application locally, use the command `node index.js` (assuming you have Node.js installed). Make sure to replace the `apiKey` constant with your actual ScraperAPI key.
