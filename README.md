<div align="center">
  <img src="assets/icons/logo_256.png" alt="XinMatch logo" width="200">
</div>

# XinMatch

Open-source **powder X-ray diffraction (XRPD) phase analysis** platform — a
clean-room implementation guided by publicly documented XRD phase-analysis
workflows, published algorithms and open reference data (COD).

> ✅ **v3.6.3.** Core computation kernel + full GUI + dual-mode search-match
> (peak-list FoM / FPFM full-profile fitting (Full Pattern Fitting Match, formerly SMPF)) + **sequential
> multi-phase identification** (confirm a phase → re-search on the remaining
> unexplained peaks → confirm the next) + true March-Dollase preferred
> orientation modeling + GSAS-II refinement pipeline + quantitative Rietveld
> (main-phase wt% < 3 on certified samples) are complete and packaged
> (Windows installer / portable). v3.2.0 adds **phase-level identity**
> (`core/search/phase_key.py`): the candidate list folds cards that describe
> the same phase into one row (expandable, with each card's unit cell one
> hover away), and the benchmark is scored both per entry and per phase —
> same library, phase-level Top-1 goes from 7/13 to **10/13** simply because
> "found the right phase on a sibling card" is no longer counted as a miss.
> It also ships the refreshed logo/icon set and a regenerated splash.
> v3.3.0 adds **sparse-phase marks** in the residual candidate list: a card
> whose strongest reference line sits on a strong leftover peak, that is
> positionally accurate and coherent over its own reflections, is flagged
> with `★` (the FoM counts *how many* peaks a candidate explains, so a
> 6-line metal is always outvoted by a 150-reflection card). The mark is
> informational only — ranking is unchanged, because the same rule also
> flags a wrong phase on real data (see `docs/基准报告-物相检索-v3.md` §11.5).
> v3.4.0 adds **phase-analysis export** (`文件 → 导出物相分析（.xinm）…`):
> the anchor pattern, the selected phases' COD CIFs and their metadata are
> packed into a self-contained zip that the sister project
> [XinRefinement](../XinRefinement) imports in one click to start
> full-profile refinement — no re-importing the pattern, no hunting CIFs in
> the 522 K-file COD archive. Format contract: `docs/JOINT_PLAN_xinm_xinr.md`.
> v3.0.0 replaced the last legacy reference
> formats with the single **v3 columnar `.xinDB`** layout and ships the
> **COD-Inorg** library as the built-in default:
>
> * default library = `COD-Inorg-<snapshot>.xinDB`, bundled at `data/` in the
>   portable build → **works out of the box**, no separate download needed;
> * one reader, one search path (`search_match_v3`); the v2 SQLite
>   (`cod_inorganics.db`), PolyXRD-dump and PDF-2 readers were **deleted**,
>   not deprecated;
> * still mountable from any folder (设置→参考数据库…, or
>   `xinmatch libraries --add <path>`), `.xinDB` only.
>
> **v3.6.3** reworks element constraints into a **four-state + closed-loop** model
> (aligned with the sibling PolyXRD project; interfaces only added, never changed):
> ① element states grew from "must-include / exclude / no-restriction" to
> "**must-have**" (AND), "**contains**" (OR, at least one),
> "**possible**" (only widens the allowed pool), "**absent**" plus no-restriction; the
> click order now puts the strictest filter "must-have" last;
> ② a new closed-loop toggle "limit to selected elements" treats any element without a
> state as "absent", so "only allow the elements detected in the sample" no longer needs
> 113 button clicks; ③ prescreening gains an `elements_any` path (previously only
> "must include all" and "reject if any present"); the four-state conversion now converges
> in one place, `element_constraint_sets()`; ④ the panel adds a one-click "add light
> elements" that marks O/C/H/N/S as "contains". Old saves and old usage behaviour are
> unchanged bit-for-bit (closed-loop is off by default); benchmark numbers are unchanged.
> ⑤ **phase identification now defaults to FPFM full-profile fitting (no peak search)**;
> the dropdown can still switch back to "peak-list FoM (peak search)" with one click.
> ⚠️ Note: the FPFM search chain does NOT accept element-constraint conditions — **to use
> element constraints, switch back to peak-list FoM**; when constraints are present under
> FPFM, the toolbar "sample elements" button permanently shows a "｜not effective under FPFM" hint.
> **Download**: [GitHub Release v3.6.3](https://github.com/PolyXRD/XinMatch/releases/tag/v3.6.3)
> (Windows installer, with the built-in COD-Inorg default library, ready to search out of the
> box); see [docs/RELEASE-NOTES-v3.6.3.md](docs/RELEASE-NOTES-v3.6.3.md).
>
> **v3.6.2** reworks the pattern-area interaction (no interface or data-format changes):
> ① a new **reference-line partition** under the pattern — whichever phase the candidate
> list highlights, its peak positions and intensities are drawn directly beneath the pattern
> (one row per phase, formula labelled on the left, x-axis aligned with the pattern); confirmed
> phases are listed too, so you can see at a glance "which peaks are not yet matched by any phase";
> a checkbox toggles "position only / position + intensity";
> ② the top "X-axis / Y-axis / fit data range" control bar is hidden but its functions are kept,
> moved to **clicking the axes** (left-click cycles, right-click opens a menu);
> ③ a row of **quick icons** was added above the pattern (reset / horizontal box-select /
> vertical box-select / region zoom / pan left-right / step zoom / crosshair), ported from the
> sibling XinRefinement implementation.
> See [docs/RELEASE-NOTES-v3.6.2.md](docs/RELEASE-NOTES-v3.6.2.md).
>
> **v3.6.1** is a pure bug-fix release, fixing three field-reported issues with no interface or
> data-format changes:
> ① each curve in the legend appeared **twice** (pyqtgraph's `PlotItem.addItem()` already
> auto-adds the legend, and the code added it again manually — there was always only 1 curve,
> the duplicate was the legend entry);
> ② the Rietveld refinement wizard **white-screened + froze the whole window** (refinement ran
> the GSAS-II subprocess synchronously on the GUI thread, causing "(Not Responding)", while the
> "Start refinement" button slid to the "Next" position, so double-clicks mis-triggered it) —
> now moved to a background thread with the action button moved inside the page;
> ③ the list's "crystal system" column marked **hexagonal phases as monoclinic** (it only used
> the "number of non-90° angles" rule, while the only non-right angle in hexagonal is γ=120°) —
> H/R handling was added.
> See [docs/RELEASE-NOTES-v3.6.1.md](docs/RELEASE-NOTES-v3.6.1.md).
>
> **v3.6.0** fixes "clickable but no response": 11 of 15 function modules only played a
> "module skeleton in place" message in the status bar, while `core.quant` / `core.micro` /
> `core.index` were long complete. Now they all connect to real dialogs — Profile Fitting
> (F5, four profile shapes + Rwp + curve overlay), RIR quantification (adiabatic method, wt%
> written back to the match list), Scherrer / Williamson-Hall microstructure (D / ε / R²),
> Treor90 / DicVol06 indexing (candidate cell table), and a data-export aggregation menu
> (pattern ASCII + three CSV tables + `.xinm` + CIF). Bonus: the candidate list now shows 50
> rows by default (family-level coverage 81/98 → **89/98**, at zero compute cost); peak-position
> refinement switched to LM, 207-peak preprocessing **35.2 s → 0.35 s**, CLI end-to-end
> **36 s → 2.3 s**; the periodic table was reworked for size and three-state encoding (no longer
> clipped by the global QSS). Default search behaviour is unchanged item by item; see
> [docs/RELEASE-NOTES-v3.6.0.md](docs/RELEASE-NOTES-v3.6.0.md).
>
> See [docs/ROADMAP_v3.md](docs/ROADMAP_v3.md) for the full implementation plan and
> [docs/STATUS.md](docs/STATUS.md) for current progress.

