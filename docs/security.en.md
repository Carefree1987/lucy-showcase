# Security Model & Practices

## Security by Design
Lucy is built with security as a core requirement, especially given the sensitive nature of career and student data.

### 1. Secret Scanning
We use pre-commit hooks and GitHub Actions to scan for secrets, API keys, and credentials before they ever reach the repository.
- Tool: `detect-secrets`
- Policy: Zero-tolerance for hardcoded credentials.

### 2. Data Encryption
- **In Transit**: All API communication is forced over TLS/SSL.
- **At Rest**: Sensitive database fields are encrypted using industry-standard algorithms.

### 3. Identity & Access Management (IAM)
- JWT-based authentication for API access.
- Role-based access control (RBAC) to ensure users only see their own guidance results.

### 4. Privacy-First (GDPR)
- Minimal data collection (Data Minimization).
- Automatic data expiration policies.
- Specialized handling for users under 18 (Privacy-by-Default).

### 5. Audit Trails
Every deployment and critical decision in the backend triggers a cryptographic hash generation, stored in an audit log to ensure the integrity of the guidance results.

---
*LUCY — High-Integrity Career Intelligence*
