# rateGJDemon21.php

Rates the demon difficulty of a demon level - only works for Geometry Dash moderators.

## Parameters

### Required Parameters

**gameVersion** - 22

**binaryVersion** - 42

**secret** - Wmfp3897gc3

**accountID** - The accountID of the user who's rating the demon's difficulty

**gjp** - The [GJP](/topics/gjp.md) of the user who's rating the demon's difficulty

**levelID** - The ID of the demon being rated

**rating** - 1 for Easy Demon, 2 for Medium Demon, 3 for Hard Demon, 4 for Insane Demon and 5 for Extreme Demon.

### Optional Parameters

**gdw** - 0 

## Response

For Normal Players: Internal Server Error or returns `-1`.

For Moderators: Returns level ID.

## Example

<!-- tabs:start -->

### **Python - Normal Players**

```py
import requests

headers = {
}

data = {
    "secret": "Wmfp3897gc3",
    "levelID": 3979721,
    "rating": 5
}

req = requests.post('http://www.boomlings.com/database/rateGJDemon21.php', headers=headers, data=data)
print(req.text)
```

**Response**
```plain
-1
```

### **Python - Moderators**

```py
import requests

headers = {
}

data = {
    "gameVersion": 21,
    "binaryVersion": 35
    "accountID": 71,
    "gjp": *********, #the GJP of the moderator
    "secret": "Wmfp3897gc3",
    "levelID": 4284013,
    "rating": 3
}

req = requests.post('http://www.boomlings.com/database/rateGJDemon21.php', headers=headers, data=data)
print(req.text)
```

**Response**
```plain
4284013
```

<!-- tabs:end -->
