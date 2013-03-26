---
category: Export
path: '/api/samples/export/status/{exportId}'
title: 'Get Export Status Detail'
type: 'GET'

layout: nil
---

Returns the status of an export

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

Sends back the status of the Export

<table>
	<thead>
		<tr>
	        <th>Parameter</th>
	        <th>Description</th>
	    </tr>
    </thead>
    <tbody>
	    <tr>
	        <td>status</td>
	        <td>Status of the Export: <em>waiting</em>, <em>processing</em>, <em>finished</em>, or <em>failed</em> </td>
	    </tr>
	    <tr>
	        <td>message</td>
	        <td>Details on the status. If the status is <em>failed</em> this will contain details about the error.</td>
	    </tr>
    </tbody>
</table>


```Status: 200 OK```

#### json

```{
	"exportId": 226,
	"status": "Waiting",
	"message": "Export is waiting",
	"downloadUrl": "http://submit.agvise.com/api/samples/export/226"
}```

#### xml

```<ExportStatus>
    <ExportId>64</ExportId>
    <Status>Finished</Status>
    <Message>Export is finished</Message>
    <DownloadUrl>http://submit.agvise.com/api/samples/export/64</DownloadUrl>
</ExportStatus>```

For errors responses, see the [response status codes documentation](#response-status-codes).