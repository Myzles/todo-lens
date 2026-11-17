# Changelog

## 1.4.1

- New name: TODO Lens is now **Todoscope**. Another extension already used the old name. Nothing else changes: same extension ID, settings, commands and licence keys, so your setup and Pro licence keep working.

## 1.4.0

Pro, for reviewing and managing TODOs across a team. Everything free before is still free.

- Pro: **Copy PR Summary**. Lists the TODOs your branch adds and the ones it resolves (a TODO that only moved is not counted as resolved), as a Markdown checklist on your clipboard, ready for a PR description. Includes uncommitted and new files.
- Pro: **TODO Trend From Git History**. Counts TODOs at the end of each past week (12 by default, `todoLens.trendWeeks` up to 52) and shows the change, with a sparkline. Uses the same comment-aware matching and your exclude filters.
- Pro: **Team Health Report**. TODOs by owner (the name in the TODO, or the git author of the line), overdue, stale, oldest, hotspots. Open it, copy Markdown, or save JSON for a CI script or dashboard.
- Free now: **Export > Markdown to clipboard** works without Pro (a plain checklist). CSV, JSON, Markdown files and the age and author columns stay in Pro.
- Locked Pro commands show what they would produce for your workspace, in one line, in the message you asked for (for example "3 TODOs added and 1 resolved since main"). The free status bar tooltip says how many TODOs are past their due date. Pro shows that count next to the total.
- Pro prompts: at most one unsolicited Pro message per session (trial notices obey it); a prompt only ever appears because you clicked a locked command.
- Pro status bar shows overdue count.

## 1.3.2

- Listing: price and 7-day trial on the first screen, how licences work, and a "Moving from Todo Tree" section listing what the import copies and what it does not. No code changes.

## 1.3.1

- The empty tree now says why it is empty: still scanning, no folder open, filters hiding everything (with a Clear Filters button), a narrow scope setting, or genuinely no TODOs (with a Show Log button).
- Choosing Pro opens checkout and then tells you where the license key will arrive and where to paste it. A wrong key offers Try Again.
- Export: new "Markdown to clipboard" option, a clear message instead of an empty file when nothing matches, CSV opens correctly in Excel (accents), and a failed save explains itself.
- "Added since branch" falls back from main to master (or origin/main) when your repo has no main, and a missing branch suggests what to try.
- Todo Tree import lists what it copied and what it does not carry over (keybindings, named scopes).
- The Getting Started page opens once on a fresh install.

## 1.3.0

- A short Getting Started walkthrough (Help > Welcome, or it opens on install): open the list, import Todo Tree settings, and an optional 7-day Pro trial.
- New command "TODO Lens: Start 7-Day Pro Trial". No card needed.
- If you start the trial, TODO Lens tells you once the day before it ends and once after, so Pro features don't just disappear. Free features always keep working.

## 1.2.0

- After a few successful scans, TODO Lens asks once whether you would like to rate it on the Marketplace. Pick "No thanks" or close it and it never asks again.

## 1.1.0

- New setting `todoLens.scope`: show the whole workspace, only files open in tabs, or only the file you are editing. Todo Tree users asked for this one.
- New setting `todoLens.gutterIcons`: a coloured dot in the gutter on each TODO line.
- The TODO count now also shows as a badge on the activity bar icon.
- Vim script comments (`" TODO: ...`) are found in .vim, .vimrc and .vader files. The Vim and Neovim repos yield 861 more TODOs than before.
- Scanner uses up to 16 threads instead of 10 on big machines.
- Editor highlights are skipped for files over 4 MB instead of 20 MB, so one huge file cannot stall the editor.

## 1.0.0

- First release: workspace TODO tree (file, folder, tag and assignee groupings), editor highlights, live updates, filters, next/previous navigation, Todo Tree settings import.
- Built-in multi-threaded scanner: no ripgrep, respects .gitignore, skips binaries, minified and lock files.
- Pro: TODOs added since a branch, git author and age, stale and overdue filters, due dates and assignees, Markdown/CSV/JSON reports. 7-day free trial.
