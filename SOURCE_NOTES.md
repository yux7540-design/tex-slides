# Source and compilation notes
Source: course complete RITS consultation source ZIP, https://gerardjk.github.io/rits-consultation/ . Fonts and figures retained. The PDF was compiled locally from the supplied TeX, not copied from the reference PDF.

Compiler: Tectonic (XeTeX engine), `tectonic --keep-logs --reruns 1 rits-consultation-deck.tex`. The source header explicitly supports Tectonic. The session instructions specify XeLaTeX; this build uses its XeTeX-based alternative, with two TeX passes. Compilation emitted warnings in the supplied source; see compile.log and verification.json. No claim is made that these warnings were all corrected.

Diagram: “DvP/PvP lock and release”, source frame begins at line 3236. A label is `\node[wl] at (0.5,0.5) {RITS};`. A shaped box is `\node[bx] (l1) at (2.1,1.6) {lock};`; the bx style defines its border and fill. A connection is `\draw[ctl] (l1.south) -- (2.1,1.05) -| ([xshift=-.13cm]s1.north);`, which routes an arrow from the lock node to settlement. The diagram distinguishes locking, cash settlement and release, while the accompanying slide text explains their risks.

The related https://www.rtgs.cash/ returned HTTP 404 during this run. Its interactive behaviour has therefore not been reviewed, and no personal exploration is claimed. Student review remains necessary.
