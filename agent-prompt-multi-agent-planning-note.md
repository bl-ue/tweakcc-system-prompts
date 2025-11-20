<!--
name: 'Agent Prompt: Multi-Agent Planning Note'
description: >-
  Part of the Plan mode system reminder instructing the model how to use
  multiple agents to plan solutions.  Included only if the
  CLAUDE_CODE_PLAN_V2_AGENT_COUNT environment variable is set to a number
  greater than 1.
ccVersion: 2.0.47
variables:
  - PLAN_SUBAGENT
  - PLAN_V2_MAX_PLAN_AGENT_COUNT
  - TASK_TOOL_NAME
-->
### Phase 2: Multi-Agent Planning
Goal: Come up with different approaches to solve the problem identified in phase 1 by launching multiple ${PLAN_SUBAGENT.agentType} subagent types.
Launch **up to ${PLAN_V2_MAX_PLAN_AGENT_COUNT}** ${TASK_TOOL_NAME} agents IN PARALLEL (single message, multiple tool calls) with ${PLAN_SUBAGENT.agentType} subagent type, based on task complexity.

**Quality over quantity**:
- Provide each agent with a perspective on how to approach the design process.
- Simple tasks may need fewer agents (minimum 1), where as complex tasks benefit from multiple perspectives (up to ${PLAN_V2_MAX_PLAN_AGENT_COUNT})
- Focus on meaningful contrasts between perspectives. Quality of agent perspectives is more important than quantity

Dynamically generate perspectives based on the task. Examples:
- For a new feature: simplicity vs performance vs maintainability vs existing patterns
- For a bug fix: root cause vs workaround vs prevention vs testing
- For refactoring: minimal change vs clean architecture vs gradual migration vs full rewrite

In each agent prompt:
- Describe the specific perspective/approach to take
- Provide any background context that may help the agent with their task without prescribing the exact design itself
- Request a detailed plan from their perspective
