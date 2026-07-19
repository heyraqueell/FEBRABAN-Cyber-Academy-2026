# Módulo 7: Ataques Cibernéticos (Parte 2) ☣︎


## Objetivo Principal
O objetivo deste resumo é detalhar as etapas de um ataque cibernético, permitindo compreender a lógica por trás da ação do atacante. Ao dominar esse passo a passo, é possível identificar em qual fase o ataque se encontra, o que é fundamental para construir defesas mais eficazes, direcionadas e estratégicas, tanto para quem ataca (Red Team) quanto para quem defende (Blue Team).

---

## Introdução: Como um Ataque Acontece 💻
Todo ataque segue uma lógica e um processo estruturado, com fases bem definidas. Entender esse ciclo é crucial porque:
- Permite identificar em qual fase o ataque está.
- Ajuda a construir defesas mais eficazes.
- Fornece uma visão estratégica.
- Uma segurança eficaz interrompe o ataque antes que ele conclua todas as etapas.

---

## Fases de um Ataque Cibernético ⚠️

### Reconhecimento (Recon) 
*   **O que é:** Fase inicial de coleta de informações sobre o alvo, sem levantar suspeitas.
*   **Como é feito:** Pesquisas em fontes abertas (Google, redes sociais, LinkedIn), consultas a registros (WHOIS, DNS) ou busca por vazamentos antigos (e-mails, senhas).
*   **Ferramentas comuns:** Google Dorks, Recon-ng, Shodan, Maltego.
*   **Mentalidade:** "Conheça o alvo melhor do que ele mesmo". Quanto mais informações coletadas, maior a chance de sucesso nas próximas fases.

### Enumeração 
*   **O que é:** Mapeamento dos caminhos para invadir após o reconhecimento. Identifica serviços, portas abertas e vulnerabilidades.
*   **Como é feito:** Varredura de rede (ping sweep, port scan), identificação de sistemas operacionais e versões de serviços ativos, enumeração de compartilhamentos e permissões.
*   **Ferramentas comuns:** Nmap, Netcat, Gobuster, Enum4linux.
*   **Importância:** O atacante começa a interagir com o sistema alvo. Sinais dessa atividade podem ser detectados por ferramentas de segurança.

### Exploração (Invasão) 
*   **O que é:** Fase onde a invasão ocorre. O atacante explora uma vulnerabilidade identificada para ganhar acesso inicial.
*   **Como é feito:** Phishing, exploração de falhas conhecidas (ex: Log4Shell, SQL Injection), uso de credenciais fracas.
*   **Ferramentas comuns:** Metasploit, SQLmap, ExploitDB.
*   **Momento decisivo:** A "porta" se abre para o atacante. É o momento em que a defesa deve atuar para impedir o avanço.

### Pós-Exploração e Persistência 
*   **O que é:** Garantir que o atacante mantenha o acesso, mesmo após reinicializações ou tentativas de remoção.
*   **Como é feito:** Instalação de backdoors, criação de usuários ocultos, uso de tarefas agendadas, técnicas de "Living Off the Land" (LotL) usando ferramentas legítimas do sistema.
*   **Objetivo:** Ideal para espionagem ou roubo prolongado de dados.

### Exfiltração e Ação Final 
*   **O que é:** A missão cumprida. O atacante rouba dados, causa dano ou executa seu objetivo principal.
*   **Como é feito:** Exfiltração de dados, ataques de ransomware (criptografia), defacement (desfiguração de páginas).
*   **Lição:** Se a detecção falhou nas fases anteriores, esta fase representa o prejuízo real.

---

## Cyber Kill Chain 🔗

É um modelo criado pela Lockheed Martin para descrever o **ciclo de um ataque cibernético**, inspirada na lógica de combate militar.

- **Conceito:** "Se você quebra um elo da corrente, a missão falha."
- **Aplicação:**
    - **Blue Team:** Ajuda a projetar defesas específicas para cada etapa do ataque.
    - **Red Team:** Simula cada fase para atingir um objetivo real.

### As 7 fases da Kill Chain

| **Etapa** | **Descrição simplificada** |
| --- | --- |
| Reconhecimento | Coleta de informações sobre o alvo |
| Armazenamento da arma  | Criar ou configurar o malware/exploit |
| Entrega | Enviar o vetor de ataque (E-mail, link, USB, etc.) |
| Exploração | Executar o código malicioso no sistema da vítima |
| Instalação | Instalar backdoor, trojan ou malware persistente |
| Comando e Controle | Estabelecer comunicação com o servidor do atacante |
| Ações sobre o alvo | Exfiltração de dados, sabotagem, sequestro, etc. |

<img width="1024" height="275" alt="image" src="https://github.com/user-attachments/assets/d04c9bd3-9898-4526-a382-6a55bb0a11f1" />

### Modelos complementares

A **Cyber Kill Chain** mostra a estrutura geral de um ataque. Mas às vezes, **precisamos ir além** — entender **como** o ataque aconteceu, **quais técnicas** foram utilizadas, e **qual o comportamento** do invasor.

**Modelos complementares ajudam a:**

1. Mapear **técnicas específicas** utilizadas por atacantes reais.
2. Investigar o **comportamento prático** durante o ataque.
3. Criar **defesas mais eficazes e focadas.**

**Os dois mais utilizados no mundo da cibersegurança:**

1. **MITRE ATT&CK**
2. **Diamond Model**

### Comparando Kill Chain x MITRE x Diamond

| Modelo | Foco Principal | Melhor para… |
| --- | --- | --- |
| Kill Chain | Fases do ataque | Entender onde parar o atacante |
| MITRE | Técnicas detalhadas | Detecção, simulação e hunting |
| Diamond | Relações entre elementos do ataque | Investigação e Inteligência |

---

## Como se Proteger 🛡️

### Medidas de Segurança Pessoal 👤
*   Use senhas fortes e únicas.
*   Ative a autenticação em dois fatores (2FA).
*   Cuidado com links, e-mails ou mensagens suspeitas (phishing).
*   Evite Wi-Fi público sem proteção (use VPN).

### Boas Práticas para Empresas 🏢
*   Políticas de controle de acesso (privilégio mínimo).
*   Atualizações constantes (patch management).
*   Monitoramento de rede e endpoints (EDR, SIEM).
*   Treinamento constante dos usuários (conscientização contra phishing).
*   Backups regulares e testados.
*   Segmentação de rede para conter danos.

### Ferramentas e tecnologias úteis

| Tipo de ferramenta | Exemplos |
| --- | --- |
| Antivírus / EDR | Windows Defender, CrowdStrike, SentinelOne |
| Firewall | pfSense, iptables, firewalls |
| SIEM | Elastic, Splunk, Wazuh |
| Backup | Veeam, Acronis, rsync |
| VPN | OpenVPN, WireGuard |
---

## Conclusão 🏁
"Não é preciso ser especialista para começar. Mas é preciso começar para um dia se tornar um especialista."

A segurança cibernética não é um produto, é um processo contínuo. A prevenção é sempre a melhor arma. O primeiro passo já foi dado! Continue estudando, praticando em plataformas como TryHackMe e Hack The Box, e participe de comunidades de segurança.

