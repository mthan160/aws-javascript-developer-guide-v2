--------

The AWS SDK for JavaScript version 3 \(v3\) is a rewrite of v2 with some great new features, including modular architecture\. For more information, see the [AWS SDK for JavaScript v3 Developer Guide](https://docs.aws.amazon.com/sdk-for-javascript/v3/developer-guide/welcome.html)\.

--------

# Loading Credentials in Node\.js from a JSON File<a name="loading-node-credentials-json-file"></a>

You can load configuration and credentials from a JSON document on disk using `AWS.config.loadFromPath`\. The path specified is relative to the current working directory of your process\. For example, to load credentials from a `'config.json'` file with the following content:

```
{ "accessKeyId": <YOUR_ACCESS_KEY_ID>, "secretAccessKey": <YOUR_SECRET_ACCESS_KEY>, "region": "us-east-1" }
```

Use the following command:

```
AWS.config.loadFromPath('./config.json');
```

**Note**  
Loading configuration data from a JSON document resets all existing configuration data\. Add additional configuration data after using this technique\. Loading credentials from a JSON document is not supported in browser scripts\.