--------

The AWS SDK for JavaScript version 3 \(v3\) is a rewrite of v2 with some great new features, including modular architecture\. For more information, see the [AWS SDK for JavaScript v3 Developer Guide](https://docs.aws.amazon.com/sdk-for-javascript/v3/developer-guide/welcome.html)\.

--------

# Amazon CloudWatch Examples<a name="cloudwatch-examples"></a>

Amazon CloudWatch \(CloudWatch\) is a web service that monitors your Amazon Web Services resources and applications you run on AWS in real time\. You can use CloudWatch to collect and track metrics, which are variables you can measure for your resources and applications\. CloudWatch alarms send notifications or automatically make changes to the resources you are monitoring based on rules that you define\.

![\[Relationship between JavaScript environments, the SDK, and CloudWatch\]](http://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/images/code-samples-cloudwatch.png)

The JavaScript API for CloudWatch is exposed through the `AWS.CloudWatch`, `AWS.CloudWatchEvents`, and `AWS.CloudWatchLogs` client classes\. For more information about using the CloudWatch client classes, see [https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/CloudWatch.html](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/CloudWatch.html), [https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/CloudWatchEvents.html](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/CloudWatchEvents.html), and [https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/CloudWatchLogs.html](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/CloudWatchLogs.html) in the API reference\.

**Topics**
+ [Creating Alarms in Amazon CloudWatch](cloudwatch-examples-creating-alarms.md)
+ [Using Alarm Actions in Amazon CloudWatch](cloudwatch-examples-using-alarm-actions.md)
+ [Getting Metrics from Amazon CloudWatch](cloudwatch-examples-getting-metrics.md)
+ [Sending Events to Amazon CloudWatch Events](cloudwatch-examples-sending-events.md)
+ [Using Subscription Filters in Amazon CloudWatch Logs](cloudwatch-examples-subscriptions.md)