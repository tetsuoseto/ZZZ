## Einführung

Die rasche Verbreitung von Large Language Models (LLMs) in verschiedenen Branchen hat den dringenden Bedarf an fortschrittlichen Datensicherheitspraktiken hervorgehoben. Da diese KI-Systeme immer komplexer werden, bringen sie beispiellose Risiken mit sich, einschließlich möglicher Verstöße gegen sensible Informationen und Schwierigkeiten bei der Einhaltung strenger Datenschutzvorschriften. Dieses Whitepaper skizziert eine umfassende Reihe von Best Practices für die Datensicherheit von LLMs, die darauf ausgelegt sind, diese neuen Schwachstellen anzugehen und die damit verbundenen Risiken effektiv zu mindern.

Diese Initiative ergänzt die OWASP Top 10 für LLM AI-Anwendungen 2025 und unterstreicht unser fortwährendes Engagement für ein sicheres und verantwortungsbewusstes KI-Ökosystem. Ziel dieses Papiers ist es, zu informieren, aufzuklären und Einblicke in den Schutz von Daten im Kontext von LLMs sowie deren Best Practices zu geben. Wir bringen eine neue Perspektive mit zusätzlichem, von der Community erstelltem Inhalt. Ergänzend zu anderen nützlichen Dokumenten des Projekts, wie der LLM-Cybersicherheits- und Governance-Checkliste, dem LLM GenAI Security Center of Excellence, dem Leitfaden zur Vorbereitung auf und Reaktion bei Deepfake-Ereignissen, dem AI Security Solution Landscape Guide und dem GenAI Red Teaming Guide. Verfasst und präsentiert vom Data Gathering Methodology Team, bringt dieses Whitepaper einen rigorosen und methodischen Ansatz zur Datenerhebung und -analyse ein, wodurch sichergestellt wird, dass unsere Empfehlungen sowohl praxisnah als auch mit globalen Sicherheitsrahmenwerken abgestimmt sind.

### Warum Datensicherheit für LLMs kritisch ist

Datensicherheit ist für Large Language Models (LLMs) aufgrund der erheblichen Risiken und Verwundbarkeiten, die mit ihrer Nutzung und Entwicklung verbunden sind, von entscheidender Bedeutung. Daten sind das „Lebenselixier“ aller LLMs; deren Schutz umfasst:

#### Schutz sensibler Informationen

LLMs werden häufig auf umfangreichen Datensätzen trainiert, die sensible oder vertrauliche Informationen enthalten können. Die Gewährleistung der Datensicherheit ist entscheidend, um:
- Verhindern Sie unbefugten Zugriff auf persönliche, finanzielle oder proprietäre Daten
- Wahren Sie die Privatsphäre und das Vertrauen der Benutzer
- Einhaltung der Datenschutzbestimmungen
  ​
  Die Implementierung starker Verschlüsselung, Zugriffskontrollen und Anonymisierungstechniken trägt dazu bei, sensible Daten, die beim Training und Betrieb von großen Sprachmodellen (LLM) verwendet werden, zu schützen.
  ​
#### Sicherstellung der Datenintegrität und Zuverlässigkeit

Die Wahrung der Integrität und Zuverlässigkeit der von LLMs verwendeten Daten ist entscheidend für:
- Erzeugung genauer und vertrauenswürdiger Ergebnisse
- Verhinderung der Verbreitung von Fehlinformationen oder voreingenommenen Inhalten
- Sicherstellung, dass die Leistung des Modells mit seinem beabsichtigten Zweck übereinstimmt
  ​
  Die Implementierung von Datenvalidierungsprozessen und kontinuierlicher Überwachung hilft dabei, potenzielle Bedrohungen zu erkennen und darauf zu reagieren, die die Datenintegrität gefährden könnten.
  ​
#### Ansprechen von Datenschutzbedenken

LLMs werfen erhebliche Datenschutzbedenken auf aufgrund ihrer Fähigkeit, menschenähnlichen Text zu verarbeiten und zu generieren. Robuste Datensicherheitsmaßnahmen sind notwendig, um:
- Schützen Sie Benutzereingaben und verhindern Sie unbefugte Offenlegung persönlicher Informationen
- Sicherstellung der Einhaltung von Datenschutzvorschriften wie der DSGVO
- Das Vertrauen der Nutzer in KI-gestützte Anwendungen bewahren
  ​
  Die Einführung von datenschutzfördernden Technologien wie Differential Privacy und föderiertem Lernen kann dazu beitragen, die Privatsphäre Einzelner zu schützen und gleichzeitig LLMs das Lernen aus umfangreichen Dateninsichten zu ermöglichen.
  ​
#### Abmilderung aufkommender Bedrohungen

