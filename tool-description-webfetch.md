<!--
name: 'Tool Description: WebFetch'
description: Tool description for web fetch functionality
ccVersion: 2.0.14
-->

Retrieve and analyze web content from a URL (processed with AI)
- URL must a fully-formed
- HTTP is automatically upgraded to HTTPS
- Prompt must describe what information you want to extract from the page
- Responses are cached 15-minutes - be aware of this when making multiple requests
- On a redirect, make a new WebFetch request to it
