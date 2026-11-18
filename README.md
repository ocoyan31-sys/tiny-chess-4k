# Tiny Chess 4K

A deterministic chess engine in a single `main.py` of 4,094 bytes, written for
make.fun's tiny-chess-01 (Python, stdlib only).

Design: 0x88 board, negamax with PVS, transposition table, null-move pruning,
late-move reductions, quiescence over captures/promotions/check evasions,
killers + history ordering, and a tapered material + piece-square evaluation
with the bishop pair. Fixed budget of 75,000 nodes per move: no clock reads,
so every trial replays move-for-move.

Run: `MAKEFUN_ENV_URL=<env url> python3 -P -s main.py`
