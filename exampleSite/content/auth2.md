---
weight: 13
title: Auth2
---

## Validate Token

```go
package main

import "github.com/bep/kittn/auth"

func main() {
	api := auth.Authorize("meowmeowmeow")

	_ = api.GetKittens()
}
```

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl --request GET \ 
--url 'http://{{url}}/ws/token/validate' \ 
--header 'token: {{token}}' 
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns sample response like this:

```json
Valid
```

Check if authentication token is valid or invalid.

### HTTP Request

`GET {{url}}/ws/token/validate`

To use a REST API with SNYPR, you must be authenticated. You can use the Generate Token API to authenticate and obtain a token, which you must then use with every API request

Sample

Base URL |  
--------- | -------
{{url}} | It must be in the following format: https://<hostname or IPaddress>/Snypr 

### Headers

| Headers  |                                             
|----------|---------------------------------------------
| token | {{token}} Valid authentication token     |



