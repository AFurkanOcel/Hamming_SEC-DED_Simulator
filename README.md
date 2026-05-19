<h1 align="center">Hamming SEC-DED Simulator</h1>

<p align="center">
A desktop-based Hamming code simulator built with Python and Tkinter for encoding binary data, injecting bit errors, calculating syndrome values, and correcting single-bit transmission errors.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Language-Python-blue"/>
  <img src="https://img.shields.io/badge/GUI-Tkinter-green"/>
  <img src="https://img.shields.io/badge/Algorithm-Hamming%20Code-orange"/>
  <img src="https://img.shields.io/badge/Error%20Handling-Single--Bit%20Correction-red"/>
  <img src="https://img.shields.io/badge/Platform-Desktop-lightgrey"/>
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen"/>
</p>

---

## Project Overview

**Hamming SEC-DED Simulator** is an educational desktop application that
demonstrates the core workflow of Hamming-based error detection and correction.
The application accepts binary input, generates a Hamming code, allows the user
to flip a selected bit, calculates the syndrome value, and corrects the detected
single-bit error.

The project is designed for learning and demonstration purposes, especially for
students studying digital communication, error-correcting codes, computer
architecture, or fault-tolerant systems.

---

## Technologies Used

| Technology | Purpose |
|-----------|---------|
| Python 3 | Main programming language |
| Tkinter | Desktop graphical user interface |
| Hamming Code | Error detection and single-bit correction logic |
| Local text logging | Runtime operation history in `hamming_log.txt` |

No external Python packages are required.

---

## Project Structure

```text
Hamming_SEC-DED_Simulator/
|-- .gitattributes
|-- .gitignore
|-- hamming_sec_ded.py
|-- LICENSE
|-- README.md
|-- assets/
|   |-- icons/
|   |   `-- settings.ico
|   `-- screenshots/
|       `-- application-screenshot.png
```

---

## Main Components

| Component | Responsibility |
|----------|----------------|
| `calculate_parity_bits()` | Calculates the required parity bits and generates the Hamming code |
| `detect_error()` | Calculates the binary and decimal syndrome values from received data |
| `flip_bit()` | Simulates a transmission error by flipping a selected bit |
| `HammingApp` | Builds and controls the Tkinter user interface |
| `hamming_log.txt` | Stores generated code, injected error, syndrome, and correction history |

---

## Features

- Desktop GUI built with Tkinter
- Selectable input lengths:
  - `4-bit`
  - `8-bit`
  - `16-bit`
  - `32-bit`
  - `64-bit`
- Binary input validation
- Dynamic parity bit calculation
- Hamming code generation
- Manual bit-flip error injection
- Syndrome calculation in binary and decimal form
- Single-bit error localization
- Automatic correction for detected single-bit errors
- Built-in help dialog
- Local runtime logging
- Repository-managed screenshot and icon assets

---

## Application Workflow

```text
Select binary data length
   |
   v
Enter binary data
   |
   v
Generate Hamming code
   |
   v
Enter bit position to flip
   |
   v
Inject transmission error
   |
   v
Calculate syndrome
   |
   v
Locate and correct the single-bit error
   |
   v
Write operation details to hamming_log.txt
```

---

## Screenshot

<img width="570" alt="Hamming SEC-DED Simulator desktop interface" src="assets/screenshots/application-screenshot.png" />

---

## Demo Video

Watch the demo on YouTube:

https://www.youtube.com/watch?v=rHKQKSCRnW0

---

## How to Run

Clone the repository:

```bash
git clone https://github.com/AFurkanOcel/Hamming_SEC-DED_Simulator.git
cd Hamming_SEC-DED_Simulator
```

Run the application:

```bash
python hamming_sec_ded.py
```

Requirements:

```text
Python 3.x
```

---

## Example Workflow

Input:

```text
10110011
```

Generated Hamming Code:

```text
001101100011
```

Injected Error Position:

```text
5
```

Corrupted Data:

```text
001101110011
```

Detected Syndrome:

```text
Binary: 0101
Decimal: 5
```

Corrected Output:

```text
001101100011
```

---

## Error Logging

The application writes runtime operation details to:

```text
hamming_log.txt
```

The log file includes generated Hamming codes, injected error positions,
corrupted data, syndrome values, and corrected output. Since this file is a
local runtime output, it is ignored by Git.

---

## Algorithm Notes

The simulator demonstrates the main ideas behind Hamming-code-based error
handling:

| Step | Description |
|------|-------------|
| Parity position selection | Reserves power-of-two positions for parity bits |
| Parity calculation | Computes parity values over the related bit groups |
| Syndrome generation | Recomputes parity checks from the received data |
| Error localization | Converts the syndrome value into the detected bit position |
| Correction | Flips the detected bit back to restore the original Hamming code |

The current implementation focuses on single-bit error correction through
syndrome analysis. Explicit double-error detection can be added in a future
version by extending the encoded data with an overall parity bit.

---

## Syntax Verification

The Python source file can be checked without generating cache files:

```bash
python -c "import ast, pathlib; ast.parse(pathlib.Path('hamming_sec_ded.py').read_text(encoding='utf-8'))"
```

A successful run produces no output and confirms that the source file is
syntactically valid.

---

## Limitations and Future Work

- Add explicit double-error detection with an overall parity bit
- Move algorithm logic into a separate module if the project grows
- Add automated tests for parity calculation, syndrome detection, and correction
- Add random error generation for demonstration scenarios
- Add step-by-step parity visualization
- Add export options for generated results

---

## Author

**A. Furkan &Ouml;CEL**

---

## License

This project is licensed under the terms included in the repository's
`LICENSE` file.
