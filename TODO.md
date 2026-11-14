# To-do

Shared to-do list of the thesis. Edit this file on GitHub (pencil icon) and commit:

- **Tick** a task: change `[ ]` to `[x]`.
- **Add** a task: a new line `- [ ] what to do` under a phase heading. No ID needed.
- **Rename** a task: edit the text after the bold ID. Please keep the ID.

The indented line under a task (chapter, tags, notes) is regenerated at each sync,
so edits there are lost; use an issue to discuss a task.

Last synced 2026-11-14.

## Phase A · journal core (2/15)

- [x] **X1** Byte-accurate data-volume cost model
  - Ch 2, 5, 7 · code — Done 2026-11-13. 3-band volumes were understated 1.5–1.75×. Per-tile download view still open.
- [ ] **X3** Data-quality audit (umbrella): all checks below done and reported
  - Ch 5 · data — Write findings to a short audit report and update Ch 5 numbers (E5.0) if anything changes. Subtasks X3.1–X3.5.
- [ ] **X3.1** Cross-tile duplicate polygons: are any in the GISTAM (Ch 5) train/test splits?
  - Ch 5 · data · code — 16% of polygon files were duplicates across tiles (~6% test leakage in the earlier GUNEYDOGU split). Match by polygon ID and coordinates.
- [ ] **X3.2** Cotton/maize class swap: does it affect the regional class groupings used in Ch 5?
  - Ch 5 · data
- [ ] **X3.3** Missing H5 chunks (TRAKYA, EGE): which Ch 5 regions were trained on incomplete data?
  - Ch 5 · data — Chunk-numbering bug left most fields out (e.g. 92% of Trakya maize).
- [ ] **X3.4** Forward-filled time slots: confirm the real-observation mask is used everywhere it should be
  - Ch 5, 6, 7 · data · code — 24–40% of Turkish slots are copies, not acquisitions. Affects retrieval counts and band-selection inputs.
- [ ] **X3.5** Write the audit report and decide on reruns (E5.0)
  - Ch 5 · text · data — If Ch 5 numbers move, the thesis states the difference from the published GISTAM paper.
- [x] **S6.0** Choose the journal
  - Ch 6 · admin — IEEE JSTARS, regular submission. Manuscript set up in IEEEtran journal template.
- [ ] **E6.1** In-season (causal) setting: decision day, cloudy attempts counted as cost
  - Ch 6 · experiment · code — Exact on GEE Estonia, approximate on EuroCropsML.
- [ ] **E6.2** Spatial transfer Latvia → Estonia
  - Ch 6 · experiment
- [ ] **E6.3** Growing-degree-day time axis for the cross-year shift
  - Ch 6 · experiment · code · data — Classifier loses 7.6 points 2019–21 → 2022. If GDD fixes it, reframe as phenology-aligned date selection.
- [ ] **W6.1** Write the oracle selection-bias section
  - Ch 6 · text — Already measured; writing only.
- [ ] **W3.1** Write the 2026 retrospective for the benchmark chapter
  - Ch 3 · text · literature
- [ ] **W1/2** Polish Chapter 1; write the Chapter 2 cost framework
  - Ch 1, 2 · text
- [ ] **X4** Merge bibliographies (export GISTAM references.bib from Overleaf)
  - All · literature

## Phase B · Chapters 5 and 7 (0/10)

- [ ] **E5.2** Cross-year band selection: select on 2019–21, test on 2022
  - Ch 5 · experiment — 3 bands lose ~5 points across years.
- [ ] **E5.4** Band rankings for EuroCropsML Latvia and Estonia
  - Ch 5, 7 · experiment
- [ ] **E5.1** Baselines at equal k: PCA, LDA, mutual information, random subsets
  - Ch 5 · experiment · code
- [ ] **E5.3** Report band savings in bytes with the cost model
  - Ch 5 · text
- [ ] **E7.0** Train the any-subset classifier on random band and date subsets
  - Ch 7 · code · experiment
- [ ] **E7.1** Region-specific bands for every dataset
  - Ch 7 · experiment — Needs E5.4.
- [ ] **E7.2** Joint vs sequential selection at equal byte budget
  - Ch 7 · experiment · code — Core Ch 7 result. Price actions in B10E; try cheaper 20 m red-edge bands.
- [ ] **E7.3** Cross-year transfer of the joint selection
  - Ch 7 · experiment
- [ ] **E7.4** Stopping with reduced bands
  - Ch 7 · experiment
- [ ] **E6.4** Label-free stopping threshold calibration on the target year
  - Ch 6 · experiment · code — Threshold overstates accuracy by ~5 points across years.

## Phase C · Turkish benchmark and JSTARS submission (0/3)

- [ ] **DATA** Finish the L2A dataset rebuild (TRAKYA/EGE re-download, class grouping fix)
  - Ch 6 · data · code
- [ ] **E6.5** Turkish multi-region, multi-year benchmark with double crops
  - Ch 6 · experiment · data — GUNEYDOGU, EGE, TRAKYA, AKDENIZ, 2019–2022. Rerun E7.3 on it.
- [ ] **S6.1** Write and submit the JSTARS manuscript
  - Ch 6 · text

## Phase D · consolidation (0/6)

- [ ] **X2** Unified cost–accuracy figures for every chapter
  - All · figure · code
- [ ] **W4.1** FLOPs per frame for the video detection chapter
  - Ch 4 · code · figure
- [ ] **W4.2** Discuss newer dynamic and ROI inference work
  - Ch 4 · literature · text
- [ ] **W7/8** Write Chapter 7, Chapter 8, Summary and Samenvatting
  - Ch 7, 8 · text
- [ ] **X5** Code and data availability statement per chapter
  - All · text
- [ ] **OPT** Optional: re-benchmark on current stack (E3.1), re-time detectors (E4.1), Ch 7 letter (E7.5)
  - Ch 3, 4, 7 · experiment
