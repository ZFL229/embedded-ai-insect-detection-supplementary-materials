# Supplementary Image Data

This folder contains supplementary image materials for the thesis project **Design and Implementation of an Embedded AI Vision System**.

These images are provided as supporting materials for the appendix of the thesis. They are not part of the main source code repository. Since the final thesis is submitted as a PDF file, the complete image records are stored externally in this supplementary materials repository for traceability.

The images are organized according to the development stage and their role in the system validation process.

## Folder Structure

| Folder | Description | Role in the Thesis |
|---|---|---|
| `test_images` | Local insect images used during the early AI validation stage and the MCU-communication-AI closed-loop validation stage. These images were downloaded from the Internet and used as test inputs before the real camera acquisition chain was established. | Supports the early validation of the PC-side AI inference baseline and the image-based closed-loop verification before real camera integration. |
| `capture_picture` | Images actually captured by the OV2640 camera during the camera integration stage and the key-triggered capture system development stage, mainly corresponding to Phase 6 and Phase 7. This folder includes both normal captured images and images generated during camera debugging, such as distorted or color-shifted outputs. | Supports the analysis of camera integration, JPEG acquisition, image distortion, ISP/AWB state drift, and capture-chain recovery mechanisms. |
| `AI_Inference_picture` | Images saved during the final system experiments after AI inference. These images were generated when the complete system was running and were used to observe the final detection behavior. | Supports the validation of the complete system pipeline, including camera capture, image transmission, PC-side reconstruction, AI inference, and result feedback. |

## Notes

The materials in this repository are used only as supplementary evidence for the thesis. The main thesis body already includes representative images and discusses the key observations, design decisions, and validation results.

The purpose of this repository is to preserve the complete image records for:

- development traceability;
- camera debugging evidence;
- image-quality comparison;
- AI inference validation;
- final system verification.

The main source code of the project is stored in a separate repository:

```text
https://github.com/ZFL229/embedded-ai-insect-detection-system.git
