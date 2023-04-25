---
title: How to validate a POST API using Python Requests
author: mohit
type: post
date: 2022-01-20T04:50:00+00:00
draft: true
url: /?p=2570
categories:
  - Python
tags:
  - api
  - json
  - post
  - python

---
You can use the Python requests to validate a POST API during development. This can be done as follows

You can use json document to supply the various parameters in the body.

Please note that for that you need to set the headers to correct value.

<pre><code class="language-python">import json
import requests

r = requests.post(
    "&lt;Post URL&gt;",
    data=json.dumps({
    "key1": "value1",
    "key2": "value2",
    "key3": "value3"
    }),
    headers={"Content-Type": "application/json"},
)
</code></pre>