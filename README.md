# Awesome Mind Map Software

A curated catalog of **mind mapping software** — open source and proprietary, from apps and libraries to text-to-map tools, file formats, and interop bridges.

> Verified against live repos, registries, and vendor sites in **November 2026**. Status legend: 🟢 active · 🟡 slow/dormant · 🔴 archived/unmaintained · ⛔ shut down. Licenses and prices change — always double-check before committing.
>
> "Mind map" here means the radial/tree diagram where ideas branch from a central node. *Concept maps* (labeled graphs) and *argument maps* (claims + relations) are close cousins and get their own sections.

## Contents

- [Top picks](#top-picks)
- [Apps — Open Source](#apps--open-source)
  - [Open source desktop apps](#open-source-desktop-apps)
  - [Open source web / self-hosted apps](#open-source-web--self-hosted-apps)
  - [Text- & markdown-based map generators](#text--markdown-based-map-generators)
  - [CLI & terminal tools](#cli--terminal-tools)
- [Libraries & SDKs](#libraries--sdks)
- [Editor & knowledge-base integrations](#editor--knowledge-base-integrations)
  - [Obsidian](#obsidian)
  - [VS Code](#vs-code)
  - [Neovim / Vim](#neovim--vim)
  - [Emacs / Org-mode](#emacs--org-mode)
  - [JetBrains](#jetbrains)
  - [Joplin / Zotero / TiddlyWiki](#joplin--zotero--tiddlywiki)
- [Proprietary Software](#proprietary-software)
  - [Dedicated mind mapping SaaS](#dedicated-mind-mapping-saas)
  - [Desktop apps (proprietary)](#desktop-apps-proprietary)
  - [Whiteboard & visual collaboration suites](#whiteboard--visual-collaboration-suites)
  - [AI-powered map generators](#ai-powered-map-generators)
  - [Outliners & tree-thinking tools](#outliners--tree-thinking-tools)
- [Adjacent mapping genres](#adjacent-mapping-genres)
  - [Concept mapping](#concept-mapping)
  - [Argument mapping](#argument-mapping)
  - [Outliners & tree-thinking tools](#outliners--tree-thinking-tools)
  - [Freeform canvas & "brain" tools](#freeform-canvas--brain-tools)
- [File Formats & Interoperability](#file-formats--interoperability)
  - [Formats](#formats)
  - [Interop matrix](#interop-matrix)
  - [Converters & parsers (npm / PyPI / GitHub)](#converters--parsers-npm--pypi--github)
  - [APIs, SDKs & MCP servers](#apis-sdks--mcp-servers)
- [Historical / unmaintained but influential](#historical--unmaintained-but-influential)
- [Related content repositories](#related-content-repositories)
- [Contributing](#contributing)

---

## Top picks

Don't want to read 400 lines? (Though we'd love you to.)

| You want… | Pick |
|---|---|
| The most powerful OSS desktop app | [Freeplane](https://github.com/freeplane/freeplane) |
| A beautiful, native-feeling OSS desktop map | [Minder](https://github.com/phase1geo/Minder) (Linux) / MindNode (macOS, closed) |
| Open-source Miro clone with mindmaps | [Drawnix](https://github.com/plait-board/drawnix) |
| Markdown notes → interactive map | [markmap](https://github.com/markmap/markmap) · VS Code: `markmap-vscode` · Obsidian: Mindmap NextGen / Enhancing Mindmap |
| Diagram-as-code inside docs | Mermaid `mindmap` or PlantUML `@startmindmap` |
| Embed a map in your own web app | [mind-elixir](https://github.com/SSShooter/mind-elixir-core) (zero deps) or [Simple Mind Map](https://github.com/wanglin2/mind-map) (full-featured, yjs collab) |
| Keyboard-only, in the terminal | [h-m-m](https://github.com/nadrad/h-m-m) |
| Hand-drawn/organic Buzan style | [Ayoa](https://www.ayoa.com) (paid) or Linwood Butterfly (OSS) |
| Largest SaaS ecosystem & templates | Miro / FigJam / XMind |
| Map your whole knowledge graph | [TheBrain](https://www.thebrain.com) (free desktop now) or organize in Obsidian/Logseq |
| Files your grandkids can still open | `.mm` (FreeMind XML) or an indented Markdown outline |

---

## Apps — Open Source

### Open source desktop apps

- **[Freeplane](https://github.com/freeplane/freeplane)** — GPL-2.0 · Win/macOS/Linux (Java) · 🟢 (~4.5k★, active Nov 2026) — The most feature-rich OSS mind mapper, successor to FreeMind.
    - LaTeX/markdown in node text, Groovy scripting, addons, encrypted maps, outliner views, project-management features
    - Built-in **MCP server** for AI workflows (docs §4.5)
    - Exports: Markdown, OPML, Asciidoc, LaTeX, Office formats, PDF, SVG, PNG, XHTML; completed format XSD at [docs.freeplane.org](https://docs.freeplane.org)
- **[FreeMind](https://freemind.sourceforge.io)** — GPL-2.0+ · Win/macOS/Linux (Java) · 🔴 (last release 1.0.1, 2014) — The genre's granddaddy (still ~2k downloads/week on SourceForge). Imported MindManager `.mmap` as early as 0.9b9. Superseded by Freeplane; see [Historical](#historical--unmaintained-but-influential).
- **[View Your Mind (VYM)](https://github.com/insilmaril/vym)** — GPL-2.x (SPDX "Other") · Win/macOS/Linux (Qt/C++) · 🟢 (~200★, active Oct 2026) — Veteran Java-free mapper with strong linking and export (PNG/SVG/PDF); rare SourceForge-era project still maintained.
- **[Minder](https://github.com/phase1geo/Minder)** — GPL-3.0 · Linux (GTK/Vala, elementary OS flagship) · 🟢 (~1.2k★, active Nov 2026) — Polished native mapper with themes, node notes/tasks, auto-layout, markdown/PDF/SVG export.
- **[MindForger](https://github.com/dvorka/mindforger)** — GPL-2.0 · Win/macOS/Linux (C++/Qt) · 🟡 (~2.7k★) — "Thinking notebook": markdown IDE where notes ARE outline/mindmap entries; mind-map view over your notes.
- **[TreeSheets](https://github.com/aardappel/treesheets)** — Zlib · Win/macOS/Linux (C++/wxWidgets) · 🟢 (~3.2k★, active Nov 2026) — "Hierarchical spreadsheet" positioned explicitly as a replacement for outliners, mind mappers *and* spreadsheets; single-file docs, now even ships Claude-Code scripting. A genuine hipster gem.
- **[Heimer](https://github.com/juzzlin/Heimer)** — GPL-3.0 · Win/macOS/Linux (C++/Qt6) · 🟢 (~1k★, active 2026) — Lightweight mind map + network-diagram + notes app, saves PNG/SVG.
- **[Mindolph](https://github.com/mindolph/Mindolph)** — GPL-3.0 · Win/macOS/Linux (JavaFX) · 🟢 (~200★, active Sep 2026) — Personal knowledge workspace: FreeMind-compatible mind maps (`.mm`-family) plus PlantUML, Markdown, CSV editors, Gen-AI support.
- **[DesktopNaotu](https://github.com/NaoTu/DesktopNaotu)** — MIT · Win/macOS/Linux (Electron) · 🟢 (~5.1k★, active Sep 2026) — Offline desktop build of Baidu's 脑图 (Naotu/KityMinder), `.km` JSON format.
- **[VNote](https://github.com/vnotex/vnote)** — LGPL-3.0 · Win/macOS/Linux (C++/Qt) · 🟢 (~13k★, very active) — Markdown note platform "majoring in Markdown, MindMap, Typst" — includes a built-in mind map editor mode.
- **[Vex (维刻)](https://github.com/dotnet9/Vex)** — MIT · cross-platform (C#/Avalonia) · 🟢 (active Nov 2026) — Markdown editor with a live mind-map side view, no Electron.
- **[Blumind](https://github.com/funwaywang/Blumind)** — MIT · Windows (C#/WinForms) · 🟡 (~100★, dormant 2021) — Tiny lightweight Windows mapper.
- **[VUE (Visual Understanding Environment)](https://github.com/VUE/VUE)** — license unmaintained (historically Apache-family, *(verify)*) · Java · 🔴 (last push Jan 2024; tufts.edu site needs Wayback) — Tufts University's concept/mind mapping + presentation-in-map tool.
- **[Semantik](https://waf.io/semantik.html)** (repo on GitLab, `ita1024/semantik`) — GPL-3.0 · Linux (KDE/Qt, Python) · 🟡 (last release Mar 2024) — kdissert heir: build a mind map, generate a LaTeX/OpenOffice/HTML document from it.
- **SciaReto** — free, source in [raydac/netbeans-mmd-plugin](https://github.com/raydac/netbeans-mmd-plugin) (Apache-2.0) · Win/macOS/Linux (Java) · 🟢 — Standalone editor for the Markdown-compatible **MMD** plain-text format; the engine also powers the most-downloaded JetBrains mindmap plugin (208k+ downloads).
- **[KIKUmap](https://github.com/tang1693/KIKUmap)** — MIT · macOS (Swift, menu bar) · 🟢 (very active, Nov 2026) — Visualize Claude/ChatGPT/AI conversations as a live mind map.
- **[Linwood Butterfly](https://github.com/LinwoodDev/Butterfly)** — AGPL-3.0 · Win/macOS/Linux/Android/Web (Flutter) · 🟢 (~2.1k★) — Minimalist open-source sketchbook/note canvas usable for hand-drawn maps.

### Open source web / self-hosted apps

- **[Drawnix](https://github.com/plait-board/drawnix)** — MIT · Web (local-first) · 🟢 (~15k★, active) — All-in-one FOSS whiteboard with a genuinely good **mindmap module** (on the Plait framework): mindmap + flowchart + freehand + Mermaid import. The best "open-source Miro-with-mindmaps" today.
- **[AFFiNE](https://github.com/toeverything/AFFiNE)** — BlockSuite core MPL-2.0/MIT (mixed) · Web + self-host + desktop · 🟢 (~74k★, very active) — "More than Notion and Miro": docs + canvas + databases.
    - Mind map is a **first-class BlockSuite canvas element**: own `mindmap` schema, snapshot module, 5 preset layout styles (`@blocksuite/affine-model`)
    - Yjs CRDT underneath → intrinsic realtime collaboration, and a built-in AI mind-map generator
- **[Simple Mind Map (app)](https://wanglin2.github.io/mind-map/)** ([repo](https://github.com/wanglin2/mind-map)) — MIT (lib; "Pro" companion is commercial) · Web/self-host · 🟢 (~12.9k★, active Aug 2026) — Commercial-grade web mindmap editor + the library behind it.
    - Many layouts; ~25 optional plugins: minimap, KaTeX formulas, watermark, focus mode, web-worker rendering
    - Collaboration via `yjs` + `y-webrtc`
    - Imports XMind/OPML/markdown; exports PNG/SVG/PDF/JSON/SMMD/markdown
    - Docs mostly Chinese (i18n partial)
- **[my-mind](https://github.com/ondras/my-mind)** — MIT · Web (single-page, offline-capable) · 🟢 (~3.4k★, active Oct 2026) — Elegant keyboard-centric single-author classic by Ondřej Žára; supports XMind/FreeMind import, storage in localStorage/Google Drive.
- **[TeamMapper](https://github.com/b310-digital/teammapper)** — AGPL-family *(verify)* · Self-host (NestJS) · 🟢 (~520★, very active Nov 2026) — Collaborative shared mind-mapping sessions; popular in education.
- **[mindmaps](https://github.com/drichard/mindmaps)** — MIT · Web (static/offline HTML5) · 🔴 (dormant 2023, ~2.9k★) — "Open source, offline capable, mind mapping application." Root of TeamMapper.
- **[WiseMapping](https://www.wisemapping.com/)** ([repo](https://github.com/wisemapping/wisemapping-open-source), Java) — ⚠️ custom **WiseMapping Public License** — ⚠️ Apache-2.0 **plus a mandatory "powered by WiseMapping" attribution** on every screen (removable via email waiver) · Web + Docker self-host + Desktop · 🟢 (active Oct 2026)
    - The veteran (2007) collaborative OSS mindmap *suite*; 200k+ Docker pulls
    - Imports/exports Freeplane/XMind/MindManager; ships a ChatGPT "Mind Map Copilot" GPT
- **[Mindmapp](https://github.com/cedoor/mindmapp)** — AGPL-3.0 · Web/Electron (Angular) · 🟡 (~520★) — Simple, minimalist web mind mapper.
- **[Blink Mind Desktop](https://github.com/awehook/blink-mind-desktop)** — license *(unverified on repo)* · 🟡 (~730★, dormant 2022) — Electron mindmap + outline app; also has a VS Code extension.
- **[Neurite](https://github.com/satellitecomponent/Neurite)** — license *(unverified)* · 🟡 (~2.2k★, semi-active Mar 2026) — "Fractal Graph-of-Thought" rhizomatic mind-mapping web desktop with AI agents.
- **[MindGeniusAI](https://github.com/xianjianlf2/MindGeniusAI)** — license *(unverified)* · 🟢 (~285★, self-hostable) — AI agent: PDFs → editable mind maps (AntV X6, BYO LLM key, built-in RAG).
- **[Mind-Map-Wizard](https://github.com/linus-sch/Mind-Map-Wizard)** — license *(unverified)* · 🟢 (active Jul 2026) — Local-first AI-assisted mindmapping in the browser.
- **[mindmapvault](https://github.com/mindmapvault/mindmapvault-server)** — AGPL-3.0 · Docker self-host · 🟢 (new/small) — Zero-knowledge-encrypted mindmap server.
- **[SmallSO (小书匠)](https://github.com/suziwen/markdownxiaoshujiang)** — license *(unverified)* · 🟢 (~1.7k★, active) — Local-first Chinese note app shipped with a built-in mindmap editor.
- **[lx-doc](https://github.com/wanglin2/lx-doc)** — license *(unverified)* · 🟡 (~330★) — Self-hosted cloud docs suite including mindmap/whiteboard modes.

### Text- & markdown-based map generators

- **[markmap](https://github.com/markmap/markmap)** — MIT · 🟢 (~13.8k★, very active Nov 2026) — *The* Markdown → interactive mindmap tool.
    - CLI: `npx markmap-cli notes.md` → standalone, fully-offline interactive HTML
    - Layouts via frontmatter: tree / two-sided / org-chart; themes + `<!-- markmap: fold -->` comments
    - Ecosystem packages: `markmap-lib`, `markmap-view` (d3-based), `markmap-autoloader`, `markmap-toolbar`, `markmap-html-parser`, `<markmap-view>` web component, katex/prism plugins
    - ⚠️ Nov 2026 restructure added scoped names (`@markmap/parse`, `@markmap/core`, `@markmap/canvas`, `@markmap/page`) *alongside* the legacy `markmap-*` packages
    - Siblings: [markmap-vscode](https://github.com/markmap/markmap-vscode), [mkdocs_markmap](https://github.com/markmap/mkdocs_markmap), [coc-markmap](https://github.com/markmap/coc-markmap); community action [bssm-oss/markmap-actions](https://github.com/bssm-oss/markmap-actions) (no official action exists)
- **[Mermaid — `mindmap` diagram](https://mermaid.js.org/syntax/mindmap.html)** ([repo](https://github.com/mermaid-js/mermaid)) — MIT · 🟢 (~91k★) — Indented-text `mindmap` syntax rendered natively inside GitHub, GitLab, VS Code, Docusaurus, etc. CLI renderer: [mermaid-cli](https://github.com/mermaid-js/mermaid-cli) (`mmdc` → SVG/PNG/PDF).
- **[PlantUML — `@startmindmap`](https://plantuml.com/mindmap)** ([repo](https://github.com/plantuml/plantuml)) — GPL-3.0+/EPL · Java · 🟢 — Org-chart-style mind maps in PlantUML syntax with a huge server-integration ecosystem.
- **[Argdown](https://argdown.org/)** ([repo](https://github.com/argdown/argdown)) — MIT *(verify in repo)* · Web/VS Code/CLI · 🟢 (v2.0 released Dec 2025) — Markdown-family syntax for **argument maps**: `+`/`-` support and attack relations between claims; ArgVu font with dedicated ligatures; PDF/SVG/web-component export. (Also listed under [Argument mapping](#argument-mapping).)
- **[mindr](https://github.com/pzhaonet/mindr)** — R/CRAN · 🟢 (~580★, active Oct 2026) — Markdown/Rmd ↔ mindmap conversions (FreeMind/XMind output) from the R world.
- **[lini](https://github.com/monfa-red/lini)** — MIT · Rust (CLI) · 🟢 — Plain-text mini-language emitting mindmaps, trees, charts and ER schemas (Mermaid-ish, in Rust).
- **[crumbs](https://github.com/lucasepe/crumbs)** — MIT · Go (CLI) · 🔴 (2020) — Asterisk-indented text → mindmap image.
- **[mdSilo](https://github.com/mdSilo/mdSilo-app)** — license *(unverified)* · 🟢 (~850★, Tauri) — Knowledge base with mind-map views of your silo.
- **GitHub topics worth browsing directly** — dozens more small "markdown→map" utilities live under [`topic:mindmap`](https://github.com/topics/mindmap) (988 repos) and [`topic:mind-map`](https://github.com/topics/mind-map) (363 repos).

### CLI & terminal tools

- **[h-m-m](https://github.com/nadrad/h-m-m)** — GPL-3.0 · Terminal (PHP) · 🟢 (~2.3k★, active Jul 2026) — *Hackers Mind Map*: fast keyboard-centric TUI editor for text-tree mindmaps; pipes to/from editors (Emacs etc.), scriptable.
- **[tmmpr](https://github.com/tanciaku/tmmpr)** — MIT · Terminal (Rust, ratatui) · 🔴 (~350★, archived) — Interactive TUI mindmap editor.
- **markmap-cli** — see [markmap](#text--markdown-based-map-generators) — `npx markmap-cli` renders markdown to interactive HTML offline.
- **mermaid-cli** — see above — `mmdc -i mindmap.mmd -o out.svg`.
- **@xmindltd/xmind-cli** — official XMind CLI — "Create and edit `.xmind` files for AI Agents" (v0.2.3, Aug 2026; keywords include claude-code/cursor/codex).
- **[Dagzet](https://github.com/PaulBatchelor/Dagzet)** — Rust · 🟡 — Text format for DAG-Zettelkasten-style mindmap graphs.
- **[oxmap](https://github.com/RohanAdwankar/oxmap)** — TUI mindmaps (tiny).
- **[rmm (Recon MindMap)](https://github.com/Alevsk/rmm)** — MIT · Go · 🟡 — Tool and format for pentesting recon mindmaps.

---

## Libraries & SDKs

For embedding mind maps in your own apps. Rendering-approach and dependency details verified from npm registry metadata (Nov 2026).

- **[mind-elixir](https://github.com/SSShooter/mind-elixir-core)** (npm `mind-elixir`) — MIT · 🟢 (v6.0.0, Nov 2026) — Framework-agnostic TypeScript mindmap core. **Zero runtime dependencies.**
    - Rendering: DOM + SVG; data model: plain `{topic, children[]}` tree; `getData()` / `init(data)` / inline markdown topics
    - Plugin contract: `mind.install(plugin)`, event bus `mind.bus`, context-menu slots; `@mind-elixir/plugin-*` (richtext, i18n, layout, hotkeys)
    - Format plugins: `import-xmind`, `import-freemind`, `import-markdown`, `export-xmind`, `export-html`, image export; community `@erseco/mind-elixir-export-mermaid`
    - Core exports SVG/PNG/HTML · Docs: [docs.mind-elixir.com](https://docs.mind-elixir.com) · Hosted app: [app.mind-elixir.com](https://app.mind-elixir.com)
- **[Simple Mind Map (library)](https://github.com/wanglin2/mind-map)** (npm `simple-mind-map`) — MIT · 🟢 (0.14.x, Jul 2026) — SVG rendering on `@svgdotjs/svg.js`; the full-featured sibling of [mind-elixir](https://github.com/SSShooter/mind-elixir-core).
    - Deps: `quill` (rich text), `katex`, `jszip`, `pdf-lib`, `xml-js` (xmind/opml parsing), `mdast-util-from-markdown`, `yjs` + `y-webrtc` (realtime)
    - ~25 optional plugins, theming system, web-worker rendering for large maps
- **[jsMind](https://github.com/hizzgdev/jsmind)** (npm `jsmind`) — **BSD-3-Clause** (not MIT!) · 🟡 (0.9.1, Dec 2025) — Vanilla ES6 mindmap library from the Baidu KityMinder ecosystem.
    - No framework, DOM/CSS rendering, UMD/legacy builds; data model: `{meta, format: 'node_tree'|'node_array', data}`
    - Plugin system (`$jm.plugin.register`) with official `draggable-node` and `screenshot` plugins in-tree
- **[kityminder-core](https://github.com/fex-team/kityminder-core)** — BSD-3-Clause · 🔴 — Baidu's mindmap engine (`fex-team`, 2012-era): the `.km` JSON format lives on via DesktopNaotu and the VS Code extensions below.
    - Family: `kityminder` (~4.8k★, frozen 2019), `kityminder-editor` (~3.2k★), `kityminder-core` (~1.4k★)
- **[BlockSuite](https://github.com/toeverything/blocksuite)** (npm `@blocksuite/*`) — MPL-2.0/MIT family · 🟢 — AFFiNE's editor toolkit; mind map is a native element type (`@blocksuite/affine-model` ships `elements/mindmap/` with 5 style presets + snapshot modules); Yjs-driven.
- **[React Flow / Svelte Flow](https://github.com/xyflow/xyflow)** (npm `@xyflow/react`, `@xyflow/svelte`) — MIT · 🟢 (~39k★) — The go-to node-graph UI library; not mindmap-specific (no first-party mindmap layout — verified), but countless mindmap editors are built on it.
- **[Vue Flow](https://github.com/bcakmakoglu/vue-flow)** (npm `@vue-flow/core`) — MIT · 🟢 — Vue sibling of React Flow; mindmap canvases are userland examples.
- **[Butterfly](https://github.com/alibaba/butterfly)** — MIT/Apache · 🔴-ish (dormant May 2024) — Alibaba's diagramming engine (React/Vue) with tree/mindmap layouts, used in Alibaba Cloud consoles.
- **[graphview](https://github.com/nabil6391/graphview)** — MIT · Flutter/Dart · 🟢 (~470★) — Tree/graph layout widget used for mindmap-style UIs on mobile.
- **[android-thinkmap-treeview](https://github.com/guaishouN/android-thinkmap-treeview)** — MIT · Java/Android · 🟢 (~550★) — Thinkmap-style tree/mindmap custom view for Android.
- **[xmindltd/xmind-sdk-js](https://github.com/xmindltd/xmind-sdk-js)** · 🟡 (dormant Oct 2024) — Official SDK for generating `.xmind` files headlessly; superseded by the npm `xmind` package (v2+, renamed from `xmind-sdk`), `xmind-generator`, and the official [`xmind-embed-viewer`](https://github.com/xmindltd/xmind-embed-viewer) for rendering `.xmind` files on any website.
- **[GoJS](https://github.com/NorthwoodsSoftware/GoJS)** — ⚠️ commercial (evaluation-only source) — Proprietary treeLayout/graphLinks engine frequently used in commercial mindmap apps; the common OSS alternative is React Flow.

---

## Editor & knowledge-base integrations

### Obsidian

*(Obsidian itself and its Canvas feature are closed-source, but `.canvas` files are open JSON.)*

- **[obsidian-enhancing-mindmap](https://github.com/MarkMindCkm/obsidian-enhancing-mindmap)** — MIT · 🟡 (~710★, active Jan 2026) — Editable mind maps over markdown notes; markmap-based read mode + rich edit mode; exports PNG/Markdown/Xmind.
- **[Mindmap NextGen](https://github.com/james-tindal/obsidian-mindmap-nextgen)** — 🟢 (~410★, active Oct 2026) — Interactive markmap views of notes, embedded mindmap code blocks, LaTeX, checkboxes; successor to lynchjames' original.
- **[obsidian-advanced-mindmap](https://github.com/junhuihuang/obsidian-advanced-mindmap)** — MIT · 🟢 — Updated markmap-based fork of Mindmap NextGen.
- **[Obsidian-Canvas-MindMap](https://github.com/Quorafind/Obsidian-Canvas-MindMap)** — license *(unverified)* · 🔴 (dormant Sep 2024, ~370★) — Makes Obsidian Canvas behave like a mindmap (sibling auto-arrangement etc.).
- **[obsidian-kity-mind](https://github.com/eightHundreds/obsidian-kity-mind)** — license *(unverified)* · 🟢 — Baidu Naotu (kityminder) engine inside Obsidian.
- **obsidian-markmind** ([MarkMindCkm/obsidian-markmind](https://github.com/MarkMindCkm/obsidian-markmind)) — ⚠️ partially closed-source (rich mode proprietary; basic mode OSS) — Popular mind map + outline + PDF-annotation plugin.
- **[Obsidian Excalidraw mindmap scripts](https://github.com/zsviczian/obsidian-excalidraw-plugin)** — Excalidraw for Obsidian has **no native mindmap layout** (verified against release notes); mindmaps come from Automate Script Library entries like *Mindmap format* (by pandoralink) and *Mindmap connector*, converting markdown outlines into drawn nodes+arrows.

### VS Code

- **[markmap-vscode](https://github.com/markmap/markmap-vscode)** (id `gera2ld.markmap-vscode`, also on Open VSX) — MIT · 🟢 — "Open as markmap" live preview of markdown files; themes/layouts via frontmatter; offline export to HTML/SVG/PNG.
- **[markmap-universe/vscode-extension](https://github.com/markmap-universe/vscode-extension)** — MIT · 🟢 — Markmap ecosystem's own preview extension.
- **[souche/vscode-mindmap](https://github.com/souche/vscode-mindmap)** — AGPL-3.0 · 🔴 (2022) — The standard KityMinder-based editor for `.km`/`.xmind` files; JetBrains port exists (see below).
- **[vscode-blink-mind](https://github.com/awehook/vscode-blink-mind)** · 🔴 (2022) — blink-mind-based mindmap editor.
- **[oorzc/vscode-mindmap](https://github.com/oorzc/vscode-mindmap)** — MIT · 🟢 (active May 2026) — Another kityminder-descendant editor.
- **[vscode-markdown-markmap](https://github.com/phoihos/vscode-markdown-markmap)** — MIT · 🔴 (2023) — Markmap inside the markdown preview.
- **[Dendron](https://github.com/dendronhq/dendron)** — Apache-2.0 · 🔴 (company wound down) — Hierarchy-first PKM ("notes as trees"); historically significant, effectively unmaintained.
- **[felisMindmap](https://github.com/season-studio/felisMindmap)** — license *(unverified)* · 🟡 — PWA + VS Code mindmap editor (small).

### Neovim / Vim

- **[markmap.nvim](https://github.com/Zeioth/markmap.nvim)** — GPL-3.0 · 🟢 — Visualize markdown notes as markmap mindmaps from within Neovim.
- **mind.nvim** — the famous Phaazon plugin ("The power of trees at your fingertips") had its original repo **deleted**; maintained forks exist ([williamboman/mind.nvim](https://github.com/williamboman/mind.nvim), [malramsay64/mind.nvim](https://github.com/malramsay64/mind.nvim)) — treat as fork-maintained.
- **[muhfaris/mindmap.nvim](https://github.com/muhfaris/mindmap.nvim)** · 🟢 (Aug 2026) — Spatial terminal mindmapping.
- **[nvim-codebase-mindmap](https://github.com/gosvig123/nvim-codebase-mindmap)** — LSP-based call-graph mindmaps (tiny).

### Emacs / Org-mode

- Org-mode itself ([orgmode.org](https://orgmode.org), GPL-3.0) is the original outliner-as-file-format; the ecosystem below renders org trees as maps:
- **[org-mind-map](https://github.com/the-ted/org-mind-map)** — GPL-3.0 · 🟡 (last push 2023) — MELPA package: renders Org trees as Graphviz SVG/PDF/PNG "mind maps".
- **[org-brain](https://github.com/Kungsgeten/org-brain)** — MIT · 🟢 (~1.75k★) — Org-mode wiki/concept-mapper; its Viz mode renders a mindmap of your brain.
- **[org-graph-view](https://github.com/alphapapa/org-graph-view)** — license *(unverified)* · 🟡 (~250★) — Clickable graphical mindmap view of Org buffers.
- **[eaf-mindmap](https://github.com/emacs-eaf/eaf-mindmap)** — GPL-3.0 · 🔴 (2023) — Keyboard-driven mindmap editor via the Emacs Application Framework.
- **[xmind-org-el](https://github.com/akirak/xmind-org-el)** — GPL-3.0 · 🟡 — XMind → Org conversion.

### JetBrains

- **SciaReto Mind Map** ([plugin](https://plugins.jetbrains.com/plugin/8045), source in [raydac/netbeans-mmd-plugin](https://github.com/raydac/netbeans-mmd-plugin)) — Apache-2.0 · 🟢 — **208k+ downloads**: the dominant JetBrains mindmap plugin; edits Markdown-compatible MMD files in IntelliJ/NetBeans/most Jetbrains IDEs.
- **markdown-editor** ([shuzijun](https://plugins.jetbrains.com/plugin/10173-markdown-editor)) — huge JetBrains markdown editor embedding a KityMinder-based mindmap.
- **Mindmap (mindmapx, `com.souche.mindmap.idea`)** — JetBrains port of souche/vscode-mindmap (`.km`/`.xmind`).
- **[mindmap – Call Graph Visualizer](https://github.com/vishal2376/mindmap)** — MIT · 🟢 (Kotlin/Android) — Android Studio plugin rendering code call graphs as mindmaps.

### Joplin / Zotero / TiddlyWiki

- **[joplin-plugin-kity-minder](https://github.com/xeden3/joplin-plugin-kity-minder)** — MIT · 🔴 (Apr 2023) — KityMinder mindmaps in Joplin.
- **[Kminder](https://github.com/calandradas/Kminder-Mindmap-Joplin-Plugin)** — license *(unverified)* · 🟢 (~35★) — Joplin mindmap plugin with XMind/MindManager/markdown import, JSON/PNG/MD export.
- **[Zotero Better Notes](https://github.com/windingwind/zotero-better-notes)** — AGPL-3.0 · 🟢 (~8.4k★, active) — Zotero note manager with embedded **markmap** mindmap views over your literature notes.
- **[TiddlyMap](https://github.com/felixhayashi/TW5-TiddlyMap)** — license *(unverified; historically BSD-family)* · 🟡 (~910★, updated Jan 2026) — TiddlyWiki plugin drawing topic/concept maps from wiki topology.

---

## Proprietary Software

### Dedicated mind mapping SaaS

- **[MindMeister](https://www.mindmeister.com)** — 🟢 · Web + iOS/Android · Freemium (3 free maps; Personal ~$3.50/user/mo, Pro $5.50, Business $8.50 billed annually) — The classic collaborative mapper (MeisterLabs); now has Meister AI generation and a Claude MCP integration. Historical REST API at `mindmeister.com/api` — current status *(verify)*.
- **[Coggle](https://coggle.it)** — 🟢 · Web · Freemium (unlimited public diagrams; 3 private on free; Awesome $5/mo, Organization $8/member/mo; on-prem Enterprise) — Loopy shared-diagram model with real-time collab, loops/multi-roots, Visio/Freemind export; documented **public API** (JSON nodes, OPML import via official `coggle-opml-importer` sample, npm `coggle` client).
- **[Mindomo](https://www.mindomo.com)** — 🟢 · Web + native desktop (offline) + iOS/Android · Freemium; Premium ~€6/mo, Team ~€13.5/user/mo; one-time desktop edition — Education-focused (assignment workflows), Gantt/outline views, AI generator.
- **[XMind](https://xmind.app)** — 🟢 · Win/macOS/Linux/iOS/Android/Web · Freemium (10 free online maps; Pro $4.92/mo, Premium $8.25/mo annually; one sub = 5 desktops + 5 mobiles) — The most polished commercial mapper (Supermind Pte. Ltd., Singapore); Premium adds realtime collab, Gantt, tasks, 500 AI credits/mo. ⚠️ History: XMind 3.x from ~2008 was **GPL open source**; modern XMind (2018+) is fully proprietary.
- **[bubbl.us](https://bubbl.us)** — 🟢 · Web · Freemium (~$5–6/mo Premium) — Bubble-style mapping since 2005; real-time collaboration.
- **[GitMind](https://gitmind.com)** — 🟢 · Web + desktop + mobile · Freemium — Pivoted into an "AI second brain": text/video/audio/PDF/image → mind maps, flowcharts, UML.
- **[Scrintal](https://www.scrintal.com)** — 🟢 · Web + desktop (Electron) · Freemium/subscription — Infinite-canvas visual studying/research (blocks → docs), Gobu AI research assistant.
- **[Mind42](https://mind42.com)** — 🟢 but feature-frozen ~a decade · Web · Free (closed, ad-supported) — Surviving 2007-era simple mapper.
- **[SpiderScribe](https://spiderscribe.net)** — 🟡 (site maintained, blog dormant since 2016) · Web (+iPad "Jr.") · Free tier; Business $25/mo — Maps mixing notes, files, images, calendar events, geo-locations.
- **[Mapify](https://mapify.so)** — 🟢 · Web + mobile + extension · Freemium/credits — AI summarizer → mind maps (PDF/YouTube/webpage/audio); product of **Supermind Pte. Ltd. — the XMind company** (descended from ChatMind / Xmind AI).

### Desktop apps (proprietary)

- **[MindManager](https://www.mindmanager.com)** — 🟢 · Win/macOS + web "Essentials" + Go mobile viewer · Subscription (~$99/yr Essentials; Professional one-time/perpetual option ≈$479 + $199/yr *(verify — JS-rendered pricing)*) — The enterprise heavyweight (Corel): Gantt, integrations (Teams/SharePoint/Jira), IT admin controls. `.mmap` = zip-wrapped XML (namespace `schemas.mindjet.com/MindManager/Application/2003`).
- **[MindNode](https://www.mindnode.com)** — 🟢 · Apple-only (Mac/iPhone/iPad/Watch/Vision Pro) · Free core app + **MindNode Plus** $2.99/mo or $24.99/yr; in Setapp — The nicest mapping experience on Apple platforms; rich import/export (FreeMind, OPML, XMind, Markdown, TaskPaper, TextBundle); ships a local **MCP server** (Settings → AI) for Claude Desktop/Claude Code/ChatGPT/Codex agents.
- **[SimpleMind](https://simplemind.eu)** — 🟢 (v2.10, Aug 2026) · Win/macOS/iOS/Android · **One-time purchase per platform, no subscriptions** — Free-form layout, local-first data ownership; free edition + Viewer.
- **[TheBrain](https://www.thebrain.com)** — 🟢 (v15, 2026) · Win/macOS/Linux/iOS/Android/Web · ⚠️ **Desktop app now completely free**; paid Pro Service $15/mo (sync+AI), TeamBrain $25/user/mo, Max $40/mo — Dynamic associative "brain" of thoughts/parents/children/jump links, 28+ years old; Cerebro AI add-on. Formerly "PersonalBrain".
- **[EdrawMind](https://www.edrawmind.com)** (formerly MindMaster) — 🟢 · Win/macOS/Linux/web/mobile · Freemium + subscription or perpetual — Wondershare's mapper with heavy AI push (PDF/YouTube → map, map → slides), template gallery.
- **[Ayoa](https://www.ayoa.com)** (formerly iMindMap/ThinkBuzan) — 🟢 (page updated Oct 2026) · Web + desktop + mobile · Freemium (10 free maps) — Organic hand-drawn Buzan-lineage maps (Chris Griffiths) + task boards + Gantt + AI.
- **[Scapple](https://www.literatureandlatte.com/scapple)** (Literature & Latte) — 🟢 · macOS/Windows · ~$31 one-time — Freeform notes where every note is independent and only connections you draw exist — the deliberately anti-hierarchy mind mapper.
- **i2Brain** — 🟡 · Java/Windows · $59 — "Multi-dimensional" mind mapping (up to 15 data dimensions mapped onto position/size/color). Niche classic.
- **iThoughts / iThoughtsX** ([toketaware.com](https://toketaware.com)) — ⛔ **company ceased trading Jan 2024** — apps still run, no updates/new licenses; author recommends migrating out via ITMZ/MindManager/XMind/FreeMind exports.

### Whiteboard & visual collaboration suites

*(All have mind-map shapes/expand-AI; all closed-source, freemium.)*

- **[Miro](https://www.miro.com)** — 🟢 · Web/desktop/mobile · Free (3 boards), Starter ≈$8/user/mo — Market-leading canvas; "Miro Mind Map" template + Miro AI topic expansion.
- **[FigJam](https://www.figma.com/figjam/)** (Figma) — 🟢 · Free (3 files), ~$3/editor/mo Pro — Whiteboards + mindmap connectors + AI, inside the Figma ecosystem.
- **[Whimsical](https://whimsical.com)** — 🟢 · Web + desktop · Free (50 objects/mo), Pro $10/editor/mo — ⚠️ **Acquired by Figma (2022)**; first-class "Whimsical AI Mind Maps".
- **[Mural](https://www.mural.co)** — 🟢 · Freemium — Facilitation-oriented whiteboard (mind-map clustering, timer, voting).
- **[Lucidchart / Lucidspark](https://www.lucidchart.com)** — 🟢 · Freemium (3 docs) — Lucidspark whiteboard has mind-map/freeform clustering; Lucidchart covers structured diagrams incl. concept-map templates.
- **[Canva Whiteboards](https://www.canva.com)** — 🟢 · Free tier — Built-in free mind-map app type among Canva templates.
- **[Heptabase](https://heptabase.com)** — 🟢 · Desktop + mobile · Pro $8.99/mo … Premium+ $53.99/mo — Infinite-whiteboard PKM for researchers where notes sit on map-like canvases.

### AI-powered map generators

- **[Napkin AI](https://www.napkin.ai)** — 🟢 · Web · Freemium (weekly free credits; PNG/PDF free export, PPT/SVG paid) — Paste text → editable mind maps/flowcharts/infographics; SOC 2 Type II, ISO 27001.
- **[MyMap.AI](https://mymap.ai)** — 🟢 · Web · Freemium *(verify — 403 to automated fetch)* — One of the original "prompt → map" tools.
- **[TreeMind (树图)](https://shutu.cn)** — 🟢 · Web + desktop + mobile (Chinese; Shanghai Jushita) · Freemium + VIP — One-sentence-to-mindmap; AI plugin partner of Baidu Ernie, iFlytek Spark, ByteDance Coze; enterprise SDK/API.
- OSS/local-first counterparts: [MindGeniusAI](https://github.com/xianjianlf2/MindGeniusAI), [Mind-Map-Wizard](https://github.com/linus-sch/Mind-Map-Wizard), [Neurite](https://github.com/satellitecomponent/Neurite), [KIKUmap](https://github.com/tang1693/KIKUmap).
- AI topic-expansion is now a standard checkbox inside XMind, EdrawMind, Mindomo, MindMeister, Miro, Whimsical, GitMind, AFFiNE, etc.

---

## Adjacent mapping genres

### Concept mapping

Concept maps are labeled graphs (nodes + *linking phrases*), not radial trees — different intellectual genre, related tools.

- **[IHMC CmapTools](https://cmap.ihmc.us/)** — 🟢 (©2026) · Win/macOS/Linux/iPad · **Free but closed-source** ("public domain" claim unverified) — The academic standard for concept maps (Florida Institute for Human & Machine Cognition); plus CmapCloud and CmapServer for shared knowledge models.
- **[VUE](https://github.com/VUE/VUE)** — 🔴 (Tufts; unmaintained since Jan 2024) — concept-mapping presentation tool (also listed above).
- **[CompendiumNG](http://compendiumng.org/)** · 🔴 (site/news frozen 2016; forum abandoned) — OSS IBIS-style dialogue & issue mapping (successor to Open University Compendium, which is defunct).
- **[yEd](https://www.yworks.com/products/yed)** — 🟢 (v3.25.x) · Free-of-charge but **closed-source** (yWorks) · Java cross-platform — Not a mapper per se, but its automatic graph layouts + Excel/XML import make it the Swiss-army knife for one-off concept/spider graphs. (Browser sibling: yEd Live.)

### Argument mapping

- **[Argdown](https://argdown.org/)** — MIT · 🟢 (v2.0 Dec 2025) — Markdown-family argument-mapping language; VS Code extension, CLI, ArgVu font, PDF/SVG/web-component export. (Full entry above.)
- **[Kialo](https://www.kialo.com)** — 🟢 · Web · Free to use — Debate-tree platform at internet scale (34k+ public debates); Kialo Edu variant for classrooms.
- **[Rationale](https://www.rationaleonline.com/)** — 🟢 (ReasoningLab) · Web · Subscription + student tiers — Reason/objection argument-map editor used in logic courses (Princeton, UvA…). ⚠️ `rationale.com.au` is now an unrelated site — use `rationaleonline.com`.

### Outliners & tree-thinking tools

Tree-editing is mind mapping's linear twin; many mappers import/export these formats. *(Listed here by function rather than by license.)*

- **[Workflowy](https://workflowy.com)** — 🟢 · Web/desktop/mobile · Freemium — The infinite-zoom bullet outliner; OPML export.
- **[Dynalist](https://dynalist.io)** — 🟢 (slow development) · Web/desktop/mobile · Freemium — Infinitely-nesting outliner by the future Obsidian team; documented API.
- **[Checkvist](https://checkvist.com)** — 🟢 (Checkvist s.r.o., active 2026) · Web · Freemium — Keyboard-first checklist/outliner with markdown and an open API.
- **[Tana Outliner](https://outliner.tana.inc)** — 🟢 · Web/desktop · Freemium — ⚠️ The Tana PKM **pivoted** in 2025 to an "agentic meeting platform" (tana.inc); the Supertags/nodes outliner survives separately — link the outliner URL, not the corporate site.
- **[Roam Research](https://roamresearch.com)** — 🟢 · Web · Paid subscription — The original bi-directional-link outliner.
- Org-mode — see the [Emacs section](#emacs--org-mode).

### Freeform canvas & "brain" tools

- **[Novastart](https://novastart.com/)** — proprietary (verify) · Web/desktop (verify), active · Infinite canvas workspace for apps, shared canvases, and AI agents; Free plan, Pro $10/month, Team $20/month per user. A freeform workspace rather than a dedicated radial mind-map editor.

- **[TheBrain](https://www.thebrain.com)** — the associative-network category king (see desktop entry above).
- **[mymind](https://mymind.com)** — 🟢 · Web · Subscription — "Remember everything, organize nothing": private AI-assisted associative space, not a map editor per se.
- **[Heptabase](https://heptabase.com)** — canvas-based PKM (whiteboard section above).

---

## File Formats & Interoperability

### Formats

Quick reference (full structure details below):

| Format | Body | Primary users |
|---|---|---|
| **FreeMind `.mm`** / `.mmz` (zipped) | XML | FreeMind, Freeplane; the de-facto interchange standard |
| **Freeplane `.mm`** dialect | XML superset | Freeplane (superset with extra elements) |
| **XMind `.xmind`** | ZIP archive | XMind 8 ("legacy") and XMind 2020+/"Zen" (JSON) |
| **MindManager `.mmap`** | ZIP of XML (v5+) | MindManager |
| **KityMinder `.km`** | JSON | Baidu Naotu family, DesktopNaotu, VS Code extensions |
| **OPML 2.0** | XML outline | MindNode, Freeplane, XMind, Workflowy, pandoc |
| **Markdown outline** | headings / indented bullets | markmap, mind-elixir, Simple Mind Map, MindNode, mindr |
| **Org `.org`** | outline | Emacs; bridged to OPML/`.mm` |
| **Coggle** | server-side JSON | Coggle (API objects `{_id, text, offset}`) |
| **mind-elixir / jsMind / markmap** | JSON / markdown | see their entries above |

<details>
<summary><strong>Full format structure details</strong></summary>

- **FreeMind `.mm`** — XML: `<map version="…">` → nested `<node TEXT="…">` with `<icon/>`, `<edge/>`, `<richcontent TYPE="NOTE">` XHTML. Versions `0.7.1`–`1.0.1`. ⚠️ Never fully formally specified (an XSD exists only in the FreeMind SVN integration branch) — yet it remains the interchange lingua franca of the genre.
- **Freeplane `.mm` dialect** — XML superset: adds `<attribute*>`, `<hook>`, connector labels on `<arrowlink>`, encrypted maps, LaTeX/markdown/formula nodes. Version strings like `freeplane 1.1.x`; can also export "old format". Completed XSD published at [docs.freeplane.org](https://docs.freeplane.org/attic/old-mediawiki-content/Current_Freeplane_File_Format.html).
- **XMind `.xmind`** — ZIP archive, two generations: **XMind 8** (legacy: `content.xml` XML + manifest/meta/styles) and **XMind 2020+/"Zen"** (`content.json` + `metadata.json`; `children.attached` structure *(verify exact keys)*).
- **MindManager `.mmap`** — ZIP of XML (v5+): `ap:Map → ap:OneTopic → ap:Topic` tree, relationships in `ap:Relationships`; v4 and older = raw XML.
- **KityMinder `.km`** — JSON; kept alive by DesktopNaotu and `@ljheee/xmind-parser`.
- **OPML 2.0** — XML outline (`<outline text="">` nesting); spec at [opml.org/spec2](https://opml.org/spec2.opml). Recommended npm writer: [opml (Dave Winer)](https://github.com/scripting/opmlpackage); the PyPI `opml` lib is read-only & 2008-era — prefer hand-rolled ElementTree for writing.
- **Markdown outline** — headings and indented bullets; the de-facto import format everywhere.
- **Org `.org`** — bridges: `Org2OPML` (org → OPML for MindNode/FreeMind), `freemind.el`, `mm2outline`/`outline2mm` Perl scripts (FreeMind wiki), org-mind-map rendering.
- **markmap I/O** — input: markdown (headings/bullets → branches, other blocks → popovers) with frontmatter (`theme`, `layout`, `foldLevel`); output: offline HTML, SVG, PNG, or the `<markmap-view>` web component.
- **mind-elixir data** — JSON `{topic, id, style, tags, icons, hyperLink, image, expanded, children[]}`; inline-markdown topics.
- **jsMind data** — JSON `{meta, format: 'node_tree'|'node_array', data}`; `node_tree` = `{id, topic, children[]}`.

</details>

### Interop matrix

What each tool can **read**. (Export formats are listed in each tool's entry above.) Verified claims only; "(v)" = vendor claims — check in-app.

| Tool | `.mm` (FreeMind) | `.xmind` | `.mmap` | OPML | Markdown |
|---|---|---|---|---|---|
| **Freeplane** | ✓ | — | ✓ (direct import, 0.9b9+) | export; import (v) | export (v) |
| **FreeMind** | native | — | ✓ (0.9b9+) | — | — |
| **XMind** | ✓ (import) | native | historically (v) | ✓ (official flow, v) | (v) |
| **MindNode** | ✓ | ✓ | — | ✓ (in & out) | ✓ |
| **Coggle** | — | — | — | via API only | text via API |
| **mind-elixir** | ✓ (plugin) | ✓ (plugin) | — | — | ✓ (plugin) |
| **Simple Mind Map** | ✓ (v) | ✓ (v) | — | ✓ (v) | ✓ |
| **markmap** | — | — | — | via pandoc | ✓ (native input) |
| **WiseMapping** | ✓ (v) | ✓ (v) | ✓ (v) | — | — |
| **pandoc** | — | — | — | ✓ (in + out) | ✓ |

### Converters & parsers (npm / PyPI / GitHub)

**npm (JavaScript)**

| Package | Role | Notes |
|---|---|---|
| `xmind` (v2+, official) | build XMind Zen-era `.xmind` files | MIT; successor to `xmind-sdk` |
| `xmind-embed-viewer` (official) | render `.xmind` files in any webpage | |
| `@xmindltd/xmind-cli` (official) | headless `.xmind` create/edit for AI agents | 2026-08 |
| `@ljheee/xmind-parser` | **bidirectional XMind 8-XML *and* 2020-JSON ↔ KityMinder `.km`** | v1.1.3 (Apr 2026), ~31k dl/mo |
| `xmindparser` (JS, guanhuaxie) | XMind ↔ KityMinder (older sibling) | ⚠️ distinct from the PyPI package of the same name |
| `xmind-generator`, `@makerbi/xmind-generator`, `xmind-creator` | XMind file generation | 2025–2026 |
| `@wllzhang/xmind-to-canvas` | XMind → Obsidian JSON Canvas (`.canvas`) | 2026-01 |
| `lakeboard-converter` (`lakeward-converter`) | Yuque `.lakeboard` & XMind → Markdown | 2026-10 |
| `coggle` (official) | Coggle API client | 2014-era, still canonical |
| `json-to-freemind` | JSON → FreeMind `.mm` | |
| `opml` (Winer), `opmlparser`, `opml-to-json`, `opml-generator`, `opml-to-markdown` (azu, OmniOutliner-flavored), `feedsmith` | OPML read/write ecosystem | |
| `markmap-lib`, `markmap-view`, `markmap-cli` | markmap pipeline (legacy names) | ⚠️ monorepo *folders* still use legacy names — don't infer package names from repo paths |
| `@markmap/parse`, `@markmap/render`, `@markmap/page`, `@markmap/canvas`, `@markmap/autoloader`, `@markmap/element` | markmap pipeline (new scoped names, Nov 2026) | |
| ⚠️ trap packages | `freemind` (npm) is an unrelated web framework; `@xmindltd/xmindparser` **does not exist**; `modelicious` **does not exist** | don't cite these |

**PyPI (Python)**

| Package | Role | Notes |
|---|---|---|
| `xmindparser` (tobyqin) | XMind 8 + Zen + "Xmind 2026" → dict/json/xml/md/yaml; CLI `xmindparser file.xmind -markdown` | v1.2.2 (Feb 2026) |
| `xmind` (zhuifengshen) | create/parse/update XMind 8 workbooks (`content.xml`) | v1.2.0 (2019), still functional |
| `opml` (Nathan Yergler) | OPML **reader only** | 2008; ⚠️ abandoned — use JS lib or hand-rolled for writing |
| (no `freemind` PyPI package) | parse `.mm` with ElementTree/BS4 — the XML is trivial | |

**GitHub converters & bridges**

- [`lifehackjohn/mmap-tools`](https://github.com/lifehackjohn/mmap-tools) — read/write/convert MindManager `.mmap` in pure Python, zero deps.
- [`awardat/mmap2md`](https://github.com/awardat/mmap2md), [`pmanyeh/mmap-mcp-server`](https://github.com/pmanyeh/mmap-mcp-server) (MCP server reading `.mmap` without MindManager), [`lonjoy/mmap2json`](https://github.com/lonjoy/mmap2json) (Go) — MindManager bridges.
- [`ellockie/markdown-2-mindmap-converter`](https://github.com/ellockie/markdown-2-mindmap-converter) — markdown (e.g. ChatGPT output) → styled `.mm`; [`CodeJohnw/markdown_to_xmind`](https://github.com/CodeJohnw/markdown_to_xmind) — markdown → XMind.
- [`romilly/fm2md`](https://github.com/romilly/fm2md), [`null-none/freemind2markdown`](https://github.com/null-none/freemind2markdown), [`jutkko/mindown`](https://github.com/jutkko/mindown) (Go) — FreeMind `.mm` → markdown.
- [`GregoryHappy/mindmap_converter`](https://github.com/GregoryHappy/mindmap_converter) — MindMup/Freeplane/XMind/OPML/markdown/Word ↔, 100% in-browser.
- [`semk/Org2OPML`](https://github.com/semk/Org2OPML) — org-mode → OPML (MindNode/FreeMind-compatible).
- [`jiangxin/freemind-mmx`](https://github.com/jiangxin/freemind-mmx) — FreeMind fork with git-friendly fragment XML saves.
- [`bssm-oss/markmap-actions`](https://github.com/bssm-oss/markmap-actions) — community GitHub Action (no official markmap action exists).

### APIs, SDKs & MCP servers

The 2025–26 wave: mindmap apps exposing themselves to AI agents.

- **Coggle API** — documented at coggle.it/developer; bearer-token REST: `listDiagrams`, `createDiagram`, `getNodes()` (`{_id, text, offset}`), `addChild`, `arrange`; official npm `coggle` client; OPML import sample app.
- **MindMeister API** — legacy REST documented at mindmeister.com/api; community clients date to 2011–2022; current status *(verify — shutdown not confirmed)*.
- **XMind** — official npm `xmind` SDK, `xmind-embed-viewer`, `@xmindltd/xmind-cli`; community MCP servers: `@41px/mcp-xmind`, `xmind-generator-mcp`, `@lifeng688/xmind-mcp`, `liyilin` variant, etc.
- **Freeplane** — built-in **MCP server** (official docs §4.5) + Groovy scripting API over `.mm`.
- **MindNode** — local **MCP server** on macOS (read-only by default, optional agent mutation; one-click Claude Desktop setup).
- **Miro / Mural / FigJam** — general board/plugin APIs can manipulate shapes (usable for hand-rolled mindmaps) but none expose a dedicated mindmap-node-tree widget API *(verify)*.

---

## Historical / unmaintained but influential

The genre's museum wing — understand these to understand the file formats and UX conventions of everything above.

> 🗿 Dead projects already listed inline above (with 🔴) are not repeated here: FreeMind, VUE, KityMinder, mindmaps, Blink Mind, Dendron, mind.nvim, CompendiumNG. The entries below have no other home in this list.

- **[MindMup](https://www.mindmup.com)** — ⚠️ historical OSS (2013–2016) carried a **non-compete clause**, making it non-free; current mindmup.com is proprietary; GitHub org holds only archived legacy repos (incl. `mapjs` render library once powering it). Best-in-class export list in its day.
- **[DeepaMehta](https://www.deepamehta.de)** — GPLv3 "post-desktop metaphor" topic-map platform; archived (last stable 4.9.2, 2018); succeeded by **DMX** ([dmx.systems](https://dmx.systems), v5.0 Aug 2020).
- **[Labyrinth](https://github.com/labyrinth-team/labyrinth)** — GPL-2.0, Python/GTK3 port of the GNOME mind mapper; official description: *"looking for maintainers"* (unmaintained since 2021). Sugar-learning fork: [labyrinth-activity](https://github.com/sugarlabs/labyrinth-activity).
- **Cayra** — 2008-era .NET/Silverlight concept mapper; site gone (tombstone).
- **XMind open-source editions (2008–~2013)** — GPL-licensed Eclipse-based XMind 3.x; code abandoned before the commercial pivot; no verified live repo link *(verify before citing)*.
- **Popplet** — ⛔ shut down **Aug 1, 2026** (announced on official site); the team's successor project is the K-12 concept-mapping tool Superstructures.io.
- **iThoughts (toketaWare)** — ⛔ ceased trading Jan 2024; apps still run (see [desktop entry](#desktop-apps-proprietary)).
- **Original Compendium (Open University)** — defunct; see CompendiumNG above.

---

## Related content repositories

Not software — collections of ready-made mindmaps (`\*.mm`/markmap files) useful as references or starters:

- [dformoso/machine-learning-mindmap](https://github.com/dformoso/machine-learning-mindmap) (~6.3k★) — ML tree of concepts.
- [Orange-Cyberdefense/ocd-mindmaps](https://github.com/Orange-Cyberdefense/ocd-mindmaps) (GPL-3.0) — offensive-security pentest mindmaps.
- [matro7sh/BypassAV](https://github.com/matro7sh/BypassAV) — AV-evasion map.
- [mdecrevoisier/Microsoft-eventlog-mindmap](https://github.com/mdecrevoisier/Microsoft-eventlog-mindmap) — Windows eventlog trees.
- [dsopas/MindAPI](https://github.com/dsopas/MindAPI) — API security assessment map.
- [dsopas/assessment-mindset](https://github.com/dsopas/assessment-mindset) — pentest mindset map.
- [5bhuv4n35h/pentestmindmap](https://github.com/5bhuv4n35h/pentestmindmap), [Alevsk/rmm](https://github.com/Alevsk/rmm), [automateyournetwork/mind_nmap](https://github.com/automateyournetwork/mind_nmap) (markmap-generated Nmap result maps).

---

## Contributing

PRs welcome — please keep one entry per line, in this shape:

```
- **[Name](https://link-to-repo-or-site)** — license · platform/status — one-line description incl. fine details.
```

Mark anything you can't personally verify as *(verify)*. Confirm repos still exist before adding; note dead projects explicitly rather than silently dropping them — this list doubles as an archive of the genre.

## License

This list's **text** is published under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/); each listed project keeps its own license.

---

*Data snapshot: 2026-11-08. Stars approximate at time of verification; pricing marked *(verify)* where vendor pages render via JS.*
