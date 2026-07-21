# 🛡️ Modulo 08: Segurança Cibernética Ofensiva (Parte 1)

### Objetivo Principal

Desmistificar o papel do atacante ético, demonstrando que a simulação de ataques reais é a única forma eficaz de testar controles de segurança, identificar vulnerabilidades não mapeadas e antecipar ações de agentes mal-intencionados.

---

## 🛡️ Conceitos de Segurança Cibernética Ofensiva

- Para proteger bem, é essencial **pensar como o atacante**.
- Segurança ofensiva consiste em um **conjunto de técnicas**, **ferramentas** e **metodologias** utilizadas para **simular** ataques reais a sistemas, redes e pessoas.
- **Objetivo:** Testar controles de segurança, identificar vulnerabilidades e corrigi-las antes que criminosos as explorem.
- **Diferença fundamental:** A segurança ofensiva é realizada de forma ética e autorizada, ao contrário do cibercrime.
- **Empresa madura:** É aquela que se antecipa ao atacante, sendo proativa em vez de apenas reagir.

---

## Diferença entre Defensiva x Ofensiva

| Aspecto | Segurança **Defensiva** | Segurança **Ofensiva** |
| --- | --- | --- |
| Objetivo | Detectar e responder a ataques | Simular e antecipar ataques |
| Atuação | Monitoramento e proteção contínua | Testes, simulações, exploração controlada |
| Perfil | Blue Team | Red Team / Pentesters |
| Foco | Reagir | Prevenir e Antecipar |

## 📈 Importância das Atividades Ofensivas

- **Mudança de mentalidade:** Do reativo ao proativo.
- **Prevenção de riscos:** Ajuda a evitar incidentes graves antes que ocorram.
- **Conformidade e Auditoria:** Atendimento a normas exigentes como LGPD, ISO 27001 e PCI-DSS, que frequentemente exigem testes regulares de segurança.
- **Maturidade Organizacional:** Simular ataques gera oportunidades de evolução contínua.

## Onde a ofensiva atua?

| Domínio | Exemplos |
| --- | --- |
| Aplicações Web | Testar login, injeção de SQL, upload malicioso |
| Infraestrutura | Enumeração de portas, exploração de serviços |
| Usuários | Simular phishing, engenharia social |
| OSINT | Coletar dados públicos que ajudam na invasão |

### Por que adotar uma postura ofensiva na segurança?

- A maioria das organizações investe em ferramentas defensivas (firewall, antivírus, monitoramento), mas só descobre suas falhas **quando é atacada de verdade**.
- A segurança ofensiva permite identificar **vulnerabilidades reais**, muitas vezes ignoradas por ferramentas automatizadas, e simular o comportamento de atacantes para saber **onde estão os pontos fracos mais críticos.**

## Diferença entre vulnerabilidade, ameaça e risco

| **Conceito** | **Definição** | **Exemplo** |
| --- | --- | --- |
| **Ameaça** | Quem pode explorar a falha | Um hacker **tentando** invadir seu site |
| **Vulnerabilidade** | A falha existente | Um serviço desatualizado e exposto na internet |
| **Risco** | A probabilidade da ameaça explorar a falha + impacto | A chance do hacker invadir e causar prejuízo |

---

## Ciclo de Análise de Vulnerabilidades

O processo não é aleatório, seguindo um fluxo lógico:

1. **Planejamento e Escopo:** Definição do que será testado (site, redes, servidores).
2. **Coleta de Informações:** Mapeamento de hosts, portas e serviços.
3. **Varredura (Scan):** Utilização de ferramentas para identificar falhas técnicas.
4. **Análise dos Resultados:** Eliminação de **falsos positivos** e verificação da gravidade.
5. **Relatório Técnico:** Documentação detalhada com falhas, riscos e recomendações de mitigação.

### Métodos de análise:

- **Automatizada**: Ferramentas rápidas, mas com possibilidade de falsos positivos.
- **Manual**: Foco em especialistas, interpretação de testes e análise direcionada.
- **Híbrida**: Combinação ideal que busca equilíbrio entre agilidade e profundidade.

### 🛠️ Ferramentas Comuns de Análise de Vulnerabilidades

O autor reforça que **as ferramentas não substituem o conhecimento. Elas potencializam quem sabe usá-las**. As soluções automatizadas ajudam a acelerar o processo, mas exigem validação humana para evitar falsos positivos.

As principais ferramentas de mercado são:

- **Nmap:** Focado na descoberta de *hosts*, portas abertas e serviços ativos na rede. É o padrão da indústria para mapeamento inicial de infraestrutura.
- **Nessus:** Um *scanner* comercial amplamente utilizado que conta com interface gráfica para identificar vulnerabilidades conhecidas em sistemas operacionais e redes.
- **OpenVAS:** Uma alternativa robusta de código aberto (*open-source*) para varredura de vulnerabilidades corporativas.
- **Nikto:** Ferramenta especializada em varreduras em aplicações web para encontrar arquivos perigosos, CGIs desatualizados e problemas de configuração em servidores web.
- **Burp Suite:** A ferramenta líder de mercado para testes manuais e automatizados em aplicações web (interceptação de tráfego HTTP/HTTPS, testes de injeção, etc.).
- **Wappalyzer:** Utilizado para identificar tecnologias, frameworks e CMSs utilizados em aplicações web durante a fase de reconhecimento.

---

## Teste de Invasão (Pentest)

Um **teste de invasão (pentest)** é uma simulação controlada de ataque a sistemas, redes ou aplicações, realizadas com **autorização**, com o objetivo de: 

- Encontrar vulnerabilidades exploráveis
- Avaliar a eficácia dos controles de segurança
- Fornecer recomendações para correção

O Pentest é uma simulação de ataque que se divide em metodologias:

- **Black Box:** Simula um atacante externo (mais realista).
- **White Box:** Simula um ataque com acesso parcial (ex: funcionário com poucos privilégios).
- **Grey Box:** Simula um ataque interno ou auditoria profunda.

---

## 🌐 OSINT (Open Source Intelligence)

Parte fundamental de qualquer operação ofensiva. Consiste na coleta de dados públicos sobre o alvo (indivíduo ou instituição) para aumentar a superfície de ataque e entender o contexto antes de interagir com os sistemas.

Fontes comuns:

- Motores de busca (Google, Bing)
- Redes sociais
- Sites institucionais e portais de notícias
- Vazamentos públicos (leaks)
- WHOIS, DNS, Shodan

### Principais locais de fontes OSINT

| **Ferramenta** | **Função Principal** |
| --- | --- |
| **Google Dorks** | Pesquisas avançadas em motores de busca |
| **TheHarvester** | Coleta de e-mails, subdomínios e hosts |
| **Shodan** | Busca por dispositivos e serviços expostos |
| **Maltego** | Visualização gráfica de relacionamentos |
| **Recon-ng** | Framework modular para coleta OSINT |
| **Spiderfoot** | Varredura automatizada de várias fontes |