Da Large Language Models (LLMs) immer verbreiteter werden, bringen sie neue Sicherheitsherausforderungen mit sich:
- Ausgeklügelte Phishing-Angriffe unter Verwendung von KI-generiertem Inhalt
- Manipulation von Online-Informationen im großen Maßstab
- Automatisierte Cyberangriffe unter Nutzung von LLM-Fähigkeiten
- Fehlinformation
- Unbegrenzter Verbrauch
  ​
  Robuste Datensicherheit ist für LLMs unerlässlich, um deren verantwortungsvolle Entwicklung und Einsatz zu gewährleisten. Durch die Umsetzung umfassender Sicherheitsstrategien können Organisationen die Leistung von LLMs nutzen und gleichzeitig sensible Informationen schützen und das Vertrauen der Nutzer erhalten. Die Implementierung fortschrittlicher Sicherheitsmaßnahmen und die Wachsamkeit gegenüber sich entwickelnden Bedrohungen sind entscheidend, um LLMs und deren Nutzer zu schützen.
  ​
### Traditionelle vs. LLM-spezifische Datensicherheit

![fig1](images/fig1.png)
Quelle:[Rob van der Veer (Software Improvement Group)](https://www.linkedin.com/posts/robvanderveer_ai-aisecurity-activity-7274736168255074304-g9yq?utm_source=share&utm_medium=member_desktop)
##### Abbildung 1: Auswirkungen, Vermögenswerte und Bedrohungen

#### Traditionelle Datensicherheitsmaßnahmen

Traditionelle Sicherheitspraktiken wie Verschlüsselung, Zugangskontrolle, Datenmaskierung und Netzwerksicherheit bilden die Grundlage zum Schutz von Daten in Large Language Models (LLMs). Diese bewährten Methoden gewährleisten einen Basis-Schutz und helfen, die Einhaltung von Vorschriften in jedem robusten System sicherzustellen. Beispielsweise schützt die Verschlüsselung im Ruhezustand (z. B. AES-256) und während der Übertragung (z. B. TLS 1.3) Daten bei der Speicherung und Kommunikation, während rollenbasierte Zugangskontrolle (RBAC) und Multi-Faktor-Authentifizierung (MFA) unbefugten Zutritt einschränken. Datenmaskierung oder Anonymisierungstechniken mindern das Risiko versehentlicher Offenlegung, und sorgfältige Prüfungen sowie Protokollierungen liefern eine Prüfspur für Fehlerbehebung oder Compliance-Berichte. Firewalls, VPNs und Einbruchserkennungssysteme stärken zudem die Netzwerkgrenzen, um sicherzustellen, dass nur legitimer Datenverkehr passieren kann. Zusammen bilden diese Kontrollen das Fundament für die Anwendung zusätzlicher, spezialisierter Protokolle für LLMs.

#### LLM-spezifische Sicherheitsanpassungen

Diese traditionellen notwendigen Maßnahmen müssen erweitert werden, um die einzigartigen Herausforderungen zu bewältigen, die im gesamten KI-Lebenszyklus auftreten. Management des Modelllebenszyklus und Governance-Rahmenwerke, die Versionskontrolle, Rückrollmöglichkeiten und die Einhaltung von Unternehmensstandards umfassen, helfen dabei, die Herkunft der Trainingsdaten zu überwachen und Nachvollziehbarkeit sicherzustellen. Sichere Entwicklungsprozesse und verifizierte Lieferketten minimieren Schwachstellen, die durch externe Bibliotheken und benutzerdefinierte Skripte eingeführt werden. Bedrohungsbewertungen wie adversariales Testen, Modellinversionsanalyse und Penetrationstests decken Systemschwächen auf, bevor diese zu Kompromittierungen führen. Für den täglichen Betrieb sind Vorfallreaktionsprotokolle, unterstützt durch kontinuierliche Überwachung und Echtzeit-Anomalieerkennung, entscheidend für die schnelle Eindämmung von Sicherheitsvorfällen oder Datenlecks. Diese Kontrollen überschneiden sich zudem mit breiteren rechtlichen und ethischen Aspekten, einschließlich der Einhaltung von Datenresidenzvorschriften und der Minderung unbeabsichtigter Verzerrungen.

#### POTENZIELLE RISIKEN & AUSWIRKUNGEN

Die OWASP Top 10 für LLM GenAI-Anwendungen 2025 Liste, organisiert und kuratiert von einer Gruppe von Experten, präsentiert die wichtigsten Sicherheitsrisiken und die potenziellen Auswirkungen im Zusammenhang mit Large Language Models. Sechs von zehn sind spezifisch für Datensicherheit:

RISIKO:[LLM01:2025 Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/)
ERKLÄRUNG: Böswillige Akteure können Eingabeaufforderungen manipulieren, um das Verhalten des Modells zu verändern, was zur Erzeugung unerlaubter Inhalte oder zur Durchführung ungewollter Aktionen führt.
STATISTIK: Forschungen zeigen, dass selbst ausgefeilte Abwehrmechanismen wie Retrieval Augmented Generation (RAG) diese Schwachstellen nicht vollständig verhindern.

RISIKO:[LLM02:2025 Sensitive Information Disclosure](https://genai.owasp.org/llmrisk/llm022025-sensitive-information-disclosure/)
ERLÄUTERUNG: LLMs laufen Gefahr, persönlich identifizierbare Informationen (PII), proprietäre Algorithmen oder vertrauliche Geschäftsdaten durch ihre Ausgabe preiszugeben. Beispielsweise können schlecht bereinigte Daten zu unbeabsichtigten Lecks führen.
STATISTIK: Untersuchungen zeigen, dass selbst ausgeklügelte Abwehrmechanismen wie Retrieval Augmented Generation (RAG) diese Schwachstellen nicht vollständig verhindern.

RISIKO:[LLM04:2025 Data and Model Poisoning](https://genai.owasp.org/llmrisk/llm042025-data-and-model-poisoning/)
ERKLÄRUNG: Angreifer können Trainingsdaten oder das Modell selbst manipulieren, was dazu führen kann, dass irreführende Ausgaben erzeugt werden oder die Integrität des Modells beeinträchtigt wird.
STATISTIK: Adversariale Beispiele haben gezeigt, dass sie eine Erfolgsrate von 35 % bei der Beeinflussung von Modellausgaben erzielen, selbst wenn Abwehrmechanismen vorhanden sind.

RISIKO:[LLM03:2025 Supply Chain Vulnerabilities](https://genai.owasp.org/llmrisk/llm032025-supply-chain/)
ERKLÄRUNG: Unsichere Abhängigkeiten und Bibliotheken können Risiken in LLM-Implementierungen einführen. Angreifer können diese externen Quellen kompromittieren, um Zugriff auf Modelle und Daten zu erhalten.
STATISTIK: Der „Proof Pudding“-Angriff (CVE-2019-20634) zeigte, wie offengelegte Trainingsdaten die Modellauslagerung erleichterten, was zu erheblichen Verletzungen der Privatsphäre und Sicherheit führte.

RISIKO:[LLM05:2025 Improper Output Handling](https://genai.owasp.org/llmrisk/llm052025-improper-output-handling/)
ERKLÄRUNG: LLMs können unbeabsichtigt schädliche Inhalte erzeugen oder sensible Informationen preisgeben, wenn ihre Ausgaben nicht ordnungsgemäß validiert und kontrolliert werden.
STATISTIK: Jüngste Sicherheitsverletzungen zeigten, dass ungefilterte LLM-Antworten in 12 % der analysierten Fälle zu Datenexpositionsvorfällen beitrugen.

RISIKO:[LLM07:2025 System Prompt Leakage](https://genai.owasp.org/llmrisk/llm072025-system-prompt-leakage/)
ERKLÄRUNG: Wenn Angreifer Zugang zu Systemaufforderungen erhalten, können sie Details zur Konfiguration des Modells extrahieren und diese für weitere Angriffe ausnutzen.
STATISTIK: Adversariale Beispiele haben eine Erfolgsrate von 35 % bei der Beeinflussung der Modellausgaben gezeigt, selbst wenn Abwehrmechanismen vorhanden sind.

#### BREITERER EINFLUSS

Datenrisiken im Zusammenhang mit großen Sprachmodellen (LLMs) erstrecken sich über mehrere Dimensionen und haben bedeutende weitreichende Auswirkungen, darunter:

1.  Fehlinformationen und Manipulation: LLMs können ausgenutzt werden, um falsche oder irreführende Informationen zu erzeugen und zu verbreiten, was zu Folgendem führen kann:
- Social-Engineering-Angriffe
- Vertrauensverlust in KI-Systeme
- Potenzielle gesellschaftliche Auswirkungen
- Link-Fallen
  ​
2. Übermäßige Abhängigkeit von KI-generierten Informationen: Das Vertrauen auf LLM-Ergebnisse ohne angemessene Validierung kann zu folgendem führen:
- Sicherheitsverletzungen
- Rechtliche Fragen
- Reputationsschäden
  ​
3. Ethische Bedenken: Der Einsatz von LLMs wirft Fragen auf bezüglich:
- Vorurteile in der KI-Entscheidungsfindung
- Fairness und Diskriminierung
- Verantwortlichkeit für KI-generierte Inhalte
- Transparenz
  ​
  Die Minderung dieser Risiken erfordert von Organisationen die Umsetzung robuster Sicherheitsmaßnahmen, einschließlich Daten
  Anonymisierung, Eingabevalidierung, Ausgabe-Säuberung, kontinuierliche Überwachung von LLM-Systemen und mehr.
  ​
  Darüber hinaus ist die Entwicklung ethischer Richtlinien und die Aufrechterhaltung menschlicher Aufsicht bei kritischen Entscheidungsprozessen entscheidend für den verantwortungsvollen Einsatz von KI.
  ​
  Diese Bemühung steht in engem Zusammenhang mit dem umfassenderen OWASP LLM- und Generative AI-Sicherheitsprojekt, das fundierte Anleitungen zur Minderung dieser Risiken und zur Etablierung sicherer Entwicklungs- und Bereitstellungspraktiken bietet. Der OWASP AI Security and Privacy Guide (Ref.1) bietet eine wertvolle übergeordnete Perspektive, die Datenschutz, ethische Implikationen und verantwortungsbewusste KI-Entwicklung behandelt. Der OWASP AI Exchange (Ref.2) dient als zentrales Repository für Informationen und fördert die Zusammenarbeit in diesem Bereich.
  ​
  [Ref.1 - OWASP AI Security and Privacy Guide](https://owasp.org/www-project-ai-security-and-privacy-guide/)
  [Ref.2 - OWASP AI Exchange](https://owaspai.org/)
  ​
  Während diese Initiativen direkt die Sicherheit von LLMs angehen, bieten etablierte OWASP-Projekte wertvolle, übertragbare Erkenntnisse. Der OWASP Application Security Verification Standard (ASVS) (Ref.3) stellt einen Rahmen zur Überprüfung der Sicherheit von Anwendungen bereit, die LLMs integrieren, während der OWASP Testing Guide und Web Security Testing Guide (WSTG) (Ref.4) Methoden bereitstellt, die auf LLM-basierte Systeme anwendbar sind.
  ​
  [Ref.3 - OWASP Application Security Verification Standard (ASVS)](https://owasp.org/www-project-application-security-verification-standard/)
  [Ref.4 - OWASP Testing Guide and Web Security Testing Guide (WSTG)](https://owasp.org/www-project-web-security-testing-guide/)
  ​
  ​
  Die OWASP Cheat Sheet Series (Ref.5) bietet prägnante Anleitungen zu spezifischen Sicherheitstechniken, und das OWASP Threat Modeling Project (Ref.6) zusammen mit dem Threat Dragon-Tool (Ref.7) ermöglichen eine effektive Bedrohungsanalyse für den Einsatz von LLM.
  ​
  [Ref.5 - OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)
  [Ref.6 - OWASP Threat Modeling Project](https://owasp.org/www-project-threat-model/)
  [Ref.7 - Threat Dragon tool](https://owasp.org/www-project-threat-dragon/)
  ​
  Die Sicherheit der Lieferkette für LLM-Abhängigkeiten kann mit OWASP Dependency-Check und Dependency-Track (Ref.8) verwaltet werden. Darüber hinaus erleichtert die Anwendung des OWASP Software Assurance Maturity Model (SAMM) (Ref.9) die Entwicklung robuster Software-Sicherheitsprogramme, die den gesamten LLM-Lebenszyklus umfassen, und das OWASP DevSecOps Maturity Model (DSOMM) (Ref.10) unterstützt die Integration von Sicherheit in die betrieblichen Aspekte der LLM-Infrastruktur und Datenverwaltung.
  ​
  [Ref.8 - OWASP Dependency-Check and Dependency-Track](https://owasp.org/www-project-dependency-track/)
  [Ref.9 - OWASP Software Assurance Maturity Model (SAMM)](https://owasp.org/www-project-samm/)
  [Ref.10 - OWASP DevSecOps Maturity Model (DSOMM)](https://owasp.org/www-project-devsecops-maturity-model/)
  ​
  Prinzipien aus dem OWASP Code Review Guide (Ref.11) sind unerlässlich für die Überprüfung von Code, der mit LLMs interagiert, und der OWASP Security Knowledge Framework (SKF) (Ref.12) bietet eine breite Grundlage sicherheitsrelevanten Wissens, das in verschiedenen Sicherheitsbereichen von LLMs anwendbar ist.
  ​
  [Ref.11 - OWASP Code Review Guide](https://owasp.org/www-project-code-review-guide/)
  [Ref.12 - OWASP Security Knowledge Framework (SKF)](https://www.securityknowledgeframework.org/)
  ​
  Dieses umfassende Set von OWASP-Ressourcen ist entscheidend für die Etablierung und Umsetzung effektiver Best Practices zur Datensicherheit von LLM.
  ​
  Für weitere Informationen zur OWASP Top 10 für LLM 2025-Liste besuchen Sie:[https://genai.owasp.org/llm-top-10/](https://genai.owasp.org/llm-top-10/)

