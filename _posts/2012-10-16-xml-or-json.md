---
title: 'XML or JSON'

layout: nil
---

The API uses XML by default but also supports Content Negotiation. For best results (especially when using Json), always set both the *Accept* and *Content-Type* headers in your requests.

- To indicate what format of data your are submitting, set the *Content-Type* of the Request to either *application/json* or *application/xml*

- To indicate what format of data you want in the Response, set the *Accept* header in the Request to either *application/json* or *application/xml*

- Alternatively, to indicate what format of data you want in the Response, append a *.json* or *.xml* extension to any url. Example: **/api/samples/export/45.json**