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

```
[
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
    },
    {
        "id": 845,
        "referenceNumber": 10001,
        "labNumber": "AA0001",
        "labBoxNumber": 0,
        "gridNumber": 70,
        "sampleDescription": "5",
        "fertilizerGuideline1": null,
        "fertilizerGuideline2": null,
        "fertilizerGuideline3": null
    }
]
```

#### xml

```
<SampleExports>
    <SampleExport>
        <Id>844</Id>
        <ReferenceNumber>10001</ReferenceNumber>
        <LabNumber>AA0001</LabNumber>
        <LabBoxNumber>0</LabBoxNumber>
        <GridNumber>70</GridNumber>
        <SampleDescription>4</SampleDescription>
    </SampleExport>
    <SampleExport>
        <Id>845</Id>
        <ReferenceNumber>10002</ReferenceNumber>
        <LabNumber>AA0001</LabNumber>
        <LabBoxNumber>0</LabBoxNumber>
        <GridNumber>70</GridNumber>
        <SampleDescription>5</SampleDescription>
    </SampleExport>
</SampleExports>
```

For errors responses, see the [response status codes documentation](#response-status-codes).