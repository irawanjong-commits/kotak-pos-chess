# Kotak Pos — tiny chess engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/irawanjong-commits/kotak-pos-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/irawanjong-commits/kotak-pos-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

Kotak Pos ("mailbox") is an engine for the 4 KB limit: a 64-square mailbox board, pseudo-legal moves from precomputed steps and sliding rays, legality by make-move plus own-king test, with castling, en passant, promotion.

Search is iterative-deepening alpha-beta with a transposition table (Zobrist keys from a fixed in-code table), quiescence (captures, stand-pat), ordering by TT move, MVV-LVA, killer and history, plus futility pruning, razoring. Eval is material plus procedural piece-square tables — formulas over rank/file, tapered by phase — and a cheap mobility term. Moves use a fixed 40,000-node budget, never a clock.

The readable `engine_src.py` is packed into `main.py` with `makefun compress` (lzma payload plus unpacker); the source ships beside the transcripts, not in the snapshot.

<sub>Entered on [make.fun](https://make.fun/?ref=tdkggc6z&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
