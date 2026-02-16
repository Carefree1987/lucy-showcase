# Das Proof-System

## Konzept: Forensische Integrität
Lucy generiert für jede wichtige Beratungsentscheidung ein **Proof Pack**. Dies ist ein Zip-Archiv, das Nachweise enthält, dass die Entscheidungslogik korrekt befolgt wurde und der Systemzustand konsistent war.

### Was enthält ein Proof Pack?
1. **Gate Reports**: JSON-Logs, die zeigen, dass alle Validierungs-Gates (Schema, Logik, Daten) bestanden wurden.
2. **System-Status**: Snapshots der Umgebung (z.B. `docker ps`, `pip freeze`).
3. **Audit Trail**: Kryptografische Hashes der genutzten Konfiguration und des Quellcodes.
4. **Manifest**: Eine signierte Integritätsliste aller Dateien im Paket.

## Warum ist das wichtig?
In sensiblen Bereichen wie der Berufsorientierung sind „Black Box“-Entscheidungen inakzeptabel. Das Proof-System sichert:
- **Rechenschaftspflicht (Accountability)**: Wir können belegen, *warum* eine bestimmte Empfehlung ausgesprochen wurde.
- **Reproduzierbarkeit**: Die exakte Entscheidungsumgebung kann später wiederhergestellt werden.
- **Vertrauen**: Nutzer und Stakeholder können die Integrität des Systems prüfen, ohne Einblick in den Quellcode oder private Daten nehmen zu müssen.

---
*LUCY — Automated Career Intelligence*
