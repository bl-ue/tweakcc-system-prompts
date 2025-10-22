<!--
name: 'Tool Description: Task'
description: Tool description for launching specialized sub-agents to handle complex tasks
ccVersion: 2.0.14
variables:
  - AGENT_TYPE_REGISTRY
  - agentTypeEntry
  - propertiesText
  - runsInBackground
  - hasAccessToCurrentContext
  - TOOL_REGISTRY
  - READ_TOOL
  - GLOB_TOOL
  - TASK_TOOL
  - WRITE_TOOL
-->
Launch a new agent to handle complex, multi-step tasks autonomously.  Call multiple Task tools in one message to maximize performance by running them in parallel.

Available agent types and the tools they have access to:
${AGENT_TYPE_REGISTRY.map((agentTypeEntry)=>{let propertiesText="";if(agentTypeEntry?.runsInBackground||agentTypeEntry?.hasAccessToCurrentContext)propertiesText="Properties: "+(agentTypeEntry?.runsInBackground?"runs in background; ":"")+(agentTypeEntry?.hasAccessToCurrentContext?"access to current context; ":"");return`- ${agentTypeEntry.agentType}: ${agentTypeEntry.whenToUse} (${propertiesText}Tools: ${agentTypeEntry.tools.join(", ")})`}).join(`
`)}

When using the ${TOOL_REGISTRY} tool, you must specify a subagent_type parameter to select which agent type to use.
