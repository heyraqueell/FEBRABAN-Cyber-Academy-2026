# Aula 2: Pilares da Segurança da Informação

### Objetivo Principal
Compreender os pilares fundamentais da segurança da informação, os diferentes estados dos dados ao longo de seu ciclo de vida, os conceitos essenciais de gestão de riscos e os frameworks normativos utilizados internacionalmente.

---

## 🏛️ Propriedades da Segurança da Informação

A base da segurança fundamenta-se em três pilares essenciais:

*   **Confidencialidade:** Propriedade pela qual se assegura que a informação não esteja disponível ou não seja revelada à pessoa, ao sistema, ao órgão ou à entidade não autorizados nem credenciados (Manter seguro e sob sigilo).
*   **Integridade:** Propriedade pela qual se assegura que a informação não foi modificada ou destruída de maneira não autorizada ou acidental (Garantir que nada foi alterado ou corrompido).
*   **Disponibilidade:** Propriedade pela qual se assegura que a informação esteja acessível e utilizável, sob demanda, por uma pessoa física ou determinado sistema, órgão ou entidade devidamente autorizados (Estar disponível quando necessário).

<p align="center">
  <img width="806" height="526" alt="Tríade CIA" src="https://github.com/user-attachments/assets/b0b02d21-12df-4b98-bcc8-a97b93704d37" />
</p>

### 🔑 Analogia do Cofre
*   **Confidencialidade:** Só você tem a chave do cofre.
*   **Integridade:** O conteúdo do cofre está intacto.
*   **Disponibilidade:** Você consegue abrir o cofre sempre que precisa.

---

## 🔄 Estados da Informação

A proteção deve cobrir a informação em seus três estados básicos dentro do ciclo de vida dos dados:

### 1. Em Repouso (Armazenada)
Dados guardados de forma estática em mídias físicas ou digitais.
*   *Exemplos:* Arquivos salvos no computador pessoal (como PDFs ou planilhas) e bancos de dados corporativos armazenados em servidores.
*   *Proteção típica:* Criptografia em discos ou em bancos de dados, controle de acesso físico e lógico.

### 2. Em Trânsito (Trafegando)
Dados que estão sendo transmitidos entre dois pontos através de uma rede.
*   *Exemplos:* O ato de enviar um e-mail ou o tráfego de credenciais de usuário e senha ao submeter um formulário em um site protegido por HTTPS.
*   *Proteção típica:* Criptografia de comunicação utilizando protocolos de rede como TLS/SSL (Transport Layer Security / Secure Sockets Layer).

### 3. Em Uso (Sendo Processada)
Dados que estão sendo ativamente manipulados pelos sistemas.
*   *Exemplos:* A validação de uma senha na memória no momento do login ou a edição em tempo real de um documento carregado na memória RAM.
*   *Proteção típica:* Controle de acesso à memória, execução segura e ferramentas de DLP (Data Loss Prevention).

---

## 📐 Cubo da Segurança de McCumber

Desenvolvido em 1991 por John McCumber, este modelo conceitual estabelece que a proteção da informação depende do equilíbrio entre três fatores críticos:

*   **Pessoas (O elemento humano):** Os usuários continuam operando os sistemas. Se um indivíduo cai em um golpe, compartilha credenciais ou deixa terminais desbloqueados, a segurança técnica falha. O treinamento e a conscientização moldam o comportamento seguro.
*   **Tecnologias (As ferramentas de proteção):** Sistemas e equipamentos aplicados para a salvaguarda dos dados, como antivírus, firewalls, mecanismos de autenticação de dois fatores e rotinas de backup. Devem ser constantemente atualizados e configurados.
*   **Processos (As regras do jogo):** Rotinas, políticas e normas que padronizam as ações seguras na organização, eliminando adivinhações. Exemplos incluem políticas de senhas fortes e regras para o bloqueio de estações de trabalho ao se afastar da mesa.

<p align="center">
  <img width="1029" height="515" alt="Cubo de McCumber" src="https://github.com/user-attachments/assets/a643b2bd-c68a-4642-8419-e6e5e94a9afb" />
</p>

---

## 📜 Políticas e Normas (ISO)

O sistema de gestão de segurança da informação (SGSI) preserva a confidencialidade, integridade e disponibilidade através de processos de gestão de riscos. A padronização internacional utiliza duas normas principais:

*   **ISO 27001:** Fornece um guia estruturado focado em riscos que dita o que a organização precisa fazer para proteger seus dados.
*   **ISO 27002:** Funciona como um guia de referência que detalha as boas práticas e diretrizes de como implementar os controles descritos na ISO 27001.

> 🔒 **Nota sobre a sigla:** ISO significa Organização Internacional de Padronização (International Organization for Standardization). A ISO 27001 define o que fazer; a ISO 27002 orienta como fazer.

