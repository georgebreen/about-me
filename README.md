# Tools I Like to Use

A short list of the tools I reach for when troubleshooting, wrangling data, and automating work — plus the essentials on any new machine.

## Troubleshooting, Data Wrangling & Automation

### [jq](https://jqlang.org)
For manipulating data to and from JSON-based APIs. Also great for templating when combined with [go-task](https://github.com/go-task/task).

### [yq](https://github.com/mikefarah/yq)
Ansible requires a lot of YAML, so I often build with yq. One of its benefits is that it also supports CSV — I prefer working with CSV over proprietary Excel formats (best when there aren't multiple sheets in a single workbook).

### [go-task](https://github.com/go-task/task)
I've worked with developers on Linux, macOS, and Windows, and it's nice to have a tool that works across all of them. Multi-platform support is key.

A common thread with these tools: they run as a single binary with no prerequisites, which makes it easy to quickly transfer them to any system I'm troubleshooting or pulling data from.

## Must-Have Developer & Media Tools

When setting up a new machine, I rely on [Ninite](https://ninite.com). My typical install:

- **[Vivaldi](https://vivaldi.com)** — Chromium-based, so well supported. Supports RSS feeds directly in the client, and Vivaldi Sync lets you define an encryption key so not even Vivaldi can see your data.
- **Spotify** — I've been a member since it was a UK-only service.
- **[Audacity](https://www.audacityteam.org)** — For editing sound clips for soundboards during streams and Discord calls.
- **[Discord](https://discord.com)** — For game-based communities and talking to friends.
- **[7-Zip](https://www.7-zip.org)** — Because really, who's paying for WinRAR?
- **[Paint.NET](https://www.getpaint.net)** — For quick image edits like removing transparencies.
- **[ShareX](https://getsharex.com)** — For quickly marking up screenshots (redaction, step ordering, highlights, OCR via Tesseract).
- **[Everything](https://www.voidtools.com) (voidtools)** — The fastest file search tool, and super lightweight.
- **[Notepad++](https://notepad-plus-plus.org)** — It's lost some ground to VS Code and other editors, but the [plugin support](https://github.com/notepad-plus-plus/nppPluginList/blob/master/doc/plugin_list_x64.md) is still top-notch.
- **[WinSCP](https://winscp.net/eng/download.php)** — The most reliable SFTP client I've found over years of troubleshooting. 

### Standout Notepad++ Plugins

- **[JsonTools](https://github.com/molsonkiko/JsonToolsNppPlugin)** — The tree view and filtering are extremely helpful for debugging API outputs.
- **[XML Tools](https://github.com/morbac/xmltools)** — *shudder* If you have to work with XML, this is a huge help.

## Markdown & VS Code

[VS Code](https://code.visualstudio.com) is my preferred markdown editor, with a few extensions:

- **[Markdown All in One](https://markdown-all-in-one.github.io/docs/guide/#features)** — Adds nice QoL keyboard shortcuts, table building support, and other formatting autocompletes.
- **[Markdownlint](https://github.com/DavidAnson/markdownlint)** — A linter is important because it catches inconsistencies and style issues as you write, ensuring your markdown renders correctly across different platforms and stays readable for both humans and tools.
- **[Markdown Preview Enhanced](https://github.com/shd101wyy/vscode-markdown-preview-enhanced)** — Works great when combined with Pandoc. LaTeX support enables quite a lot of possibilities. Also allows previewing GitHub Flavored Markdown.

A one-liner to install the above on a new machine.
```bash
code --install-extension yzhang.markdown-all-in-one \
     --install-extension davidanson.vscode-markdownlint \
     --install-extension shd101wyy.markdown-preview-enhanced
```

### Markdown testing

For testing markdown, I prefer markdown-it due to its adherence to [CommonMark](https://commonmark.org) — arguably the original design spec for Markdown.

## Diagramming & Mapping

### [Figma](https://www.figma.com)
I've been following Figma since the early days. Adobe attempted to acquire them, but the deal fell through due to regulatory scrutiny — Figma subsequently went public via IPO instead. What fascinated me most about Figma was that they were one of the first companies to really incorporate [multiplayer collaboration](https://www.figma.com/blog/how-figmas-multiplayer-technology-works/) besides Google Docs.

### [TLDraw](https://www.tldraw.com)
[Steve Ruiz](https://x.com/steveruizok) seems like a really cool guy — some of his demos show just how expansive and customizable TLDraw is. Take a look at this [ever-growingly prophetic demo](https://examples.tldraw.com/xkcd-dependency).

TLDraw has roots in PartyKit, which is now used in Cloudflare Durable Objects. Go figure — [Sunil Pai](https://blog.partykit.io/posts/everything-is-better-with-friends/), the inventor of PartyKit, currently works at Cloudflare.

### [Excalidraw](https://excalidraw.com)
Another excellent whiteboard tool. Funny bit of history: Excalidraw runs on Socket.IO, which was invented by Guillermo Rauch — the founder of Vercel.

It's funny to imagine the origins of the Cloudflare vs Vercel rivalry starting out over whiteboard apps.

## Second Brain Tooling

### [Notion](https://www.notion.com)
Notion is the most extensive platform I've used for building a knowledge repo. The extreme flexibility of everything being blocks allows you to easily build reusable templates, manage user access, and create beautiful dashboards. The only downside is that trying to leave Notion is quite a pain — the export capabilities are quite primitive. It's a cloud product, so I can quickly drop notes in from anywhere and access them from anywhere.

### [Obsidian](https://obsidian.md)
Obsidian is the gold standard of notes apps. The main flaw is that every non-local storage option has been kind of hacky. This has been changing in recent years as they improve Obsidian Sync and roll out mobile apps.

