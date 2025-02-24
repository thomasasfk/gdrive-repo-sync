**Disclaimer:** This tool is now deprecated as Claude offers native GitHub integration.

---

# GDrive Repo Sync

- Clones repositories, processes contents into docx files, and syncs to Google Drive
- Creates Google Drive-compatible documents that Claude can read for use with Claude projects
- Requires rclone installed and configured with a Google Drive remote named "gdrive"

## Usage
```
usage: gdrive-repo-sync.py [-h] [--repo-list REPO_LIST] [--max-lines MAX_LINES] [--exclude EXCLUDE] [--no-sync] [--debug]

options:
  -h, --help            show this help message and exit
  --repo-list REPO_LIST  Path to JSON file with repo URLs
  --max-lines MAX_LINES  Maximum number of lines per file
  --exclude EXCLUDE     Comma-separated list of file extensions to exclude
  --no-sync             Skip syncing to Google Drive
  --debug               Enable debug output
```

## Example repos.json
```json
[
  "https://github.com/username/repo1.git",
  "https://github.com/username/repo2.git"
]
```

## Use with uv

```bash
uv run gdrive-repo-sync.py
```
