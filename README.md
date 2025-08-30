# bindump

Binary deployment and persistence script for Windows environments. Uses NetExec (formerly CrackMapExec) to deploy binaries across multiple Windows hosts with persistence mechanisms.

## What it does

**win_bindump.sh** - Automated binary deployment script:
- Downloads Windows host list from GitHub repository
- Deploys binaries via HTTP download to Windows targets
- Configures persistence through multiple methods:
  - Windows Services (with failure recovery)
  - Scheduled Tasks (runs every 15 minutes as SYSTEM)
  - Registry keys (Run/RunOnce entries)
- Uses NetExec for SMB authentication and PowerShell execution
- Supports creating target directories if they don't exist

## Features

- Interactive prompts for deployment configuration
- Multiple persistence mechanism options
- Automatic binary unblocking on target systems
- Service failure recovery configuration
- Registry key preservation options
- Batch deployment across host lists

## Usage

```bash
chmod +x win_bindump.sh
./win_bindump.sh

# Follow prompts to configure:
# - Binary location (HTTP URL)
# - Target credentials
# - Deployment path and filename
# - Persistence method (service/task/registry)
```

## Requirements

- NetExec (formerly CrackMapExec)
- Valid Windows credentials for target hosts
- HTTP server hosting the binary to deploy

---
*For authorized penetration testing and red team operations only*
