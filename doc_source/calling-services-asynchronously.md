--------

The AWS SDK for JavaScript version 3 \(v3\) is a rewrite of v2 with some great new features, including modular architecture\. For more information, see the [AWS SDK for JavaScript v3 Developer Guide](https://docs.aws.amazon.com/sdk-for-javascript/v3/developer-guide/welcome.html)\.

--------

# Calling Services Asychronously<a name="calling-services-asynchronously"></a>

All requests made through the SDK are asynchronous\. This is important to keep in mind when writing browser scripts\. JavaScript running in a web browser typically has just a single execution thread\. After making an asynchronous call to an AWS service, the browser script continues running and in the process can try to execute code that depends on that asynchronous result before it returns\.

Making asynchronous calls to an AWS service includes managing those calls so your code doesn't try to use data before the data is available\. The topics in this section explain the need to manage asynchronous calls and detail different techniques you can use to manage them\.

**Topics**
+ [Managing Asychronous Calls](making-asynchronous-calls.md)
+ [Using an Anonymous Callback Function](using-a-callback-function.md)
+ [Using a Request Object Event Listener](using-a-response-event-handler.md)
+ [Using async/await](using-async-await.md)
+ [Using JavaScript Promises](using-promises.md)