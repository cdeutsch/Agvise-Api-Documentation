---
category: Export
path: '/api/samples/{year}/{referenceNumber}'
title: 'Get Sample'
type: 'GET'

layout: nil
---

This method returns the test results of a single Sample.

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
	        <td>{year}</td>
	        <td>Year of the Reference Number for the Sample to return</td>
	    </tr>
	    <tr>
	        <td>{referenceNumber}</td>
	        <td>Reference Number of the Sample to return</td>
	    </tr>
    </tbody>
</table>

### Response

Sends back a sample

```Status: 200 OK```

#### json

```
{
    "id": 844,
    "referenceNumber": 10001,
    "labNumber": "AA0001",
    "labBoxNumber": 0,
    "gridNumber": 70,
    "sampleDescription": "4",
    "fertilizerGuideline1": null,
    "fertilizerGuideline2": null,
    "fertilizerGuideline3": null
}
```

#### xml

```
<SampleExport>
    <Id>844</Id>
    <ReferenceNumber>10001</ReferenceNumber>
    <LabNumber>AA0001</LabNumber>
    <LabBoxNumber>0</LabBoxNumber>
    <GridNumber>70</GridNumber>
    <SampleDescription>4</SampleDescription>
</SampleExport>
```

For errors responses, see the [response status codes documentation](#response-status-codes).