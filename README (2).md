# ECHO — The Signal That Was Never Sent

**Project:** Entangled Minds: The Quantathon  
**Organizers:** Qubits Qrew · CS&IT, NED University of Engineering & Technology, Karachi  
**Team:** [Add your team name]  
**Investigator:** [Add your name]  
**Notebook:** `ECHO_Quantum_Investigation_Notebook_READY_FOR_GITHUB.ipynb`  
**Simulator:** Qiskit Aer

## Overview

ECHO is a quantum-computing investigation based on a fictional case involving a disputed signal and a claim that quantum entanglement could be used to communicate faster than light.

Using quantum circuits and simulations, this project explores single-qubit gates, superposition, entanglement, measurement, Bell correlations, classical error correction, and quantum teleportation.

**Our scientific conclusion:** Entanglement produces correlations, but it does not provide a controllable faster-than-light communication channel. Quantum teleportation also requires classical communication before the receiver can reconstruct the tested state.

## Modules Covered

| Module | Level | Main result |
|---|---|---|
| **01 — The Gatekeeper** | Mandatory | The X gate flips `0` to `1`; H creates an approximately balanced measurement distribution; applying H twice returns the qubit to `0`; the circuit also prepares the target pattern `101`. |
| **02 — The Honest Coin** | Stretch · Partial | An ideal H-gate quantum coin is simulated, and a theoretical sample-size reference is provided. The original recovered seed circuit is not included, so no conclusion about its bias is claimed. |
| **03 — The Two Observers** | Mandatory | A Bell pair produces correlated outcomes. A pre-agreed classical bit can reproduce agreement in one basis, while a CHSH test examines correlations across four measurement-setting pairs. |
| **04 — The Erased Measurement** | Stretch | Reversible gate sequences are compared with an intermediate measurement to illustrate how measurement affects the state and its recoverability. |
| **05 — The Damaged Message** | Mandatory | Majority voting over 32 received bit triples decodes the supplied message as `ECHO`. The three-bit repetition code corrects one bit flip per triple but can decode incorrectly if two bits flip. |
| **06 — The Impossible Claim** | Stretch | A teleportation circuit tests the input state `|+⟩` using classical feed-forward. A comparison without classical feed-forward shows why the receiver cannot recover the tested state from the shared entanglement alone. |

## Key Findings

- **Superposition and interference:** An H gate creates a superposition from `|0⟩`. Applying H again restores `|0⟩`, demonstrating `H² = I`.
- **Correlation is not communication:** A Bell pair produces correlated measurement outcomes, but agreement in one basis alone does not establish entanglement.
- **CHSH correlations:** The notebook estimates correlations using four measurement-setting pairs and compares the CHSH value with the local-hidden-variable bound of `|S| ≤ 2`.
- **Measurement:** An intermediate measurement removes relative-phase information, so a later gate cannot simply reverse the original coherent evolution.
- **Classical error correction:** Majority voting decodes the supplied 32 triples as **`ECHO`**. One bit flip per triple is correctable; two flips can silently produce an incorrect result.
- **Teleportation needs classical communication:** Bob's correction operations depend on Alice's two measured classical bits. Without those bits, Bob cannot recover the tested `|+⟩` state.
- **No faster-than-light messaging:** The simulations do not demonstrate faster-than-light communication.

## Final Verdict

**The simulations do not support the claim that ECHO sent a message faster than light.** Entanglement creates quantum correlations, but those correlations do not let a sender transmit a controllable message through the receiver's local measurement statistics. Quantum teleportation requires classical measurement information and correction operations.

The notebook's experiments do not establish what happened to Dr. Mahmud, identify who may have altered the fictional logs, or determine anyone's responsibility. Those questions remain open within the case narrative.

## Run the Notebook

### Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Select **File → Upload notebook**.
3. Upload `ECHO_Quantum_Investigation_Notebook_READY_FOR_GITHUB.ipynb` (or the final notebook filename in this repository).
4. Select **Runtime → Run all**.
5. Wait for the cells to finish and review the outputs, plots, and final reproducibility check.
6. Save or download the executed notebook if you want to preserve the run outputs.

The setup cell installs Qiskit and Qiskit Aer if they are not already available.

### Main dependencies

- `qiskit`
- `qiskit-aer`
- `numpy`
- `matplotlib`

Install locally with:

```bash
pip install qiskit qiskit-aer numpy matplotlib
```

The project uses simulation and does not require physical quantum hardware.

## Reproducibility Check

The final notebook cell collects the main results, checks deterministic circuits, verifies the decoded `ECHO` message, performs a statistical CHSH check, verifies the tested teleportation state, and plots selected measurement distributions.

Probabilistic counts and CHSH estimates may vary between runs because the simulator uses a finite number of shots.

A successful run should display:

```text
All deterministic, CHSH-statistical, decoding, and teleportation checks passed.
```

## Limitations

- The notebook uses an ideal simulator; it is not a physical quantum-hardware experiment.
- **Module 02 is partial:** the original recovered seed circuit is not included, so its bias has not been measured and Modules 02 Silver/Gold are not claimed complete.
- The CHSH estimate is subject to finite-shot statistical fluctuations. A simulator result is not a loophole-free physical Bell test.
- Module 05 demonstrates a classical three-bit repetition-code decoder; it does not implement a quantum error-correction code.
- Module 06 tests the specific input state `|+⟩`; it does not by itself demonstrate teleportation of every possible unknown state or prove the general no-signalling theorem.
- The simulations cannot determine the fictional case's historical events, identify a culprit, or establish a character's actions.

## Repository Contents

The repository may include:

- `README.md` — project overview and run instructions
- `ECHO_Quantum_Investigation_Notebook_READY_FOR_GITHUB.ipynb` — executable investigation notebook
- `ECHO_Case_Report.md` — case investigation report, if included
- `ECHO_Pitch_and_Defense_Guide.md` — presentation and defense notes, if included

## References

- Nielsen and Chuang, *Quantum Computation and Quantum Information*.
- Clauser, Horne, Shimony, and Holt (1969), work on the CHSH inequality.
- Qiskit documentation: https://qiskit.org/
- Wootters and Zurek (1982), work on the no-cloning theorem.

## AI Assistance

AI tools assisted with drafting and development. The notebook was run in Google Colab and its outputs were reviewed. The original Module 02 recovered seed circuit was not available in the notebook and is not claimed as completed.
