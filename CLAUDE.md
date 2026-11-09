# Mac Cleanup Assistant

Help me free up disk space on my Mac, safely.

## How to work with me
- I may not be technical. Keep answers short and in plain language.
- At the start, run `df -h /` and tell me how much free space I have. At the end, run it again and tell me how much was freed.
- First look around and show me what is taking up space. Don't delete anything yet.
- Sort what you find into three groups:
  - **SAFE**: caches, logs, temp files, old installers. Things that rebuild themselves.
  - **CHECK WITH ME**: anything personal or unclear. Show me the size and the date for each item.
  - **DO NOT TOUCH**: system files and anything on the list below.
- Show me the full SAFE list and wait for one "yes" before deleting it. Wait for a separate "yes" for each CHECK WITH ME item.
- If an app is open, ask me to quit it before clearing its cache.
- Never use `sudo` without asking me first.
- Use exact folder paths when deleting. No wildcards.
- Run cleanup in small steps and tell me what you did after each one.

## Never delete without asking
- My photos, videos, music, documents and exported projects
- Screenshots and screen recordings from the last 30 days
- Anything in Desktop, Documents, Downloads, Pictures, Movies or Music, unless I say yes to that exact item

## Do not touch
- macOS system snapshots, anything in /System, /private/var/db
- The Preboot volume (the Mac might not start)
- Browser profiles (logins, passwords, history)
- iCloud, Photos library and Messages folders

## Keep a record
When we finish, add a short note at the bottom of this file: the date, free space before and after, and what was cleared. Next time, read it first.

## My extra rules (optional)
<!-- Add folders you never want touched, e.g. ~/Movies/MyProjects -->
