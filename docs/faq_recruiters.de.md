# FAQ für Technische Recruiter

## 1. Was ist die „Decision Pipeline“?
Es ist ein Architektur-Pattern, um LLM-Aufrufe in eine verifizierbare Ausführungsumgebung einzubetten. Statt dem Output des LLMs blind zu vertrauen, leitet Lucy diesen durch mehrere „Gates“ (Schema-Validierung, logische Konsistenz, Abgleich mit Datenquellen), um Verlässlichkeit zu garantieren.

## 2. Warum FastAPI?
FastAPI wurde aufgrund seiner hohen Performance (Starlette/Pydantic), seiner asynchronen Architektur und der automatischen Generierung interaktiver API-Dokumentation (Swagger/Redoc) gewählt. Es erlaubt schnelle Entwicklung bei maximaler Ausführungsgeschwindigkeit.

## 3. Wie wird der Datenschutz für Minderjährige gehandhabt?
Lucy folgt einem „Privacy-by-Design“-Ansatz. Für Nutzer unter 18 werden personenbezogene Daten (PII) entweder gar nicht erst erhoben oder nur im lokalen Session-State gehalten. Das Matching erfolgt auf anonymisierten Vektor-Profilen.

## 4. Wie ist die Matching-Engine aufgebaut?
Die Matching-Engine nutzt Vektor-Embeddings von Nutzerinteressen und Skills, die mittels Cosine Similarity mit dem ESCO-Datensatz (European Skills, Competences, Qualifications and Occupations) abgeglichen werden. Dies stellt sicher, dass Empfehlungen auf realen Berufsstandards basieren.

## 5. Wie sieht die CI/CD-Strategie aus?
Wir nutzen GitHub Actions für automatisierte Tests (Pytest), Linting (Ruff/Black) und Security-Scanning. Jeder Commit löst die Generierung eines Audit-Trails aus, um die Production-Readiness des Codes sicherzustellen.

---
*Dennis Dittfurth — Full-Stack Developer & System Architect*
