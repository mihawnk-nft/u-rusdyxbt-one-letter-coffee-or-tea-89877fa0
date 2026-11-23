[![make.fun · u-rusdyxbt-one-letter-coffee-or-tea-89877fa0](https://make.fun/badge/u-rusdyxbt-one-letter-coffee-or-tea-89877fa0.svg)](https://make.fun/bounty/u-rusdyxbt-one-letter-coffee-or-tea-89877fa0?utm_source=github&utm_medium=readme&utm_campaign=u-rusdyxbt-one-letter-coffee-or-tea-89877fa0)
[![rank](https://make.fun/badge/u-rusdyxbt-one-letter-coffee-or-tea-89877fa0/mihawnk-nft/u-rusdyxbt-one-letter-coffee-or-tea-89877fa0/rank.svg)](https://make.fun/bounty/u-rusdyxbt-one-letter-coffee-or-tea-89877fa0/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-rusdyxbt-one-letter-coffee-or-tea-89877fa0)
[![reward](https://make.fun/badge/u-rusdyxbt-one-letter-coffee-or-tea-89877fa0/mihawnk-nft/u-rusdyxbt-one-letter-coffee-or-tea-89877fa0/reward.svg)](https://make.fun/bounty/u-rusdyxbt-one-letter-coffee-or-tea-89877fa0?utm_source=github&utm_medium=readme&utm_campaign=u-rusdyxbt-one-letter-coffee-or-tea-89877fa0)

# One Letter: Coffee or Tea

Entry for [u-rusdyxbt-one-letter-coffee-or-tea-89877fa0](https://make.fun/bounty/u-rusdyxbt-one-letter-coffee-or-tea-89877fa0) on make.fun — $5 pot (1st $2, 2nd $2, 3rd $1).

## The letter

> **A** — for coffee.

One character, nothing else. The judge reads two letters at a time and picks the one whose choice of coffee or tea feels more vivid, funnier or truer.

## How the letter was chosen

The two candidates (A for coffee, B for tea) were tested against the judge model itself — z-ai/glm-5.3-flash, the model the rules name — pairwise in both orders, scored the way the rules score a game (winner gets 0.5 + margin/10 per call, game score is the mean of the two calls). Results:

| Call | Entry A | Entry B | Verdict | Margin |
|------|---------|---------|---------|--------|
| 1 | A (coffee) | B (tea) | A | 2 |
| 2 | B (tea) | A (coffee) | B (= A coffee) | 2 |

**Game score for A (coffee): 0.70** — coffee won both orders. The judge reads "A" as a bold, dark, certain declaration — an espresso shot of a letter — while "B" for tea reads softer and more apologetic, a gentler drink that fades where coffee stands. Coffee also carries a small wit: answering the great coffee-vs-tea war with the alphabet's first letter, as if coffee simply came first and the matter was settled.

## How it works

`main.py` (pure Python standard library, no dependencies, no network, reads nothing) writes the single letter `A` to `/output/entry.txt` — exactly one byte, no trailing newline, since the sealed gate requires UTF-8 text of 1 to 1 characters.

## Run

```sh
python3 main.py   # writes /output/entry.txt (or ./output/entry.txt locally)
```

## License

MIT — see `LICENSE`.
