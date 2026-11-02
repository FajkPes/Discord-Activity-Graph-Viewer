# Discord Activity Graph Viewer

A local viewer for seeing how your Discord message activity changes over time.

## What it does

This local viewer turns a Discord data export into an activity graph, so you can explore when you sent messages without uploading your conversations to a service.

## Features

- View activity by day, week or year and select a date range.
- Filter people, groups and servers; inspect active days, hours and frequently used words.
- Deduplicate message IDs and show skipped or invalid files.
- Process the selected export locally in Chrome or Edge.

## Use it

1. Download and extract the ZIP from [Releases](https://github.com/FajkPes/Discord-Activity-Graph-Viewer/releases/latest), then open `index.html`.
2. Select the messages folder from your Discord data export.
3. Optionally load the messages and server index files to add conversation and server names.
4. Select a date range and use the filters above the graph.

The current interface is in Czech. Each valid record counts as a message, including messages without text. The app does not store or upload the selected data.

[Detailed documentation](README-DETAILS.md) · [All releases](https://github.com/FajkPes/Discord-Activity-Graph-Viewer/releases)

## Reading the results

Use one activity filter to compare all messages with a person, group or server over a chosen period. The top lists show conversations, days, hours and words and can be expanded or searched. Duplicate message IDs are counted once; invalid files or timestamps are reported. The word-frequency list excludes common Czech words and links, so its filtering is not language-neutral.

## Credits

**Idea, concept and design:** FajkPes  
**Coding:** ChatGPT Codex, Claude and Google Antigravity
