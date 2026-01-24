## Introdução

A rápida proliferação dos Grandes Modelos de Linguagem (LLMs) em diversos setores destacou a necessidade crítica de práticas avançadas de segurança de dados. À medida que esses sistemas de IA se tornam mais sofisticados, apresentam riscos sem precedentes, incluindo possíveis violações de informações sensíveis e desafios para cumprir regulamentações rigorosas de proteção de dados. Este white paper descreve um conjunto abrangente de melhores práticas para a segurança de dados em LLMs, projetado para abordar essas vulnerabilidades emergentes e mitigar os riscos associados de forma eficaz.

Esta iniciativa complementa a lista OWASP Top 10 para Aplicações LLM AI 2025, reforçando nosso compromisso contínuo com um ecossistema de IA seguro e responsável. O objetivo deste artigo é informar, educar e fornecer insights sobre a proteção de dados no contexto dos LLMs e suas melhores práticas. Apresentamos uma nova perspectiva com conteúdo adicional feito pela comunidade e para a comunidade. Complementando os outros documentos úteis criados pelo projeto, como o Checklist de Cibersegurança e Governança para LLM, o Centro de Excelência em Segurança GenAI para LLM, o Guia para Preparar e Responder a Eventos de Deepfake, o Guia do Panorama de Soluções de Segurança em IA e o Guia de Red Teaming para GenAI. Redigido e apresentado pela Equipe de Metodologia de Coleta de Dados, este white paper traz uma abordagem rigorosa e metódica para a coleta e análise de dados, garantindo que nossas recomendações sejam práticas e alinhadas com os frameworks globais de segurança.

### Por que a Segurança de Dados é Crítica para LLMs

A segurança dos dados é crítica para Modelos de Linguagem de Grande Porte (LLMs) devido aos riscos significativos e vulnerabilidades associadas ao seu uso e desenvolvimento. Os dados são a “força vital” de todos os LLMs; garantir sua proteção inclui:

#### Protegendo Informações Sensíveis

Os LLMs são frequentemente treinados em grandes conjuntos de dados que podem conter informações sensíveis ou confidenciais. Garantir a segurança dos dados é crucial para:
- Prevenir o acesso não autorizado a dados pessoais, financeiros ou proprietários
- Manter a privacidade e a confiança do usuário
- Cumprir as regulamentações de proteção de dados
  ​
  Implementar criptografia forte, controles de acesso e técnicas de anonimização ajuda a proteger dados sensíveis usados no treinamento e operação de LLM.
  ​
#### Garantindo a Integridade e Confiabilidade dos Dados

Manter a integridade e a confiabilidade dos dados usados por LLMs é essencial para:
- Produzindo resultados precisos e confiáveis
- Prevenindo a disseminação de desinformação ou conteúdo tendencioso
- Garantindo que o desempenho do modelo esteja alinhado com seu propósito previsto
  ​
  Implementar processos de validação de dados e monitoramento contínuo ajuda a detectar e responder a ameaças potenciais que poderiam comprometer a integridade dos dados.
  ​
#### Abordando Preocupações com Privacidade

LLMs levantam preocupações significativas de privacidade devido à sua capacidade de processar e gerar texto semelhante ao humano. Medidas robustas de segurança de dados são necessárias para:
- Proteger as entradas do usuário e evitar a divulgação não autorizada de informações pessoais
- Garantir conformidade com regulamentos de privacidade como o GDPR
- Manter a confiança do usuário em aplicações com tecnologia de IA
  ​
  Adotar tecnologias que aprimoram a privacidade, como privacidade diferencial e aprendizado federado, pode ajudar a proteger a privacidade individual enquanto permite que os LLMs aprendam com insights amplos de dados.
  ​
#### Mitigando Ameaças Emergentes

