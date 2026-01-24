# McRalph

Autonomous AI agent system combining multiple context engineering patterns.

@README.md
@AGENTS.md

---

## Integrated Systems

### 1. Bart & Ralph (Core)
Master agents for planning and execution.

```
/bart new              # Start planning
/bart research         # Research codebase
/bart requirements     # Define stories
/bart create-prd       # Generate prd.json

/ralph                 # Execute stories
/ralph status          # Show progress
/ralph retry US-XXX    # Retry failed
```

### 2. Brain-Wave (Memory)
Persistent context across sessions.

```
use brain-wave-init agent    # Initialize memory
use alpha-wave agent         # Index files
use beta-wave agent          # Create maps
use rem agent                # Sync sessions
```

### 3. Planning-with-Files (Workflow)
Manus-style markdown planning.

```
/planning-with-files         # Start persistent planning
```

Creates:
- `task_plan.md` - Phases & progress
- `findings.md` - Research & discoveries
- `progress.md` - Session logs

### 4. Get-Shit-Done Agents (Specialists)
Parallel research and execution agents.

| Agent | Purpose |
|-------|---------|
| `gsd-project-researcher` | Investigate stack & features |
| `gsd-phase-researcher` | Phase-specific research |
| `gsd-planner` | Create atomic task plans |
| `gsd-plan-checker` | Verify plans |
| `gsd-executor` | Execute tasks |
| `gsd-verifier` | Verify completion |
| `gsd-debugger` | Diagnose failures |
| `gsd-codebase-mapper` | Map codebase structure |

---

## Recommended Workflow

### New Project
```
1. use brain-wave-init agent     # Set up memory
2. /bart new                      # Plan features
3. /ralph                         # Execute stories
4. use rem agent                  # Sync context
```

### Complex Tasks
```
1. /planning-with-files           # Start tracked planning
2. [work through phases]
3. use rem agent                  # Capture session
```

### Research Heavy
```
1. use gsd-project-researcher     # Deep codebase analysis
2. use gsd-planner                # Create atomic tasks
3. use gsd-executor               # Execute in parallel
```

---

## Key Files

| File | Purpose |
|------|---------|
| `prd.json` | Project requirements |
| `progress.txt` | Learnings (append-only) |
| `skills/ralph-master/` | Ralph orchestrator |
| `skills/bart/` | Bart planning |
| `skills/planning-with-files/` | Persistent planning |
| `skills/gsd/` | Get-Shit-Done agents |
| `.claude/agents/` | Brain-Wave agents |

---

## Memory Folders (after brain-wave-init)

- `alpha-wave/` - File indexes
- `beta-wave/` - Architecture maps
- `rem/` - Sessions & discoveries

---

## Sources

- [Ralph Pattern](https://ghuntley.com/ralph/) - Master/worker architecture
- [Get Shit Done](https://github.com/glittercowboy/get-shit-done) - Multi-agent orchestration
- [Planning with Files](https://github.com/OthmanAdi/planning-with-files) - Filesystem persistence
- [Brain-Care](https://github.com/agentmcmillan/Claude-Brain-Care) - Session memory

## Project Notes

[Add project-specific notes here]
