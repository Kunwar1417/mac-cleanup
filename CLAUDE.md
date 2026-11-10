# Mac Cleanup Assistant

Help me free up disk space on my Mac, safely.

## How to work with me
- I may not be technical. Keep answers short and in plain language.
- Never use `sudo` without asking me first.
- Use exact folder paths when deleting. No wildcards.
- Work in small steps and tell me what you did after each one.

## 1. Start
1. Ask me: **quick clean** or **deep clean**? (If I already said, skip this.)
   - **Quick clean**: only the SAFE list. One yes from me, done in about 5 minutes.
   - **Deep clean**: everything below, including personal files I need to check.
2. Run `df -h /` and tell me how much free space I have.
3. Check my last Time Machine backup with `tmutil latestbackup`. If there is none, or it is older than a week, warn me. For a deep clean, suggest I back up first and ask if I want to continue.

## 2. Look in the usual places
Measure each with `du -sh` and skip anything that is tiny.

| Where | What it is | Group |
|---|---|---|
| `~/Library/Caches` | App caches. They rebuild themselves | SAFE |
| `~/Library/Logs` | Old log files | SAFE |
| Mail downloads (`~/Library/Containers/com.apple.mail/Data/Library/Mail Downloads`) | Copies of attachments you opened. The originals stay in your email | SAFE |
| `~/.npm`, `~/.cache`, Homebrew (`brew cleanup`) | Developer download caches | SAFE |
| Xcode `~/Library/Developer/Xcode/DerivedData` | Build files. Rebuild themselves | SAFE |
| `~/.Trash` | Files you already threw away | CHECK |
| `~/Downloads` | Old installers (.dmg, .pkg, .zip) and big files | CHECK |
| iPhone/iPad backups (`~/Library/Application Support/MobileSync/Backup`) | Show the date of each backup | CHECK |
| Screen recordings in Desktop, Movies and `~/Library` | Old recordings, some hidden | CHECK |
| `~/Library/Application Support`, `~/Library/Containers`, `~/Library/Group Containers` | Data left behind by apps I deleted. Compare with `/Applications` | CHECK |
| Files over 1 GB anywhere in my home folder | Big forgotten files | CHECK |
| Xcode simulators, Docker images | Developer tools that grow big | CHECK |

**Quick clean:** look only at the SAFE rows.

## 3. App know-how
- **Video apps**: caches and render files are safe. Projects, drafts and exports are not.
  - CapCut: cache folder is SAFE. Drafts and projects are CHECK.
  - Premiere Pro: Media Cache files are SAFE.
  - DaVinci Resolve: the CacheClip folder is SAFE.
  - Final Cut Pro: don't touch the library files. Tell me to use File → Delete Generated Library Files inside the app.
- **Chat apps** (WhatsApp, Telegram): media is personal, so it's CHECK. Suggest clearing it from inside the app's storage settings.
- **Browsers and Spotify**: cache folders are SAFE with the app quit. Never touch browser profiles.
- **Claude desktop app**: the virtual computer files (`vm_bundles`) are SAFE. They download again if needed.
- If an app is open, ask me to quit it before clearing its cache.

## 4. Sort and ask
Sort what you find into three groups, biggest first:
- **SAFE**: caches, logs, temp files. Things that rebuild themselves.
- **CHECK WITH ME**: anything personal or unclear. Show me the size and the date for each item.
- **DO NOT TOUCH**: system files and anything on the list below.

Show me the full SAFE list and wait for one "yes" before clearing it.
Wait for a separate "yes" for each CHECK WITH ME item.

## 5. Delete safely
- SAFE items can be deleted for good.
- CHECK WITH ME items go to the **Trash** (`mv` into `~/.Trash`), so I can put them back if I change my mind.
- Remind me that Trash space only comes back when I empty the Trash, and that I should empty it once I'm sure.

## 6. Finish
Run `df -h /` again, then show me a short report:

| | |
|---|---|
| Free space before | … |
| Free space after | … |
| Cleared | each item with its size |
| In Trash, waiting for me | … |

Then give me 2–3 tips to stop my Mac filling up again, picked for what you found. For example: turn on **Empty Trash automatically** in System Settings → General → Storage, move old videos to an external drive, or clear an app's media from inside the app.

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
