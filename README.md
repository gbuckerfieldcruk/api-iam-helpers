# API Gateway IAM Helpers

A collection of utilities to make submitting IAM authenticated requests to AWS API Gateway deployments simpler. Documentation on what AWS expects in an IAM authenticated request is available here:
http://docs.aws.amazon.com/general/latest/gr/sigv4_signing.html
http://docs.aws.amazon.com/general/latest/gr/sigv4-signed-request-examples.html

## Usage:

```
>>> from api_iam_helpers import build_req
>>> url,headers = build_req.get_signed_request(access_key,secret_key,'eu-west-1',api_id,'','/api/v1')
>>> r = requests.get(url,headers=headers)
>>> print r.text
Hello World
```
