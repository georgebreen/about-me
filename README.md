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

For testing markdown, I prefer [markdown-it](https://markdown-it.github.io) due to its adherence to [CommonMark](https://commonmark.org) — arguably the original design spec for Markdown.

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

## Media Tools

### [LosslessCut](https://losslesscut.app)
Extremely useful for trimming shortform clips, for when only a light touch is needed.

### [Shutter Encoder](https://www.shutterencoder.com)
Uses the wonderful, internet load-bearing software FFmpeg. The middleweight of video editing.

### [DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve)
If you are making a very big project that you want to be movie-grade, bring out the heavyweight.

### [OBS Studio](https://obsproject.com)
Fully extensible, allows you to create product demos with ease. A great feature is the customizable instant replay feature — it allows you to have always-on recording but save on disc space.

## Spreadsheet Tools

### [qsv](https://github.com/dathere/qsv)
Wrangle CSV files in scripts and search. Blazing-fast data-wrangling toolkit built in Rust.

### [VisiData](https://www.visidata.org)
A better Excel — terminal based, not for the faint of heart. True data lovers only. Use with WSL2 in windows. Use a modern terminal client as well.

## Remote Access Tooling

### [Tailscale](https://tailscale.com)
I've recently converted and I'm a huge fan for its ease of use and impressed by its security features. I'd be willing to pay a few bucks to them to keep up the good work. Has SSO, MFA, clean logging <kcite></kcite>.

### [RustDesk](https://rustdesk.com)
This is a clean alternative to TeamViewer, open-source. I've found it works on every platform I've tried. I've moved my family IT support away from using Chrome Remote Desktop and just have them install RustDesk. If I can coach my grandma to install it, you can too <kcite></kcite>.

### [WireGuard](https://www.wireguard.com)
I've personally not set this up, but I hear it's quite simple. The streets say easier than OpenVPN management <kcite></kcite>.

### [OPNsense](https://opnsense.org) / [pfSense](https://www.pfsense.org)
I like to keep my homelab simple, but if you are interested in a well-supported software-based firewall, I'd pick one of these — leaning towards OPNsense for its open-source nature. There are plenty of guides on how to get it running on Proxmox <kcite></kcite>.

## Backup Software

### [Veeam](https://www.veeam.com)
Tried and true, verified over 10,000s of installs during my time at an MSP. There are free versions for home PC backup. Buy an external drive, be sure to encrypt your backup, check for data integrity, and run a full backup every two weeks. The peace of mind is priceless.

### [Backblaze](https://www.backblaze.com)
If you need a dead-easy, set-and-forget backup for your family members, cough up a couple bucks and get a Backblaze subscription. Loved by /r/datahoarders around the world.

### [Amazon S3 Glacier](https://aws.amazon.com/s3/storage-classes/glacier/)
Are you a true data hoarder? Running out of tape drives? Throw it all in an S3 Glacier bucket. It's the cheapest I've found.

## Web Troubleshooting

For most basic webpage troubleshooting, you can get by using the built in debugger of Chrome/Firefox. For closed source software, you gotta bring out the big guns.

### [mitmproxy](https://mitmproxy.org)
An interactive HTTPS proxy that lets you intercept, inspect, and modify HTTP and HTTPS traffic in real time. Great for debugging API calls and seeing exactly what your apps are sending. 

### [Telerik Fiddler](https://www.telerik.com/fiddler)
A classic web debugging proxy for inspecting HTTP/HTTPS traffic. The go-to for many Windows-based workflows.

### [Wireshark](https://www.wireshark.org)
The gold standard for network protocol analysis. When you need to dig into packets at every layer of the stack, this is the tool.

### [HTTP Toolkit](https://httptoolkit.com)
A modern, developer-friendly alternative to Fiddler/Charles. Open-source and great for intercepting and debugging HTTP from browsers, apps, and more.

### [Postman](https://www.postman.com)
It's one of the most widely adopted API clients for building, testing, and documenting HTTP requests. Supports environment variables, collections, and automated testing, making it a staple for anyone working with REST or GraphQL APIs. PayPal, Datadog, DocuSign, Microsoft, and others are all part of the Postman API Network and provide easy-to-use collections for testing.


## Network Troubleshooting

If you're new to network troubleshooting, you can often find the basics by searching "tool + cheat sheet". Nmap cheat sheet will get you running with the basics, but I encourage you to do your own research.

### [PingPlotter](https://www.pingplotter.com)
A graphical traceroute and ping tool that's actively maintained — great for visualizing network latency and packet loss over time. Useful for diagnosing connectivity issues, gaming lag, and ISP problems. The 14 day trial provides enough time to diagnose most issues, but a license is pretty cheap.

### [iperf3](https://iperf.fr)
A lightweight bandwidth testing tool. Run it between two machines to quickly diagnose network throughput issues. When they say the VPN makes their connection slow, you can use this do to point to point testing to prove, it was the user's home internet.

### [nmap](https://nmap.org)
The undisputed standard for network scanning — 25+ years old and still actively maintained. Discovers hosts, maps open ports, and identifies services and OS fingerprints. Essential for answering "is this port actually open?" Runs as a single binary with no prerequisites. Available on Windows with the Zenmap GUI. Onboarding a new client? Help find those old boxes on the network hidden in the ceiling somewhere.

### [curl](https://curl.se)
The internet's most ubiquitous CLI tool, shipping on virtually every OS for 25+ years. If you need to test an HTTP request from a script or terminal, this is the tool. Single binary, no dependencies, transfers easily to any system.

### [testssl.sh](https://github.com/drwetter/testssl.sh)
A free command-line tool that checks a server's TLS/SSL configuration — ciphers, protocols, and known vulnerabilities (Heartbleed, POODLE, etc.). Single script, no dependencies. Widely recommended in sysadmin communities.

## Security & Recon

### [masscan](https://github.com/robertdavidgraham/masscan)
The fastest open-source port scanner in existence — capable of transmitting 10 million packets per second and scanning the entire IPv4 internet in under 6 minutes from a single machine. Created by Robert Graham in 2013, its usage and parameters are similar to nmap, but it's designed for internet-scale reconnaissance rather than in-depth scanning of individual hosts. A common workflow is to use masscan for rapid broad discovery of open ports, then hand off the results to nmap for detailed service fingerprinting.

> **Caution:** Do not run this tool against the entire internet all willy-nilly. You will get your home IP blacklisted from A LOT of websites and it will be a pain for everyone on your network.

### [nuclei](https://github.com/projectdiscovery/nuclei)
A fast, customizable vulnerability scanner built on a simple YAML-based DSL, powered by a community-curated library of templates. It can scan thousands of hosts in minutes, making it a go-to for bug bounty hunters and security researchers.

> **Praise for PD:** Nuclei is part of [ProjectDiscovery](https://github.com/projectdiscovery), an open-source security company that builds an entire suite of tools following the Unix philosophy — each tool does one thing well and they pipe together seamlessly. Other standout tools in the ecosystem include [subfinder](https://github.com/projectdiscovery/subfinder) (passive subdomain enumeration), [httpx](https://github.com/projectdiscovery/httpx) (multi-purpose HTTP probing), and [naabu](https://github.com/projectdiscovery/naabu) (fast port scanner written in Go). A typical recon pipeline: `subfinder` to find subdomains → `httpx` to identify live hosts → `nuclei` to scan for vulnerabilities.

I can't stress enough, they are really good at what they do.

### [Shodan](https://www.shodan.io)
The world's first search engine for internet-connected devices. Often called "the most dangerous search engine on the internet," Shodan indexes internet-facing devices and services — routers, webcams, industrial control systems, databases — rather than web pages. Invaluable for reconnaissance and understanding your own attack surface. I recommend following them on their socials, at some point every year they usually do a cheap $5 lifetime upgrade. It's a no-brainer pick up if you have any interest in cybersecurity.

### [GreyNoise](https://www.greynoise.io)
A threat intelligence platform that helps you separate internet "noise" from real threats. GreyNoise collects and labels data on IPs that mass-scan the internet, so you can confidently identify which alerts are background noise vs. actual targeted attacks. Integrates with SIEMs, SOAR, and EDR platforms. The founder Andrew Morris is a bit of an odd guy, but that's what I like about em. Greynoise saves a lot of time during IR response.

### [MaxMind GeoIP](https://www.maxmind.com)
The creator of GeoIP and the industry standard for IP geolocation data, trusted by businesses for 20+ years and covering 99.9999% of IP addresses in use. Offers downloadable databases (no per-query charges, no network latency) and API web services. Also provides [GeoLite2](https://www.maxmind.com/en/geolite-free-ip-geolocation-data), a free GeoIP dataset built with open source values. No need to pay platforms like IPInfo (still love them, but they are costly).

My advice? Setup a cronjob to download the updated GeoIP Database and tie it into your Elastic Search ingestion pipeline for effective and effcient coarse location tracking. For extra points, throw in ElastAlert2 and write a superman rule (impossible travel) to find out if your users are compromised. 

### [crt.sh](https://crt.sh)
A web-based Certificate Transparency (CT) log search engine that lets you find SSL/TLS certificates issued for a given domain or organization. An essential passive recon tool — search by domain name, organization, or certificate fingerprint to discover subdomains and exposed assets without generating any traffic against the target. CRT.SH is a reminder to not use Let's Encrypt for internal services even though it makes it simple. You may expose your internal hostnames unexpectedly.

> **Privacy note:** crt.sh searches all CT logs, not just Let's Encrypt — any publicly-trusted certificate from any CA will appear here, because modern browsers require CT log submission for public trust. This is a reminder to be careful using public CAs like Let's Encrypt for internal/non-internet-facing services: your internal hostnames become publicly discoverable. For internal services, consider a private CA like [step-ca](https://smallstep.com/docs/step-ca/) or [HashiCorp Vault](https://www.vaultproject.io/) to avoid exposing internal infrastructure through CT logs.

## Hall of Fame — IT Pro Resources

### [SS64](https://ss64.com)
Forget how to use diskpart? Trying to find the right DISM command? SS64 has your back. A comprehensive command-line reference for Windows CMD, PowerShell, macOS/Linux bash, and SQL Server.

### [Graham Helton — SSH Cheatsheet](https://grahamhelton.com/blog/ssh-cheatsheet)
"An Excruciatingly Detailed Guide To SSH (But Only The Things I Actually Find Useful)." SSH tunnels are a red teamer's best friend, but they're also insanely practical for everyday sysadmin work. This guide breaks down port forwarding, jump hosts, and SSH config in a way that actually makes sense.

### [CyberChef](https://gchq.github.io/CyberChef/)
The Cyber Swiss Army Knife — a web app for encryption, encoding, compression, and data analysis, built by GCHQ. Found some malware? Start decoding that base64 with CyberChef. Runs entirely in your browser with no server-side component, so your data never leaves your machine.

### [Rebane — SSH Secret Menu](https://x.com/rebane2001/status/2031037389347406054)
Did you know SSH has a little-known secret menu? Rebane is a mystical computer wizard and the reason I have a strong appreciation for CSS — they also built [x86CSS](https://github.com/rebane2001/x86CSS), a working x86 CPU emulator written entirely in CSS with no JavaScript.

### [Office365ITPros — Tony Redmond](https://github.com/12Knocksinna/Office365itpros)
Tony Redmond has made a career on explaining the dark hidden magic of Microsoft cloud products. This repo holds over 300 PowerShell scripts for interacting with Microsoft 365 and Entra ID, companion to the [Office 365 for IT Pros eBook](https://office365itpros.com) <kcite></kcite><kcite></kcite>.

### [awesome-entra — Merill Fernando](https://github.com/merill/awesome-entra)
A curated list of awesome Microsoft Entra tools, guides, and resources. Merill Fernando is a Principal Product Manager on the Microsoft Entra team — as far as I'm concerned, he's the Father of Entra. He also runs a [weekly Entra podcast](https://merill.net) and regularly shares Entra ID masterclass labs for free.

### [NirSoft](https://www.nirsoft.net)
A long legacy of killer freeware utilities for Windows — password recovery, system tools, browser history viewers, network sniffers, and much more. All developed by Nir Sofer. Portable and incredibly useful for troubleshooting.

### [MFCMAPI](https://github.com/microsoft/mfcmapi/releases)
Pray you never need this tool. Microsoft's own MAPI editor that provides low-level access to Exchange and Outlook stores for troubleshooting the deepest, darkest mailbox corruption issues. Actively maintained — the June 2026 release is current.

### [ForensiT — ProfWiz & TransWiz](https://www.forensit.com/downloads.html)
User Profile Wizard (ProfWiz) and TransWiz are worth paying for. ProfWiz migrates user profiles between domains (including Azure AD) without copying data — it reconfigures the profile in place. TransWiz transfers a full user profile to a new machine. lifesavers for domain migrations and machine replacements.

### [Nucleus Technologies (Kernel)](https://www.nucleustechnologies.com)
Don't pay the big guys to migrate Exchange. These people are the real deal — their Kernel-branded tools handle EDB-to-PST conversion, Exchange migration, and PST repair. I've saved countless CEOs with multiple 50GB archives using their tooling.
