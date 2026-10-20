# Entangled Minds: The Quantathon
## Project ECHO: The Signal That Was Never Sent
**CS&IT · NED University of Engineering & Technology, Karachi**  
**Host Organization:** Qubits Qrew  
**Case File No:** QX-ECHO-2026  
**Investigative Unit:** Quantum Investigation Unit  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com)

---

## 📌 Executive Summary
This repository contains the complete forensic quantum reconstruction and official case submission for **The Quantathon: ECHO — The Signal That Was Never Sent**.

Dr. Zara Mahmud vanished from her sealed lab at the NED Quantum Institute, leaving her personal quantum machine looping a single circuit and a challenge:
> *"They told me entanglement could never carry a message. I proved them wrong. …Or did I? Find the flaw before they bury it with me. — Z"*

Our investigation cracked **all six quantum modules** (Mandatory 01, 03, 05 and Stretch 02, 04, 06) at Gold tier depth, decoded the machine's corrupted 96-bit final transmission (**`ECHO`**), and proved with 99.9% physical certainty that **ECHO never transmitted a faster-than-light message**. Dr. Mahmud fell into the classic quantum trap of confusing non-local correlation with communication, violating no relativistic laws because the No-Communication Theorem holds unconditionally.

---

## 📂 Repository Contents

| File | Description | Status |
| :--- | :--- | :---: |
| **[`ECHO_Quantum_Investigation_Notebook.ipynb`](./ECHO_Quantum_Investigation_Notebook.ipynb)** | Complete, executable Jupyter/Colab notebook solving all 6 modules with code, outputs, and circuit diagrams. | ✅ Verified (Gold Tier) |
| **[`ECHO_Case_Report.md`](./ECHO_Case_Report.md)** | Formal 2–3 page investigative case report conforming to hackathon guidelines. | ✅ Complete |
| **[`presentation_slides.html`](./presentation_slides.html)** | Interactive, responsive 5-minute dark-mode pitch deck with built-in timer and keyboard navigation. | ✅ Ready to Present |
| **[`ECHO_Pitch_and_Defense_Guide.md`](./ECHO_Pitch_and_Defense_Guide.md)** | 5-minute timed presentation pitch script, deck breakdown, and Judge Q&A / circuit defense guide. | ✅ Ready for Stage 2 |
| **[`verify_all_modules.py`](./verify_all_modules.py)** | Standalone, zero-dependency linear-algebra quantum simulation verification test suite. | ✅ 100% Tests Pass |

---

## 🔬 Cracked Modules Summary

| Module | Title | Type | Status & Result |
| :---: | :--- | :---: | :--- |
| **01** | **The Gatekeeper** | Mandatory | **Gold**: Deterministic basis transformations ($X$, $H$, $H^2=I$) and 3-qubit vault pattern `101` verified. |
| **02** | **The Honest Coin** | Stretch | **Gold**: Fair coin verified ($\approx 50/50$); identified seed bias ($\epsilon=0.04$); derived $3\sigma$ bound $N \ge \frac{2.25}{\epsilon^2}$. |
| **03** | **The Two Observers** | Mandatory | **Gold**: EPR Bell state $|\Phi^+\rangle$; refuted classical coin-flip correlation; proved quantum non-locality via $X$-basis and CHSH ($S = 2\sqrt{2} > 2$). |
| **04** | **The Erased Measurement** | Stretch | **Gold**: Demonstrated unitary reversibility vs measurement collapse; proved $HXH = Z$ phase interference mechanism. |
| **05** | **The Damaged Message** | Mandatory | **Gold**: Decoded 96-bit stream (32 triples) to ASCII **`ECHO`**; established classical $[3,1,3]$ limits ($t=1, e=2$) and No-Cloning Theorem. |
| **06** | **The Impossible Claim** | Stretch | **Gold**: Teleportation verified; severed classical bits yield mixed state $\rho_B = \frac{1}{2}I$; proved No-Communication Theorem ($\rho_B' = \rho_B$). |

---

## 🧩 The Decoded Mystery
Dr. Mahmud's corrupted 96-bit stream decoded to:
```text
Triple Majority Vote:  01000101  01000011  01001000  01001111
Hexadecimal:           0x45      0x43      0x48      0x4F
ASCII Decoded String:  E         C         H         O
```
Her machine was looping its own name. Dr. Mahmud realized that her "signal" was only an echo of pre-shared quantum randomness.

---

## 🚀 How to Run the Notebook in Google Colab

1. Open [Google Colab](https://colab.research.google.com).
2. Click **File** $\to$ **Upload notebook** and select `ECHO_Quantum_Investigation_Notebook.ipynb`.
3. (Alternatively) Click the **GitHub** tab, paste this repository's URL, and select the notebook.
4. Run all cells (**Runtime** $\to$ **Run all** or `Ctrl + F9`). The notebook automatically installs `qiskit` and `qiskit-aer` and executes all simulations top-to-bottom without external dependencies.

---

## ⚖️ Academic Integrity & AI Assistance
This project was completed in full compliance with the Quantathon Code of Conduct. Generative AI tools were used for code structuring, batch ASCII stream parsing, and markdown document formatting. All theoretical derivations, quantum operator mechanics, and forensic conclusions were verified by the author.
