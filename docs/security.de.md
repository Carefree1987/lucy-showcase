# Sicherheitsmodell & Praktiken

## Security by Design
Sicherheit ist eine Grundvoraussetzung für Lucy, insbesondere angesichts der Sensibilität von Bildungs- und Schülerdaten.

### 1. Secret Scanning
Wir nutzen Pre-Commit-Hooks und GitHub Actions, um nach Secrets, API-Keys und Zugangsdaten zu suchen, bevor diese das Repository erreichen.
- Tool: `detect-secrets`
- Policy: Null-Toleranz für hartkodierte Credentials.

### 2. Datenverschlüsselung
- **In Transit**: Die gesamte API-Kommunikation erfolgt zwingend über TLS/SSL.
- **At Rest**: Sensible Datenbankfelder werden mit industriellen Standardalgorithmen verschlüsselt.

### 3. Identity & Access Management (IAM)
- JWT-basierte Authentifizierung für den API-Zugriff.
- Rollenbasierte Zugriffskontrolle (RBAC), um sicherzustellen, dass Nutzer nur ihre eigenen Beratungsergebnisse einsehen können.

### 4. Privacy-First (DSGVO)
- Minimale Datenerfassung (Datensparsamkeit).
- Automatische Datenlöschungs-Richtlinien.
- Spezialisierte Handhabung für Nutzer unter 18 Jahren (Privacy-by-Default).

### 5. Audit Trails
Jedes Deployment und jede kritische Entscheidung im Backend löst die Generierung eines kryptografischen Hashs aus, der in einem Audit-Log gespeichert wird, um die Integrität der Beratungsergebnisse sicherzustellen.

---
*LUCY — High-Integrity Career Intelligence*
