--------

The AWS SDK for JavaScript version 3 \(v3\) is a rewrite of v2 with some great new features, including modular architecture\. For more information, see the [AWS SDK for JavaScript v3 Developer Guide](https://docs.aws.amazon.com/sdk-for-javascript/v3/developer-guide/welcome.html)\.

--------

# Setting the AWS Region<a name="setting-region"></a>

A Region is a named set of AWS resources in the same geographical area\. An example of a Region is `us-east-1`, which is the US East \(N\. Virginia\) Region\. You specify a Region when configuring the SDK for JavaScript so that the SDK accesses the resources in that Region\. Some services are available only in specific Regions\.

The SDK for JavaScript doesn't select a Region by default\. However, you can set the Region using an environment variable, a shared `config` file, or the global configuration object\.

## In a Client Class Constructor<a name="setting-region-constructor"></a>

When you instantiate a service object, you can specify the Region for that resource as part of the client class constructor, as shown here\.

```
var s3 = new AWS.S3({apiVersion: '2006-03-01', region: 'us-east-1'});
```

## Using the Global Configuration Object<a name="setting-region-config-object"></a>

To set the Region in your JavaScript code, update the `AWS.Config` global configuration object as shown here\.

```
AWS.config.update({region: 'us-east-1'});
```

For more information about current Regions and available services in each Region, see [AWS Regions and Endpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html) in the *AWS General Reference*\.

## Using an Environment Variable<a name="setting-region-environment-variable"></a>

You can set the Region using the `AWS_REGION` environment variable\. If you define this variable, the SDK for JavaScript reads it and uses it\.

## Using a Shared Config File<a name="setting-region-config-file"></a>

Much like the shared credentials file lets you store credentials for use by the SDK, you can keep your Region and other configuration settings in a shared file named `config` that is used by SDKs\. If the `AWS_SDK_LOAD_CONFIG` environment variable has been set to a truthy value, the SDK for JavaScript automatically searches for a `config` file when it loads\. Where you save the `config` file depends on your operating system:
+ Linux, macOS, or Unix users: `~/.aws/config`
+ Windows users: `C:\Users\USER_NAME\.aws\config`

If you don't already have a shared `config` file, you can create one in the designated directory\. In the following example, the `config` file sets both the Region and the output format\.

```
[default]
   region=us-east-1
   output=json
```

For more information about using shared config and credentials files, see [Loading Credentials in Node\.js from the Shared Credentials File](loading-node-credentials-shared.md) or [Configuration and Credential Files](https://docs.aws.amazon.com/cli/latest/userguide/cli-config-files.html) in the *AWS Command Line Interface User Guide*\.

## Order of Precedence for Setting the Region<a name="setting-region-order-of-precedence"></a>

The order of precedence for Region setting is as follows:
+ If a Region is passed to a client class constructor, that Region is used\. If not, then\.\.\.
+ If a Region is set on the global configuration object, that Region is used\. If not, then\.\.\.
+ If the `AWS_REGION` environment variable is a [truthy](https://developer.mozilla.org/en-US/docs/Glossary/Truthy) value, that Region is used\. If not, then\.\.\.
+ If the `AMAZON_REGION` environment variable is a truthy value, that Region is used\. If not, then\.\.\.
+ If the `AWS_SDK_LOAD_CONFIG` environment variable is set to a truthy value and the shared credentials file \(`~/.aws/credentials` or the path indicated by `AWS_SHARED_CREDENTIALS_FILE`\) contains a Region for the configured profile, that Region is used\. If not, then\.\.\.
+ If the `AWS_SDK_LOAD_CONFIG` environment variable is set to a truthy value and the config file \(`~/.aws/config` or the path indicated by `AWS_CONFIG_FILE`\) contains a Region for the configured profile, that Region is used\.