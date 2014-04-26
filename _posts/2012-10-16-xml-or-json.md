---
title: 'XML or JSON'

layout: nil
---

<div class="warning">
<b>IMPORTANT: We're moving to JSON only</b> <br />
Only the Export functionality support XML. <br />
Features added 2014 and later only support JSON. <br />
XML support will be removed all together at some point in the future.
</div>

The API uses XML by default but also supports Content Negotiation. For best results (especially when using Json), always set both the *Accept* and *Content-Type* headers in your requests.

- To indicate what format of data your are submitting, set the *Content-Type* of the Request to either *application/json* or *application/xml*

- To indicate what format of data you want in the Response, set the *Accept* header in the Request to either *application/json* or *application/xml*

- Alternatively, to indicate what format of data you want in the Response, append a *.json* or *.xml* extension to any url. Example: **/api/samples/export/45.json**