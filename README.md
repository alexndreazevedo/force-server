# SSL ForceServer

SSL ForceServer is a server to be used with [CORS](https://pt.wikipedia.org/wiki/Cross-origin_resource_sharing) that allow to use SSL certificates. It was designed to connect applications that use Salesforce OAuth and REST services. The original [force-server](https://github.com/ccoenraets/force-server) was created by [Christophe Coenraets](https://github.com/ccoenraets) and extended after need to connect to [SalesForce REST API](https://developer.salesforce.com/page/Getting_Started_with_the_Force.com_REST_API) without use the [SalesForce MobileSDK](https://developer.salesforce.com/docs/atlas.en-us.mobile_sdk.meta/mobile_sdk/) for to get access in special by [User-Password Flow](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_understanding_username_password_oauth_flow.htm).

SSL ForceServer allow to use SSL certificate and send requests in JSON, instead _x-www-form-urlencoded_, beyond provide two main features:

- **Proxy server** to avoid cross-domain policy issues when invoking Salesforce REST services.

- **Local web-server** to (1) serve the OAuth callback URL defined in your Connected App, and (2) serve the whole app during development and avoid cross-domain policy issues when loading files (for example, templates) from the local file system.

## Installing SSL ForceServer

Open a command prompt and type:

```
npm install -g ssl-forceserver
```

or (Unix-based systems)

```
sudo npm install -g ssl-forceserver
```

## Run the Server

Navigate to the directory where you created index.html, and type:

```
ssl-forceserver
``` 
    
This command will start the server on port 8200, and automatically load your app (http://localhost:8200) in a browser window. You'll see the Salesforce login window, and the list of contacts will appear after you log in.

You can change the port number and the web root. Type the following command for more info:

```
ssl-forceserver --help
```

## Uninstalling the CLI

To uninstall the CLI:
    
```
npm -g rm ssl-forceserver
```

or 

```
sudo npm -g rm ssl-forceserver
```

## Deploying SSL ForceServer to Heroku 

SSL ForceServer is CORS-enabled. Instead of running it locally as a development server, you can deploy it to Heroku as your Proxy Server. Click the button below to deploy SSL ForceServer to Heroku:

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)
