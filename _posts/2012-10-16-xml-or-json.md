---
title: 'XML or JSON'

layout: nil
---

The API uses XML by default but also supports Content Negotiation using the following methods.

1. Set the *Accept* header in the Request to either *application/json* or *application/xml*

2. Set the *Content-Type* of the Request to either *application/json* or *application/xml*

3. Append a *.json* or *.xml* extension to any url. Example: **/api/samples/export/45.json**