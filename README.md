# Dumpster

Set of scripts to take process/memory dumps on VMs.

## bulkProcdump.ps1
Takes proc dumps of all services in a given state.

Examples:


#### Take procdump(s) on all services with the `StopPending` state.
``` Powershell
bulkProcdump.ps1 -TargetStatus StopPending
```

#### Take procdump(s) on all services with the `StopPending` state. When done, kill the processes.
``` Powershell
bulkProcdump.ps1 -TargetStatus StopPending -ProcKill
```

#### Take procdump(s) on all services with the `StopPending` state. Runs Transcript of the script run.
``` Powershell
bulkProcdump.ps1 -TargetStatus StopPending -EnableLogging
```

### Target Status options:
- Stopped
- Running
- Paused
- StartPending
- StopPending
- ContinuePending
- PausePending
