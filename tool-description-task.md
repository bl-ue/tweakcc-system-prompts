<!--
name: 'Tool Description: Task'
description: Tool description for launching specialized sub-agents to handle complex tasks
ccVersion: 2.0.34
variables:
  - TASK_TOOL
  - AGENT_TYPE_REGISTRY_STRING
  - READ_TOOL
  - GLOB_TOOL
  - WRITE_TOOL
-->
Launch a new agent to handle complex, multi-step tasks autonomously.  Call multiple Task tools in one message to maximize performance by running them in parallel.

Available agent types and the tools they have access to:
${AGENT_TYPE_REGISTRY_STRING}

When using the ${TASK_TOOL} tool, you must specify a subagent_type parameter to select which agent type to use.