## What XinMatch does

- **Qualitative phase analysis** (search-match): identify crystalline phases
  from an experimental powder diffraction pattern against a reference database.
- **Sequential multi-phase identification** (v3.1.0): confirm the best phase,
  subtract what it explains, and re-search the **remaining unexplained peaks**
  for the next phase — repeat until no significant peak is left.  Each
  confirmation is reversible, and the residual status (peaks explained /
  left over / too weak to use) is shown next to the candidate list.
- **Phase-level candidate list** (v3.2.0): a reference library holds dozens of
  cards per phase, so near-identical entries used to flood the Top-N.  Cards
  now fold into one row per phase (identical unit cell / element set / space
  group, see `core/search/phase_key.py`); the "变体" column shows how many
  cards were folded, its tooltip lists each card with its cell, and the
  context menu expands them again.
- **Sparse-phase marks** (v3.3.0): the residual search flags candidates whose
  strongest reference line sits on a strong leftover peak (`★` in the first
  column, rule in `core/search/sequential.py`).  The FoM counts *how many*
  peaks a candidate explains, so a correct 6-line metal never outvotes a
  150-reflection card; the mark makes it visible without changing the order.
- **Quantitative phase analysis** (RIR, internal standard, Rietveld).
- **Raw data preprocessing**: smoothing, background subtraction, Kα₂ stripping,
  zero-point / displacement correction.
