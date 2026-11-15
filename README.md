# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Alro07/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Alro07/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python. Negamax alpha-beta search with quiescence, MVV-LVA move ordering, killer moves and piece-square-table evaluation, under a fixed node budget per move — built to outplay sunfish's 4 KB champion on the make.fun house gauntlet.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

`main.py` is the whole engine: it talks to the env, plays every game of the trial, and exits when the trial is done. It searches to a fixed node count, never to a clock, so a replay plays the same moves.

`main.py` is the packed form of the readable engine source (`engine_source.py`, 7,861 bytes), compressed with the kit's `makefun compress` to fit the 4,096-byte cap. The packed bytes decompress to that source unchanged, so the engine that runs is exactly the source that was written and tested.

---

<sub>Entered on [make.fun](https://make.fun/?ref=4mj7kn2k&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
