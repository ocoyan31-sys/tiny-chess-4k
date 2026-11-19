# Tiny Chess 4K

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ocoyan31-sys/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/ocoyan31-sys/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A deterministic chess engine in a single `main.py` of 4,082 bytes, written for
make.fun's tiny-chess-01 (Python, stdlib only).

Design: 0x88 board, negamax with PVS, transposition table, null-move pruning,
late-move reductions, quiescence over captures/promotions/check evasions,
killer-move ordering, and a tapered material + piece-square evaluation
with the bishop pair. Fixed budget of 100,000 nodes per move: no clock reads,
so every trial replays move-for-move.

Run: `MAKEFUN_ENV_URL=<env url> python3 -P -s main.py`
