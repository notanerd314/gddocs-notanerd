# getGJDailyLevel.php

Gets which daily level we're on and gets how much time is left.

## Parameters

### Required Parameters

**secret** - Wmfd2893gb7

### Optional Parameters

**gameVersion** - 22

**binaryVersion** - 42

**gdw** - 0

**accountID** - The user's account ID

**gjp** - The user's [GJP](/topics/encryption/gjp.md)

**weekly** - 0 for daily, 1 for weekly. Defaults to 0 if not sent

## Response

Returns the index of the current daily level and the time left in seconds, separated by a pipe `|`.

## Example

<!-- tabs:start -->

### **Python**

```py
import requests

data = {
	"weekly": 1,
    "secret": "Wmfd2893gb7"
}

req = requests.post("http://boomlings.com/database/getGJDailyLevel.php", data=data)
print(req.text)
```

### **curl**

```bash
curl http://boomlings.com/database/getGJDailyLevel.php -A "" -d "weekly=1&secret=Wmfd2893gb7"
```

**Response**
```plain
100146|121576
```

<!-- tabs:end -->
