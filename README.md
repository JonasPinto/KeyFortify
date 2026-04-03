#  KeyFortify

> **Production-Ready Quantitative Password Security Analyzer**  
> Advanced credential strength evaluation aligned with NIST SP 800-63B and OWASP Authentication best practices.

## Overview

**KeyFortify** is a security-focused Python application designed to provide measurable, audit-ready password strength analysis using real-world attack modeling.

Unlike common password checkers that provide superficial scores, KeyFortify performs:

- Quantitative entropy analysis  
- Realistic crack-time simulation  
- Threat scenario modeling  
- Privacy-preserving breach detection  
- Key Derivation Function (KDF) benchmarking  

This project demonstrates applied cryptography, secure software engineering, performance modeling, and production-grade Python packaging.

## Problem Statement

In modern cybersecurity environments:

- 90%+ of data breaches involve compromised credentials  
- Traditional password policies create false security  
- GPU clusters can break predictable passwords in minutes  
- Organizations lack measurable password security metrics  
- Compliance frameworks require audit evidence  

KeyFortify addresses these gaps using reproducible, data-driven analysis.

## Core Architecture

### Entropy Modeling

Hybrid approach combining:

- Heuristic analysis (zxcvbn-style modeling)
- Mathematical keyspace estimation
- Pattern detection
- Dictionary and substitution awareness

### Crack Time Simulation

Models realistic attacker scenarios:

- Online (rate-limited)
- Online (no rate limit)
- Offline (single GPU)
- Offline (GPU cluster / ASIC)

Formula:

```python
time_to_crack = keyspace / hash_rate
```

Benchmarked against modern hashing standards:

- Argon2id  
- bcrypt  
- scrypt  
- PBKDF2  

##  Privacy-Preserving Breach Detection

Implements k-anonymity model:

1. Password is hashed locally (SHA-1)  
2. Only first 5 hash characters are transmitted  
3. Matching suffixes are returned  
4. Comparison occurs locally  

 ✅ Zero exposure of full password  
 ✅ Zero exposure of full hash  
 ✅ Secure-by-design implementation  

##  Engineering Highlights

This repository demonstrates:

- Secure coding practices  
- Modular architecture  
- CLI application design  
- Modern Python packaging (pyproject.toml)  
- Virtual environment isolation  
- Performance-aware modeling  
- Defensive programming  
- Extensible system design  

##  Installation

```bash
git clone https://github.com/JonasPinto/KeyFortify.git
cd KeyFortfy
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
pip install -e .
```

##  Usage Example

```python
from keyfortify.analyzer import analyze_password

result = analyze_password("correcthorsebatterystaple")
print(result)
```

Output includes:

- Estimated entropy  
- Keyspace size  
- Crack time per threat model  
- Optional breach detection indicator  

##  Feature Set

- Entropy analysis (heuristic + deterministic)
- Crack-time simulation (multi-scenario)
- KDF benchmarking
- Batch password analysis
- Professional report generation:
  - PDF
  - JSON
  - CSV
- CLI interface
- Extensible architecture

##  Tech Stack

- Python 3.10+
- zxcvbn-style entropy modeling
- argon2-cffi
- bcrypt
- scrypt
- pandas
- matplotlib
- reportlab
- Hatch build system
- pyproject.toml packaging standard

##  Security & Compliance Alignment

Aligned with:

- NIST SP 800-63B  
- OWASP Authentication Cheat Sheet  
- Secure password storage best practices  
- Privacy-by-design principles  

##  Roadmap

- Full CLI argument parsing
- Streamlit Web UI
- Signed PDF export
- Extended KDF benchmarking dashboard
- Unit and integration tests
- CI/CD integration
- Docker containerization

##  Real-World Applications

- Security engineering teams
- Backend authentication validation
- DevSecOps pipelines
- Compliance audit preparation
- Security research
- Password policy validation

##  Skills Demonstrated (ATS Optimized Keywords)

- Python Development  
- Cybersecurity  
- Cryptography  
- Secure Authentication  
- Backend Engineering  
- Performance Optimization  
- Threat Modeling  
- Software Architecture  
- CLI Development  
- Secure Hashing Algorithms  
- Argon2 / bcrypt / PBKDF2  
- Security Compliance  
- Modular Code Design  
- Production Packaging  
