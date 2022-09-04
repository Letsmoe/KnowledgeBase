# API
Continuum-AI Publishing is a publishing service for hobby authors and people who want to share their stories.
As we do not want to be limited to only one frontend we offer an API so anyone who's got a license can use our API to perform requests on our database.

## Tokens
Authentication is handled via a bearer token that can be generated via the `tokens/generate` endpoint when passed the username and password via basic authentication.

Every token has specific access rights that can handle different parts of an application or all of them at the same time.

## Endpoints
There are several different endpoints depending on the data you're looking for.

### `author/info/{author_name}`
When wanting to retrieve data about a specific author you can use the info endpoint, this will return you a list of properties connected to the author.

```json
{
"preferred_language": "en_US",
"name": "Josh Demoman",
"organizations": ["TechReport", "FlowerPot"],
"articles": [{
"name": "On why humans and bees shouldn't live together",
"id": "173636bshduxhwjaj72747-3",
"date_published": "04-22-2022 19:34:21",
"organization": "hsbfhei2837hdh",
"category": "Nature",
"tags": ["Humans", "Bees"]
}]
}

```

