# Módulo 4: Leis, Regulamentações e Normas (Parte 1)

### Objetivo Principal

Este material tem como objetivo consolidar os conceitos fundamentais de governança, conformidade e segurança da informação. O foco é fornecer uma base teórica sólida sobre leis (LGPD, Marco Civil), normas internacionais (família ISO/IEC 27000, NIST) e a estrutura de implementação de controles, servindo como referência para estudos e aplicação prática no desenvolvimento de sistemas seguros.

---

A segurança da informação não é puramente tecnológica; ela se sustenta em um alicerce de conformidade dividido em três camadas complementares:

* **Leis:** Criadas pelo Poder Legislativo. Definem condutas, direitos e deveres. O descumprimento gera sanções legais e penais.
* **Regulamentações:** Detalham o cumprimento das leis em setores específicos (ex: ANPD, Banco Central).
* **Normas Técnicas:** Organizam as melhores práticas e controles reconhecidos pelo mercado (ex: ISO/IEC 27000, NIST).

### Por que Leis e Normas importam?

A governança eficaz responde a questões fundamentais de operação:

* **Responsabilidade:** Quem é responsável pela segurança e quem aprova o risco residual?
* **Proteção e Governança:** Quais dados/ativos são prioritários e quais controles são necessários?
* **Respostas a Incidentes:** Como comunicar autoridades e titulares em caso de violação?
* **Accountability:** Como demonstrar que a empresa está agindo corretamente?

---

## Marcos Regulatórios 🌐

Um marco regulatório define os direitos, deveres, limites de atuação e o papel das empresas, governo e consumidores.

### Nacionais (Brasil)

* **LGPD:** Essencial para o tratamento de dados pessoais. Prevê sanções administrativas (multas de até 2% do faturamento, limitadas a 50 milhões por infração).
* **Marco Civil da Internet:** Estabelece direitos, deveres e princípios para o uso da Internet no Brasil.
* **PSNI:** Política Nacional de Segurança da Informação; diretrizes para o setor público.

### Internacionais

* **Família ISO/IEC 27000:** Referência global para SGSI.
* **NIST Cybersecurity Framework:** Estrutura baseada em riscos para cibersegurança.
* **GDPR:** Regulamento europeu que serviu de base para a LGPD.
* **SOC 2:** Focado em auditoria de serviços (segurança, disponibilidade, confidencialidade, privacidade e integridade).
* **PCI-DSS:** Padrão de segurança para dados de cartões e pagamentos.

---

## A Família ISO/IEC 27000

Conjunto de normas interoperáveis para segurança, cibersegurança e privacidade.

| Norma | Descrição |
| --- | --- |
| **27000** | Visão geral e vocabulário |
| **27001** | Requisitos para SGSI |
| **27002** | Guia de controles |
| **27005** | Gestão de riscos de SI |
| **27017/18** | Segurança e privacidade em nuvem |
| **27035** | Gestão de incidentes |
| **27037** | Evidência digital |
| **27701** | Gestão de privacidade (extensão da 27001) |
| **29100** | Estrutura e princípios de privacidade |

### ISO/IEC 27001: O SGSI

Não é uma lista de ferramentas, mas um sistema de gestão:

1. Entenda o contexto.
2. Defina escopo e riscos.
3. Trate riscos e controles.
4. Avalie e melhore continuamente.

#### Evolução (2022-2024)

* **ISO 27001:2022:** Reorganização dos 93 controles do Anexo A em 4 grupos (Organizacionais, Pessoas, Físicos, Tecnológicos).
* **Emenda 1:2024:** Inclusão da **Resiliência Climática** como fator obrigatório de avaliação (impacto em disponibilidade, cadeia de suprimentos e infraestrutura física).

<img width="1612" height="639" alt="image" src="https://github.com/user-attachments/assets/570773b3-4072-4ac5-9c8c-f4db90fd8586" />

---

## Controles de Segurança

A **ISO 27002** orienta a execução dos controles definidos pela 27001.

| Grupo | Foco Principal |
| --- | --- |
| **Organizacionais** | Políticas, papéis, gestão de fornecedores, conformidade, inteligência de ameaças. |
| **Pessoas** | Conscientização, treinamento, responsabilidades (pré/durante/pós-vínculo). |
| **Físicos** | Segurança de áreas, proteção de ativos, descarte seguro. |
| **Tecnológicos** | Criptografia, controle de acesso, logs, backups, defesa contra malware, dev seguro. |

---

## NIST Cybersecurity Framework 2.0

Organiza a gestão de risco cibernético em **seis funções integradas**. O destaque da versão 2.0 é a função **Govern**:

* **Govern (Governança):** Contexto organizacional, estratégia, papéis, política, supervisão e gestão de riscos da cadeia de suprimentos.
* Sem Govern, o "Protect" torna-se um esforço técnico isolado.❗

<img width="869" height="690" alt="image" src="https://github.com/user-attachments/assets/bbcb288d-5945-4bac-943b-0304371a00ac" />

### Função Govern

Trata dos elementos que direcionam toda a estratégia de cibersegurança:

- Contexto organizacional
- Estratégia de cibersegurança
- Papéis e responsabilidades
- Política e Supervisão
- Gestão de riscos da cadeia de suprimentos

---

## General Data Protection Regulation (GDPR)

É a **principal referência europeia de proteção de dados pessoais** e influenciou diretamente a elaboração da LGPD brasileira.

- Proteção de dados como direito fundamental.
- Obrigações para controladores de operações.
- Direitos dos titulares.
- Comunicação obrigatória de incidentes.
- Regras para transferências internacionais.
- Sansões relevantes e alcance extraterritorial.


## Tendências Europeias (NIS2, DORA, AI Act)

* **NIS2:** Amplia obrigações para setores essenciais.
* **DORA:** Regula resiliência operacional digital no setor financeiro.
* **AI Act:** Abordagem baseada em risco para sistemas de IA (transparência e conformidade).

---

## A "Armadilha" do Checklist Cego

Um erro crítico na gestão é tratar normas como simples tarefas a serem marcadas.

- ❌ **Uso Incorreto:** Tentar implementar todos os controles de uma norma sem análise, criando check-lists apenas para cumprir tabela (geralmente resulta em auditorias que não garantem segurança real).
- ✅ **Uso Correto:** Análise de risco -> Identificação de ameaças -> Seleção de controles (justificados na SoA) -> Ciclo de melhoria contínua.

---

## Ciclo de Vida: SGSI na Prática

O SGSI funciona como um ciclo infinito de resposta:

- **Detectar:** Identificar eventos antes do impacto.
- **Classificar/Acionar:** Filtrar falsos positivos e mobilizar equipe.
- **Conter/Preservar:** Isolar ameaça e garantir evidências.
- **Comunicar/Recuperar:** Reportar conforme lei e restaurar serviços.

### Perguntas que o SGSI deve responder:

1. Quais ativos precisam ser protegidos?
2. Quais ameaças e vulnerabilidades existem?
3. Quais importam seriam relevantes?
4. Quais riscos são aceitáveis?
5. Quem aprova o risco residual?
6. Como a organização mede se está funcionando?

---

### 📚 Material de apoio
- [ISO 27001: O Padrão Ouro da Segurança da Informação Explicado ](https://www.youtube.com/watch?v=HMqWhI94xao)
