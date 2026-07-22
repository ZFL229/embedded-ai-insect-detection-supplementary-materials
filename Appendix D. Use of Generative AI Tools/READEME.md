# Appendix D – Supporting Records for Generative AI Use

This directory contains the supporting records referenced in **Appendix D: Use of Generative AI Tools** of the thesis:

**Design and Implementation of an Embedded AI Vision System for Binary Insect Detection Based on MCU–PC Collaboration**

Appendix D summarizes how generative AI tools were used during software development and thesis preparation. The materials in this directory provide representative evidence for the usage scenarios described in that appendix.

## Purpose

The purpose of this directory is to document selected examples of:

- AI-assisted design discussion;
- agent-based code implementation;
- project-level document context management;
- incremental debugging and architecture migration;
- hardware-oriented development support;
- thesis drafting and iterative author review.

These examples are intended to clarify the division of responsibility between the author and the AI tools.

The records do not represent a complete export of all AI interactions conducted during the project. They were selected as representative cases that demonstrate the principal forms of AI assistance disclosed in Appendix D.

## Case Overview

| Directory | Appendix D usage scenario | Description |
|---|---|---|
| `case 1 - Design Discussion and Agent-Based Implementation` | Design discussion and code implementation | Documents the transition from a two-button debugging workflow to a one-button capture-and-transmission workflow. The author defined the objective, limited the implementation scope, approved execution, and validated the result, while ChatGPT supported the design discussion and Codex performed the code modifications. |
| `case 2 - Project-Level Document Context Management` | Document-context retrieval | Documents the use of the eight stage summaries and the Apollo V2 hardware reference manual as persistent project context. The source materials were selected and prepared by the author, while AI was used to retrieve and reorganize relevant information. |
| `case 3 - Incremental Debugging and Architecture Migration` | Debugging and architecture planning | Documents the author’s decision to return from an unstable asynchronous implementation to a verified blocking baseline and then migrate the architecture through independently verifiable steps. |
| `case 4 - Hardware-Oriented Camera Integration` | Embedded hardware development support | Documents the layered reconstruction of the OV2640 camera integration workflow. AI provided suggested validation steps and initial test code, while the author performed IOC configuration, firmware programming, debugger operation, and physical hardware validation. |
| `case 5 - Thesis Drafting and Iterative Author Review` | Thesis drafting and revision | Documents how ChatGPT generated initial thesis drafts from author-provided outlines, stage summaries, and development records, while the author corrected the technical framing, logical order, chapter boundaries, level of detail, and final wording. |

## Contents of the Case Directories

Each case directory contains:

- screenshots of representative interactions;
- a Markdown file describing the context of the interaction;
- English translations of the relevant dialogue excerpts;
- a summary of the AI contribution;
- a summary of the author’s decisions, corrections, and verification activities.

Most original interactions were conducted in Chinese. The translated text is provided to make the records understandable to readers of the English-language thesis. The screenshots preserve the original interaction content.

## Interpretation

The cases demonstrate an author-controlled AI-assisted workflow.

Generative AI tools were used to:

- discuss possible technical approaches;
- generate initial code and implementation suggestions;
- perform code restructuring and refactoring;
- organize debugging procedures;
- retrieve information from author-provided documents;
- generate initial thesis drafts and translations.

The author remained responsible for:

- defining system objectives and requirements;
- selecting the final architecture and implementation approach;
- configuring hardware and development tools;
- reviewing and modifying generated code;
- compiling, programming, and operating the target hardware;
- designing and conducting experiments;
- interpreting results;
- correcting and approving the final thesis text.

AI-generated outputs were treated as provisional working materials and were accepted only after appropriate author review and verification.

## Relationship to Appendix D

The five directories correspond to the representative usage scenarios summarized in Appendix D.

Appendix D contains the formal disclosure of:

- the generative AI tools used;
- their principal areas of application;
- the representative usage scenarios;
- the treatment and marking of generated outputs;
- the author’s review and verification responsibilities.

The materials in this directory serve only as supporting records for that disclosure.
