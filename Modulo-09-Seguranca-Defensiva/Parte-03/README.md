# Módulo 09: Segurança Cibernética Defensiva (Parte 03)

### Objetivo Principal

Conscientizar organizações, analistas e gestores sobre a importância de tratar a segurança defensiva não como algo passivo ou focado apenas em barreiras, mas como uma disciplina estruturada baseada em provas, rastreabilidade e melhoria contínua.

---

## Evidências em Incidentes e o Papel da Perícia

- **Resposta vs. Evidência:** A resposta a incidentes resolve o problema operacionalmente (contém a ameaça), mas a evidência digital explica **o que aconteceu**, **quem** fez, **quando** e **como**.
- **Marcos Regulatórios:** Regulamentações rigorosas como a **LGPD** exigem investigação profunda para comprovar vazamentos de dados pessoais e notificar titulares e autoridades.
- **Técnicas Periciais:** Utilização de logs, imagens de disco, memória RAM e indicadores de comprometimento para comprovar se um endpoint foi comprometido e mapear o escopo do incidente.

---

## Forense Computacional 🔬

**Definição:** Conjunto de técnicas usadas para **identificar**, **preservar**, **coletar**, **examinar**, **analisar** e **apresentar evidências digitais** de forma rigorosa.

**Aplicação do Método Científico:** O perito formula hipóteses, coleta dados para testá-las e chega a conclusões objetivas: **Hipótese Verdadeira**, **Hipótese Falsa** ou **Inconclusiva**.

- **Pilares de Atuação:**
    - **Reconstruir:** Mapear eventos e ações executadas no sistema.
    - **Preservar:** Garantir a integridade absoluta da prova digital.
    - **Apoiar:** Subsidiar investigações e respostas técnicas (ex: identificar a causa-raiz).
    - **Relatar:** Produzir relatórios técnicos compreensíveis para tomadores de decisão e autoridades.

---

## Resposta a Incidentes vs. Forense Computacional

- **Resposta a Incidentes:** Foco em ***conter**, **erradicar** e **recuperar*** o ambiente. Possui prioridade operacional, decisões rápidas sob alta pressão e busca a redução imediata do impacto.
- **Forense Computacional:** Foco em ***preservar**, **examinar** e **explicar***. Possui prioridade probatória e analítica, rigor metodológico estrito e busca a reconstrução detalhada dos fatos.

Embora possuam focos distintos, são complementares e exercidas em paralelo durante crises cibernéticas.

---

## Princípios Fundamentais da Perícia Digital

Para que uma perícia tenha validade técnica e jurídica, deve seguir rigorosamente quatro princípios fundamentais:

1. **Preservação e Integridade:** Os dados coletados não devem ser alterados. (Ex: O simples ato de ligar um celular apreendido pode alterar logs e provas digitais).
2. **Autenticidade:** Garantir que a evidência é exatamente o que se afirma e possui origem verificável (números de série, modelos, hashes).
3. **Rastreabilidade (Cadeia de Custódia):** Documentação rigorosa de todo o ciclo de vida da evidência.
4. **Repetibilidade:** Utilização de métodos verificáveis e reproduzíveis por terceiros sob as mesmas condições.

*  A pergunta não é só *“o que foi encontrado”*. É também “*como foi encontrado”*. ❗

---

## Coleta Forense e Ordem de Volatilidade

**Planejamento de Coleta:** Deve ser planejado com base no caso, risco de alteração e urgência.

**Ordem de Volatilidade:** Classificação dos dados conforme sua persistência:

- **Muito Volátil:** Memória RAM, conexões ativas, processos em execução, sessões ativas (perdidos ao desligar o computador).
- **Volátil:** Tabelas temporárias, cache, arquivos temporários.
- **Menos Volátil:** Logs rotativos, dados de aplicações, imagens de disco e backups (persistem mesmo após o desligamento).


---

## Análise Forense e Linha do Tempo

**Perguntas-Chave da Análise:**

- ***Origem**:* Quando o evento começou? Qual foi o vetor inicial de comprometimento?
- ***Progresso**:* Houve movimentação lateral, exploração de vulnerabilidade ou persistência?
- ***Impacto**:* Quais sistemas e dados foram afetados? Houve exfiltração de dados sensíveis?

**Construção da Linha do Tempo:** Organiza eventos em ordem cronológica estrita usando múltiplas fontes (logs de sistema, EDR, firewall, metadados de arquivos, proxy, nuvem, e-mails). Permite identificar lacunas e testar hipóteses. Uma boa linha do tempo separa **fato**, **hipótese** e **lacuna**.

### Ferramentas Forenses

O ecossistema de ferramentas forenses é amplo. A escolha depende do contexto, mas o método é o que garante a validade das conclusões.

<img width="1518" height="523" alt="image" src="https://github.com/user-attachments/assets/e9f90b32-00b9-4b38-b341-33936c485cac" />


---

## ☁️ Forense em Nuvem e SaaS (Software as a Service)

**Desafios Modernos:** A evidência não está mais restrita ao disco local. Exige tratamento de fusos horários, dependência de APIs de terceiros, permissões e dependência de provedores.

**Escopos de Análise:** Identidade (logs de MFA, autenticação), Infraestrutura (trilhas de auditoria em nuvem, snapshots) e Aplicações SaaS (e-mails corporativos, armazenamento, logs de atividade).

---

## Cadeia de Custódia ⚖️

A cadeia de custódia registra o **percurso completo da evidência** desde o reconhecimento até o descarte. Sem rastreabilidade, a evidência perde força probatória.

<img width="1518" height="577" alt="image" src="https://github.com/user-attachments/assets/dfd50ed4-4559-492b-b061-ae58fc6dcd99" />


---

## Relatório Técnico Forense 📄

Documenta os resultados de uma análise ou investigação forense. Deve ser **tecnicamente preciso** e **compreensível** para seus destinatários, podendo subsidiar investigações, processos administrativos, judiciais ou regulatórios. 

**Estrutura Recomendada (Baseada no NIST SP 800-86):**

- Objetivo e escopo definidos.
- Metodologia aplicada.
- Evidências analisadas e ferramentas utilizadas (incluindo versões).
- Limitações e condicionantes.
- Achados com base factual.
- Linha do tempo reconstituída.
- Conclusões e anexos técnicos.
