| Endpoint                                     | Description              |
| -------------------------------------------- | ------------------------ |
| [GET /companies](#get-companiesme)           | Search for a companies   |
| [POST /companies](#get-companiesme)          | Create a new company     |
| [GET /companies/:id](#get-companiesme)       | Get company informations |
| [PATCH,PUT /companies/:id](#get-companiesme) | Update user company      |

## GET /companies

Search for a companies

### Parameters

| Name | Required     | Type   | Description     |
| ---- | ------------ | ------ | --------------- |
| `q`  | not required | string | Value to search |

### Example Request

`curl -X GET https://api.speaken.com/api/v1/companies?q=Speaken`

## POST /companies

Create a new company

### Parameters

| Name     | Required     | Type   | Description                                      |
| -------- | ------------ | ------ | ------------------------------------------------ |
| `name`   | required     | string | Company's name                                   |
| `size`   | not required | string | Company size. See /values for available values   |
| `sector` | not required | string | Company sector. See /values for available values |
| `logo`   | not required | string | Company's image                                  |

### Example Request

`curl -X POST https://api.speaken.com/api/v1/companies`

## GET /companies/:id

Get user company

### Example Request

`curl -X GET https://api.speaken.com/api/v1/companies/1`

## PATCH|PUT /companies/:id

Update user company

### Example Request

`curl -X PUT https://api.speaken.com/api/v1/companies/1`
