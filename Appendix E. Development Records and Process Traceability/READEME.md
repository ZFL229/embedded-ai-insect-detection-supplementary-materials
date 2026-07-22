# Development Logs and Stage Summaries

This directory contains the development records referenced in **Appendix E: Development Records and Process Traceability** of the thesis:

**Design and Implementation of an Embedded AI Vision System for Binary Insect Detection Based on MCU–PC Collaboration**

The archived materials are organized into two documentation layers:

1. daily development logs;
2. stage summaries.

Together with the thesis, they form the following three-layer documentation structure:

> **Daily development logs → Stage summaries → Thesis**

## Directory Structure

### `daily log`

This directory contains the daily development logs recorded during the project.

The logs preserve the chronological engineering process, including:

- tasks completed on each day;
- implementation details;
- hardware and software observations;
- encountered problems and failed attempts;
- important technical decisions;
- provisional engineering hypotheses;
- planned work for the following day.

The daily logs are working records rather than finalized technical reports. They may therefore contain incomplete reasoning, temporary assumptions, alternative explanations, or hypotheses that were later revised or rejected.

All daily logs are preserved in their original **Chinese-language version**. They are not translated because of their volume and because their main purpose is to retain the original development context and chronological record.

### `Stage Summaries`

This directory contains the eight stage summaries corresponding to the eight development phases listed in Table 1 of the thesis.

At the completion of each phase, the relevant daily logs were reviewed and consolidated into a stage summary. During this process:

- repeated debugging details were reduced;
- fragmented reasoning was reorganized;
- hypotheses rejected by later experiments were removed;
- key design decisions were retained;
- the main implementation path and validation results were summarized;
- the final state of the phase and the transition to the next phase were recorded.

The stage summaries therefore provide a more logically complete and stable account of the project than the raw daily logs, while preserving the development logic required for later thesis preparation.

Each stage summary is available in both:

- **Chinese**, preserving the original project documentation;
- **English**, providing an accessible version for readers of the English-language thesis.

## Relationship Between the Records

The two directories represent different levels of abstraction.

The daily logs preserve the most detailed record of the actual engineering process. The stage summaries extract the validated and logically complete development path from those logs. The thesis then further selects and reorganizes material from the stage summaries according to its research questions, chapter structure, and academic focus.

The relationship can therefore be summarized as:

> **Detailed chronological engineering records**  
> → **Consolidated phase-level summaries**  
> → **Research-oriented thesis presentation**

The records in this directory provide supporting material for the development-process traceability described in Appendix E.
