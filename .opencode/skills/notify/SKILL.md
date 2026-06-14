---
name: notify
description: Play a Windows notification sound and show a toast after completing a task
---

## Instructions
After finishing the requested task, run this PowerShell command to notify the user:

```powershell
[System.Media.SystemSounds]::Asterisk.Play()
```

This plays the standard Windows asterisk sound through the system speakers.

The last message to the user should always be: "✅ {resumo do que foi feito} + 🔔"
