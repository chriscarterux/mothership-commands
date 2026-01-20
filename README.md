# Mothership Commands for Claude Code

AI-driven development orchestration slash commands for [Claude Code](https://claude.ai/claude-code).

## Installation

Copy the contents of this repository to your Claude Code commands directory:

```bash
cp -r * ~/.claude/commands/mothership/
```

Or clone directly:

```bash
git clone https://github.com/chriscarterux/mothership-commands.git ~/.claude/commands/mothership
```

## Quick Start

```
/mothership:next      # See current phase and what to do next
/mothership:status    # View checkpoint state
/mothership:onboard   # Scan project and create codebase.md
```

## Core Workflow

Mothership follows a structured development cycle:

```
plan → build → test → review → deploy → done
  ↑                                       │
  └───────────────────────────────────────┘
```

Each phase has a dedicated agent:

| Phase | Command | Agent | Description |
|-------|---------|-------|-------------|
| Plan | `/mothership:plan` | Cipher | Create stories from feature description |
| Build | `/mothership:build` | Vector | Implement features |
| Test | `/mothership:test` | Cortex | Run and fix tests |
| Review | `/mothership:review` | Sentinel | Code quality review |

## All Commands

### Guidance
| Command | Description |
|---------|-------------|
| `/mothership` | Overview and help |
| `/mothership:next` | Smart guidance with current phase and recommendations |

### Core Loop
| Command | Description |
|---------|-------------|
| `/mothership:plan [feature]` | Create stories (Cipher agent) |
| `/mothership:build [story]` | Build features (Vector agent) |
| `/mothership:test [story]` | Run/fix tests (Cortex agent) |
| `/mothership:review [story]` | Code review (Sentinel agent) |
| `/mothership:status` | Show checkpoint state |
| `/mothership:onboard` | Scan project, create codebase.md |

### Checkpoint Management
| Command | Description |
|---------|-------------|
| `/mothership:checkpoint` | View/edit checkpoint state |
| `/mothership:checkpoint:next` | Advance to next workflow phase |

### Extended Agents
| Command | Agent | Description |
|---------|-------|-------------|
| `/mothership:deploy` | Pulse | Deployment pipeline |
| `/mothership:prioritize` | Nexus | Backlog prioritization |
| `/mothership:monitor` | Vigil | Production health monitoring |
| `/mothership:document` | Archive | Documentation generation |
| `/mothership:cleanup` | Purge | Tech debt removal |

### Enterprise
| Command | Agent | Description |
|---------|-------|-------------|
| `/mothership:resolve` | Arbiter | Conflict resolution |
| `/mothership:orchestrate` | Conductor | Blue-green/canary deployments |
| `/mothership:coordinate` | Coalition | Multi-team coordination |
| `/mothership:secrets` | Vault | Secrets management |
| `/mothership:metrics` | Telemetry | DORA metrics & analytics |

## Checkpoint File

Mothership tracks workflow state in `.mothership/checkpoint.md`:

```yaml
phase: build
project: My Project
branch: feat/my-feature
story: STORY-001
```

## Agents

| Agent | Role | Specialty |
|-------|------|-----------|
| **Cipher** | Planning | Decodes requirements into atomic stories |
| **Vector** | Building | Implements code with precision |
| **Cortex** | Testing | Analyzes behavior through comprehensive tests |
| **Sentinel** | Review | Guards code quality |
| **Pulse** | Deploy | Sends deployment signals |
| **Nexus** | Prioritize | Central coordination for backlog |
| **Vigil** | Monitor | Vigilant production watch |
| **Archive** | Document | Stores and organizes knowledge |
| **Purge** | Cleanup | Removes obsolete code and tech debt |
| **Arbiter** | Resolve | Detects and resolves conflicts |
| **Conductor** | Orchestrate | Manages complex deployments |
| **Coalition** | Coordinate | Multi-team coordination |
| **Vault** | Secrets | Secure secrets management |
| **Telemetry** | Metrics | Analytics and reporting |

## Getting Started

### New Project

```
/mothership:onboard              # Scan project structure
/mothership:plan "user auth"     # Create your first stories
/mothership:build                # Start building
```

### Existing Project with Checkpoint

```
/mothership:next                 # See what to do next
```

## Directory Structure

```
~/.claude/commands/mothership/
├── SKILL.md              # Main /mothership command
├── next.md               # /mothership:next
├── plan.md               # /mothership:plan
├── build.md              # /mothership:build
├── test.md               # /mothership:test
├── review.md             # /mothership:review
├── status.md             # /mothership:status
├── onboard.md            # /mothership:onboard
├── deploy.md             # /mothership:deploy
├── prioritize.md         # /mothership:prioritize
├── monitor.md            # /mothership:monitor
├── document.md           # /mothership:document
├── cleanup.md            # /mothership:cleanup
├── resolve.md            # /mothership:resolve
├── orchestrate.md        # /mothership:orchestrate
├── coordinate.md         # /mothership:coordinate
├── secrets.md            # /mothership:secrets
├── metrics.md            # /mothership:metrics
└── checkpoint/
    ├── SKILL.md          # /mothership:checkpoint
    └── next.md           # /mothership:checkpoint:next
```

## Related

- [Mothership Core](https://github.com/chriscarterux/Mothership---Core) - The shell script orchestrator
- [Claude Code](https://claude.ai/claude-code) - Anthropic's CLI for Claude

## License

MIT
