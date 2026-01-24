## Audiência

Este documento aborda três papéis críticos na implantação segura e na gestão da segurança de dados em Grandes Modelos de Linguagem (LLMs):

### 1. Líderes Técnicos de Cibersegurança

#### Funções
Arquitetos de segurança, engenheiros de segurança e equipes SOC
#### Foco
- Adote estratégias de defesa em profundidade (por exemplo, criptografia em camadas, enclaves seguros).
- Aplicar frameworks padrão da indústria (NIST SP 800-53, ISO/IEC
  27001/20547/5338/38507/23894/24028/23053/22989/42001, MITRE ATLAS) e garantir conformidade (GDPR, CCPA, HIPAA, Regulamento Europeu de IA, Plano de Ação de IA).
- Implemente monitoramento robusto (SIEM/XDR) e resposta a incidentes para pipelines de LLM.
  ​
### 2. Desenvolvedores (Engenheiros e Cientistas de Dados)

#### Funções
Engenheiros de ML, desenvolvedores de software e cientistas de dados
#### Foco
- Integre codificação segura e validação de dados nos pipelines de CI/CD.
- Utilize a assinatura de artefatos e registros de modelo verificados (por exemplo, MLflow) para garantir a integridade do modelo.
- Implemente frameworks de testes adversariais e métodos seguros de ingestão de dados.
  ​
### 3. CISOs (Diretores de Segurança da Informação)

#### Funções
Líderes executivos responsáveis pela estratégia de cibersegurança e gerenciamento de riscos
#### Foco
- Alinhar o uso de LLM com o apetite de risco organizacional e mandatos de conformidade.
- Institucionalize modelos de zero-trust e governança robusta de acesso.
- Incentivar a colaboração interfuncional (Jurídico, Privacidade, Conformidade) para políticas holísticas de segurança de IA.

