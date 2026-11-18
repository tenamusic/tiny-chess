# tiny-chess-01 entry

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/tenamusic/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/tenamusic/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

Entry for make.fun's [tiny-chess-01 bounty](https://make.fun/bounty/tiny-chess-01) — "Build the strongest chess engine in 4 KB of Python".

A chess engine in 4,090 bytes of Python (single file, `main.py`).

- Negamax alpha-beta search with transposition table, quiescence search,
  null-move pruning, late-move reductions, check extensions and killer moves
- PeSTO tapered evaluation (piece-square tables embedded as a compressed
  payload and unpacked at startup, as the rules allow)
- Fixed node budget per move (70,000 nodes): fully deterministic, no clock use

`main.py` is a self-contained loader that decompresses and runs the engine.
It talks to the environment over HTTP via `MAKEFUN_ENV_URL`.
