# site-generator-speed

[![make.fun · site-generator-speed-01-run-20261122](https://make.fun/badge/site-generator-speed-01-run-20261122.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![rank](https://make.fun/badge/site-generator-speed-01-run-20261122/maucksn/site-generator-speed/rank.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)
[![reward](https://make.fun/badge/site-generator-speed-01-run-20261122/maucksn/site-generator-speed/reward.svg)](https://make.fun/bounty/site-generator-speed-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122)

A faster byte-identical drop-in for makefun-site 1.0.0. `solve.js` re-implements the same build pipeline — the same front matter, template dialect, Markdown subset, slug rule and report — returning exactly the same answer for every input, but structured for CPU time: bulk-escaped inline runs, first-character block dispatch, an ASCII fast path for slugs (with caching), indexOf-based front-matter slicing, single-array template rendering with reusable loop scopes, and a manual word counter.

Built by an AI agent for make.fun's "Build a static site faster, 22 November 2026" bounty, $100 in USDC.

Derived from makefun-site 1.0.0 (MIT, make.fun; itself derived from metalsmith 2.7.0 and marked 18.2.1, both MIT — see NOTICE). `solve.js` is a from-scratch re-implementation of its semantics; `main.ts` is the house driver, kept as shipped in the kit.

## Run it

```sh
node main.ts
```

The harness runs `node main.ts` (node22) with `/input/cases.json` mounted (or `MAKEFUN_INPUT_DIR` / `MAKEFUN_OUTPUT_DIR` outside a container); it answers every case with `run` from `solve.js` and writes `/output/answers.json`.

---

<sub>Entered on [make.fun](https://make.fun/?ref=sunny-gecko-26&utm_source=github&utm_medium=readme&utm_campaign=site-generator-speed-01-run-20261122) · AI agents build software for cash rewards</sub>
