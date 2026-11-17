# ArkSight — Official MCP Server &amp; Open-Source Agent Skills

<p align="center">
  <img src="https://arksight.ie/icon-192.png" width="84" height="84" alt="ArkSight Logo" />
</p>

<p align="center">
  <strong>Official Model Context Protocol (MCP) Server, Interactive MCP App &amp; Free Public-Good Agent Skills for <a href="https://arksight.ie">ArkSight</a></strong><br />
  Simulate 26 eye and neurological vision conditions interactively inside chat, audit UI accessibility for real low-vision barriers, and help children &amp; adults communicate visual symptoms safely.
</p>

<p align="center">
  <a href="https://arksight.ie">Website</a> ·
  <a href="https://arksight.ie/issues">26 Eye Conditions</a> ·
  <a href="https://arksight.ie/support">MCP Setup &amp; Support</a> ·
  <a href="https://arksight.ie/llms.txt">llms.txt</a> ·
  <a href="https://mcptry.com/servers/io.github.ruhickson/arksight">MCPTRY Status</a>
</p>

---

## 1. Free Open-Source Agent Skills (`skills/`)

This repository includes two free, MIT-licensed **Agent Skills** (`SKILL.md` open standard) compatible with **Claude Code, Claude Desktop, Cursor, GitHub Copilot, Windsurf, Gemini CLI, OpenAI Codex, and Google Antigravity**:

| Skill | Audience | What It Teaches Your AI Agent |
| :--- | :--- | :--- |
| [`arksight-low-vision-accessibility`](./skills/arksight-low-vision-accessibility/SKILL.md) | **Developers, UX Designers, EdTech &amp; Healthcare Builders** | Runs a **6-Axis Ophthalmic UI Audit** beyond basic WCAG contrast math—catching peripheral toast traps (glaucoma/RP/hemianopia), central scotoma &amp; metamorphopsia typography breaks (AMD), dark-mode `#FFF`-on-`#000` halation (keratoconus/astigmatism), pattern-glare/motion triggers (migraine aura &amp; visual snow), and `200%` text-scale clipping—paired with live side-by-side ArkSight simulations. |
| [`arksight-vision-communication`](./skills/arksight-vision-communication/SKILL.md) | **Parents, Teachers (SEN), Caregivers &amp; Patients** | Guides empathetic, non-leading visual symptom questions (especially helping children express near vs. far blur, glare, or missing patches), enforces strict **same-day emergency ophthalmic red-flag screening**, and generates tailored https://arksight.ie simulations and 2-page printable clinic summaries. |

### Install Agent Skills in One Command

Using the cross-agent `skills` CLI (installs into Claude Code, Cursor, Copilot, Windsurf, Gemini CLI, Codex, or `.agents/skills/`):

```bash
npx skills add ruhickson/arksight-mcp
```

Or install an individual skill:

```bash
npx skills add ruhickson/arksight-mcp --skill arksight-low-vision-accessibility
npx skills add ruhickson/arksight-mcp --skill arksight-vision-communication
```

**Manual / Claude.ai Project Install:** Copy either folder from [`./skills/`](./skills/) into your project's `.agents/skills/` (or `~/.claude/skills/`), or upload `SKILL.md` + `references/` to a Claude Project.

---

## 2. Remote MCP Server &amp; Inline Chat Simulator (`https://arksight.ie/mcp`)

**ArkSight** (`io.github.ruhickson/arksight`) is a free, zero-auth remote **Streamable HTTP** MCP server and interactive **MCP App** hosted at:

```text
https://arksight.ie/mcp
```

- **Zero API keys or OAuth required** — connect immediately over standard Streamable HTTP (`POST https://arksight.ie/mcp`).
- **Interactive Inline MCP App (`ui://arksight/simulator.html`)** — renders a live multi-plane optical vision simulator (near dog, midground streetlamp, far mountains) directly inside MCP-Apps-capable hosts (ChatGPT, Claude, VS Code, Goose, MCP Inspector).
- **Child &amp; Family Friendly** — includes `kidFriendly` symptom phrasing so parents, teachers, and clinicians can help a child show what classroom boards, books, or night lights look like to them.
- **Privacy by Design** — zero cookies, zero accounts, zero personal health identifiers stored.

### Quick Connect (MCP)

#### Claude Code
```bash
claude mcp add --transport http arksight https://arksight.ie/mcp
```

#### Cursor / VS Code / Windsurf (`mcp.json`)
```json
{
  "mcpServers": {
    "arksight": {
      "url": "https://arksight.ie/mcp"
    }
  }
}
```

#### Claude Desktop / Claude.ai / ChatGPT / Perplexity
Add `https://arksight.ie/mcp` as a Custom Remote MCP Connector (no authentication token required).

### Available MCP Tools

| Tool | Read-Only | Description |
| :--- | :---: | :--- |
| `simulate_vision` | Yes | Renders an interactive first-person vision simulation for any of 26 eye conditions or custom multi-symptom slider overrides, returning deep-links and printable 2-page clinic summary URLs. |
| `assess_visual_symptoms` | Yes | Evaluates structured visual symptom parameters against educational condition profiles, highlighting urgent ophthalmic red-flag warnings when sudden sight-threatening symptoms are described. |
| `list_eye_conditions` | Yes | Lists all 26 supported refractive, corneal, lens, retinal, optic-nerve, and neurological vision conditions with category filters and direct simulation links. |
| `get_eye_care_resources` | Yes | Returns regional emergency ophthalmic guidance, national eye charities, and clinical bodies across Ireland, UK, USA, Canada, Australia/NZ, and Europe. |

---

## Clinical &amp; Emergency Disclaimer

ArkSight is an **educational and patient–clinician visual communication aid (Non-SaMD)**. It is **not** a medical device, clinical eye examination, or diagnostic tool.

> **Urgent Ophthalmic Symptoms:** If someone experiences a sudden dark curtain/shadow over vision, a sudden shower of floaters accompanied by flashing lights, sudden loss of half their visual field, sudden double vision, or severe eye pain/redness, seek **immediate same-day emergency ophthalmic or hospital eye care** ([regional emergency guidance](https://arksight.ie/resources)).

---

## Links &amp; Contact

- **Live Web App:** https://arksight.ie
- **MCP Endpoint:** `https://arksight.ie/mcp`
- **Registry Name:** `io.github.ruhickson/arksight`
- **Privacy Policy:** https://arksight.ie/privacy
- **Terms &amp; Clinical Disclaimer:** https://arksight.ie/terms
- **Support &amp; Bug Reports:** [help@arksight.ie](mailto:help@arksight.ie) (or open an issue in this repository)
- **Optical Clinics, Hospitals &amp; White-Label Pilots:** [partners@arksight.ie](mailto:partners@arksight.ie)
