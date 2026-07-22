# case 4 - Hardware-Oriented Camera Integration - Staged Camera Integration and Hardware Debugging

## Usage

This workflow applies AI guidance to rebuild and verify an embedded camera chain from the hardware configuration upward. The user keeps only the relevant IOC pin configuration and asks for a minimal debug-first integration. The AI separates the work into observable stages so that each hardware layer can be validated before image capture is attempted.

Typical sequence:

1. Provide the current IOC configuration and relevant source files.
2. Rebuild the software logic from a minimal initialization path.
3. Expose debug variables that can be inspected in the debugger.
4. Verify the I/O expander and camera power-control path first.
5. Read and verify the OV2640 SCCB device ID.
6. Only then proceed to JPEG configuration, DCMI, DMA, and complete image capture.

## Approximate Conversation Translation

**User:** I have kept only the relevant IOC pin settings. Now I want to restart camera integration and debug it in debug mode.

**AI:** That is the right approach: keep the IOC pin configuration but rebuild the software logic from zero, so old code cannot hide the fault. We will avoid relying on serial output and instead use observable debug variables plus GPIO and register state to verify the camera chain layer by layer.

**AI:** The first `main.c` should only initialize GPIO, DMA, I2C2, and DCMI. For the first stage, do not touch DCMI or capture an image. Verify that the PCF8574 can be addressed and written. Watch `dbg_step`, `dbg_i2c_status`, and `hi2c2.ErrorCode`; `HAL_OK` confirms that the PCF8574 path is working.

**AI:** In the second stage, verify the OV2640 SCCB ID only. Use the PCF8574 to release camera power-down, perform a hardware reset, and read the sensor ID over SCCB. Do not initialize JPEG or DCMI yet. Expected values are approximately PID `0x26` and version `0x42`; obtaining these values confirms that the power, reset, and SCCB control path is alive.
