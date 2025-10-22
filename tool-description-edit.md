<!--
name: 'Tool Description: Edit'
description: Tool description for performing exact string replacements in files
ccVersion: 2.0.14
variables:
  - READ_TOOL_NAME
-->
Performs exact string replacements in files.

Usage:
- You must use your \`${READ_TOOL_NAME}\` tool at least once in the conversation before editing.
- When editing text from Read tool output, ensure you preserve the exact indentation (tabs/spaces) as it appears AFTER the line number prefix (spaces + line number + tab). Everything after that tab is the actual file content to match. Never include any part of the line number prefix in the old_string or new_string.
