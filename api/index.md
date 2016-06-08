# API Authentication

There are one way to authenticate through Speaken v1.
Requests that require authentication will return 403 Forbidden.

## OAuth2 Token (sent in a header)

``
curl -H "Authorization: Bearer OAUTH-TOKEN" https://api.speaken.com
``

Read more about OAuth2. Note that OAuth2 tokens can be acquired programmatically, for applications that are not websites.

## Hypermedia

All resources may have one or more *_url properties linking to other resources. 
These are meant to provide explicit URLs so that proper API clients don't need to construct URLs on their own. 
It is highly recommended that API clients use these. 
Doing so will make future upgrades of the API easier for developers. All URLs are expected to be proper RFC 6570 URI templates.


## Pagination

Requests that return multiple items will be paginated to 30 items by default. 
You can specify further pages with the ?page parameter. 
For some resources, you can also set a custom page size up to 100 with the ?per_page parameter. 
Note that for technical reasons not all endpoints respect the ?per_page parameter, see events for example.

```
curl 'https://api.speaken.com/v1/conversations?page=2&per_page=100'
```

Note that page numbering is 1-based and that omitting the ?page parameter will return the first page.
