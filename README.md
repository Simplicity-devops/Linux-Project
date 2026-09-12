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

Departments get their own folder because the next phase of this project locks each one down so only the relevant team can read or write to it. Funmi's invoices shouldn't be visible to Yusuf, and vice versa. The shared folder exists because not everything belongs to one department, the company handbook and holiday schedule are things everyone needs regardless of role.

## Status

- [x] Directory structure created
- [x] Departments populated with realistic working files
- [ ] Users and groups per department
- [ ] Permissions locked down, including SGID on department folders and the sticky bit on `shared/`
- [ ] Process/monitoring scenario
- [ ] SSH key-based access, basic firewall rules
- [ ] Automated backup via cron

This file gets updated as each phase gets built, including what broke and what had to be fixed, not just the finished state.
