---
weight: 15
title: Auth3
---


## Renew Token

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
--url 'http://{{url}}/ws/token/generate' \ 
--header 'password: {{password}}' \ 
--header 'username: {{username}}' \ 
--header 'validity: 365'
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns sample response like this:

```json
530bf219-5360-41d3-81d1-8b4d6f75956d
```

Renew an existing authentication token.

### HTTP Request

`GET {{url}}/ws/token/renew`


Sample

Base URL |  
--------- | -------
{{url}} | It must be in the following format: https://<hostname or IPaddress>/Snypr 

### Headers

| Headers  |                                             
|----------|---------------------------------------------
| username | {{username}} Username for the account.      |
| password | {{password}} Password for the account.      |
| validity | The number of days the token will be valid. |


<aside class="success">
The Auth classification generates a token that is used for subsequent requests.
</aside>