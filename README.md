# 🔐 Side-Channel Attack Resistant Cryptographic Libraries

## 🧠 Objective

To design and implement **constant-time** (side-channel resistant) versions of the following cryptographic algorithms:

- AES (Advanced Encryption Standard)
- RSA (Rivest–Shamir–Adleman)
- ECC (Elliptic Curve Cryptography)

And to **evaluate their resistance** against common side-channel attacks using timing analysis and power leakage simulations.

---

### Install Dependencies

pip install -r requirements.txt

### Run in Google Colab

1. Upload the entire folder to Google Drive.
2. Open `evaluation_report.ipynb` in Colab.
3. Run all cells to simulate timing/power attacks and analyze defenses.
---

## 🛡️ Side-Channel Attack Resistance Strategy

All implementations follow constant-time principles:

- No data-dependent branching.
- Fixed memory access patterns.
- Bit-masking and blinding techniques.

Evaluation metrics include:

- Timing variance analysis
- Differential power analysis (simulated)
- Entropy of leakage

---

## 📈 Evaluation Report

A full evaluation of:

- Side-channel leakage before/after optimization.
- Benchmark charts comparing execution time and leakage score.
- Effectiveness against synthetic power trace analysis.

View the interactive evaluation in `Evaluation/evaluation_report.ipynb`.

---

## 🧪 Testing

All crypto modules are tested using Python’s `unittest` framework to ensure:

- Correct encryption/decryption (AES)
- Valid signature and verification (RSA/ECC)
- Invariance under repeated runs (timing stability)

---

## 🔒 Cryptographic Notes

- AES: T-table replaced with bitwise operations and S-box masking.
- RSA: Uses Montgomery multiplication and exponent blinding.
- ECC: Implements scalar multiplication using constant-time laddering.

---

## 📚 References

- [Cryptographic Engineering by N. Koblitz & A. Menezes]
- https://cryptojedi.org
- https://www.chosenplaintext.ca

---

## 📄 License

MIT License

---
