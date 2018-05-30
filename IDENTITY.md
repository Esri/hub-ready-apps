# Use OAuth 2.0 to implement ArcGIS Identity

Good news! Identity is implemented in ArcGIS Hub like the rest of ArcGIS Online using a common web standard called OAuth2.

> Learn more about the [benefits of ArcGIS Identity](http://www.esri.com/products/arcgis-capabilities/) and how to start [implementing ArcGIS Identity](https://developers.arcgis.com/documentation/core-concepts/security-and-authentication/) in your application.

Hub ready apps have the _unique_ privilege of helping the public access premium ArcGIS features via a free account of their own unlocked with social media credentials.

To accomplish this, we need to point new users at the appropriate community organization when its time to sign in.

```js
const info = new OAuthInfo({
    // ...
    portalUrl: communityPortalUrl,
    // ...
});

```
You can find a demonstration of how to do this on GitHub: https://github.com/Esri/configurable-app-examples-4x-js/tree/master/hub-auth-js

## When an app lives on `*.arcgis.com`

For apps that live on *.arcgis.com specifically, there is one _more_ catch. The default behavior of the ArcGIS API for JavaScript when authenticating users using OAuth2 is to force redirect to https://www.arcgis.com/home/signin.html for sign in.

We'll need to override that behavior (and use a generic popup or inline redirect) and point folks straight at their own community organization. 

```js
IdentityManager.useSignInPage = false;
```
IdentityManager - [API Reference](https://developers.arcgis.com/javascript/latest/api-reference/esri-identity-IdentityManager.html#useSignInPage)