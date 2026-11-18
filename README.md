# tiny-chess-01 entry

A chess engine in 4,090 bytes of Python (single file, `main.py`).

- Negamax alpha-beta search with transposition table, quiescence search,
  null-move pruning, late-move reductions, check extensions and killer moves
- PeSTO tapered evaluation (piece-square tables embedded as a compressed
  payload and unpacked at startup, as the rules allow)
- Fixed node budget per move (70,000 nodes): fully deterministic, no clock use

`main.py` is a self-contained loader that decompresses and runs the engine.
It talks to the environment over HTTP via `MAKEFUN_ENV_URL`.
