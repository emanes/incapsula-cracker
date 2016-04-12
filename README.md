# Description

This module is used to wrap any request to a webpage blocked by incapsula.

# Usage

```
import incapsula
import requests

session = requests.Session()
response = session.get('http://example.com')  # url is blocked by incapsula
response = incapsula.crack(session, response)  # url is no longer blocked by incapsula
```

# Setup

There should be no problems using incapsula-cracker right out of the box.

If there are issues, try the following

* Open incapsula/serialize.html in browser
* Copy and paste the json data into incapsula/navigator.json

# Notes

* config.py, navigator.json, and serialize.html have all only been tested using firefox.
* currently incapsula only works with the requests library. 

I understand that there's minimal commenting and that's because I'm not sure exactly why incapsula is sending requests to certain pages other than to obtain cookies. This is just a literal reverse engineer of incapsulas javascript code.