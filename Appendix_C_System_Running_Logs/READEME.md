# Appendix C. System Running Logs

This folder contains supplementary system running logs preserved during the final stage of the thesis project **Design and Implementation of an Embedded AI Vision System**.

The logs were mainly generated during the final integrated-system experiments. They include runtime records from both the key-triggered system and the periodic-triggered system. Since these two systems share a large part of the same communication, image transmission, AI inference, and session-management logic, the logs are not strictly separated by trigger mode.

Instead, the logs are preserved according to the original experiment records. Experiments with clear validation purposes are named accordingly, such as error-injection tests, long-term running tests, single-sample validation tests, or final system validation tests.

## Scope of the Logs

The logs in this folder may include records of:

- PC-side serial communication startup;
- MCU-PC handshake process;
- JPEG image reception and reconstruction;
- image ID, chunk count, and received byte length;
- AI inference task execution;
- AI detection results such as `YES`, `NO`, or `BUSY`;
- result return from the PC side to the MCU side;
- TX_DONE and DONE_ACK end-handshake process;
- abnormal image handling or recovery-related behavior;
- error-injection and robustness validation;
- long-term or repeated system operation.

## Organization Principle

The logs are not intended to reconstruct every development step of the project. Earlier development stages produced many temporary debugging outputs, screenshots, and partial terminal records, but these records were not preserved as complete system logs.

Therefore, this appendix focuses only on the final-stage logs that were saved in a more complete and traceable form. These records are used as supplementary runtime evidence for the final system validation.

## Relationship to the Thesis

This folder corresponds to **Appendix C: System Running Logs** of the thesis.

The main thesis body discusses the key observations, system behavior, robustness mechanisms, and validation conclusions. The logs stored here provide additional runtime traceability for those discussions, especially for the final integrated system.

## Related Repositories

The main source code repository is available at:

```text
https://github.com/ZFL229/embedded-ai-insect-detection-system.git
