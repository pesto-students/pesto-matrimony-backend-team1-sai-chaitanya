# Express API Quickstart Sample Code for Integrating with Okta

This repository contains a sample of protecting API endpoints using [Okta](https://www.okta.com/) in a [Node Express API](https://developer.okta.com/docs/guides/protect-your-api/nodeexpress/main/).

The sample uses the [Okta JWT Verifier SDK](https://github.com/okta/okta-jwt-verifier-js). Read more about getting started with Okta and authentication best practices on the [Okta Developer Portal](https://developer.okta.com).

This code sample demonstrates
* Configuring Okta
* Protecting routes
* Verifying the JWT

## Getting started

To run this example, run the following commands:

```shell
git clone https://github.com/okta-samples/okta-express-api-quickstart.git
cd okta-express-api-quickstart
npm ci
```

## Create an OIDC organization in Okta

Create a free Okta Developer account to create your Okta organization. You can do this through the [Okta CLI](https://cli.okta.com/) or through the [Okta Developer admin](https://developer.okta.com) dashboard.

When using the Okta CLI run the following command:

```shell
okta register
```

You will need your Okta domain and Audience.

Update server.js with your Okta settings.

```js
const oktaJwtVerifier = new OktaJwtVerifier({
    issuer: 'https://{yourOktaDomain}/oauth2/default'
});
const audience = 'api://default';
```

Start the app by running

```shell
npm start
```

Use your favorite HTTP Client to call the API. For authenticated calls, follow the steps in [Send a request to your API endpoint using Postman]() of the quick start.

## Helpful resources

* [Learn about Authentication, OAuth 2.0, and OpenID Connect](https://developer.okta.com/docs/concepts/)
* [Get started with Express](https://expressjs.com/)

## Help

Please visit our [Okta Developer Forums](https://devforum.okta.com/).
