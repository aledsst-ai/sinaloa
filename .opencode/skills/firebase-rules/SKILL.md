---
name: firebase-rules
description: Update and manage Firebase Realtime Database security rules for the Sinaloa project
---

## Rules file
- Located at `database.rules.json` in the project root

## Email domain rule
- All authenticated users must have `@sinaloa.app` email domain
- The `emailDomain` validation rule is:
  ```json
  "auth.token.email.matches('.*@sinaloa.app$')"
  ```

## Data structure
- All app data lives under the `sinaloa-data` node:
  - `sinaloa-data/membros`
  - `sinaloa-data/viaturas`
  - `sinaloa-data/apreensoes`
  - `sinaloa-data/user-info`
- Rules outside `sinaloa-data` (e.g. `users`, `rocam-data` nodes) are wide open for backward compatibility

## Backup rule
- Before editing `database.rules.json`, suggest copying the current rules from the Firebase Console as a backup
- After editing, remind the user to upload the rules via Firebase Console → Realtime Database → Rules

## Auth
- Auth providers: Email/Password only
- Accounts: admin@sinaloa.app, membros@sinaloa.app (and others as needed)
