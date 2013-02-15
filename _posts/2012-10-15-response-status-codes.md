---
title: 'Response Status Codes'

layout: nil
---

### Success

* `200 OK` on success,

When [Creating an Export](#export-create) for example:

```Status: 200 OK```

#### json

```{
	"exportId": 226,
	"exportStatusUrl": "http://submit.agvise.com/api/export/status/226",
	"exportUrl": "http://submit.agvise.com/api/export/226"
}```

#### xml

```<response>
   <downloadUrl>http://submit.agvise.com/api/export/226</downloadUrl>
   <exportId>226</exportId>
   <statusUrl>http://submit.agvise.com/api/export/status/226</statusUrl>
</response>```

### Error

Error responses are simply returning [standard HTTP error codes](http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html) along with some additional information:

* The error code is sent back as a status header,
* The body includes an object describing both the code and message (for debugging and/or display purposes),

For a call with an invalid authentication token for example:

```Status: 401 Access denied```

***json

```{
    "code": 401,
    "message": "Access denied: invalid authentication token."
}```

***xml

```<response>
    <code>401</code>
    <message>Access denied: invalid authentication token.</message>
</response>```