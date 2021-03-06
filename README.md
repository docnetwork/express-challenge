## Google Books API ... API

For this challenge you will be creating a rudimentary Express API to query and store results from the Google Books API. This is a test of basic NodeJS and back end proficiency.

### Instructions
- Clone this repository and complete the challenge according to the specifications below.
- Once finished, email your [patch](https://robots.thoughtbot.com/send-a-patch-to-someone-using-git-format-patch) to jobs+dev@docnetwork.org and we will review your submission. **(Do _Not_ Open A Pull Request)**

### Specifications
- Research the [Google Books Volume API](https://developers.google.com/books/docs/v1/reference/volumes) to determine how to search for books given a query. You will need to create an [API key](https://developers.google.com/books/docs/v1/using#APIKey). Keys are not required for making requests to the Google API, but supporting them is required for this challenge.
- Implement an API route that accepts a search query, passes that along to the Books API (using a utility such as [https](https://nodejs.org/api/https.html), [axios](https://www.npmjs.com/package/axios), or [request](https://www.npmjs.com/package/request) to name a few), and responds with a collection of book results in a JSON format that includes the following details:
  - Title
  - Authors
  - Description (First 140 characters)
  - Categories
  - Publisher
  - Published Date
  - Preview Link
- Each query should store the search query and associated responses in a database or other format (such as writing to a local file). Entries should include all of the above information as well as a timestamp of when the entry was created. DocNetwork uses and recommends PostgreSQL for a DB driver, but you are free to choose whatever you are most comfortable with.
- When a search is run using a query that's already stored in your DB, return the results from your DB. If no existing match is found, continue with the Books API call and return those results as usual.
- Security is important, so don't send us your Books API key! The key should be loaded in through an external file that is not included in your patch.
- Include instructions for a reviewer to set up and use your application. This could be scripts, migration files, or just plain text describing the schema and required steps to get everything running.
- All code must be your own. Do not plagiarize, copy, or steal code.

### Resources
- NodeJS https://nodejs.org/en/
- ExpressJS https://expressjs.com/
- PostgreSQL https://www.postgresql.org/docs/, https://node-postgres.com/
- Google Books API https://developers.google.com/books/docs/v1/reference/
- DocNetwork! If you have any questions about the specifications or how to implement something, feel free to reach out to us. It will not count against your final review, and may even end up being a plus.