- **Profile fitting & peak search**.
- **Rietveld / Le Bail refinement** (delegated to GSAS-II).
- **Powder indexing** (Treor / Dicvol).
- **Microstructure**: crystallite size (Scherrer), microstrain, crystallinity.
- **Reports & export**, **GUI** (PySide6), **CLI / batch scripting**.
- **Reference-database mounting**: besides the bundled `COD-Inorg` library, any
  other `.xinDB` library can be mounted from **any folder**
  (设置→参考数据库…, or `xinmatch libraries --add <path>`). v3 libraries are
  self-contained columnar files, so nothing is copied or converted.
- **3COD libraries are split by provenance** (`tools/split_3cod.py`):
  `COD-Inorg` (experimental, 79 k), `PCOD-Inorg` (predicted, 1.06 M),
  `TCOD-Inorg` (theoretical, 47 k). Mount all three side by side in XinMatch;
  PolyXRD only ever picks up the experimental one, because the other two ship
  without a `phases` table. See
  [docs/ACCEPTANCE-3COD-20261020.md §6](docs/ACCEPTANCE-3COD-20261020.md).
- **Reference libraries are built in the sibling repo, not here.**
  `XinMatch-DataBase` builds all six libraries (`COD` / `PCOD` / `TCOD` ×
  `Inorg` / `Full`); the CIF sources live one level up in
  `../sync-COD` (override with `XRD_DATA_ROOT`), and the built `.xinDB`
  files default to `XinMatch-DataBase/data/`. See that repo's
  [`docs/构建与验收手册.md`](../XinMatch-DataBase/docs/构建与验收手册.md) for
  the build/validate/acceptance commands.

## Design principles

1. **Clean-room**: no disassembly or decompilation of proprietary software.
   Specifications come from official documentation + published algorithms +
   black-box file-format observation for interoperability.
2. **Kernel / GUI decoupled**: everything in `xinmatch/core/` is pure
   computation (numpy arrays + dataclasses), unit-testable without a display.
   The GUI in `xinmatch/ui/` is a thin layer on top.
