# file_deleter

Find and delete files from a user-supplied list. All implementations search a chosen directory and all its subdirectories recursively for matching filenames.

![Windows Quick Access Manager](./screen%20capture.png)



---


### GUI features

- **Search Directory** — browse to any folder; the search recurses into all subfolders.
- **Filenames input** — type filenames directly, load them from a text file, or drag and drop a `.txt` list into the filenames area.
- **Flexible matching by default** — if you enter a filename without an extension, the GUI matches by basename regardless of extension. If you include an extension, the comparison is case-insensitive by default.
- **Enforce extension check** — optional checkbox that switches matching to exact full filename comparison, including case and extension.
- **Quick-add temporary file targets** — one button adds common junk files such as `._.DS_Store`, `.DS_Store`, and `Thumbs.db` to the list.
- **Find Matching Files** — starts disabled until at least one valid filename target is present, then searches the chosen directory and populates the results list.
- **Multi-select** — select individual files or use *Select All* / *Deselect All*.
- **Delete Selected Files** — asks for confirmation, then removes selected files from the results list after processing.
- **Removal behavior** — most files are moved into `deleted_files`; `._.DS_Store`, `.DS_Store`, and `Thumbs.db` are deleted in place.
- **Operation Log** — records searches, imports, quick-add actions, removals, and errors.
- **Log actions** — `Open "deleted_files.txt"` opens the log file if it exists (otherwise it stays disabled), and `Clear Operation Log` clears the on-screen log panel.
- **About dialog** — includes version, build date, and repository link.
- **Dark mode and theme toggle** — switch between dark and light themes at runtime from the View menu.
- **High-DPI and font scaling** — the GUI automatically adapts to your monitor's DPI and adjusts font sizes for crisp, readable text on all displays. DPI and theme changes are handled dynamically when moving the window between monitors.



Example `list.txt`:
```
# photos to remove
20210522_161348.jpg
20240702_092330.jpg
```

---


