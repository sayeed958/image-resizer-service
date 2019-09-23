# image-resizer-service

This serverless application deploys a Lambda function and API Gateway to your AWS account that reads images from a S3 bucket (whose name defined at deployment) and serves them through API Gateway.

The API Gateway respects the file organization on S3 bucket.

# How to use ?
Go inside APIGateway > ImageResizerAPI > stages > production > API_INVOKE_URL

For example, an image stored in `s3://example-bucket/example-folder/example.jpg` will be served from `API_INVOKE_URL/example-folder/example.jpg`

To resize the same image, simply give dimensions as `width` and `height` GET parameters e.g.
   
    API_INVOKE_URL/example-folder/example.jpg?height=200&width=200

**After deploying the application, you are strongly recommended to deploy a CDN distribution in front of API Gateway, so your responses are cached and it will improve performance and reduce costs significantly.

## Release Notes

### 0.1.1

- Major refactor, increase test coverage, full ES6 migration.
- ability to adjust Lambda memmory size.

### 0.1

Initial version

## License

MIT License (MIT)