3. **Open data first**: the reference database is built from the
   [COD](https://www.crystallography.net/cod/) (CC0) public dump.
4. **Small, verifiable steps**: every task ships with pytest acceptance
   criteria so an AI agent can build, test, and debug independently.

## Project layout

```
xinmatch/
├── core/            # pure computation kernel (no GUI)
│   ├── model/       # Pattern, Peak, Entry, Phase, Restraints, Project
│   ├── io/          # 33 diffraction formats + CIF + exporters
│   ├── preprocess/  # smoothing, background, Kα2, zero point, ...
│   ├── peak/        # peak search, profile fitting, shapes
│   ├── db/          # SQLite reference database (COD) + user DB
│   ├── search/      # FoM search-match, PFSM, restraints
│   ├── index/       # Treor / Dicvol indexing
│   ├── refine/      # Le Bail / Rietveld (delegated to GSAS-II)
│   ├── quant/       # RIR, internal standard, Rietveld quant
│   ├── micro/       # crystallite size, microstrain, DOC
│   └── report/      # report data model + rendering
├── ui/              # PySide6 GUI
├── cli/             # command-line / batch interface
├── utils/           # registration + build variant (stdlib only, no Qt)
tests/               # pytest suite + fixtures + reference baseline
docs/                # analysis docs (reference help retained externally)
tools/               # helper scripts (doc extraction, baseline building)
```

## Getting started

```powershell
# (optional) create a virtual environment
python -m venv .venv
.venv\Scripts\Activate.ps1

# install in editable mode with dev + gui extras
pip install -e ".[dev,gui]"

# run the test suite (fast subset; the ``slow`` marker is excluded by default)
pytest

# include the numerically heavy suite (turn-on least squares, GSAS-II
# subprocesses, L3 acceptance curve_fit) — tens of minutes
pytest -m slow

# full local CI (ruff + mypy + tests), mirrors .github/workflows/ci.yml
powershell -File tools/ci.ps1
```

> The reference libraries (`*.xinDB`, ~110 MB–1.7 GB) are not in the repository;
> the source checkout resolves them from `../XinMatch-DataBase/data`
> (`XINMATCH_XINDB_DIR` overrides).  Tests that need them skip themselves.

### Run the working tree without building

`run_dev.bat` starts the code in the working tree in place — no PyInstaller
build and no install step, so what you see is always the latest source.
Without arguments it opens the GUI; any other arguments are forwarded to the
CLI (`python -m xinmatch.cli.main`):

```bat
run_dev.bat                                  :: GUI
run_dev.bat search pat.txt --db ..\XinMatch-DataBase\data\COD-Inorg-20261020.xinDB --top-n 5 --json
run_dev.bat libraries --json                 :: list available .xinDB libraries
```

The interpreter is resolved in this order and echoed on startup:
`%XINMATCH_DEV_PYTHON%` → `.venv\Scripts\python.exe` →
`venv\Scripts\python.exe` → `D:\Project\XRD\python310\python.exe` →
`python` on `PATH`. Because the batch file `cd`s to the repository root,
`python -m` loads the local `xinmatch/` package even when a different
copy is installed in site-packages.

## Builds & registration

Starting from v1.7.0, two binaries are produced. **From v3.0.0 both variants bundle the default
library** `COD-Inorg-<snapshot>.xinDB` (unpack/install and it is ready to search; located at
`<program dir>\data\`; you may replace it or mount other `.xinDB` libraries):

| Build | Artifact | Registration | Right edge of status bar |
|---|---|---|---|
| **Release** | `XinMatch-Setup-<v>.exe` (choose install location) | **Yes**: checks registration status on every launch | `Registered: <org/department name>` / `Not registered` |
| **Internal evaluation** | `XinMatch-Internal-<v>.zip` (portable, self-use) | **No** | **red bold** `Internal evaluation build` |

**v3.4.0 release artifacts**:

| Attachment | Size | SHA-256 (first 16) |
|---|---|---|
| `XinMatch-Setup-3.4.0.exe` (release installer, bundled COD-Inorg library) | 242.4 MiB | `4962defa7d0e4cf7…` |
| `XinMatch-Internal-3.4.0.zip` (portable = internal evaluation build, red-text marked, bundled COD-Inorg library) | 351.4 MiB | `fb82ce897bf4227a…` |
| `SHA256SUMS.txt` | — | — |

The reference library is unchanged in this release; both binaries bundle `COD-Inorg-20261020.xinDB`
(rebuilt, 78,035 phases). `.xinm` export requires **XinRefinement 1.1.0** to work with.
Larger external libraries (`PCOD` / `TCOD` / `Full` / Materials Project) are distributed from the
sibling repo [XinMatch-DataBase Releases](https://github.com/PolyXRD/XinMatch-DataBase/releases):
download `*.xinDB.zip` → unzip → **Settings → Reference database…** or
`XinMatch.exe libraries --add <path>` to mount; multiple libraries can coexist; see
`docs/RELEASE-NOTES-v3.4.0.md` §7.

When the release build is unregistered, a prompt pops up on every launch:

> This software is unregistered. All rights reserved; commercial use is prohibited.
> To register, contact <CONTACT_REDACTED>

Click **OK** to dismiss the prompt and use the software as usual (the prompt reappears next launch);
click **Enter registration code** and paste the code — once verified, registration completes and the
prompt stops. You can also register at any time via **Help → Enter registration code (&R)…**.

Registration codes are generated by the developer from the "organization/department name" you provide:
`PXRD1-XXXX-XXXX-…` (Base32 payload `UTF8(org name) + HMAC-SHA256[:8]`); the software re-verifies
locally and can recover the org name for display in the status bar; no network connection or machine ID
is required, and the same organization can use it on multiple machines. The algorithm is unified with
the PolyXRD family (reusing `D:\Project\XRD\PolyXRD-Reg`; this repo's copy is
`xinmatch/utils/registration.py`).

## License

This software is distributed under a **dual license** (Academic + Commercial), consistent with the upstream PolyXRD project.

- **English**: [LICENSE](LICENSE)
- **Chinese (Simplified)**: [LICENSE-CN](LICENSE-CN)

Academic use is free under the Academic License; any commercial use requires a separate written Commercial License from the copyright holder (see license text).