À medida que os LLMs se tornam mais prevalentes, eles introduzem novos desafios de segurança:
- Ataques sofisticados de phishing utilizando conteúdo gerado por IA
- Manipulação de informações online em larga escala
- Ciberataques automatizados aproveitando as capacidades de LLM
- Desinformação
- Consumo ilimitado
  ​
  A segurança robusta de dados é essencial para LLMs para garantir seu desenvolvimento e implantação responsáveis. Ao implementar estratégias de segurança abrangentes, as organizações podem aproveitar o poder dos LLMs enquanto protegem informações sensíveis e mantêm a confiança dos usuários. Implementar medidas avançadas de segurança e manter-se vigilante contra ameaças em evolução é crucial para proteger os LLMs e seus usuários.
  ​
### Segurança de Dados Tradicional vs. Específica para LLM

![fig1](images/fig1.png)
Fonte:[Rob van der Veer (Software Improvement Group)](https://www.linkedin.com/posts/robvanderveer_ai-aisecurity-activity-7274736168255074304-g9yq?utm_source=share&utm_medium=member_desktop)
##### Figura 1: Impacto, Ativos e Ameaças

#### Medidas Tradicionais de Segurança de Dados

Práticas tradicionais de segurança, como criptografia, controle de acesso, mascaramento de dados e segurança de rede, constituem a camada fundamental para a proteção de dados em Modelos de Linguagem Grandes (LLMs). Esses métodos comprovados garantem uma proteção básica e ajudam a manter a conformidade em qualquer sistema robusto. Por exemplo, a criptografia em repouso (ex.: AES-256) e em trânsito (ex.: TLS 1.3) protege os dados durante o armazenamento e a comunicação, enquanto o controle de acesso baseado em função (RBAC) e a autenticação multifator (MFA) limitam o acesso não autorizado. Técnicas de mascaramento ou anonimização de dados mitigam o risco de divulgação acidental, e auditorias e registros meticulosos fornecem uma trilha de auditoria para solução de problemas ou relatórios de conformidade. Firewalls, VPNs e sistemas de detecção de intrusão fortalecem ainda mais os perímetros de rede para garantir que apenas o tráfego legítimo possa passar. Juntos, esses controles formam a base para a aplicação de protocolos adicionais e mais especializados para os LLMs.

#### Adaptações de Segurança Específicas para LLM

Essas medidas tradicionais necessárias devem ser ampliadas para abordar desafios únicos que surgem ao longo do ciclo de vida da IA. Estruturas de governança e gerenciamento do ciclo de vida do modelo que abrangem controle de versão, capacidades de reversão e conformidade com os padrões corporativos ajudam a monitorar a proveniência dos dados de treinamento e a manter a rastreabilidade. Processos de desenvolvimento seguro e cadeias de suprimentos verificadas minimizam vulnerabilidades introduzidas por bibliotecas externas e scripts personalizados. Avaliações de ameaças, como testes adversariais, análise de inversão de modelo e exercícios de penetração revelam fraquezas do sistema antes que levem a compromissos. Para as operações diárias, protocolos de resposta a incidentes, suportados por monitoramento contínuo e detecção em tempo real de anomalias, são essenciais para o rápido contenção de violações ou eventos de vazamento de dados. Esses controles também se cruzam com considerações legais e éticas mais amplas, incluindo a conformidade com regras de residência de dados e a mitigação de vieses não intencionais.

#### RISCOS E IMPACTOS POTENCIAIS

A lista OWASP Top 10 para Aplicações LLM GenAI 2025, organizada e curada por um grupo de especialistas, apresenta os principais riscos de segurança e os impactos potenciais associados aos Modelos de Linguagem de Grande Porte. Seis dos dez são específicos para a segurança de dados:

RISCO:[LLM01:2025 Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/)
EXPLICAÇÃO: Ator maliciosos podem manipular prompts para alterar o comportamento do modelo, resultando na geração de conteúdo não autorizado ou na execução de ações não intencionais.
ESTATÍSTICAS: Pesquisas mostram que até mesmo defesas sofisticadas como Geração Aumentada por Recuperação (RAG) não previnem totalmente essas vulnerabilidades.

RISCO:[LLM02:2025 Sensitive Information Disclosure](https://genai.owasp.org/llmrisk/llm022025-sensitive-information-disclosure/)
EXPLICAÇÃO: Os LLMs correm o risco de revelar informações pessoais identificáveis (PII), algoritmos proprietários ou dados comerciais confidenciais por meio de sua saída. Por exemplo, dados mal higienizados podem levar a vazamentos não intencionais.
ESTATÍSTICAS: Pesquisas mostram que até mesmo defesas sofisticadas como a Geração Aumentada por Recuperação (RAG) não previnem completamente essas vulnerabilidades.

RISCO:[LLM04:2025 Data and Model Poisoning](https://genai.owasp.org/llmrisk/llm042025-data-and-model-poisoning/)
EXPLICAÇÃO: Os atacantes podem corromper os dados de treinamento ou o próprio modelo, fazendo com que ele gere resultados enganosos ou comprometa sua integridade.
ESTATÍSTICAS: Exemplos adversariais demonstraram uma taxa de sucesso de 35% na influência dos resultados do modelo, mesmo com mecanismos de defesa em vigor.

RISCO:[LLM03:2025 Supply Chain Vulnerabilities](https://genai.owasp.org/llmrisk/llm032025-supply-chain/)
EXPLICAÇÃO: Dependências e bibliotecas inseguras podem introduzir riscos nas implementações de LLM. Atacantes podem comprometer essas fontes externas para obter acesso a modelos e dados.
ESTATÍSTICAS: O ataque “Proof Pudding” (CVE-2019-20634) demonstrou como dados de treinamento divulgados facilitaram a extração do modelo, levando a violações significativas de privacidade e segurança.

RISCO:[LLM05:2025 Improper Output Handling](https://genai.owasp.org/llmrisk/llm052025-improper-output-handling/)
EXPLICAÇÃO: Os LLMs podem inadvertidamente gerar conteúdo prejudicial ou vazar informações sensíveis se suas saídas não forem devidamente validadas e controladas.
ESTATÍSTICAS: Quebras recentes revelaram que respostas não filtradas de LLM contribuíram para incidentes de exposição de dados em 12% dos casos analisados.

RISCO:[LLM07:2025 System Prompt Leakage](https://genai.owasp.org/llmrisk/llm072025-system-prompt-leakage/)
EXPLICAÇÃO: Se os invasores obtiverem acesso aos prompts do sistema, eles podem extrair detalhes sobre a configuração do modelo e explorá-los para ataques adicionais.
ESTATÍSTICAS: Exemplos adversariais demonstraram uma taxa de sucesso de 35% em influenciar resultados de modelos, mesmo com mecanismos de defesa em vigor.

#### IMPACTO MAIS AMPLO

Os riscos de segurança de dados associados aos grandes modelos de linguagem (LLMs) se estendem por várias dimensões, com impactos mais amplos significativos, incluindo:

1.  Desinformação e Manipulação: LLMs podem ser explorados para gerar e disseminar informações falsas ou enganosas, levando a:
- Ataques de engenharia social
- Erosão da confiança em sistemas de IA
- Potenciais impactos sociais
- Armadilhas de link
  ​
2. Excesso de Dependência em Informações Geradas por IA: Confiar nos resultados de LLM sem validação adequada pode resultar em:
- Violação de segurança
- Questões legais
- Dano reputacional
  ​
3. Preocupações Éticas: O uso de LLMs levanta questões sobre:
- Viés na tomada de decisão em IA
- Equidade e discriminação
- Responsabilidade pelo conteúdo gerado por IA
- Transparência
  ​
  A mitigação desses riscos requer que as organizações implementem medidas robustas de segurança, incluindo dados
  anonimização, validação de entrada, sanitização de saída, monitoramento contínuo de sistemas LLM e mais.
  ​
  Além disso, desenvolver diretrizes éticas e manter a supervisão humana em processos críticos de tomada de decisão é crucial para a implantação responsável da IA.
  ​
  Este esforço está alinhado de perto com o projeto mais amplo OWASP LLM e Segurança de IA Generativa, que fornece orientações detalhadas sobre como mitigar esses riscos e estabelecer práticas seguras de desenvolvimento e implantação. O Guia de Segurança e Privacidade de IA da OWASP (Ref.1) oferece uma perspectiva mais ampla e valiosa, abordando privacidade de dados, implicações éticas e desenvolvimento responsável de IA. O OWASP AI Exchange (Ref.2) serve como um repositório central de informações e facilita a colaboração dentro do campo.
  ​
  [Ref.1 - OWASP AI Security and Privacy Guide](https://owasp.org/www-project-ai-security-and-privacy-guide/)
  [Ref.2 - OWASP AI Exchange](https://owaspai.org/)
  ​
  Embora essas iniciativas abordem diretamente a segurança de LLM, os projetos estabelecidos da OWASP oferecem insights valiosos e transferíveis. O OWASP Application Security Verification Standard (ASVS) (Ref.3) fornece uma estrutura para verificar a segurança de aplicações que integram LLMs, enquanto o OWASP Testing Guide e o Web Security Testing Guide (WSTG) (Ref.4) oferecem metodologias aplicáveis a sistemas baseados em LLM.
  ​
  [Ref.3 - OWASP Application Security Verification Standard (ASVS)](https://owasp.org/www-project-application-security-verification-standard/)
  [Ref.4 - OWASP Testing Guide and Web Security Testing Guide (WSTG)](https://owasp.org/www-project-web-security-testing-guide/)
  ​
  ​
  A Série de Cartilhas OWASP (Ref.5) fornece orientações concisas sobre técnicas específicas de segurança, e o Projeto de Modelagem de Ameaças OWASP (Ref.6), juntamente com a ferramenta Threat Dragon (Ref.7), possibilitam uma análise eficaz de ameaças para implementações de LLM.
  ​
  [Ref.5 - OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)
  [Ref.6 - OWASP Threat Modeling Project](https://owasp.org/www-project-threat-model/)
  [Ref.7 - Threat Dragon tool](https://owasp.org/www-project-threat-dragon/)
  ​
  A segurança da cadeia de suprimentos para dependências de LLM pode ser gerenciada usando OWASP Dependency-Check e Dependency-Track (Ref.8). Além disso, a aplicação do OWASP Software Assurance Maturity Model (SAMM) (Ref.9) facilita o desenvolvimento de programas robustos de segurança de software que abrangem os ciclos de vida do LLM, e o OWASP DevSecOps Maturity Model (DSOMM) (Ref.10) apoia a integração da segurança nos aspectos operacionais da infraestrutura do LLM e na gestão de dados.
  ​
  [Ref.8 - OWASP Dependency-Check and Dependency-Track](https://owasp.org/www-project-dependency-track/)
  [Ref.9 - OWASP Software Assurance Maturity Model (SAMM)](https://owasp.org/www-project-samm/)
  [Ref.10 - OWASP DevSecOps Maturity Model (DSOMM)](https://owasp.org/www-project-devsecops-maturity-model/)
  ​
  Os princípios do Guia de Revisão de Código OWASP (Ref.11) são essenciais para examinar o código que interage com LLMs, e o Framework de Conhecimento em Segurança OWASP (SKF) (Ref.12) fornece uma base abrangente de conhecimento em segurança aplicável a diversos domínios de segurança de LLM.
  ​
  [Ref.11 - OWASP Code Review Guide](https://owasp.org/www-project-code-review-guide/)
  [Ref.12 - OWASP Security Knowledge Framework (SKF)](https://www.securityknowledgeframework.org/)
  ​
  Este conjunto abrangente de recursos OWASP é crucial para estabelecer e implementar as melhores práticas eficazes de segurança de dados para LLM.
  ​
  Para mais informações sobre a lista OWASP Top 10 para LLM 2025, visite:[https://genai.owasp.org/llm-top-10/](https://genai.owasp.org/llm-top-10/)

