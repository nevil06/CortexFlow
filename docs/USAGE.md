# Usage Guide

## Overview

CortexFlow enables AI agents to share context. One AI plans, another executes.

## Typical Workflow

### 1. Planning Phase (ChatGPT/Gemini)

```
User: "Plan a REST API for user authentication"

ChatGPT calls write_context:
- Creates project with tasks
- Adds planning notes
- Sets phase to "execution"
```

### 2. Execution Phase (Claude Code/Cursor)

```
User: "Continue the auth API project"

Claude Code calls read_context:
- Reads all tasks and notes
- Understands the plan
- Starts implementing
```

### 3. Progress Updates

```
Claude Code calls:
- update_task: Mark task in_progress
- add_note: Document decisions
- mark_task_complete: Finish tasks
```

### 4. Review Phase

```
Any AI can:
- read_context: Check progress
- add_note: Leave feedback
- set_phase: Move to review/completed
```

## Running Modes

### MCP Mode (Default)
For Claude Code, Cursor, VS Code:
```bash
cortexflow
```

### HTTP Mode
For ChatGPT, web clients:
```bash
cortexflow --http
```

### Both Modes
```bash
cortexflow --both
```

## Agent Roles

| Role | Purpose | Typical AI |
|------|---------|------------|
| Planner | Design, architecture, task breakdown | ChatGPT, Gemini |
| Executor | Implementation, coding | Claude Code, Cursor |
| Reviewer | Testing, validation | Any AI |

## Note Categories

- **general**: General observations
- **decision**: Design/architecture decisions
- **blocker**: Issues blocking progress
- **insight**: Discoveries or learnings

## Task Statuses

- **pending**: Not started
- **in_progress**: Currently being worked on
- **blocked**: Waiting on something
- **completed**: Done
- **cancelled**: No longer needed

## Tips

1. **Be descriptive**: Good task titles help other AIs understand quickly
2. **Use notes liberally**: Document decisions for context
3. **Update status promptly**: Keeps all agents in sync
4. **Use priorities**: 1 = highest, 5 = lowest
