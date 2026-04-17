# Windows Quick Access Manager

For managing File Explorer Quick Access pin order on Windows 11.
After some many Windows 11 updates, I noticed the quick access stopped working for changing the order or in some cases adding a new item.
I tried many methods explained online but couldn't find any that actually works.
The only way to reorder them was to remove all items, then add them in the order that I want one by one.
This GUI tool allows much more flexibility.




## What This Project Is

- Drag-drop and multi-select reordering for Quick Access folders
- Explicit apply model: changes in the list are not written until you click Apply to Windows
- Backup and restore support using JSON files

## UI Overview

### Header

- Title: Windows Quick Access Manager
- Inline author/project text
- Version label: v1.1.0

### Left Panel

- Displays current working list of Quick Access folders
- Supports multi-select with Ctrl+Click and Shift+Click
- Drag a row to reorder
- Drag folders from Explorer into the list to add
- While dragging external folders, a visible insertion line shows exactly where they will be inserted

### Right Panel Sections

#### Reorder

- Move Up
- Move Down
- Remove Selected [Del]

#### Apply / Revert

- Apply to Windows
- Revert to Default

#### Backup / Restore

- Backup to File
- Restore from File
- Reload from Windows

#### Activity Log

- Startup hints
- Operation status and warnings
- Error details when actions fail

## Apply Button Behavior

- Disabled (gray) when no changes are pending
- Enabled (green) only when the working list differs from current Windows state
- Empty-list apply is allowed when that represents a real change (clear all pinned folders)

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| Up Arrow | Move selected item(s) up |
| Down Arrow | Move selected item(s) down |
| Delete | Remove selected item(s) |

## Backup/Restore

- Backup file name format: windows_quick_access_manager_YYYYMMDD.json
- Restore first checks for JSON files in the current folder
- If none selected automatically, a file picker is shown

## Notes

- Applying/removing Quick Access entries does not delete real folders
- The UI is DPI-aware for improved rendering on high-resolution displays
