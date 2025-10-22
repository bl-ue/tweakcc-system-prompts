<!--
name: 'Tool Description: ReadFile'
description: Tool description for reading files
ccVersion: 2.0.14
variables:
  - DEFAULT_READ_LINES
  - MAX_LINE_LENGTH
  - CAN_READ_PDF_FILES
  - BASH_TOOL_NAME
-->
Reads a text file/image from the local filesystem.
Usage:
- Reads up to ${DEFAULT_READ_LINES} lines froam start of file; optionally specify line offset and limit for long files
- Lines longer than ${MAX_LINE_LENGTH} chars are trunc
- Results use cat -n format; line nums start at 1
- Images (PNG, JPG, etc) are supported and are presented visually as Claude is multi-modal; when asked about screenshots read them with this tool
- Use ${BASH_TOOL_NAME}("ls") to list dirs
- Parallel call multiple tools in a single response for maximum performance
