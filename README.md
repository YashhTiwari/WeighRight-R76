# WeighRight R76

**From test bench to certified report, automatically.**

A web application that generates test reports for Non-Automatic Weighing Instruments (NAWI) as per **OIML R 76**. Built for Smart India Hackathon 2025.

- **Problem Statement:** Development of a Software Program/Application for Generation of Test Reports for NAWI as per OIML R-76
- **Category:** Software

## Problem

Test reports for weighing instruments are prepared today with spreadsheets and Word templates. This leads to manual calculation errors, inconsistent report formats, rework and slow turnaround.

## Solution

WeighRight R76 digitizes the whole R 76 type-evaluation workflow:

1. **Enter**: instrument registry, lab and environment log, test data forms
2. **Calculate**: automatic error and MPE (Maximum Permissible Error) engine
3. **Verify**: pass / fail compliance verdict
4. **Report**: PDF / DOCX report generator, searchable repository and dashboard

## Key Features

- Guided forms with live validation and green/red compliance indicators
- Versioned rule engine: R 76 limits are configuration, so an OIML revision needs only a rule update, not a redeploy
- Smart validation: out-of-range, missing, unit mismatch and anomaly flags
- Standard report in PDF and editable DOCX, with optional digital signature
- Tamper-evident reports (QR code / hash verification)
- Audit trail, role-based access, optional offline data entry

## Tests Covered (per R 76)

Weighing performance, eccentricity, repeatability, discrimination, tare, zero-setting, temperature, power supply variation, creep, span stability, and others per R 76.

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React + Vite, Tailwind CSS |
| Backend | Python FastAPI, Pydantic |
| Database | PostgreSQL; MinIO / S3 for files |
| Rule engine | Versioned JSON/YAML rule sets; NumPy / Pandas |
| Reports | ReportLab / WeasyPrint (PDF), python-docx (Word) |
| Security | JWT auth, RBAC (Admin / Tester / Reviewer / Viewer), audit trail |
| Optional | DSC / eSign, Docker, CI/CD |

## Architecture

Client (React UI) <-> API & Rule Engine (FastAPI) <-> Database & File Storage (PostgreSQL, MinIO / S3)

## Roadmap

1. Requirements
2. Rule modelling
3. Core build
4. Testing with sample data
5. Deployment and documentation

## References

- OIML R 76-1 and R 76-2 (Non-Automatic Weighing Instruments)
- Legal Metrology Act, 2009
- Legal Metrology (General) Rules, 2011
- Department of Consumer Affairs / Legal Metrology portal
