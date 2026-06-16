# Kappture Terminal Checker

Browser-based tool for analysing Kappture Terminal Status and Session Activity exports, generating operational reports, and assisting with daily venue checks.

---

## Overview

The Kappture Terminal Checker is a single-page, browser-based utility designed to streamline daily EPOS checks across venues.

It supports importing Kappture CSV exports, identifying actionable issues, managing exclusions, and generating clear Daily and Weekly reports.

The tool runs entirely in the browser — no installation, backend, or external dependencies required.

---

## Features

### Import & Processing
- Import Terminal Status CSV
- Import Terminal Session Activity CSV
- Process both datasets together
- Apply filtering rules to identify actionable issues

### Review & Workflow
- Identify offline terminals and open sessions
- Ignore items temporarily using **Ignore today**
- Re-include items using **Include again**
- Scroll behaviour optimised for efficient bulk actions

### Reporting
- Daily Report view per venue
- Weekly overview across multiple days
- Manual override support with automatic reversion to Imported state
- Clear distinction between:
  - Imported data
  - Manual override

### Venue Management
- Manage exclusions for:
  - Venues
  - Outlets
  - Terminals
- Import/export configuration as JSON

### UI / UX
- Fully browser-based (no dependencies)
- Responsive layout (desktop + mobile use)
- Button state handling and feedback
- Stable row heights in reporting tables
- Colour-coded statuses (Offline / Sessions)

---

## Version

Current version:
