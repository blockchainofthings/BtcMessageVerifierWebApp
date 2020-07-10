# Bitcoin Message Verifier Web App

A web application used to verify a message that had been signed using Bitcoin's approach.

## Rationale

Bitcoin's client reference implementation, Bitcoin Core, provides an RPC method to sign a message with a bitcoin
 address (`signmessage`) and another to verify the signed message (`verifymessage`). However, as of this writing,
 Bitcoin Core is not able to sign and verify messages using segregated witness (bech32) addresses. Also, it is not
 possible to verify a signed message using a public key hash instead of a bitcoin address.

This web application was put together to overcome these two limitations.

## Design

This web application has been designed as a single HTML page, making use of [Bootstrap](https://getbootstrap.com) for
 the UI and the [btc-message-verifier](https://github.com/blockchainofthings/btc-message-verifier) JavaScript library to
 actually verify the message.

### Browser compatibility

The web application's HTML page is compatible with modern web browsers.

It has been tested on the following web browsers:

- Safari ver. 13.1 (on macOS Catalina 10.15)
- Google Chrome ver. 83.0 64 bits (on macOS Catalina 10.15, Windows 10)
- Google Chrome ver. 83.0 32 bits (on Windows 8.1)
- Firefox ver. 78.0 64-bits (on macOS Catalina 10.15)
- Microsoft Edge ver. 83.0 64 bits (on macOS Catalina 10.15, Windows 8.1, Windows 10)

> **Note**: Internet Explorer is **not** supported.

## Deployment

To deploy this web application, just copy the `btc-message-verifier.html` HTML page along with the `assets` directory
 and its contents to a web server.

## Usage

Fill up the input fields with the proper data, paying attention to the following:

- Either a **bitcoin address** or a **public key hash** can be entered in the first field.

- If a **public key hash** is entered, it should be in hex format.

- The **signature** should be entered as a base64-encoded string.

- Do not forget to select the appropriate **Bitcoin blockchain network**.

When done, click the `Verify` button.

## License

This web application is released under the [MIT License](LICENSE). Feel free to fork, and modify!

Copyright © 2020, Blockchain of Things Inc.