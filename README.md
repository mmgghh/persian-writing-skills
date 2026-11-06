# Persian writing skills for Claude

Two Agent Skills that teach Claude to write Persian properly, split by register.

| Skill | For |
|:--|:--|
| `persian-formal` | Official letters (نامه اداری), reports, contracts, proposals, articles, bilingual business documents |
| `persian-informal` | Chat messages, informal email, social posts, personal notes |

Both cover دستور خط (نیم‌فاصله and friends), Persian punctuation, numbers and dates, bilingual Persian/English handling, and right-aligned RTL markdown tables. The formal skill adds sentence structure, a word-choice table (می‌باشد → است, گردید → شد, گزارشات → گزارش‌ها …) and a نامه اداری skeleton. The informal skill adds شکسته‌نویسی rules built on the syllable-reduction test.

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

## License

MIT — see `LICENSE`.
