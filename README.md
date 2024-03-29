# Dumpster

Set of scripts to take process/memory dumps on VMs.

# bulkProcdump.ps1
Takes proc dumps of all services in a given state. By default, the output is dumped to the local directory.

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

<br>


## Parameters
| Param | Description | Default |
| --- | --- | --- |
| `-TargetStatus` | The target status for services to be in scope for the script. | |
| `-ProcKill` | Kills processes after the dumps have been collected. | `$False` |
| `-EnableLogging` | Takes Powershell transcript of the script execution | `$False` |
| `-OutputDir` | Custom output directory for the memory dumps. | `$PWD/ProcDump` |



#### `-TargetStatus` options :
- Stopped
- Running
- Paused
- StartPending
- StopPending
- ContinuePending
- PausePending