---
category: Export
path: '/api/samples/export/{exportId}'
title: 'Download Export'
type: 'GET'

layout: nil
---

This method returns the Sample data created by the Export.

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
	        <td>{exportId}</td>
	        <td>ExportId returned by the POST to <a href="#samples">/api/samples/export</a></td>
	    </tr>
    </tbody>
</table>


### Response

Sends back a sample

```Status: 200 OK```

#### json

```{
	"samples": [
		{
			"sample": {
				"ReferenceNumber": 1
			}
		},
		{
			"sample": {
				"ReferenceNumber": 2
			}
		}
	]
}```

#### xml

```<response>
   <samples>
      <element>
         <sample>
            <ReferenceNumber>1</ReferenceNumber>
         </sample>
      </element>
      <element>
         <sample>
            <ReferenceNumber>2</ReferenceNumber>
         </sample>
      </element>
   </samples>
</response>```

For errors responses, see the [response status codes documentation](#response-status-codes).