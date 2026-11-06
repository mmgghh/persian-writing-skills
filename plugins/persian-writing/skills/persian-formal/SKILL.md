---
name: persian-formal
description: Rules for writing formal and professional Persian — official letters (نامه اداری), reports, contracts, proposals, articles, and bilingual Persian/English business documents. Covers register, word choice, orthography (نیم‌فاصله), punctuation, numbers, and RTL markdown.
when_to_use: Any Persian text that is formal, official, administrative, professional, academic, financial, or legal; also when translating English business text into Persian.
---

# Formal Persian writing

This is the default register for documents. No colloquial (شکسته) forms: می‌روم, never می‌رم.

## Sentence structure

- Persian is SOV — put the verb at the end. Move it only for deliberate emphasis, and rarely.
- One idea per sentence, under ~25 words. Split long chains instead of stacking «با توجه به اینکه … لذا …».
- Prefer the active voice. Use the passive only when the agent is unknown or irrelevant, never as a politeness device.
- Keep را directly after its direct object, not stranded after a long clause.
- One topic per paragraph, three to five sentences.

## Word choice

| به‌جای | بنویس |
|---:|---:|
| می‌باشد | است، هست |
| گردید، گردیده است | شد، شده است |
| نمودن (به‌جای فعل اصلی) | کردن |
| توسطِ … انجام شد | … انجام داد |
| مورد بررسی قرار گرفت | بررسی شد |
| در رابطه با | دربارهٔ، در مورد |
| جهتِ | برایِ |
| بایستی، می‌بایست | باید |
| علی‌رغم | به‌رغمِ، با وجودِ |
| گزارشات، پیشنهادات، آزمایشات | گزارش‌ها، پیشنهادها، آزمایش‌ها |
| اساتید | استادان |
| گاهاً، تلفناً، زباناً | گاهی، تلفنی، شفاهی |

- Persian words take Persian plurals (ها / ان). Never put tanwin on a Persian word.
- No double plurals: مدارک, not مدارک‌ها.
- Cut redundancy (حشو): «بازگشت مجدد» → «بازگشت»، «تقریباً حدودِ» → «حدودِ»، «سؤال پرسید» → «پرسید».
- One term per concept, repeated. Synonym variation reads as imprecision in technical and financial text.

### Technical terms

Use the preferred equivalent, never the alternative:

| اصطلاح | بنویس | ننویس |
|---:|---:|---:|
| token | توکن | نشانه |
| production environment | محیط عملیاتی | محیط تولید |

## Orthography (دستور خط)

- Use نیم‌فاصله (ZWNJ, U+200C) — not a plain space — in: می‌/نمی‌ + verb (می‌رود), plural ها (کتاب‌ها), ‌تر/‌ترین (بزرگ‌تر — but بهتر، کمتر، بیشتر are written solid), ‌ای (خانه‌ای), compounds (دانش‌آموز), numeric adjectives (سی‌ساله).
- Prepositional به stays separate (به تهران رفت); adverbial به takes ZWNJ (به‌ویژه، به‌طور کلی، به‌جز).
- Ezāfe on words ending in ه is written ه‌ی — ه + ZWNJ + ی: خانه‌ی من. Never with a full space (خانه ی من). The Academy form خانهٔ من is the official alternative; use it when a publisher or a government body requires دستور خط فارسی. Never mix the two in one document.
- Arabic words ending in hamze drop it: املا، انشا، ابتدا → «املای من».
- Persian letters only: ی and ک, never Arabic ي and ك.
- تشنگان, not تشنه‌گان.

## Punctuation (نشانه‌گذاری)

- Persian marks: ، ؛ ؟ « » — not , ; ? " ".
- No space before . ، ؛ : ؟ ! and one space after. Brackets and quotes: no space inside, one space outside — «نقل‌قول» ، (توضیح).
- **Supplementary or optional comments go in parentheses, not dashes**: «سود خالص (پس از کسر مالیات) ۱۲٪ افزایش یافت.» Reserve — for a complete interjected clause, and use - only for numeric ranges (۱۳۹۸-۱۴۰۲).
- ؛ separates long related clauses, or list items that already contain commas.
- : introduces a list, a quotation, or an explanation.
- « » for direct quotes, the first appearance of a technical term, and titles. [ ] for your own insertion into a quotation.
- No comma after و، اما، اگر، که.
- At most one ! or ? — never !!! or ?!.

## Numbers, dates, bilingual text

- Persian digits (۰۱۲۳۴۵۶۷۸۹) in Persian prose. Decimal separator is «/» (۳/۵); thousands separator «٬» (۱٬۲۵۰٬۰۰۰).
- Space between number and noun (۲۵ تومان); ZWNJ in numeric adjectives (۲۵تومانی).
- Jalali dates as ۱۴۰۴/۰۶/۱۱. When both calendars appear, label them.
- Give the English term in parentheses at first mention, then use the Persian consistently: «حسابداری تعهدی (accrual accounting)».
- Keep Latin identifiers, filenames, code, and URLs in `backticks` so RTL rendering doesn't scramble them.
- Punctuation next to a Latin word is still Persian.

## Markdown and RTL

- Right-align every table column (`---:` in the separator row, all columns) whenever the table holds Persian content.
- Blank line before every list and after every heading.
- For HTML output, wrap the body in `<div dir="rtl">` and set `direction: rtl; text-align: right`.

## Official letter (نامه اداری)

Recipient title and name → «با سلام و احترام،» or «احتراماً،» → the purpose in the first sentence → body, one request per paragraph → «با تشکر و احترام،» → name, role, date.

- Address people as «جناب آقای …» / «سرکار خانم …», offices as «ریاستِ محترمِ …».
- State the request explicitly and early; never bury it under ta'arof. Keep to one page.

## Before delivering

- Search for ` می ` and ` ها ` written with a plain space — they should be ZWNJ.
- Confirm no می‌باشد، گردید، or توسط survived.
- Confirm no Latin digits leaked into Persian prose.
