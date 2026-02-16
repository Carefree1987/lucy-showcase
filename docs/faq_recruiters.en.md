# FAQ for Technical Recruiters

## 1. What is the "Decision Pipeline"?
It's an architectural pattern used to wrap LLM calls in a verifiable execution environment. Instead of trusting the LLM's output blindly, Lucy passes it through multiple "Gates" (Schema validation, Logical consistency, Data-source matching) to ensure reliability.

## 2. Why FastAPI?
FastAPI was chosen for its high performance (Starlette/Pydantic), asynchronous nature, and automatic generation of interactive API documentation (Swagger/Redoc). It allows for rapid development without sacrificing execution speed.

## 3. How do you handle privacy for minors?
Lucy follows a "Privacy-by-Design" approach. For users under 18, all PII (Personally Identifiable Information) is either never collected or stored only in local session state. Matching is performed on anonymized vector profiles.

## 4. How is the matching engine built?
The matching engine uses vector embeddings of user interests and skills, which are compared against the ESCO (European Skills, Competences, Qualifications and Occupations) dataset using cosine similarity. This ensures that career recommendations are mapped to real-world occupational standards.

## 5. What is the CI/CD strategy?
We use GitHub Actions for automated testing (Pytest), linting (Ruff/Black), and security scanning (Secret scanning). Every commit to main/master triggers a full audit trail generation to ensure the code remains production-ready.

---
*Dennis Dittfurth — Full-Stack Developer & System Architect*
