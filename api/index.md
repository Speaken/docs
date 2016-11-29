# Overview

This is a general review of the Speaken API. If you have any problems or requests, please create an issue on this repository.

## API Versions*

The current version of the API is **v1**. We encourage you to explicitly specify a version via the ```Accept``` header.

```Accept: application/vnd.speaken.v1+json```

## Base URL and Formats

The base URL for all API resources is ```https://api.speaken.com/v1```

All data is sent and received as JSON. Blank fields are included as ```null``` instead of being omitted.

Timestamps are returned in ISO 8601 format:

```YYYY-MM-DDTHH:MM:SSZ ```

## Self-Describing API

You can explore all the resource endpoints from the base url:

```https://api.speaken.com/v1 ```

## Authentication

We use OAuth 2.0. To authenticate the user you can add the ```access_token``` to the request in two ways:

``
curl -H "Authorization: Bearer OAUTH-TOKEN" https://api.speaken.com
``

Read more about OAuth2. Note that OAuth2 tokens can be acquired programmatically, for applications that are not websites.

#### Token send in a header
```Authorization: Bearer {ACCESS_TOKEN}```

#### Token send as a parameter
```https://api.speaken.com/v1/?access_token={ACCESS_TOKEN} ```

Requests that require authentication will return ```404 Not Found```, instead of ```403 Forbidden```, in some places.

## Rate Limiting*

## User Agent

We recommend all API clients to include a ```User-Agent``` header.
You can use your Speaken username, or the name of your application for the ```User-Agent``` header value.
This allows us to contact you if there are any problems.

Example

```User-Agent: Superduper-speaken-App```

## Hypermedia

All resources may have one or more *_url properties linking to other resources.
These are meant to provide explicit URLs so that proper API clients don't need to construct URLs on their own.
It is highly recommended that API clients use these.
Doing so will make future upgrades of the API easier for developers. All URLs are expected to be proper RFC 6570 URI templates.

## CORS - Cross Origin Resource Sharing

## Pagination

Requests that return multiple items will be paginated to 30 items by default.
You can specify further pages with the ?page parameter.
For some resources, you can also set a custom page size up to 100 with the ?per_page parameter.
Note that for technical reasons not all endpoints respect the ?per_page parameter, see events for example.

```
curl 'https://api.speaken.com/v1/conversations?page=2&per_page=100'
```

Note that page numbering is 1-based and that omitting the ?page parameter will return the first page.

## Resources

## Terms of Service*

Please review our Terms of Service for the Speaken API.

