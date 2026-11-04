# Fajela Personal Brand Kit

A personal brand audit and plan for SEO, GEO and AEO, filled in with you inside Claude.

The kit checks what Google and AI answers (ChatGPT, Gemini, Perplexity, AI Overviews) say about a person, records every fact with its source, and turns the gaps into Person schema and a task plan. It is built for founders, executives, authors, speakers and consultants who want the right facts about them on page one of Google and in AI answers.

## What you need

- The free Personal Brand Kit workbook, a Google Sheet. Get your copy at [fajela.com/personal-brand-kit](https://fajela.com/personal-brand-kit/). It arrives by email with a link that makes your own copy in Google Drive.
- Claude (the Claude app, or Claude Code).

## How to start

Ask Claude to start your personal brand kit, or run the `brand-entity` skill, and share your copy of the workbook. The skill then:

1. Asks four starting questions: your name and its spellings, your website, your role and company, and your target country.
2. Fills the workbook one block at a time, shows each block as a short table, and waits for you to confirm or correct it before it writes anything.
3. Audits your Google name search, the AI answers about you, your Knowledge Graph entities, your website schema, your profiles and your mentions.
4. Writes an interim version, then a final version with Person schema (JSON-LD), an Action Plan and an implementation brief for your developer or your own AI assistant.

## What the skill reads, sends and changes

- **Reads:** public web pages about you that Claude can open with its own web tools, such as your website, profiles and articles. When a page needs your login or blocks automated access, the skill gives you the exact URL and asks you to paste what you see.
- **Optional:** if you give it a Google Cloud API key, it queries the Google Knowledge Graph Search API for your name. The key is never written into the workbook.
- **Sends:** nothing to Fajela or to any other service. The plugin has no hooks, no MCP servers and no scripts.
- **Changes:** only your copy of the workbook, and only after you confirm each block. It never edits your website or your profiles.

## Rules the skill follows

- No fact without a source page it opened in the session, or your own answer.
- No promise of a knowledge panel, an AI mention or a timeline.
- Wikidata and Wikipedia are optional and never a task.

## Optional expert review

When your workbook is filled in, Olesia Korobka, founder of Fajela, can review it with you in a paid 60-minute session. Book at [calendly.com/fajela/60min](https://calendly.com/fajela/60min) or email info@fajela.com. The skill mentions this once, after it hands over your plan, and the kit works in full without it.

## License

Creative Commons Attribution 4.0 International (CC BY 4.0). See [LICENSE](LICENSE).

Made by [Fajela](https://fajela.com).
