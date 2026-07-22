# Supplementary Materials for Embedded AI Insect Detection System

This repository contains supplementary materials for the master’s thesis:

**Design and Implementation of an Embedded AI Vision System for Binary Insect Detection Based on MCU–PC Collaboration**

The repository supplements the thesis with image data, runtime records, AI-use documentation, and preserved development records. These materials are provided to improve transparency, reproducibility, and traceability without expanding the main thesis with large volumes of supporting files.

The primary source code and implementation repository is maintained separately:

https://github.com/ZFL229/embedded-ai-insect-detection-system

## Repository Scope

This repository contains materials associated mainly with Appendices B–E of the thesis.

The files are not required to understand the principal arguments, architecture, or results presented in the thesis. They provide additional evidence for readers who wish to inspect:

- image samples used or generated during validation;
- system and communication runtime behavior;
- error-injection and robustness experiments;
- representative generative AI usage scenarios;
- daily development logs and stage summaries;
- the traceability from detailed engineering records to the final thesis.

## Structure

### `Appendix_B_Supplementary_Image_Data/`

Contains supplementary image data used or generated during:

- AI baseline validation;
- OV2640 camera integration;
- image-quality experiments;
- target and empty-scene testing;
- final system validation.

The directory preserves image examples that support the observations presented in the thesis but were not included directly because of page limitations.

### `Appendix_C_System_Running_Logs/`

Contains selected system records, including:

- MCU–PC communication logs;
- image-transmission logs;
- AI-inference and binary-decision outputs;
- error-injection logs;
- robustness-test records;
- repeated-session and long-term validation logs.

These records document observable system behavior under normal and selected abnormal operating conditions.

### `Appendix_D_Generative_AI_Use/`

Contains representative records supporting the generative AI disclosure in Appendix D of the thesis.

The materials are organized into several typical use cases:

- design discussion and agent-based implementation;
- project-level document context management;
- incremental debugging and architecture migration;
- hardware-oriented camera integration;
- thesis drafting and iterative author review.

Each case includes selected screenshots and a Markdown description containing context, translated dialogue excerpts, and a summary of the respective roles of the author and the AI tool.

The examples are representative rather than a complete export of all AI interactions conducted during the project.

### `Appendix_E_Development_Records_and_Process_Traceability/`

Contains the preserved project documentation used to support development-process traceability.

The directory includes:

- daily development logs;
- eight stage summaries.

The daily logs preserve detailed chronological records of implementation work, technical decisions, provisional hypotheses, failed attempts, and planned next steps. These logs are retained in Chinese.

The stage summaries were produced after the completion of each of the eight development phases. They consolidate the corresponding daily records into logically complete phase-level accounts. Both Chinese and English versions are provided.

Together with the thesis, these materials form the following three-layer documentation structure:

> **Daily development logs → Stage summaries → Thesis**

## Relationship Between the Repositories

The project materials are divided between two repositories.

### Main implementation repository

https://github.com/ZFL229/embedded-ai-insect-detection-system

Contains the principal source code, implementation structure, configuration files, and project documentation.

### Supplementary-materials repository

https://github.com/ZFL229/embedded-ai-insect-detection-supplementary-materials

Contains supporting images, logs, AI-use records, and development-process documentation referenced in the thesis appendices.

## Interpretation of the Materials

Some files in this repository are working records rather than finalized technical reports.

In particular, daily development logs may contain:

- incomplete reasoning;
- preliminary assumptions;
- alternative explanations;
- unsuccessful approaches;
- hypotheses that were later revised or rejected.

Final technical claims should therefore be interpreted according to the thesis, the corresponding stage summaries, the implemented source code, and the completed validation results.

The stage summaries represent a more consolidated account of the project phases, while the thesis presents the final research-oriented interpretation.

## Language

Most original development work and AI interactions were recorded in Chinese.

English translations are provided where necessary for accessibility, particularly for:

- stage summaries;
- representative AI-use cases;
- descriptions referenced directly by the English-language thesis.

The original Chinese records are preserved where they provide the most complete account of the development process.

## Traceability and Responsibility

The materials in this repository support the traceability of:

- system design decisions;
- implementation evolution;
- experimental observations;
- robustness validation;
- AI-assisted development and writing;
- the transformation from daily engineering records to the final thesis.

Generative AI outputs were treated as provisional working materials. Final system decisions, hardware configuration, experiments, validation, interpretation of results, and submitted thesis content remained the responsibility of the author.

## Usage

The repository is intended primarily for academic review and project traceability.

Readers may consult the individual appendix directories for more detailed README files describing the contents and interpretation of each material group.
