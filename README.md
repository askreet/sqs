# Simple Go SQS wrappers

Simple SQS helper module wrapping github.com/mikedewar/aws4. This module is a
thin layer it does not abstract anything from the SQS API.

## Example: Sending a message
```
client, err := sqs.NewClient("YourAccessKeyId", "YourSecretAccessKey", "us-east-1")
if err != nil {
	// wrong region?
}

err = client.SendMessage("https://my.queue/url", "My message")
if err != nil {
	// unable to sent the message
}
```

## References
 * Amazon SQS API Documentation
   http://docs.aws.amazon.com/AWSSimpleQueueService/latest/APIReference/Welcome.html
