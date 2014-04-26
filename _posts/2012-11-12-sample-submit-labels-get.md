---
category: Samples
path: '/api/samples/submit/labels/{sampleOrderID}'
title: 'Get Sample Labels'
type: 'GET'

layout: nil
---

<div class="warning">
<b>JSON ONLY</b>: all features added 2014 and later only support JSON. XML support will be removed all together at some point in the future.
</div>

Gets the labels in PDF format for the Sample Orders specified. This is the API version of clicking <b>Print Barcoded Labels for Selected Fields</b> for the selected Samples on the [History & Print Bar-Code Labels](https://submit.agvise.com/history) page

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

### Alernative Resource URI

<table>
    <thead>
        <tr>
            <th>Parameter</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="white-space:nowrap;">?id=1&amp;id=2&amp;id=3</td>
            <td>
                Alternative you can drop the ID from the path of the url like this <em>/api/samples/submit/labels/</em> and use the query string to specify multiple SampleOrderIDs.
            </td>
        </tr>
    </tbody>
</table>

### Response

If successful, it returns a PDF of the labels for the SampleOrderIDs specified .

### Success

* `200 OK` on success,

PDF in binary format.

### Error

Error responses are simply returning [standard HTTP error codes](http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html) along with some additional information:

```
{
    "data": null
    "error": {
        "message": "Failed to create PDF labels."
    }
}
```
