# Eventstock -- Shared Server Setup

## What this is

A portfolio project built alongside a Linux for DevOps course, structured as a real scenario instead of isolated command practice: setting up a shared Linux server for a small event production company.

This is a fictional practice exercise inspired by the world of real event production work, not actual company infrastructure or data. Every person, file, and figure here was made up for this project.

## The team

- **Tunde** -- Production Coordinator
- **Chioma** -- Content Lead
- **Yusuf** -- Social Media Assistant
- **Emeka** -- Client Relations
- **Funmi** -- Admin & Finance

## Structure

```
/srv/eventstock/
├── production/
├── content/
├── ops/
├── finance/
└── shared/
```

One folder per department, plus a shared folder everyone needs access to. Each one is populated with realistic working files, run sheets, invoices, content calendars, instead of empty placeholders, so navigating and organizing them actually means something.

## Why this structure

Departments get their own folder so only the relevant team can read or write to it, Funmi's invoices aren't visible to Yusuf, and vice versa. The shared folder exists because not everything belongs to one department, the company handbook and holiday schedule are things everyone needs regardless of role.

## Status

- [x] Directory structure created
- [x] Departments populated with realistic working files
- [x] Users and groups created per department (Tunde/production, Chioma+Yusuf/content, Emeka/ops, Funmi/finance)
- [x] Permissions locked down: department folders owned by their group with SGID set (new files inherit the group automatically), sticky bit on `shared/` (everyone can write, only owners can delete)
- [x] Access control verified by testing as a restricted user: denied entry to folders outside the department, allowed into the correct one
- [ ] Process/monitoring scenario
- [ ] SSH key-based access, basic firewall rules
- [ ] Automated backup via cron

This file gets updated as each phase gets built, including what broke and what had to be fixed, not just the finished state.
