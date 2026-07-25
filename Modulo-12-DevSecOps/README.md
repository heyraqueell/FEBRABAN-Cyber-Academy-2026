# Modulo 12: Desenvolvimento Seguro (DevSecOps) ♾️


### Objetivo principal

Demonstrar como a integração da segurança no ciclo DevOps (DevSecOps), por meio de automação e da cultura shift-left, permite entregas rápidas e contínuas sem abrir mão da mitigação de riscos e da conformidade.

---

## O que é DevOps?

**É a união de pessoas, processos e tecnologia para fornecer continuamente valor aos clientes.**

Permite que funções anteriormente isoladas — *desenvolvimento, operações de TI, engenharia de qualidade e segurança* — atuem de forma coordenada e colaborativa para gerar produtos melhores e mais confiáveis.

As equipes ganham a capacidade de responder melhor ás necessidades dos clientes, aumentar a confiança nos aplicativos que constroem e cumprir as metas empresariais mais rapidamente.

<img width="846" height="416" alt="image" src="https://github.com/user-attachments/assets/7a6d7954-0eca-4da9-9ce4-c54335b388de" />


## O que é DevSecOps e sua importância

A sigla representa a união de **Development (Desenvolvimento) + Security (Segurança) + Operations (Operações)**

- **Cultura e Integração:** Elimina os silos tradicionais, unindo desenvolvedores, operadores e especialistas em segurança para trabalharem colaborativamente.
- **Shift Security Left:** Consiste em antecipar as verificações de segurança para o início do ciclo de desenvolvimento (planejamento), reduzindo drasticamente os custos e mitigando falhas antes que cheguem aos ambientes de produção.

<details>
<summary><strong>Clique para expandir</strong></summary>

<img width="3000" height="3900" alt="image" src="https://github.com/user-attachments/assets/e1406f54-f53a-4108-b049-f6ce5f5c8ee5" />

</details>
    

## Por que a Adoção de DevSecOps é Crítica?

O crescimento exponencial de **ataques cibernéticos** direcionados a softwares exige defesas robustas e contínuas.

Com entregas cada vez mais rápidas impulsionadas pelo DevOps, há um risco latente de as equipes "pularem etapas de segurança" para cumprir prazos de lançamento.

Vazamentos de dados e incidentes de segurança geram custos altíssimos e danos irreparáveis à imagem da instituição. DevSecOps transforma a segurança em um facilitador da **agilidade com controle**, deixando de ser um bloqueio burocrático.

---

## Integração e Controles no Ciclo de Desenvolvimento (Pipeline CI/CD)

Práticas e ferramentas de segurança distribuídas ao longo das fases do pipeline:

<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/248e1138-e8d4-45e9-a997-dccffb28accc" />


<img width="1000" height="603" alt="image" src="https://github.com/user-attachments/assets/082c9132-d3ae-48be-ba4e-f081eda4e088" />


---

## Por que Automatizar a Segurança?

- **Acompanhar a Velocidade do DevOps:** O ciclo de entrega contínua exige que a segurança acompanhe o ritmo acelerado de commits e deploys sem criar gargalos operacionais.
- **Redução de Erros Humanos:** Processos manuais frequentemente deixam passar falhas críticas por fadiga, desatenção ou limitação de escopo analítico.
- **Consistência nas Verificações:** Garante que os mesmos critérios e regras de segurança sejam aplicados uniformemente a cada nova modificação no código.

## Principais Tipos de Testes Automatizados 🔍

#### 1. SAST (*Static Application Security Testing*)

- **Conceito:** Conhecido como **testes estáticos de segurança**, auditoria de código ou testes *whitebox* (caixa branca). Analisa diretamente o código-fonte da aplicação.
- **Funcionamento:** Ocorre sem que a aplicação precise estar em execução. A ferramenta analisa o repositório de código fonte em busca de padrões vulneráveis, falhas de lógica, validação de entradas e má implementação de criptografia.

#### 2. DAST (*Dynamic Application Security Testing*)

- **Conceito:** Conhecido como **testes dinâmicos de segurança** ou testes *blackbox* (caixa preta). Testa a aplicação **em execução**.
- **Funcionamento:** Dispara requisições e simula tentativas reais de ataque contra a aplicação em um ambiente em execução (como homologação, testes ou stage) para analisar sua resposta e comportamento frente a explorações.

#### 3. SCA (*Software Composition Analysis*)

- **Conceito:** Análise de Composição de Software (ou análise de dependências / segurança de código aberto). Ganhou enorme relevância devido ao crescimento expressivo de ataques à **cadeia de suprimentos de software** (*supply chain*).
- **Funcionamento:** Analisa as bibliotecas e dependências de terceiros utilizadas no projeto, identificando versões desatualizadas ou vulnerabilidades publicamente conhecidas (CVEs).

#### 4. IAST (*Interactive Application Security Testing*)

- **Conceito:** Abordagem interativa que combina análises estáticas e dinâmicas, monitorando a aplicação de dentro para fora durante a execução dos testes.

#### 5. Scanning de Containers e Imagens

- **Conceito:** Escaneamento de imagens Docker e artefatos empacotados para identificar vulnerabilidades tanto no sistema operacional base (*base image*) quanto nas camadas de software da aplicação.

## Controles de Segurança em Pipelines (CI/CD) 🛡️

- **Objetivo:** Garantir que somente código seguro chegue ao ambiente produtivo através de barreiras automatizadas.
- **Práticas Comuns:** Validação de *secrets*, *scanning* de infraestrutura como código (IaC), testes automatizados (SAST/SCA/DAST), assinatura de artefatos e controle rigoroso de permissões.
- **Segurança Contínua:** Premissa de que **cada commit é analisado** de forma automatizada para manter o risco da aplicação em patamares aceitáveis pela governança da empresa.

---

## Práticas Recomendadas

- **Shift-left e Shift-right**: Testar cedo no ciclo de desenvolvimento (*left*) e monitorar continuamente após o deploy (*right*).
- **Cultura de segurança compartilhada**: O conceito de que *"segurança é responsabilidade de todos"* (*everyone's responsibility*).
- **Treinamentos contínuos para desenvolvedores**: Capacitação constante para que saibam escrever códigos seguros desde a universidade/início da carreira.
- **Menor privilégio e Gestão de Segredos**: Uso rigoroso de cofres seguros, como **HashiCorp Vault** ou **AWS Secrets Manager**, evitando exposição de tokens.
- **Adoção de frameworks de maturidade**: Utilização de diretrizes como **OWASP SAMM** e **NIST SSDF** para avaliar a maturidade organizacional.

## Benefícios da Adoção de DevSecOps

Integrar segurança ao desenvolvimento traz vantagens estratégicas fundamentais:

- **Redução de riscos e vulnerabilidades**: Mitigação precoce de falhas críticas.
- **Menor custo de correção**: Encontrar e corrigir bugs de segurança nas etapas iniciais é significativamente mais barato do que corrigi-los em produção.
- **Releases mais rápidas e seguras**: Agilidade sem abrir mão da conformidade.
- **Maior colaboração entre equipes**: Rompimento de silos entre times de desenvolvimento, operações e segurança (*Dev*, *Ops* e *Sec*).
- **Conformidade regulatória e confiança**: Atendimento a requisitos legais (*compliance*) e aumento da confiança dos clientes na organização.
