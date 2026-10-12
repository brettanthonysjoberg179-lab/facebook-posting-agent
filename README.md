# Facebook Posting Agent & Media Generator

Production-ready autonomous AI agent for publishing growth updates, marketing posts, generated graphics, and videos securely to a Facebook Page via Meta Graph API and Meta MCP Server workflows.

## Features
- **Dynamic Media Generation:** Automatically generates professional 1200x630 social media graphics with custom titles, subtitles, and branding using Pillow (`--generate-image`).
- **Meta Graph API Integration:** Supports both text feeds (`/feed`) and photo attachments (`/photos`) using Page Access Tokens (`METAGRAPH_API_KEY`).
- **Meta MCP Server Compatibility:** Designed to integrate seamlessly with Meta Social Technologies & WhatsApp Business Remote MCP servers.
- **Dry-Run & Live Modes:** Safely test posts and media locally before publishing live.
- **Structured Audit Logging:** Automatically generates JSON audit reports (`logs/facebook_agent_report.json`).

## Setup & Configuration

1. Copy `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```
2. Configure credentials in `.env`:
   ```env
   METAGRAPH_API_KEY=your_page_access_token_here
   META_PAGE_ID=your_facebook_page_id_here
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Run dry-run mode with generated social image:
```bash
python facebook_posting_agent.py --dry-run --generate-image
```

Post from a markdown file with generated graphic:
```bash
python facebook_posting_agent.py --file post.md --generate-image --live
```
