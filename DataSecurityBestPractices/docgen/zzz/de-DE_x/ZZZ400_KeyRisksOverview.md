## Übersicht der Haupt-Risiken: Datensicherheit in LLMs

Die rasche Einführung von Large Language Models (LLMs) hat beispiellose Risiken in der Datensicherheit mit sich gebracht. Dieses Whitepaper präsentiert unsere Sichtweise auf Datensicherheit und basiert auf den anderen vom Projekt erstellten Inhalten. Während Organisationen ihre Abhängigkeit von LLMs ausweiten, werden die Herausforderungen beim Schutz sensibler Informationen, der Sicherstellung von Compliance, Datenschutz und der Abwehr sich entwickelnder Bedrohungen immer dringlicher. Dieser Abschnitt untersucht die kritischen Risiken im Zusammenhang mit Daten in LLMs und bietet zukunftsorientierte Lösungen zum Schutz der Datenintegrität und -sicherheit im Jahr 2025.

### 1. Offenlegung sensibler Informationen

LLMs werden auf umfangreichen Datensätzen trainiert, von denen einige unbeabsichtigt sensible oder persönlich identifizierbare Informationen (PII) enthalten können. Selbst bei strenger Datenaufbereitung können Modelle sensible Informationen „memorieren“ und diese in ihren Ausgaben reproduzieren, was erhebliche Risiken darstellt.

#### Hauptsächliche Risiken:
- Datenmemorierung: Speicherung sensibler oder proprietärer Informationen, die zu unbeabsichtigten Offenlegungen während der Inferenz führen können.
- Unsichere Datenausgaben: Schlecht gestaltete Mechanismen zur Ausgabehandhabung können vertrauliche Informationen oder Geschäftsgeheimnisse offenlegen.
#### Auswirkung:
- Nicht-Einhaltung von Datenschutzbestimmungen wie GDPR oder CCPA.
- Rufschädigung durch Datenschutzverletzungen.
- Abbau des Nutzungsvertrauens in KI-Systeme.
#### Minderungsstrategien:
- Anonymisierung: Entfernen Sie direkte Identifikatoren und verwenden Sie fortschrittliche Techniken wie k-Anonymität oder die Generierung synthetischer Daten.
- Differenzielle Privatsphäre: Statistisches Rauschen in Datensätze und Ausgaben einfügen, um sensible Informationen zu verschleiern und gleichzeitig die Nutzbarkeit zu erhalten.
- Ausgabe-Filterung: Implementieren Sie robuste Filter, um potenziell sensible Inhalte zu erkennen und zu entfernen, bevor die Modellausgaben freigegeben werden.
  ​
### 2. Datenverletzungen

LLMs verarbeiten große Datensätze, was sie zu lukrativen Zielen für Cyberkriminelle macht. Verstöße können durch unzureichende Speichersicherheit, schwache Verschlüsselungsmethoden oder Schwachstellen in den Lieferketten entstehen.

#### Hauptsächliche Risiken:
- Sicherheitsfehlkonfiguration: Öffentlich zugängliche Datenspeicherung bietet Angreifern einen Einstiegspunkt.
- Unverschlüsselte Speicherung: Das Versäumnis, ruhende Daten zu sichern, erhöht das Risiko von Diebstahl.
- Schwachstellen in der Lieferkette: Open-Source-Modelle und Abhängigkeiten von Drittanbietern können Einstiegspunkte für Angreifer sein.
#### Auswirkung:
- Verlust von geistigem Eigentum, finanzielle Strafen und betriebliche Störungen.
- Offenlegung sensibler Trainingsdatensätze, die personenbezogene Daten (PII) oder firmeneigene Geschäftsdaten enthalten.
#### Minderungsstrategien:
- Verschlüsselung: Verschlüsseln Sie Daten im Ruhezustand und während der Übertragung mit robusten Algorithmen wie AES-256 und TLS 1.3.
- Zero-Trust-Architektur: Beschränken Sie den Datenzugriff ausschließlich auf authentifizierte und autorisierte Benutzer.
- Lieferkettensicherheit: Führen Sie regelmäßige Audits von Drittanbieterkomponenten durch und verwenden Sie Werkzeuge, um Schwachstellen in Open-Source-Abhängigkeiten zu überwachen.
  ​
### 3. Daten- und Modellvergiftung

Angreifer können bösartige Daten in Trainingspipelines einschleusen, wodurch die Integrität von LLMs gefährdet wird. Poisoning-Angriffe zielen darauf ab, das Modellverhalten zu verzerren oder Schwachstellen einzuführen, die später ausgenutzt werden können.

#### Hauptsächliche Risiken:
- Beschädigung der Trainingsdaten: Einfügen irreführender Daten, die die Modellausgaben beeinflussen.
- Versteckte Hintertüren: Auslösephrasen, die in das Modell eingebettet sind, um spezifische Antworten hervorzurufen.
#### Auswirkung:
- Voreingenommene oder schädliche Inhaltserstellung, die das Vertrauen der Nutzer beeinträchtigt.
- Sicherheitslücken in nachgelagerten Anwendungen, die auf dem Modell basieren.
#### Minderungsstrategien:
- Datenvalidierung und -bereinigung: Etablieren Sie automatisierte Pipelines, um Anomalien in Trainingsdaten zu erkennen und zu entfernen.
- Adversariales Training: Einschluss von adversarialen Beispielen während des Trainings, um die Modellresilienz aufzubauen.
- Verhaltensüberwachung: Kontinuierliche Analyse der Modellausgaben auf unerwartete Muster oder Verhaltensweisen, die auf eine Vergiftung hinweisen könnten.
  ​
