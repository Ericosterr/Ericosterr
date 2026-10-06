# Data Security Engineering Portfolio Roadmap

Target role: **Data Security Engineer / Technical Data Protection**

This roadmap turns a software-engineering background into a hands-on Data Security portfolio through realistic fintech-style labs.

## Portfolio Structure

### 1. Enterprise DLP & Data Security Lab — flagship project

Goal: demonstrate an end-to-end data protection workflow.

Planned capabilities:
- Sensitive-data discovery in files and databases
- PII / PCI / secrets detection
- Luhn validation for payment-card candidates
- Data classification labels
- Configurable DLP policies
- Simulated external transfer / exfiltration scenarios
- Security-event generation
- Elasticsearch ingestion
- Kibana dashboards
- ES|QL detection queries
- n8n incident automation
- Jira-ready incident payloads
- AWS S3 / IAM / KMS scenarios
- Documentation, runbooks and test cases

Suggested stack:
- Python
- FastAPI
- PostgreSQL
- Elasticsearch
- Kibana
- Docker Compose
- n8n
- AWS
- Pytest

---

### 2. Sensitive Data Scanner

Focused Python project demonstrating:
- Regex + validation-based detection
- Credit-card PAN detection with Luhn validation
- Email, phone, IBAN and secrets detection
- File scanning
- Structured findings
- Confidence / severity
- Classification output
- Unit tests

Example output:

```json
{
  "file": "customers.csv",
  "classification": "RESTRICTED",
  "findings": {
    "pan": 3,
    "email": 100,
    "api_key": 0
  }
}
```

---

### 3. Elastic Security Detection Lab

Focused SIEM project demonstrating:
- Security-event ingestion
- Elasticsearch mappings
- ES|QL queries
- Detection rules
- Kibana visualisations
- Alert triage examples
- False-positive tuning notes

---

### 4. Cloud Data Protection Lab

Focused AWS project demonstrating:
- Private S3 storage
- IAM least privilege
- KMS encryption
- CloudTrail audit events
- Secrets-management patterns
- Misconfiguration scenarios
- Security-control validation

---

# 10-Day Intensive

## Day 1 — DLP foundations + project skeleton

Learn:
- DLP architecture
- Data at rest / in motion / in use
- PII vs PCI vs secrets
- Classification
- Leakage channels
- False positives / false negatives

Build:
- Create the flagship repository
- Add professional README
- Create Python package structure
- Add Docker Compose skeleton
- Add sample synthetic data
- Add threat model

Deliverable:
- Repository compiles/runs
- Clear architecture diagram
- First README screenshots or CLI output

Interview outcome:
- Explain what DLP is and where controls can be enforced

---

## Day 2 — Sensitive-data scanner

Learn:
- Detection strategies
- Regex limitations
- Validators
- Context-aware detection

Build:
- PAN detector
- Luhn validator
- Email detector
- IBAN detector
- Basic secret detector
- Scanner result schema
- Unit tests

Deliverable:
- CLI: scan a directory and emit JSON findings

Interview outcome:
- Explain why regex alone is insufficient for PCI detection

---

## Day 3 — Classification + policy engine

Learn:
- Public / Internal / Confidential / Restricted
- Business context
- Policy precedence
- Block vs alert vs allow

Build:
- Classification rules
- YAML policy definitions
- Policy evaluator
- External-destination simulation
- Decision logging

Deliverable:
- Same file receives different decisions depending on destination/context

Interview outcome:
- Explain how to tune policy without destroying business usability

---

## Day 4 — Elasticsearch + Kibana

Learn:
- Events
- Indices
- Mappings
- Search
- SIEM concepts

Build:
- Add Elasticsearch/Kibana to Docker Compose
- Ship DLP events
- Create mappings
- Build first dashboard

Deliverable:
- Searchable DLP events in Elastic
- Kibana visualisation

Interview outcome:
- Trace an alert from generation to investigation

---

## Day 5 — ES|QL + detection engineering

Learn:
- Detection logic
- Aggregation
- Thresholds
- Correlation
- Baselines

Build:
- ES|QL queries
- Repeated-exfiltration detection
- High-volume record access
- High-risk destination rule
- Tuning examples

Deliverable:
- Five documented detection rules with expected test data

Interview outcome:
- Explain false-positive reduction and rule validation

---

## Day 6 — Incident investigation + automation

Learn:
- Triage
- Evidence
- Severity
- Escalation
- Playbooks

Build:
- n8n workflow
- Elastic alert → enrichment → incident payload
- Jira-ready ticket fields
- Notification path
- Incident response playbook

Deliverable:
- Automated workflow from alert to incident object

Interview outcome:
- Walk through a suspected data-leak investigation

---

## Day 7 — AWS data protection

Learn:
- IAM
- S3 policies
- KMS
- CloudTrail
- Secrets
- Least privilege

Build:
- Secure S3 example
- IAM policy examples
- KMS usage notes
- CloudTrail event sample
- Misconfigured vs corrected policy

Deliverable:
- Cloud-control documentation and test scenarios

Interview outcome:
- Explain how you would protect sensitive objects in S3

---

## Day 8 — Database / application protection

Learn:
- PostgreSQL permissions
- RBAC
- Masking
- Tokenisation
- Encryption
- Secrets handling

Build:
- PostgreSQL demo schema
- Role-based access
- Masked view
- Tokenised-value demo
- Environment/secrets patterns

Deliverable:
- Demonstrate that different roles see different data

Interview outcome:
- Clearly distinguish encryption, masking and tokenisation

---

## Day 9 — Testing, hardening and documentation

Build:
- Pytest suite
- Negative tests
- Edge cases
- Policy regression tests
- Runbook
- Architecture documentation
- Troubleshooting section
- Security assumptions

Deliverable:
- Reproducible lab
- Clean README
- Test results

Interview outcome:
- Show structured technical implementation rather than a demo script

---

## Day 10 — Application packaging + mock interview

Prepare:
- GitHub profile
- Pinned repositories
- CV security section
- Project bullets
- STAR stories
- Technical interview questions
- 5-minute project walkthrough

Deliverable:
- Job-ready GitHub portfolio
- Tailored CV bullets
- Interview cheat sheet

---

# Definition of Done

The portfolio is ready when a reviewer can:

1. Clone the flagship repository
2. Run it with documented commands
3. Scan synthetic sensitive data
4. See classification and policy decisions
5. Observe generated security events
6. Query those events in Elastic
7. Review detection logic
8. Follow an automated incident workflow
9. Understand cloud and database controls
10. Read tests, assumptions and response documentation

## Important

All sample data must be synthetic. Never commit real customer data, real secrets, real payment-card data, production credentials or private company information.
