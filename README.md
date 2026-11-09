# Mac Cleanup

One file that turns Claude Code into a careful cleanup assistant for your Mac.

It finds what's filling up your storage, clears safe junk like caches and logs, and asks you before it touches anything personal.

**[Try the demo](https://kunwar1417.github.io/mac-cleanup/)**

## How to use it

1. **Get Claude Code** from claude.com. You need a paid Claude plan.
2. **Make a folder** on your Desktop called `Mac Cleanup`.
3. **Download [CLAUDE.md](CLAUDE.md)** and put it in that folder. Keep the name exactly as it is.
   (Open the file, then click the download icon at the top right.)
4. **Open the folder in Claude Code** and type: *Help me free up space on my Mac*

## What Claude does

- Checks your free space before and after
- Sorts everything into three groups:
  - **Safe**: caches, logs, temp files. Cleared after one yes.
  - **Check with me**: anything personal. Shows the size and date, then waits for your yes on each one.
  - **Do not touch**: system files, your photos, videos and projects, browser logins
- Never uses admin access (`sudo`) without asking
- Keeps a short record of each cleanup at the bottom of the file

## Before you start

- **Back up with Time Machine.** It's smart before any cleanup.
- **Read before you say yes.** You're always in control.
- **Make it yours.** Add folders you never want touched at the bottom of CLAUDE.md.