---

## 📊 Matriz de Relações de Segurança

| Ameaças (Threats) | Vulnerabilidades | Riscos (Risks) |
| :--- | :--- | :--- |
| Hackers / Insiders | Falhas na Infraestrutura de Rede | Perda de Vidas |
| Funcionários Insatisfeitos | Brechas no Sistema Operacional | Fraudes Financeiras |
| Crime Organizado / Competidores | Fragilidades em Aplicações Web | Vazamento de Dados |
| Governos / Estados (APTs) | Vulnerabilidades em Bancos de Dados | Extorsão |
| Engenharia Social | Equipamentos de segurança desatualizados (CVE) | Roubo de informações valiosas |
| - | - | Descrédito de imagem e perda de confiança |

---

## 📖 Glossário Técnico Expandido

*   **Segurança da Informação:** Ações que objetivam viabilizar e assegurar a disponibilidade, integridade, confidencialidade e autenticidade das informações, independentemente do formato ou meio (digital, físico ou verbal).
*   **Segurança Cibernética:** Subconjunto da segurança da informação focado estritamente nas operações e ativos digitais, visando garantir que sistemas conectados resistam a eventos no espaço cibernético.
*   **Vulnerabilidade:** Fraqueza em procedimentos de segurança, hardware, design, implementação ou controles internos de um sistema que pode ser explorada por agentes de ameaças.
*   **Exploit:** Técnica, código, programa ou sequência de comandos criada especificamente para tirar proveito de uma vulnerabilidade.
*   **Threat (Ameaça):** Qualquer circunstância ou evento com potencial para impactar negativamente as operações através de acesso não autorizado, destruction, modificação ou negação de serviço.
*   **Risk (Risco):** O potencial para um resultado indesejado determinado pela probabilidade de uma ameaça explorar uma vulnerabilidade e causar impactos associados.
*   **Hacker:** Indivíduo com profundo conhecimento em computadores, redes e sistemas que explora falhas. Pode atuar de maneira ética e autorizada ou de forma maliciosa.
*   **Threat Agent / Actor (Adversary):** Indivíduo, grupo, organização ou governo que conduz ou intenciona conduzir atividades maliciosas motivadas por fatores financeiros, ideológicos ou políticos.
*   **APT (Advanced Persistent Threat):** Adversário altamente qualificado e com recursos significativos que executa ataques coordenados de longo prazo, conseguindo se estabelecer na rede alvo por muito tempo sem detecção. Pode explorar vulnerabilidades 0-day (falhas desconhecidas pelos fabricantes).
*   **Evento:** Qualquer atividade rastreável dentro de um sistema ou rede que seja relevante para a segurança, indicando potenciais comportamentos suspeitos.
*   **Incidente (ITIL v4):** Evento não planejado que causa interrupção ou redução na qualidade de um serviço de TI, comprometendo as operações normais do negócio.
*   **Incidente Cibernético:** Ocorrência que compromete de forma real ou potencial as propriedades de segurança de um sistema de informação ou dos dados por ele processados.
*   **SIM Swap:** Fraude baseada no desvio de chamadas e mensagens onde o criminoso transfere o número telefônico da vítima para um chip sob seu controle por meio de engenharia social com a operadora.
*   **Malware:** Termo genérico para códigos maliciosos desenhados para infiltrar e comprometer ativos de hardware e software.
*   **Ransomware:** Categoria de malware que restringe o acesso a arquivos através de criptografia forçada, exigindo transações financeiras para a disponibilização da chave de decodificação.

---

## 📉 Gestão de Riscos

O risco representa a incerteza ou a chance de um evento adverso ocorrer. A gestão de riscos em segurança consiste em identificar perigos preventivamente para escolher as melhores estratégias de mitigação. 

<p align="center">
  <img width="1538" height="682" alt="Camadas de Proteção e Gestão de Riscos" src="https://github.com/user-attachments/assets/728709a3-9d1e-4cf7-89b0-f15caec86302" />
</p>

O processo executa as seguintes etapas estruturadas:

1. Estabelecimento do contexto
2. Identificação de riscos
3. Avaliação de riscos
4. Tratamento de riscos
5. Aceitação de riscos
6. Comunicação e consulta
7. Monitoramento e análise crítica

---
### 📚 Materiais de Apoio Consultados
* [Glossário de Segurança da Informação - GSI/PR](https://www.gov.br/gsi/pt-br/seguranca-da-informacao-e-cibernetica/glossario-de-seguranca-da-informacao-1)
* [NIST Cybersecurity Glossary](https://www.nist.gov/itl/smallbusinesscyber/training/glossary)
* [CISA NICCS Glossary](https://niccs.cisa.gov/resources/glossary)
