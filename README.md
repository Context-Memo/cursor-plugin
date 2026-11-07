<p align="center"><img src="assets/logo.svg" width="64" height="64" alt="Context Memo"></p>

# Context Memo for Cursor

Connects Cursor to [Context Memo](https://contextmemo.com), so the agent can read and act on your brands: AI visibility reports, prompt results, competitor share, AI bot traffic, memos, and landing pages.

The plugin adds one hosted MCP server, `https://contextmemo.com/api/mcp`. There is nothing to install locally and no API key in this repo. Each person signs in with their own Context Memo account.

## Requirements

- A Context Memo account. Sign up at [contextmemo.com/signup](https://contextmemo.com/signup) with a work email address.
- At least one brand set up in that account. If you connect before setting one up, the sign-in page links to brand setup. Finish it, then click Connect again in Cursor.
- A new brand's reports fill in as its first scans finish, so visibility and prompt results are sparse on day one.

## Setup

1. Install **Context Memo** from the Cursor Marketplace.
2. Open **Customize** in Cursor and click **Connect** on the `contextmemo` server.
3. Sign in to Context Memo in the window that opens.
4. Choose the brands and permissions this connection may use, then approve.

You can see and revoke connections any time in Context Memo under **Settings → Connected Apps**.

## Using it

Ask the agent in plain language. It starts with `list_brands` to find the brand id, then calls the tool it needs.

- "What's our AI visibility this month, and which competitors are gaining share?"
- "Which prompts do we lose to competitors, and what content gaps explain it?"
- "Draft a memo that answers our weakest prompt."
- "Duplicate our pricing landing page and update the hero copy."

## Tools

Which tools appear depends on the permissions you approve when connecting.

| Area | Tools |
| --- | --- |
| Brands | `list_brands`, `get_brand_summary`, `get_brand_context`, `get_integration_status` |
| Visibility and reporting | `get_visibility_report`, `get_prompt_results`, `get_competitor_share`, `get_content_gaps`, `get_ai_traffic`, `get_search_console_summary`, `get_memo_performance`, `get_page_performance`, `export_dataset` |
| Memos | `list_memos`, `get_memo`, `create_memo_draft`, `update_memo` |
| Landing pages | `list_pages`, `get_page`, `create_page`, `update_page`, `duplicate_page`, `add_section`, `update_section`, `remove_section`, `upload_page_asset`, `list_page_versions`, `restore_page_version`, `get_preview_url`, `publish_page`, `set_page_share_link`, `convert_to_freeform`, `apply_freeform_layout`, `set_page_site_widgets`, `set_embed`, `get_widget_spec`, `export_deck` |
| Leads, chat, and calls | `list_offers`, `list_leads`, `get_chat_activity`, `list_calls`, `get_call` |
| Threads and presentations | `list_threads`, `get_thread`, `get_thread_results`, `get_pitch_context`, `create_presentation` |
| Feedback | `report_missing_capability` |

Every tool is annotated as read-only or not, so Cursor asks before running anything that changes data. A tool that spends AI credits first returns its estimated cost, and the agent runs it only after you approve that cost in the chat.

## Privacy and support

- Privacy policy: [contextmemo.com/privacy](https://contextmemo.com/privacy)
- Terms: [contextmemo.com/terms](https://contextmemo.com/terms)
- Support: [stephen@contextmemo.com](mailto:stephen@contextmemo.com)

## License

MIT
