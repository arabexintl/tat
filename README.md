# Arabex Translator Assessment (TAT)

A free, self-paced assessment for aspiring **English ⇄ Arabic translators**, built by
[Arabex International](https://www.arabexinternational.com).

**Live:** https://arabexinternational.com/tat/

## What it does

Candidates test their command of professional Arabic–English terminology and
translation judgement across five domains:

| Domain | Questions |
|---|---|
| Legal / Court | 840 |
| Civil & Official Documents | 494 |
| Medical | 899 |
| Education / Academic | 616 |
| Business / Commercial | 835 |

Questions come in three levels: **Easy** (1,161), **Intermediate** (2,346) and
**Hard** (185). All Arabic is Modern Standard Arabic in a professional
register, with no country-specific bias.

### Question types

- **Term translation**, English → Arabic and Arabic → English
- **Matching pairs**
- **Best translation:** choose the strongest rendering of a sentence
- **False friends** and **near-synonyms**
- **Error spotting:** find the mistake in a translation
- **Register:** choose the right level of formality

### Ways to use it

- **Quick start:** 10 easy questions across all domains, untimed (about 3 minutes).
- **Topic practice:** one domain at a chosen difficulty, untimed.
- **Mixed exam:** 20 random questions across all domains, one minute each.
- **Glossary:** browse and search the verified English–Arabic terms.
- **My progress:** a chart of recent scores, accuracy by domain, levels and badges,
  all kept in the candidate's own browser.
- **Word of the day:** one glossary term on the home page, changing daily.

### Levels and badges

Easy is open to everyone. **Intermediate** unlocks after scoring 80% or more on
an Easy test, and **Hard** after 80% or more on an Intermediate test.
To open every level straight away (for example when testing a job candidate),
send them this link: https://arabexinternational.com/tat/?all

Seven badges reward milestones: first test, five tests, an 80%+ score, a
perfect score, all five domains, passing Hard, and 70%+ on the mixed exam.

### English or Arabic

The whole interface is available in English and Arabic (right-to-left), with a
switch at the top of the home page. The choice is remembered, and visitors whose
browser is set to Arabic see Arabic first. The questions themselves are bilingual
and stay the same in both.

Every answer gets instant feedback with the correct answer and a short
explanation. At the end, candidates get a result card image (with their name, if
they want) to save or share. Keyboard shortcuts: `1`–`4` or `A`–`D` to answer, `Enter` for the next question.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app as one self-contained page: design, fonts, icons and logo are built in. |
| `questions.json` | The question bank (3,692 questions). The page loads it from the same folder. |
| `og-image.png` | Preview image shown when the link is shared (WhatsApp, LinkedIn, etc.). |
| `favicon.png`, `apple-touch-icon.png` | Browser tab and home-screen icons. |

There is no build step and no server code. Any static host works (GitHub Pages here).

## Updating the question bank

Replace `questions.json` with a new version that keeps the same shape:

```json
{
  "meta": { "title": "…", "version": "1.0" },
  "questions": [
    {
      "id": "Q0001",
      "level": "easy | intermediate | hard",
      "domain": "legal | civil | medical | education | business",
      "domain_label": "Legal / Court",
      "type": "term_en_ar",
      "question": "Choose the correct Arabic translation of: “Legal Procedures”.",
      "options": ["…", "…", "…", "…"],
      "answer_index": 3,
      "answer": "الإجراءات القانونية",
      "explanation": "Why this answer is correct."
    }
  ]
}
```

Only the five domains above are shown in the app.

The design is maintained in Claude Design. When it changes, `index.html` is
re-exported from there. The public export leaves out the internal admin tools.

## Privacy

No answers, scores or personal data are sent anywhere. Progress is saved only
in the candidate's own browser (local storage). The "Report an error" link
opens the candidate's own email app.

---

© Arabex International · Alappuzha, Kerala, India ·
[arabexinternational@gmail.com](mailto:arabexinternational@gmail.com)
