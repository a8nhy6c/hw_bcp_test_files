# CAM+SRAM submodule vec expected-output report

Reconstructed purely from the `.vec` stimulus file. Each table below is the settled state the vec expects after one write or search operation. `Q_Val` is the two storage nodes of a row (`Q_Val<2r>` `Q_Val<2r+1>`); `Q_Pol` is the polarity node. `-` means the vec asserts nothing for that node (never written / do not compare).

A second table per operation gives the Determiner verdict for each clause, read from that operation's settle row. `LID` is only meaningful when `UP` is 1.

A third table gives the chip level Combining Tree verdict, read from the tree settle row. `CID` names the winning clause and `Lit_Pos` the literal within it, so together they name a row; both are only meaningful when `UP_OUT` is 1.

Config: n=16 rows, k=3 VID bits, 4 determiners.

## Op 1: write row=1 vid=1 val=x pol=0

| Row | VID | Q_Val | Q_Pol |
|---|---|---|---|
| 0 | --- | -- | - |
| 1 | 001 | 01 | 0 |
| 2 | --- | -- | - |
| 3 | --- | -- | - |
| 4 | --- | -- | - |
| 5 | --- | -- | - |
| 6 | --- | -- | - |
| 7 | --- | -- | - |
| 8 | --- | -- | - |
| 9 | --- | -- | - |
| 10 | --- | -- | - |
| 11 | --- | -- | - |
| 12 | --- | -- | - |
| 13 | --- | -- | - |
| 14 | --- | -- | - |
| 15 | --- | -- | - |

| Determiner | Rows | CONF | UP | DONE | LID |
|---|---|---|---|---|---|
| 0 | 0-3 | - | - | - | -- |
| 1 | 4-7 | - | - | - | -- |
| 2 | 8-11 | - | - | - | -- |
| 3 | 12-15 | - | - | - | -- |

| Combining tree | CONF_OUT | UP_OUT | DONE_OUT | CID | Lit_Pos | Row named |
|---|---|---|---|---|---|---|
| chip | - | - | - | -- | -- | - |

## Op 2: search vid=1 val=0

| Row | VID | Q_Val | Q_Pol |
|---|---|---|---|
| 0 | --- | -- | - |
| 1 | 001 | 00 | 0 |
| 2 | --- | -- | - |
| 3 | --- | -- | - |
| 4 | --- | -- | - |
| 5 | --- | -- | - |
| 6 | --- | -- | - |
| 7 | --- | -- | - |
| 8 | --- | -- | - |
| 9 | --- | -- | - |
| 10 | --- | -- | - |
| 11 | --- | -- | - |
| 12 | --- | -- | - |
| 13 | --- | -- | - |
| 14 | --- | -- | - |
| 15 | --- | -- | - |

| Determiner | Rows | CONF | UP | DONE | LID |
|---|---|---|---|---|---|
| 0 | 0-3 | - | - | - | -- |
| 1 | 4-7 | - | - | - | -- |
| 2 | 8-11 | - | - | - | -- |
| 3 | 12-15 | - | - | - | -- |

| Combining tree | CONF_OUT | UP_OUT | DONE_OUT | CID | Lit_Pos | Row named |
|---|---|---|---|---|---|---|
| chip | - | - | - | -- | -- | - |

