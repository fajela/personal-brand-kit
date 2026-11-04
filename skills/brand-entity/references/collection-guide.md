# Collection guide

Where to find each field, and what to hand the user when you cannot open a page. `[Name]` = the preferred public name, URL-encoded in links (spaces as `+`).

## How to hand a page over to the user

Use this format, one numbered item per page:

> **1.** Open https://www.linkedin.com/in/[slug]/ (logged in).
> Copy and paste: your headline, the first two lines of About, your current position, and the website shown in Contact info.

Ask for a screenshot instead when layout matters (search results, a knowledge panel). Wait for the answer before you write anything from that page.

Pages you usually cannot read yourself: LinkedIn, Facebook, Instagram, Crunchbase, Google search results from the user's country, Google Business Profile, IMDb, anything behind a login or a bot check. Try once, and if you get a login wall, a 403 or a CAPTCHA, hand it over. Never try to get around a bot check.

## A. Identity

| Field | Sources |
|---|---|
| A01 to A05 names | User, their website About page, LinkedIn |
| A06 variants | Search results, Knowledge Graph entries (K block), Google's "Did you mean", how outlets spell the name. Diacritics are often dropped. |
| A08 to A11 birth, base, nationality | User only. Ask if they want each one public. |
| A12 languages | Website, LinkedIn |
| A13 headshot | Website image URL. Check one person in frame, not a selfie, same photo on profiles. |

## B. Professional

| Field | Sources |
|---|---|
| B01 role and company | LinkedIn (hand over), company team or About page |
| B02, B03 | Company site, search `site:[company domain] [Name]` |
| B04, B05 | LinkedIn experience (hand over), Crunchbase (hand over) |
| B06 expertise | Website, talks, articles by them. Propose 1 to 3 topics, the user picks. |
| B07, B08 bios | Write from confirmed fields only. Short bio opens with C01 once known. |

## C. Education and achievements

Website, LinkedIn education (hand over), award organizers' pages. Every award needs the organizer's page as source.

## D. Creations

Books: Amazon (search `[Name]` in Books), Goodreads, publisher page, ISBN on the book page. Courses: the platform page. Software: GitHub, product site.

## E. Online presence and identifiers

| Field | Sources |
|---|---|
| E01, E02 | User, search results |
| E03 to E05 profiles | Links on their website, the user, search `[Name] linkedin` etc. Confirm each is theirs. |
| E06 Crunchbase | https://www.crunchbase.com/person/[slug], hand over |
| E07 Google Business Profile | Hand over: search `[Name]` or business name on Google Maps from their country |
| E08 ISNI | https://isni.org/ search by name |
| E09 ORCID | https://orcid.org/orcid-search/search?searchQuery=[Name] |
| E10 IMDb | https://www.imdb.com/find/?q=[Name], hand over if blocked |
| E11 Wikidata | https://www.wikidata.org/w/index.php?search=[Name]. Record only. Never suggest creating one. |
| E12, E13 kgmids | See Knowledge Graph below |

## Knowledge Graph (E12, E13, K01 to K05)

Try in this order and record every id you find:

1. **Knowledge Graph Search API**, if the user has a Google Cloud API key (ask once, they can skip):
   `https://kgsearch.googleapis.com/v1/entities:search?query=[Name]&key=[KEY]&limit=10&languages=en`
   Repeat for every name variant. Record `@id` (kg:/g/...), name, `@type`, `resultScore`, description. Never write the key into the workbook.
2. **Panel share link**: if a panel shows, ask the user to click the share button on it and paste the g.co/kgs link. Opening it shows a URL with `kgmid=/g/...`.
3. **Google Trends**: ask the user to type the name at https://trends.google.com/trends/explore and paste the suggestions in the dropdown (an entity shows a type such as "Entrepreneur" or "Author"). Choosing one puts the id in the URL (`q=%2Fg%2F...`), ask them to paste that URL.
4. **Check an id**: `https://www.google.com/search?kgmid=[id]` shows what Google holds for it. Hand it over.

An empty result does not mean there is no entity. Several ids for one person means a merge task (L03). Ids that belong to namesakes go into G03, not K.

## Name Search Audit (S, T)

Hand over: "Open a private window, go to google.com, search `[Name]`, and send a screenshot of the whole first page or paste the titles and links." Your own search runs from another location and Google shows different results there.

Trigger test URLs to hand over:
- `https://www.google.com/search?q=[Name]`
- `https://www.google.com/search?q=[Name]+[company]`
- `https://www.google.com/search?q=[Name]+[city]`
- `https://www.google.com/search?q=[Name]+[topic]`
- `https://www.google.com/search?q=[variant]`

Classification: Owned (their site), Profile (their social or directory profile), About you (a page mostly about them, written by others), Mention (names them in passing), Namesake (another person), Risk (wrong, outdated or negative).

## Website schema (for W03 and the audit)

Open their homepage and About page source and find every `application/ld+json` block. Note every Person and Organization node, the plugin that printed it (AIOSEO, Yoast, Rank Math, theme), and duplicates. If the page needs JavaScript to show content, note it. If you cannot fetch the source, hand over: "Open https://validator.schema.org/ , paste your About page URL, and send a screenshot of the detected items."

## Mentions (M, F)

Search: `"[Name]" interview`, `"[Name]" podcast`, `"[Name]" speaker`, `"[Name]" -site:[their domain]`, the name plus the company, and the name in the target language. Open every result and confirm it is this person. For podcasts, check if the episode is on Apple Podcasts, Spotify, Amazon Music and YouTube. To check if an outlet has its own knowledge panel, hand over a search for the outlet name.
