# VATSIM Houston ARTCC Alias

This repository holds the source files for the Houston ARTCC alias in a modular, easily editable format. Rather than storing one massive CRC-ready alias file, each section is maintained separately here and assembled by FE Buddy into the final output used in operations.

## Purpose

The alias is split into logical sections so individual parts can be updated without editing a monolithic file. FE Buddy reads these sections and inserts them into the final alias build, making the process easier to maintain and less error-prone.

## Included sections

- `metadata.txt` — header metadata, release information, cycle data, and attribution.
- `auto_track.txt` — auto-track commands and corresponding deactivation commands.
- `facility_info.txt` — per-airport facility and procedure information notes.
- `pilot_help.txt` — pilot-facing help, callout, and bad-usage message aliases.
- `position_shortcuts.txt` — shorthand commands for clearance, departure, local, TRACON, enroute, and general operations.
- `preferred_routing.txt` — preferred route alias tables by airport and specialty.
- `loa_recall.txt` — LOA recall, coordination notes, QRC links, and specialty-to-specialty routing reminders.

## Repo workflow

This repo is the editable source of truth for the alias content. The final CRC-ready alias is generated from these pieces by FE Buddy, which merges the sections into the system-ready file.

## Editing guidance

- Keep each alias section in its dedicated file.
- Preserve the existing alias syntax and formatting conventions.
- Maintain clean entries using the same pattern style already present in the repo.
- Update release/cycle information in `metadata.txt` when required.
- Test the final merged output in FE Buddy before release.

## Contribution

If you are updating a section, make the change in the relevant file and keep the edit focused to that area. Clear PRs should note which alias section was changed and what it affects.

This repo is intended to make alias maintenance straightforward while keeping the final generated file production-ready.
