---
category: Export
path: '/api/samples/export/status'
title: 'Get All Exports Statuses'
type: 'GET'

layout: nil
---

Returns a list of all exports and their statuses

### Response

Sends back the status of each Export

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

```
[{
	"exportId": 47,
	"status": "Finished",
	"message": "Export is finished",
	"downloadUrl": "https://submit.agvise.com/api/samples/export/47"
},
{
	"exportId": 48,
	"status": "Waiting",
	"message": "Export is waiting",
	"downloadUrl": "https://submit.agvise.com/api/samples/export/48"
}]
```

#### xml

```
<ExportStatuses>
    <ExportStatus>
        <ExportId>47</ExportId>
        <Status>Finished</Status>
        <Message>Export is finished</Message>
        <DownloadUrl>https://submit.agvise.com/api/samples/export/47</DownloadUrl>
    </ExportStatus>
    <ExportStatus>
        <ExportId>48</ExportId>
        <Status>Waiting</Status>
        <Message>Export is waiting</Message>
        <DownloadUrl>https://submit.agvise.com/api/samples/export/48</DownloadUrl>
    </ExportStatus>
</ExportStatuses>
```

For errors responses, see the [response status codes documentation](#response-status-codes).