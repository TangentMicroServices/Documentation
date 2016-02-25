# User

## List All Users

```shell

curl http://api.tngnt.co/version2-userservice/users/ \
  -H 'apikey: 1234' -i
```


```python
import requests
url = "http://api.tngnt.co/version2-userservice/users/"
headers = {
	"apikey": "{your_api_key}"
}
response = requests.get(url, headers=headers)
```

### Permissions required

* Admin rights are required

### HTTP Request

`GET http://api.tngnt.co/version2-userservice/users/`



### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.


## Create a User 

`POST http://api.tngnt.co/version2-userservice/users/`

## Update a user 

`PATCH http://api.tngnt.co/version2-userservice/users/{pk}`

## Delete a user 

`DELETE http://api.tngnt.co/version2-userservice/users/{pk}`