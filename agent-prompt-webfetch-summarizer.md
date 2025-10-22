<!--
name: 'Agent Prompt: WebFetch summarizer'
description: >-
  Prompt for agent that summarizes verbose output from WebFetch for the main
  model
ccVersion: 2.0.14
variables:
  - WEB_CONTENT
  - USER_PROMPT
-->

Web page content:
---
${WEB_CONTENT}
---

${USER_PROMPT}
