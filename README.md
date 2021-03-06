# titan-url

Titan URL is a modern, free and open source URL shortener.

View it here: http://titan-url.herokuapp.com.

<br>

## Features

- Free and open source
- Custom as well as random aliases
- No sign up required

<br>


## API Usage

titan-url offers a free and easy to use Rest API for integrating titan-url into your application. And no API key is required! 



The only public endpoint is:
```
POST http://titan-url.herokuapp.com/shorten
```

The payload for the POST request must be json. The json payload must have these fields:

```json
{
	"original-url": "the url you want to shorten",
	"alias-type": "either custom or random",
	"slug": "custom-slug" // can be omitted if the alias-type is random
}
```

The response will also be of json type.
```json
{
	"ok": true,
	"message": "http://titan-url.herokuapp.com/demo"
}
```

Whether the request to the API is successfull or not, the response json schema will always be the same. Make sure to check the `ok` key to know whether the request was successfull or not. In case the request fails, the `message` key will contain the error message.

## Example extensions

The following apps have leveraged the titan-url API to level up their apps.

- [titan-url-cli](https://github.com/Shravan-1908/titan-url-cli) - A terminal client for titan-url written in javascript.
- [Alfred Discord Bot](https://github.com/alvinbengeorge/Discord) - An all in one Discord bot.