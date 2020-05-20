# Node.js + Express Login Example

This example shows how to add Login to a Node.js application.

**Prerequisites:** 

* [Node 12](https://nodejs.org/)+

> [Okta](https://developer.okta.com/) has Authentication and User Management APIs that reduce development time with instant-on, scalable user infrastructure. Okta's intuitive API and expert support make it easy for developers to authenticate, manage and secure users and roles in any application.

* [Getting Started](#getting-started)
* [Help](#help)
* [Links](#links)
* [License](#license)

## Getting Started

To install this example application, run the following commands:

```bash
git clone https://github.com/oktadeveloper/okta-nodejs-login-example.git
cd okta-nodejs-login-example
npm install
```

This will get a copy of the project locally. 

### Create a Free Okta Developer Account

If you don't have one, [create an Okta Developer account](https://developer.okta.com/signup/). After you've completed the setup process, log in to your account.

Create a new OIDC app by navigating to **Applications** > **Add Application** > select **Web**, and click **Next**. Fill in the following values:

* Name: `Node.js Login`
* Base URI: `http://localhost:3000`
* Login redirect URI: `http://localhost:3000/callback`
* Logout redirect URI: `http://localhost:3000`

Click **Done** to create your app. 

Create a `.env` file in your root directory and copy the client ID and secret into it. You can find the value for `<YOUR_ISSUER>` by navigating to **API** > **Authorization Servers**.

```
OIDC_ISSUER=<YOUR_ISSUER>
OIDC_CLIENT_ID=<YOUR_CLIENT_ID>
OIDC_CLIENT_SECRET=<YOUR_CLIENT_SECRET>
BASE_URL=http://localhost:3000
SESSION_SECRET=todo: make-this-more-secure
```
   
**NOTE**: Make sure to remove the `<...>` placeholders. Your issuer should look something like: `https://dev-123456.okta.com/oauth2/default`.

### Start the application

Start your application:

```
npm start
```

Log in to `http://localhost:3000` and enjoy your login experience!

## Links

This example uses the following libraries provided by Okta:

* [OktaDev Schematics](https://github.com/oktadeveloper/schematics#readme)
* [OIDC Middleware](https://github.com/okta/okta-oidc-js/tree/master/packages/oidc-middleware)

## Help

Please post any questions as issues in this repo, or visit our [Okta Developer Forums](https://devforum.okta.com/). 

## License

Apache 2.0, see [LICENSE](LICENSE).
