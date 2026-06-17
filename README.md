# Kappture Terminal Checks

Browser-based tool for analysing Kappture Terminal Status and Session Activity exports, generating operational reports, and supporting daily venue checks.

---

## Overview

Kappture Terminal Checks is a single-page, browser-based utility designed to streamline daily EPOS health checks across ATG venues.

It allows users to import Kappture CSV exports, identify actionable issues, manage exclusions, generate venue emails, and produce structured Daily and Weekly reporting — all within the browser.

The tool runs entirely client-side with no backend, installation, or external dependencies required.

---

## Features

### Import & Processing
- Import **Terminal Status CSV**
- Import **Terminal Session Activity CSV**
- Process both datasets together into a unified dataset
- Apply filtering rules to identify actionable issues:
  - Offline terminals (filtered by platform and rules)
  - Previous-day open sessions

---

### Review & Workflow
- Identify:
  - Offline terminals
  - Previous-day open sessions
- Temporarily suppress issues using **Ignore today**
- Restore issues using **Include again**
- Review section optimised for high-volume daily checks
- Stable scrolling behaviour for efficient bulk handling

---

### Reporting

#### In-app Reporting
- Daily Report per venue
- Weekly Report across multiple days
- Manual override system with automatic fallback to imported data
- Source tracking:
  - Imported data
  - Venue Management exclusions
  - Manual overrides

#### Excel Reporting Workbook (.xlsx)
Export a full Reporting Workbook including:

- **Ongoing Weekly Report**
  - Checkbox-based (native Excel checkboxes)
  - Tracks issues across multiple weeks

- **Issue Trends**
  - Top venues with recurring issues
  - Top terminals with recurring issues
  - 7 / 14 / 30 / 180 day views

- **Daily Detail**
  - Per-venue breakdown for selected day

- **Notes Detail**
  - Venue Management exclusions and notes

- **Issue Detail**
  - Combined issue history across runs

---

### Email Generation

- Generate emails based on included issues
- Per-venue email output with:
  - Subject
  - Body
  - To / CC / BCC
- One-click:
  - Copy To / CC / Body / Subject
  - Open in Outlook
- Track sent status per day

#### Email Groups
- Group multiple venues into a single email
- Example:
  - Opera House Manchester + Palace Theatre Manchester → one email
- Group features:
  - Combined issue output by venue
  - Group-level To / CC / BCC
  - Optional fallback to merged venue contacts
- Prevents duplicate emails for linked venues

---

### Venue Management

- Configure inclusion/exclusion at:
  - Venue level
  - Outlet level
  - Terminal level
- Hierarchical checkbox logic:
  - Parent states derived from children
  - Partial (-) state supported
- Store:
  - Email contacts (To / CC / BCC)
  - Notes per venue
- Visual hierarchy with connector lines

---

### Tool Configuration

- Export Tool Config as JSON (selective)
- Import Tool Config with preview and section selection

Config sections:
- Venue structure & exclusions
- Email contacts
- Venue notes
- Email groups
- Platform settings
- Email template
- Data control settings

---

### Settings

- Manage included Status platforms
- Configure Email Template:
  - Greeting
  - Intro
  - Section headings
  - Sign-off
- Data control rules:
  - Exclude "DO NOT DELETE"
  - Exclude blank Last Connection
  - Include outlet name in emails

---

### Data & Safety

- All data is processed **locally in the browser**
- No data is sent externally
- No backend or API usage
- Clear All Saved Data uses a **hold-to-confirm safety control**

---

### UI / UX

- Fully browser-based (no install required)
- Responsive layout (desktop and mobile)
- Optimised for:
  - Office wallboard displays
  - Laptop use
  - Mobile quick checks
- Consistent card-based UI
- Fixed background gradient for visual consistency
- Clear button hierarchy and workflow guidance

---

## Version

Current version: **v2.6.4**

---

## Known Limitations

- Data is stored locally in the browser:
  - Not shared between users or devices
  - Clearing browser storage removes saved data

- No central database:
  - Config must be exported/imported to move between devices

- Email generation:
  - Does not send emails directly
  - Relies on copy/paste or opening Outlook

- Venue matching:
  - Email Groups rely on venue name matching from Kappture
  - Minor naming differences may require adjustment

- No authentication or user separation:
  - All data on a device is shared in the same browser profile

---

## Future Improvements (Planned)

- Improved Email Group validation and visibility
- Optional in-tool Help/About page
- Enhanced reporting visuals (charts, trends dashboard)
- Shared config / hosted deployment options (future consideration)

---

## Author

Built and maintained by **Mike Ahrens**
