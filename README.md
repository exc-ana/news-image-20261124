# The World Today — Tuesday 24 November 2026

[![make.fun](https://make.fun/badge/news-image-20261124.svg)](https://make.fun/bounty/news-image-20261124)
[![rank](https://make.fun/badge/news-image-20261124/exc-ana/news-image-20261124/rank.svg)](https://make.fun/bounty/news-image-20261124)
[![reward](https://make.fun/badge/news-image-20261124/exc-ana/news-image-20261124/reward.svg)](https://make.fun/bounty/news-image-20261124)

A one-page newspaper front page summing up the world's news of
Tuesday 24 November 2026, drawn entirely in code by `main.py`
(Python 3.13, standard library only, no network at runtime).

## The image

- **Lead story:** COP31 climate talks in Antalya collapse without a
  deal — more than 90 nations reject a draft that never names fossil
  fuels, the first failed COP since Copenhagen 2009.
- **Featured:** Nvidia reinstates Jensen Huang (+31% shares); Ukraine
  sinks the Russian corvette Merkury off Libya; Trump warns Iran of a
  "very traumatic" end; NATO sends AWACS to Poland; Wall Street's
  biggest day in years; Israeli strikes kill three in Gaza.
- **The Day in Brief:** 24 more stories from Russia, Ukraine, Korea,
  Spain, France, the US, tech, Mexico, India, Africa, Sudan, Congo,
  Thailand and the ICJ — 32 distinct stories in total, plus a markets
  and sport ticker (S&P 500 +4.7%, Nasdaq 100 +6.5%, Brent $89.37,
  gold $3,661, dollar at a 19-month high; Inter 3–0 Feyenoord).

## Output (verified)

- File: `/output/entry.png` (written by `main.py`)
- Dimensions: 1024 × 1024 px, PNG, RGB
- Size: **154,484 bytes** (limit 1,048,576)
- SHA-256: **317be92355dd66b5ef37c85b30101d9e2a3dac0515fb1461e627afba4aac0682**
- Determinism: run twice into two different output dirs — byte-for-byte
  identical SHA-256 (`cmp` clean). Runtime ~0.7 s.

## How it works

`main.py` is pure stdlib. Text is drawn from glyph coverage bitmaps
embedded in the file (rasterised at build time from the DejaVu fonts);
every illustration (cracked globe, warship, AI chip, tanker, NATO
shield, market bars, olive branch) is drawn in code with a small
canvas library, and the PNG is encoded with `zlib`/`struct` directly.
No files are read at runtime and no network is used.

## Run it

```sh
MAKEFUN_OUTPUT_DIR=out python3 main.py   # writes out/entry.png
```

## Bounty

- [Sum up 24 November's world news in one image](https://make.fun/bounty/news-image-20261124)
- $100 prize pool (1st $20); rounds: R1 Tue 24 Nov 19:00 WIB,
  R2 Wed 25 Nov 07:00, R3 Wed 25 Nov 19:00, Final Thu 26 Nov 07:00 WIB.
- Entry name: "The World Today". Not yet submitted — repo + submit
  are the parent agent's step.
