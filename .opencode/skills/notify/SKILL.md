---
name: notify
description: Play a Windows notification sound and show a toast after completing a task
---

## Instructions
After finishing the requested task, run this PowerShell command to notify the user:

```powershell
[System.Console]::Beep(1200, 150); Start-Sleep -Milliseconds 100; [System.Console]::Beep(1800, 200)
```

This plays a sharp two-tone beep (1200Hz → 1800Hz) that is easily distinguishable.

The last message to the user should always be: "✅ {resumo do que foi feito} + 🔔"
