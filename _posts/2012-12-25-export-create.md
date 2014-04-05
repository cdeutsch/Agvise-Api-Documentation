---
category: Export
path: '/api/samples/export'
title: 'Create Export'
type: 'POST'

layout: nil
---

This method creates a request to export multiple Samples. 

### Parameters

<table>
	<thead>
		<tr>
	        <th>Parameter</th>
	        <th>Description</th>
	        <th>Required</th>
	        <th>Default</th>
	    </tr>
    </thead>
    <tbody>
    	<tr>
	        <td>year</td>
	        <td>Specifies the year to return Samples for.<br><br>Reference numbers aren't always unique across all years therefore this is required.</td>
	        <td>Yes</td>
	        <td> </td>
	    </tr>
	    <tr>
	        <td>account</td>
	        <td>The account number to export Samples for.</td>
	        <td> </td>
	        <td>defaults to the account associated with the ApiKey used</td>
	    </tr>
    	<tr>
	        <td>referenceNumbers</td>
	        <td>An Array of Reference Numbers to export samples for.</td>
	        <td> </td>
	        <td> </td>
	    </tr>
	    <tr>
	        <td>electronicIds</td>
	        <td>An Array of Electronic Ids to export samples for.</td>
	        <td> </td>
	        <td> </td>
	    </tr>
	    <tr>
	        <td>lastReferenceNumber</td>
	        <td>The last Reference Number you exported. All new Reference Numbers since the last one will be returned.</td>
	        <td> </td>
	        <td> </td>
	    </tr>
	    <tr>
	        <td>format</td>
	        <td>The format you want the data returned in: <em>xml</em> or <em>json</em></td>
	        <td> </td>
	        <td>defaults to the Request's format</td>
	    </tr>
	    <tr>
	        <td>statusCallbackUrl</td>
	        <td>The Url to POST to when the status of the Export changes. See <a href="#export-status">Get Export Status</a> for the format.</td>
	        <td> </td>
	        <td> </td>
	    </tr>
	    <tr>
	        <td>downloadCallbackUrl</td>
	        <td>The Url to POST the Sample data to when the Export finishes. See <a href="#export-download">Download Export</a> for the format.</td>
	        <td> </td>
	        <td> </td>
	    </tr>
    </tbody>
</table>

### Request

#### json

```
{
    "year": 2012,
	"account": "AA0001",
	"format": "json",
	"referenceNumbers": [ 1, 2 ],
	"statusCallbackUrl": "https://www.yoursite.com/agvise/export/status",
	"downloadCallbackUrl": "https://www.yoursite.com/agvise/export/download"
}
```

#### xml

```
<ExportRequest>
    <Year>2012</Year>
    <Account>AA0001</Account>
    <DownloadCallbackUrl>https://www.yoursite.com/agvise/export/download</DownloadCallbackUrl>
    <Format>xml</Format>
    <ReferenceNumbers>
        <ReferenceNumber>101</ReferenceNumber>
        <ReferenceNumber>102</ReferenceNumber>
    </ReferenceNumbers>
    <StatusCallbackUrl>https://www.yoursite.com/agvise/export/status</StatusCallbackUrl>
</ExportRequest>
```


### Response

Returns the Id of the Export.

```Status: 200 OK```

#### json

```
{
	"exportId": 226,
	"statusUrl": "http://submit.agvise.com/api/samples/export/status/62",
	"downloadUrl": "http://submit.agvise.com/api/samples/export/62"
}
```

#### xml

```
<Export>
    <ExportId>62</ExportId>
    <StatusUrl>http://submit.agvise.com/api/samples/export/status/62</StatusUrl>
    <DownloadUrl>http://submit.agvise.com/api/samples/export/62</DownloadUrl>
</Export>
```

For errors responses, see the [response status codes documentation](#response-status-codes).