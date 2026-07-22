# case 5 - Thesis Drafting and Translation - Thesis Drafting and Structural Refinement

## Usage

This workflow uses the AI as a writing and structure assistant for an engineering thesis. The user supplies an outline and stage summaries, asks for English draft sections, and then corrects the narrative emphasis. The AI does not merely translate notes; it helps identify the real technical storyline, reorganize subsections, and keep detailed protocol material in the appropriate chapter.

Typical sequence:

1. Provide the thesis outline and relevant stage summaries.
2. Ask for a draft of a specific chapter or subsection in English.
3. Review whether the draft identifies the correct system actors and technical contribution.
4. Correct the narrative when the emphasis is incomplete or misplaced.
5. Ask the AI to revise the structure, transitions, and level of detail.
6. Keep implementation details in later sections and use earlier sections to establish motivation and architecture.

## Approximate Conversation Translation

**User:** Next, write Chapter 5. Start with the introduction. I do not expect this chapter to be especially long.

**AI:** Chapter 5 should be shorter than the image-acquisition chapter. It can explain how the communication mechanism evolved from a simple closed loop into a complete session lifecycle, focusing on string communication, the CRC32 frame protocol, TCP validation, image chunking, handshakes, and session handling.

**User:** I have realized something important. The communication evolution includes not only the PC communication module but also the MCU side. Both sides evolved together, so the chapter has two protagonists.

**AI:** Correct. The chapter should describe the co-evolution of MCU-side communication behavior and the PC-side communication module. Each protocol upgrade required coordinated changes to the MCU request and feedback model and to the PC receive, parse, reconstruction, inference, and response model.

**User:** In this subsection, emphasize how the frame protocol expanded from transmitting results to transmitting images. TCP should only be treated as an intermediate validation channel. Then explain the return to blocking communication and the later image closed loop.

**AI:** The main line should be: the frame protocol becomes the underlying message structure; image chunks extend the payload layer; the PC reconstructs the image and sends it to AI inference; and the STM32 continues to query the result over UART. TCP is a temporary validation path rather than the central innovation.

**User:** The logic is still not right. Introduce TCP before the chunking protocol, or first describe the TCP communication model and why it solved the earlier problem. Also summarize the protocol in a table and refer to the PDF for error handling and reliability.

**User:** Before that, introduce Section 3.2 using the Stage 2 and Stage 3 summaries.

**AI:** Section 3.2 should explain the transition from the isolated PC-based AI baseline to an embedded communication closed loop. It should establish the architectural purpose without introducing later details such as CRC or image chunking, which belong in Chapter 5.
