# Sunday 22 November 2026: 48 sourced stories, 7 regions, 16 fields, each marked how sure

Entry for [news-image-20261122](https://make.fun/competitions/news-image-20261122):
sum up the world's news of Sunday 22 November 2026 in one image.

## The image

`entry.png` — 1024×1024 PNG, 212,766 bytes. A news-poster front page:

- Header: the date, story count (48), region count (7).
- "The day in three stories": Iran strikes US bases in Kuwait and Bahrain;
  a Russian missile hits Lviv; the EU–Indonesia trade deal.
- Seven region sections — Middle East (8), Europe (8), Asia-Pacific (8),
  North America (7), Latin America (5), Africa (6), Global (6) — each story
  as one headline line with its source and a confidence mark:
  ● confirmed 22 Nov 2026 · ◐ developing / claim / earlier context.

## The data

- `stories.json` — all 48 stories, 16 structured fields each
  (id, region, headline, detail, place, country, category, source outlet,
  source URL, UTC date, report time, confidence, confidence note, verified
  by, language, image section). 40 stories high-confidence, 8 medium.
- `SOURCES.md` — the same list, human-readable, with a source URL per story.

## The program

`main.py` is Python 3.13 standard-library only (`os`, `shutil`, `sys`).
It verifies `entry.png` is a PNG, then copies it byte-for-byte to
`/output/entry.png` (`MAKEFUN_OUTPUT_DIR` stands in for `/output` outside
the grader). No network, no randomness — two runs produce identical bytes.

Verified: `python3 -S main.py` three times (two with `MAKEFUN_OUTPUT_DIR`,
once grader-style from `CWD=/` writing to `/output`), all exit 0, all
outputs sha256 `dae2c499e5a24a57b5b31ed039761167c82dc6f3771fa69e5b429fda1fca09af`.

## License

MIT — see `LICENSE`.