### 4. Unautorisierter Zugriff und Modell Diebstahl

Ohne robuste Zugriffskontrollen sind LLMs anfällig für Diebstahl und unbefugte Nutzung. Böswillige Akteure könnten versuchen, proprietäre Modelle durch umfangreiche API-Interaktionen zu klonen oder geistiges Eigentum zu stehlen.

#### Hauptsächliche Risiken:
- API-Ausnutzung: Angreifer manipulieren APIs, um vertrauliche Ausgaben zu extrahieren oder Systeme mit Anfragen zu überlasten.
- Modellauswertung: Mit Black-Box-Techniken replizieren Angreifer das Verhalten von LLMs und erzeugen nahezu identische Klone.
#### Auswirkung:
- Verlust des Wettbewerbsvorteils und der Umsatzerlöse.
- Erstellung unregulierter, potenziell schädlicher Klone, die Schwachstellen von LLM ausnutzen.
#### Minderungsstrategien:
- Zugangskontrollen: Erzwingen Sie Multi-Faktor-Authentifizierung (MFA), rollenbasierte Zugriffskontrollen (RBAC) und fein abgestufte Berechtigungen.
- Begrenzung der Anfragerate: Beschränken Sie die Häufigkeit und das Volumen von API-Aufrufen, um Extraktionsversuche zu verhindern.
- Wasserzeichen: Identifikatoren in Modelle einbetten, um eine unautorisierte Verbreitung des Modells nachzuvollziehen; andernfalls bieten die Identifikatoren nur eine begrenzte Abschwächung gegen Bedrohungen.
  ​
### 5. Adversarielle Angriffe

Feindliche Eingaben können Schwachstellen im Modell ausnutzen, was zu schädlichen Ausgaben oder der Extraktion sensibler Daten führt. Zu diesen Angriffen gehören Prompt-Injektion, Datenumkehr und Ausgabe-Manipulation.
![fig2](images/fig2.png)
[https://www.labellerr.com/blog/what-are-adversarial-attacks-in-machine-learning-and-how-can-you-prevent-them/](https://www.labellerr.com/blog/what-are-adversarial-attacks-in-machine-learning-and-how-can-you-prevent-them/)
##### Abbildung 2: Angriffe im Bereich des Machine Learning und präventive Maßnahmen

#### Hauptsächliche Risiken:
- Prompt-Injektion: Eingaben erstellen, die Schutzmechanismen umgehen, um Informationen zu extrahieren oder das Verhalten zu manipulieren.
- Modellinversion: Rekonstruktion sensibler Trainingsdaten durch Analyse der Modellausgaben.
- Ausgabemanipulation: Erzeugung von schädlichen oder unbeabsichtigten Inhalten.
#### Auswirkung:
- Offenlegung privater Informationen, die in Trainingsdaten eingebettet sind.
- Verstärkung von Fehlinformationen oder bösartigem Verhalten in nachgelagerten Anwendungen.
#### Minderungsstrategien:
- Eingabevalidierung: Verwenden Sie robuste Sanitierungsmethoden, um bösartige Eingaben zu filtern.
- Adversarisches Training: Trainieren Sie LLMs mit adversarialen Beispielen, um die Robustheit zu verbessern.
- Ausgabemonitoring: Verwenden Sie automatisierte Systeme, um schädliche oder unangemessene Ausgaben zu erkennen und zu blockieren.
  ​
### 6. Zukünftige Überlegungen zur Datensicherheit

#### Entstehende Herausforderungen

Da sich LLMs immer stärker in kritische Operationen integrieren, treten neue Herausforderungen auf:
- Datenschutzrisiken: Die verstärkte Abhängigkeit von Nutzerinteraktionen erhöht die Exponierung gegenüber sensiblen Informationen.
- Dynamische Bedrohungslandschaft: Angreifer innovieren kontinuierlich und nutzen sowohl bekannte als auch unvorhergesehene Schwachstellen aus.
- KI-Agenten und Multi-Agenten-Systeme: Komplexe Systeme aus Planung, Schlussfolgerung und anschließenden Handlungen, die die Angriffsfläche erheblich vergrößern.
  ​
#### Zukunftsorientierte Lösungen

- Datenschutzfördernde Technologien (PETs): Föderiertes Lernen, sichere Multi-Party-Berechnung und homomorphe Verschlüsselung werden eine entscheidende Rolle bei der Sicherung sensibler Daten spielen.
- KI-Governance-Rahmenwerke: Etablieren Sie klare Richtlinien für den ethischen Einsatz von KI und gewährleisten Sie die Übereinstimmung mit globalen Standards und Vorschriften.
- Kontinuierliche Überwachung und Aktualisierungen: Regelmäßige Überprüfung und Aktualisierung der Sicherheitsmaßnahmen zur Bewältigung sich entwickelnder Bedrohungen.

