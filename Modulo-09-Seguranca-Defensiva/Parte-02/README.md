# Módulo 09: Segurança Cibernética Defensiva (Parte 01)

### Objetivo Principal

O objetivo é desmistificar a segurança operacional moderna, demonstrando que a implantação de ferramentas avançadas (como SIEM, EDR, SOAR e Inteligência Artificial) é inútil sem uma base sólida de processos estruturados, engenharia de detecção rigorosa, inventário de ativos e estratégias maduras de prevenção, tratamento de incidentes e resiliência (como backups imutáveis e planos de recuperação bem definidos).

---

## O que é um SOC e sua Estrutura Operacional

O **Security Operations Center (SOC)** é definido como o centro nervoso da defesa operacional de uma organização. Ele atua em tempo real para monitorar o ambiente corporativo. Seus pilares básicos dividem-se em:

- **Coleta e Análise:** Ingestão massiva de logs e monitoramento de alertas.
- **Investigação e Classificação:** Análise de incidentes por nível de severidade e acionamento de equipes técnicas.
- **Melhoria Contínua:** Criação de regras de detecção, documentação e refinamento contínuo de processos.

---

## Papéis e Atribuições (Pessoas em um SOC)

A operação de um SOC exige especialização em camadas hierárquicas bem definidas, embora a **decisão final permaneça estritamente humana**:

- **Analista N1:** Realiza a triagem inicial dos eventos para determinar se constituem um incidente real.
- **Analista N2:** Conduz a investigação aprofundada e a correlação de eventos.
- **Analista N3:** Executa análises avançadas e **Threat Hunting** (caça proativa a ameaças).
- **Líder de Resposta a Incidentes:** Coordena a contenção e erradicação.
- **Engenheiro de Detecção e Admin de SIEM:** Desenvolve e gerencia as regras de monitoramento.
- **Especialistas em Inteligência e Forense:** Investigam evidências profundas e o comportamento dos adversários.

---

## Processos Essenciais que Sustentam o SOC

1. **Ingestão** (coleta e normalização de logs de firewalls, endpoints, servidores e bancos de dados).
2. **Triagem** (classificação e priorização).
3. **Investigação** (analisar e escalar incidentes).
4.  **Resposta** (mitigação, revisão e melhoria).

<img width="966" height="493" alt="image" src="https://github.com/user-attachments/assets/26c74f13-4cf6-4a7d-93a1-df1d57aade83" />

---

## O Ecossistema Tecnológico do SOC

As principais tecnologias abordadas e suas funções específicas são:

- **SIEM (Security Information and Event Management):** Plataforma central de coleta, normalização e correlação de logs de múltiplas fontes. Funciona como a base da detecção.
- **EDR / XDR (Endpoint Detection & Response / Extended Detection & Response):** Monitoram estações, notebooks e servidores, detectando comportamentos suspeitos em endpoints (EDR) ou expandindo a correlação para múltiplas camadas como e-mail, identidade e rede (XDR).
- **SOAR (Security Orchestration, Automation and Response):** Automatiza tarefas repetitivas e padroniza respostas a incidentes (enriquecimento de alertas, abertura de tickets, isolamento de ativos).
- **Threat Intelligence:** Coleta e distribui contexto sobre quem pode atacar, quais técnicas usa e quais vulnerabilidades são exploradas.
- **Forense e Sandbox:** Ambientes isolados para execução de malwares e análise profunda de artefatos suspeitos (como arquivos maliciosos, scripts e e-mails de *phishing*).

---

## Engenharia de Detecção e o Framework MITRE ATT&CK

A **Engenharia de Detecção** é o ciclo contínuo de criar, testar e aprimorar regras de segurança baseadas no **MITRE ATT&CK**, que mapeia o **comportamento adversário real,** superando as limitações das assinaturas estáticas tradicionais.

<img width="1545" height="373" alt="image" src="https://github.com/user-attachments/assets/09eb41c2-9b31-46e6-9166-bed1e9f4bcda" />


---

## Métricas de Desempenho do SOC

A eficiência operacional é monitorada por indicadores cruciais:

- **MTTD (Mean Time to Detect):** Tempo médio entre o início da atividade maliciosa e a detecção pelo SOC.
- **MTTR (Mean Time to Respond / Repair):** Tempo entre a detecção e a contenção efetiva do incidente.
- **FP% (Taxa de Falso Positivo):** Percentual de alertas gerados que não representam ameaças reais, cuja alta incidência gera fadiga e exaustão nos analistas.

---

## O Papel e os Cuidados com a Inteligência Artificial

A IA atua como uma poderosa ferramenta de apoio para triagem, enriquecimento de indicadores, correlação e manipulação de grandes volumes de dados. Contudo, exige validação humana rigorosa, controle de qualidade, proteção de dados processados e prevenção contra respostas automáticas indevidas.

<img width="1622" height="494" alt="image" src="https://github.com/user-attachments/assets/bd7d1c42-8e10-46de-912e-8ffa5415b9fe" />


---

## Prevenção de Incidentes

A defesa proativa baseia-se em pilares essenciais:

- **Inventário de Ativos:** *“Você não pode proteger o que não sabe que existe.”*
- **Gestão de Vulnerabilidades:** Identificar, priorizar e corrigir falhas antes da exploração.
- **Hardening:** Configurar sistemas de forma segura desde a origem para eliminar superfícies de ataque desnecessárias.
- **MFA e Controle de Acesso:** Mitigar riscos de credenciais comprometidas.
- **Backup e Proteção de Endpoint:** Garantir recuperação e visibilidade.
- **Treinamento e Gestão de Terceiros:** Reduzir o fator de risco humano.

<img width="1622" height="595" alt="image" src="https://github.com/user-attachments/assets/f160ab3f-d846-4c19-b273-bb554b2c9575" />

---

## Ciclo de Resposta a Incidentes

O **Ciclo de Resposta a Incidentes** é abordado como um fluxo interativo e contínuo composto por 6 fases:

1. **Preparação:** Planos, equipes e playbooks estruturados antes da crise.
2. **Detecção e Análise:** Compreensão inicial do incidente (*"A primeira versão da história quase sempre está incompleta"*).
3. **Contenção:** Limitação imediata dos danos sem destruir evidências (*"Conter não é apagar tudo. É controlar o incêndio sem destruir a cena"*).
4. **Erradicação:** Remoção da causa raiz e eliminação de artefatos de persistência.
5. **Recuperação:** Restauração segura de serviços com validação de integridade (*"Voltar rápido é bom. Voltar inseguro é repetir o problema"*).
6. **Lições Aprendidas:** Revisão pós-incidente para aprimorar controles e documentação.

<img width="1278" height="667" alt="image" src="https://github.com/user-attachments/assets/9b7e384a-9249-4d27-8568-816c4414877f" />


