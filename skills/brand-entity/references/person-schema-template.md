# Person schema template

Placed on the About page (or the homepage of a personal site). Fill only with confirmed Data Hub values. Delete any property you have no confirmed value for. Never leave placeholders in the final version.

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "ProfilePage",
      "@id": "https://example.com/about/#profilepage",
      "url": "https://example.com/about/",
      "name": "About Olesia Korobka",
      "mainEntity": { "@id": "https://example.com/#person" }
    },
    {
      "@type": "Person",
      "@id": "https://example.com/#person",
      "name": "Olesia Korobka",
      "alternateName": ["Olesia Korobka", "Олеся Коробка"],
      "description": "One sentence from Strategy Canvas C01.",
      "url": "https://example.com/",
      "image": "https://example.com/images/olesia-korobka.jpg",
      "jobTitle": "Founder",
      "worksFor": {
        "@type": "Organization",
        "@id": "https://company.example/#organization",
        "name": "Fajela",
        "url": "https://fajela.com/"
      },
      "alumniOf": { "@type": "CollegeOrUniversity", "name": "University name" },
      "knowsAbout": ["Topic 1", "Topic 2"],
      "knowsLanguage": ["English"],
      "award": ["Award name, year"],
      "sameAs": [
        "https://www.linkedin.com/in/...",
        "https://x.com/...",
        "https://www.crunchbase.com/person/...",
        "https://www.google.com/search?kgmid=/g/11xxxxxxxx"
      ],
      "subjectOf": [
        { "@type": "Article", "name": "Interview title", "url": "https://outlet.example/interview" }
      ]
    },
    {
      "@type": "WebSite",
      "@id": "https://example.com/#website",
      "url": "https://example.com/",
      "name": "Olesia Korobka",
      "publisher": { "@id": "https://example.com/#person" }
    }
  ]
}
```

## Rules

- Exactly one Person node for the person on the site. If a plugin or theme prints another, the plan includes a task to turn it off (W03).
- `@id` is the same on every page of the site and on the company site's Person node.
- `alternateName`: every variant from A06, including spellings without diacritics.
- `sameAs`: profiles from E03 to E11 that belong to the person, plus `https://www.google.com/search?kgmid=[id]` for the main kgmid (and each duplicate id until merged). Every sameAs URL must also be a visible link on the page.
- `worksFor`: use the company's own Organization `@id` if its site defines one. Never describe the company in detail here, that belongs on the company site.
- `subjectOf`: only pieces from the Mentions tab that are mostly about the person.
- `birthDate`, `birthPlace`, `homeLocation`, `nationality`: only if the user confirmed they want them public.
- Books: add a separate `Book` node with `author` pointing to the Person `@id`. Courses: `Course` with `provider` or `instructor` the same way.
- WebSite node only on the homepage. On a company site, the WebSite publisher is the Organization, not the person.
- Before handing it over, parse the JSON to check it is valid. Output it inside `<script type="application/ld+json"> ... </script>`.
