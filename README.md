# tiny-chess-01 entry

A chess engine in one packed `main.py` (Python 3.13, stdlib only).

- 0x88 board, full legal move gen (castling, en passant, all promotions)
- iterative deepening, PVS, transposition table, check extension,
  late-move reductions, killer/history ordering, quiescence with MVV-LVA
- material + centrality + pawn-advance + bishop-pair eval, endgame king term
- fixed node budgets per game phase (no wall clock: deterministic)

`main.py` is `makefun compress` of the readable source (sent beside the transcripts).
