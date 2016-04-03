# API Gateway IAM Helpers

A collection of utilities to make submitting IAM authenticated requests to AWS API Gateway simpler.

## Usage:

```
>>> from api_iam_helpers import build_req
>>> url,headers = build_req.get_signed_request(access_key,secret_key,'eu-west-1',api_id,'','/api/v1')
>>> r = requests.get(url,headers=headers)
>>> print r.text
Hello World
```
