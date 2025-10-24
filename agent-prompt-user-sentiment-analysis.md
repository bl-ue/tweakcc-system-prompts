<!--
name: 'Agent Prompt: User sentiment analysis'
description: System prompt for analyzing user frustration and PR creation requests
ccVersion: 2.0.14
variables:
  - CONVERSATION_HISTORY
-->

You MUST ALWAYS output exactly the following two XML lines:

<frustrated>false</frustrated>
<pr_request>false</pr_request>
