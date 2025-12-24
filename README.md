# FPGA Audio Manager

This repository contains the full source code (custom firmware written in **PicoBlaze (KCPSM) assembly**) for an FPGA-based audio manager.  
The design is written for a Xilinx FPGA and includes a PicoBlaze (KCPSM) soft processor that handles all control logic.

After synthesizing this design and loading the generated bitstream onto the FPGA board, the board itself becomes a standalone audio manager. All interaction is performed using the physical buttons and slider(s) on the board (Up / Down / Select), and the system supports recording, playback, pause/skip, deletion of tracks, and volume control.

## Features
- Record and play audio tracks (1–5)
- Pause / resume and skip
- Delete individual tracks or wipe all
- Volume control (High / Medium / Low)
- Memory-full detection and protection

## Tech
- Platform: Xilinx FPGA
- Control logic: PicoBlaze (KCPSM) soft-core
- Language: PicoBlaze assembly + FPGA logic
- Interface: Physical buttons, on-board audio, internal FSM

## Usage
1. Synthesize the project to generate a bitstream.
2. Program the FPGA board with the bitstream.
3. Use the board’s buttons to control the audio manager.
