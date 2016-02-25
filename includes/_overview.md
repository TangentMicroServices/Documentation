# Overview

```shell
curl http://api.tngnt.co/
```

```python
import requests
url = "http://api.tngnt.co/"
response = requests.get(url)
```

> Will provide status information on all downstream services (coming soon)

```json

[
	"userservice": {
		"status": "up",
		"location": "http://api.tngnt.co/version2-userservice/"	
	},
	...
]
```

Base URL | 
--------- | 
[http://api.tngnt.co](http://api.tngnt.co/) | 



## Making requests:

Authentication is handled with token authentication

### Getting a token

<img src="https://s3-us-west-2.amazonaws.com/tangentsolutions.co.za/Screen+Shot+2016-02-25+at+10.29.44+PM.png" />

1. Direct the user to http://api.tngnt.co/login/
2. User enters their credentials at http://api.tngnt.co/login/
3. On successful login, the user is redirected back to your site with `api_token={their_api_token}`
4. Use this token to authenticate subsequent requests


### Using a token

> Authenticate with a query parameter

```shell
curl http://api.tngnt.co/version2-userservice/health/?apikey={your_api_token}
```

```python
import requests
url = "http://api.tngnt.co/version2-userservice/health/?apikey={your_api_token}"
response = requests.get(url)
```

> Authenticate with a header

```shell
curl http://api.tngnt.co/version2-userservice/health/ \
    -H 'apikey: {your_api_token}' -i
```

```python
import requests
headers = {
	"apikey": "{your_api_token}"
}
url = "http://api.tngnt.co/version2-userservice/health/"
response = requests.get(url, headers=headers)
```

* A token can be sent either as a query parameter `?apikey=...` or as a header `apikey: ...`

### Services available

Service name | Location | Description
--------- | ------- | -----------
UserService | [http://api.tngnt.co/version2-userservice](http://api.tngnt.co/version2-userservice) | Get and save information on a user
ProjectService | [http://api.tngnt.co/version2-projectservice](http://api.tngnt.co/version2-projectservice) | Track projects, aggregate project data from varous 3rd party sources
HoursService | [http://api.tngnt.co/version2-hourservice](http://api.tngnt.co/version2-hoursservice) | Track time worked at various clients

