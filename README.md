# Facebook Posting Agent

Production-ready autonomous AI agent for publishing growth updates and marketing posts securely to a Facebook Page via Meta Graph API.

## Features
- **Secure Meta Graph API Integration:** Uses Page Access Tokens (`METAGRAPH_API_KEY`) and Page IDs (`META_PAGE_ID`).
- **File & String Inputs:** Load post content directly from markdown files or CLI arguments.
- **Dry-Run & Live Modes:** Safely test and validate posts locally before publishing live.
- **Structured Audit Logging:** Automatically generates JSON audit reports of every posting execution.

## Setup & Configuration

1. Copy `.env.example` to `.env`:
   ```bash
   cp .env.example .env
   ```
2. Configure your Meta credentials in `.env`:
   ```env
   METAGRAPH_API_KEY=your_page_access_token_here
   META_PAGE_ID=your_facebook_page_id_here
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

Run in dry-run mode (default):
```bash
python facebook_posting_agent.py --dry-run
```

Post from a markdown file:
```bash
python facebook_posting_agent.py --file post.md --dry-run
```

Publish live to Facebook:
```bash
python facebook_posting_agent.py --live
```
