# IPGeolocation.io for Gemini CLI

The official IPGeolocation.io extension gives Gemini CLI 17 tools for accurate IP geolocation, company information, ASN and network data, IP security (VPN, proxy, Tor, bot, hosting and spam detection), abuse contacts, time zones, astronomy, currency data and user-agent parsing.

The extension runs `ipgeolocation-io-mcp@2.0.1` locally over stdio. It requires Node.js 22 or later, with `npx` on your PATH.

Install the extension:

```bash
gemini extensions install https://github.com/IPGeolocation/ipgeolocation-gemini-extension
```

During installation, Gemini prompts for your IPGeolocation.io API key as a sensitive setting. To install without a key, append `--skip-settings` to the install command. To configure the key later:

```bash
gemini extensions config ipgeolocation-io-mcp
```

Most tools require a key, and the tools and credits available to you depend on your plan. The `get_my_ip` tool works without a key. The other API tools return a missing-key error without sending a request. Use `get_cached_result` to retrieve cached response pages without making another API call.

Install this server through one method to avoid duplicate tool entries. Keep your other configured servers in place.

## Data and privacy

Company information includes the name, domain and type. ASN data is separate and includes the ASN number, organization, registered country, domain and type.

API lookups send their inputs and the server machine's public egress IP to IPGeolocation.io. Cached responses stay in the server process's memory. Gemini CLI manages its own configuration and logs.

See the [privacy policy](https://ipgeolocation.io/privacy.html), [security policy](https://github.com/IPGeolocation/ipgeolocation-io-mcp/blob/v2.0.1/SECURITY.md) and [tool reference](https://github.com/IPGeolocation/ipgeolocation-io-mcp/blob/v2.0.1/README.md#tool-reference). Contact [support@ipgeolocation.io](mailto:support@ipgeolocation.io) for help. License: [MIT](LICENSE).
