# tiny-chess-01 entry

A chess engine in one packed `main.py` (Python 3.13, stdlib only).

- 0x88 board, full legal move gen (castling, en passant, all promotions)
- iterative deepening, PVS, transposition table, check extension,
  late-move reductions, killer/history ordering, quiescence with MVV-LVA
- material + centrality + pawn-advance + bishop-pair eval, endgame king term
- pawn-structure eval (doubled / isolated / passed) + tempo
- eval cache, hard per-move node cap (d=1 ≤ 250k nodes ≈ 6.2 s worst case:
  no wall clock anywhere, so the move is deterministic AND no time forfeits)
- fixed node budgets per game phase

`main.py` is `makefun compress` of the readable source (sent beside the transcripts).
Practice trial-0: Elo 1191 (floor 1154), 1 win 3 draws 2 losses.
