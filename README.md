# SFG20 API Explorer

A single HTML file for sending requests to the SFG20 Approved Provider API (legacy API, version 3.4 of the API User Guide) from your browser. Each endpoint has a guide next to the request form.

## Requirements

- A current version of Chrome, Edge, Firefox or Safari.
- Credentials from SFG20: a Client (Bridge) ID and secret, and a Customer ID and secret.
- A network connection to the SFG20 API. No installation is needed. The file has no external dependencies.

## Start

1. Download `sfg20-api-explorer.html`.
2. Open the file in your browser. You can double-click it.
3. If the page cannot reach the API from a local file, serve the folder and open the address that the server prints:

   ```bash
   python3 -m http.server 8099
   ```

   Then open `http://127.0.0.1:8099/sfg20-api-explorer.html`.

## First use

1. The setup wizard opens when no configuration exists. Enter a name, select Test or Live, and enter the four credentials.
2. Open Token and select Send. The top bar shows how long the token is valid. A token is valid for 10 minutes.
3. Select an endpoint in the left menu. Enter the parameters, if the endpoint has any. Select Send.
4. Read the status and the data in the Response column. Use Copy or Download to keep the response.

## Configurations

- A configuration has a name, an environment (Test or Live) and four credentials.
- You can store more than one configuration. Select the active one in the top bar.
- Test and Live use separate credentials. Test credentials do not work on Live.
- A red banner shows when the active configuration uses Live. Every request from this page only reads data (GET).

## Cached responses

- Select Cache this response in local storage on an endpoint page to store a response.
- View cache shows the stored response. Fetch from server sends a new request.
- The Cached responses page lists every stored response. You can view, download or delete each one.
- Large responses are not cached because local storage is limited.

## Slow requests

Some requests take 15 seconds or longer for a larger library. The page waits up to two minutes. To get only the schedule IDs, use List schedule IDs. It is much faster. Then use Get a schedule for each ID.

## Reference pages

Getting started, API index (Swagger), Domain rules, Lookup tables, Glossary and Troubleshooting are in the left menu.

## Security

- The browser stores configurations, credentials and tokens in local storage. The storage is not encrypted. The data stays on your device.
- Use a browser profile that only you control.
- Delete a configuration to remove its credentials from the browser.
- The file does not contain credentials and does not send data to any host other than the API host of the active configuration.

## Hosts

| Environment | Host |
| --- | --- |
| Live | `https://api.sfg20.co.uk` |
| Test | `https://az-sfg20-api-ote.azurewebsites.net` |

## Support

Contact SFG20 support. Give the time, the URL and the status of the request.

## Licence

See [LICENSE](LICENSE).
