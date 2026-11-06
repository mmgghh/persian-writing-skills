# Persian writing skills for Claude

Two Agent Skills that teach Claude to write Persian properly, split by register.

| Skill | For |
|:--|:--|
| `persian-formal` | Official letters (نامه اداری), reports, contracts, proposals, articles, bilingual business documents |
| `persian-informal` | Chat messages, informal email, social posts, personal notes |

Both cover دستور خط (نیم‌فاصله and friends), Persian punctuation, numbers and dates, bilingual Persian/English handling, and right-aligned RTL markdown tables. The formal skill adds sentence structure, a word-choice table (می‌باشد → است, گردید → شد, گزارشات → گزارش‌ها …) and a نامه اداری skeleton. The informal skill adds شکسته‌نویسی rules (vowel shifts, verb and pronoun contractions, the ه-versus-ezāfe rule), a register matrix and before/after rewrites.

## Example prompts

- «یک نامه اداری برای ریاست محترم اداره آب بنویس و درخواست بررسی قبض این ماه را مطرح کن.» (`persian-formal`)
- «مستندات این API را به فارسی رسمی بازنویسی کن.» (`persian-formal`)
- «به علی پیام بده که امشب نمی‌تونم بیام و فردا جبران می‌کنم.» (`persian-informal`)
- «این ایمیل رسمی را خودمانی‌تر کن؛ برای یکی از همکاران نزدیکم است.» (`persian-informal`)

## Install

```shell
/plugin marketplace add mmgghh/persian-writing-skills
/plugin install persian-writing@mg-skills
```

Then write Persian as usual — Claude picks the register from the task. To force one:

```shell
/persian-writing:persian-formal
/persian-writing:persian-informal
```

## Try before installing

```bash
claude --plugin-dir ./persian-writing-skills/plugins/persian-writing
```

## House style choices

Persian orthography has live disagreements. Where one exists, these skills pick a side. If your house style differs, fork and edit the line — each is a single line.

1. **Ezāfe after final ه** is written `ه‌ی` (خانه‌ی من), not the فرهنگستان form خانهٔ من. Both are in use; the Academy form is the official one. Swap it if you publish somewhere that mandates دستور خط فارسی.
2. **Supplementary comments go in parentheses**, not dashes — a formal-register preference, not a rule.
3. **The technical-terms table** in `persian-formal` (توکن not نشانه, محیط عملیاتی not محیط تولید) is one author's termbase, included as a worked example. Replace it with your own.

## Using these outside Claude Code

The `SKILL.md` files use the `when_to_use` frontmatter field, which is Claude Code only. To upload either skill to claude.ai or the Skills API, delete that line and fold its content into `description` — those paths accept only `name`, `description`, `license`, `compatibility`, `metadata`, and `allowed-tools`, and reject anything else with a hard error.

## What it does (and doesn't)

The plugin is two plain-Markdown skills plus a manifest. It has no scripts, hooks, MCP servers or dependencies, makes no network calls, and doesn't collect, store or send any data. It only shapes how Claude words and formats Persian text; it doesn't give legal, financial or other professional advice.

## Support

Questions, bugs and security concerns: [open an issue](https://github.com/mmgghh/persian-writing-skills/issues). If a skill doesn't kick in when you expect it to, invoke it by name with `/persian-writing:persian-formal` or `/persian-writing:persian-informal`.

## License

MIT — see `LICENSE`.
