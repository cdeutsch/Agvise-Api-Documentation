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
	        <td>account</td>
	        <td>The account number to export Samples for.</td>
	        <td>Yes</td>
	        <td> </td>
	    </tr>
    	<tr>
	        <td>year</td>
	        <td>Returns all Samples for a given year.</td>
	        <td> </td>
	        <td> </td>
	    </tr>
    	<tr>
	        <td>ids</td>
	        <td>An Array of Reference Numbers to export.</td>
	        <td> </td>
	        <td> </td>
	    </tr>
	    <tr>
	        <td>lastId</td>
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

```{
	"account": "AA0001",
	"format": "json",
	"ids": [ 1, 2 ],
	"statusCallbackUrl": "https://www.yoursite.com/agvise/export/status",
	"downloadCallbackUrl": "https://www.yoursite.com/agvise/export/download"
}```

#### xml

```<request>
   <account>AA0001</account>
   <downloadCallbackUrl>https://www.yoursite.com/agvise/export/download</downloadCallbackUrl>
   <format>xml</format>
   <ids>
      <id>1</id>
      <id>2</id>
   </ids>
   <statusCallbackUrl>https://www.yoursite.com/agvise/export/status</statusCallbackUrl>
</request>```


### Response

Returns the Id of the Export.

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

For errors responses, see the [response status codes documentation](#response-status-codes).