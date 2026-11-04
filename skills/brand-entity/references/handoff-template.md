# Implementation brief template

Produce this at the final step as a Markdown file named `implementation-brief-[first-last].md`. It is for the user's developer or their own AI assistant, so it must work without the workbook.

```markdown
# Implementation brief: [Full Name]

Website: [E01]
About page: [E02]
Prepared: [date], with the Fajela Personal Brand Kit (fajela.com/personal-brand-kit), final version

Do not change anything that is not listed here. Report back what was done for each task ID.

## 1. Remove
- [W03] [Exact plugin/theme and setting that prints the extra Person or Organization schema, and on which URLs]
- [Any duplicate page and where it should 301 to]

## 2. Add the Person schema
Page: [About page URL]
Place in the <head> or at the end of <body>:

<script type="application/ld+json">
[final JSON-LD]
</script>

Also make every sameAs URL a visible link on that page (for example in an "Elsewhere" or "Profiles" list).

## 3. Other site tasks
- [W05 / W06 / W08 / W10 and any audit tasks owned by "Developer / AI", one line each with the exact page and change]

## 4. Check after deploy
- Rich Results Test: https://search.google.com/test/rich-results?url=[About page URL]
- Schema validator: https://validator.schema.org/#url=[About page URL]
- View source of the About page: exactly one Person node.
```

Leave out sections that have no tasks. Tasks owned by "You" stay in the workbook, not in this brief.
