# Private Feeds Server

Demo server for OAuth and reading feeds in JSON and XML.

## Running Locally

```
> npm install
> npm start
```

Server will be started at http://localhost:3000.

## Production

To be launched soon at http://private-feeds-server.herokuapp.com.

## API Routes

### `POST /auth`

**Request Body**

```json
{
	"username": "agnostechvalley",
	"password": "d0$ntm@tt3r"
}
```

Username and password can be any strings.

**Response Body**

```json
{
	"token": "57e10c03-61b9-4aaa-a6f8-af4d4f1e939b"
}
```

### `GET /feed`

**Request Headers**

- `Accept: application/json | application/rss+xml`
- `Authorization: Bearer 57e10c03-61b9-4aaa-a6f8-af4d4f1e939b`

**Response Body**

See `feeds/rss.json` and `feeds/rss.xml` in this repo.
