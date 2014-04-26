---
category: Samples
path: '/api/samples/submit/{sampleOrderID}'
title: 'Get Submitted Sample'
type: 'GET'

layout: nil
---

<div class="warning">
<b>JSON ONLY</b>: all features added 2014 and later only support JSON. XML support will be removed all together at some point in the future.
</div>

Get the order form data you submitted during <b>Submit Sample</b> for a Sample. This is the API version of clicking <b>View</b> for a Sample on the [History & Print Bar-Code Labels](https://submit.agvise.com/history) page

### Resource URI

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>{sampleOrderID}</td>
            <td>SampleOrderID of the Sample to return</td>
        </tr>
    </tbody>
</table>

### Response

Sends back the full details of the sample you sumbitted including the assigned SampleOrderID and sample ReferenceNumber

In order to return validiation messages, the response of this request is slightly different then the usualy way. The same ApiResponse object containing top level <em>data</em>  and <em>error</em> objects is returned for both success and failure. 

### Success

* `200 OK` on success,

```
{
    "data": {
        "sampleOrderID": 12345,
        "sampleOrderType": 2,
        ....
    }
    "error": null
}
```

### Error

Error responses are simply returning [standard HTTP error codes](http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html) along with some additional information:

```
{
    "data": null
    "error": {
        "message": "Failed to save sample data due to validation errors.",
        "validationErrors": [
            "Grower State is not a recognized value.",
            "PKApplication1 is not a recognized value.",
            "PhosphorusOption is not a recognized value.",
            "PreviousCrop is not a recognized value.",
            "AnalysisOptions is not a recognized value.",
            "AdditionalAnalysisOptions contains a value that is not recognized."
        ]
    }
}
```
