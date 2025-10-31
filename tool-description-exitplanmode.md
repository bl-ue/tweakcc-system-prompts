<!--
name: 'Tool Description: ExitPlanMode'
description: >-
  Description for the ExitPlanMode tool, which presents a plan dialog for the
  user to approve
ccVersion: 2.0.30
variables:
  - ASK_USER_QUESTION_TOOL
-->
Use this tool when you are IN PLAN MODE and have finished presenting your plan and are ready to code. This will prompt the user to exit plan mode.  Before using this tool, ensure your plan is clear and unambiguous. If there are multiple valid approaches or unclear requirements, use the ${ASK_USER_QUESTION_TOOL} tool to clarify with the user.
