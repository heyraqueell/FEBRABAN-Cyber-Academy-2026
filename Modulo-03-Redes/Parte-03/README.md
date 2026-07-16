---

# Aula 3.3:🛡️Segurança de Redes e Criptografia

### Objetivo Principal
Compreender a aplicação prática dos conceitos de segurança em redes, a importância da integração entre pessoas, processos e tecnologias na defesa em profundidade, e o funcionamento técnico de mecanismos de sigilo e integridade como a criptografia e o hashing.

A segurança de uma rede não depende de uma única ferramenta, mas de uma combinação de **Pessoas**, **Processos** e **Tecnologias** (o "Pilar da Cibersegurança").

---

## Segurança de redes: Pessoas

- **Cultura de segurança:** A conscientização e sensibilização devem ser **constantes** para criar uma mentalidade de segurança em toda organização.
- **Phishing Ético:** Campanhas autorizadas ajudam a mensurar a aderência às políticas e identificar necessidades de treinamento.
- **Apoio da gestão**: Mudanças culturais reais só ocorrem com o engajamento e patrocínio direto da alta administração.
- **Letramento digital:** Usuários comuns são alvos mais prováveis devido à falta de conhecimento técnico sobre ameaças cibernéticas.

O elo mais fraco da segurança é, frequentemente, o fator **humano**.

## Segurança de redes: Processos

Processos definem as regras e o funcionamento da segurança. Exemplos essenciais:

- **Inventários de Ativos:** Mapear todos os dispositivos (desktops, laptops, câmeras, switches, roteadores, etc.) e identificar seus responsáveis.
- **Políticas de Cibersegurança:** Definir regras claras e torná-las de conhecimento obrigatório para todos os colaboradores e parceiros. Como politicas de senhas fortes e MFA (Autenticação Multifator).
- **Gestão de Acessos:** Implementar politicas de menor privilégio e segregação de funções.
- **Classificação de Ativos:** Avaliar o valor, nível de confidencialidade, direitos de acesso e métodos de descarte para cada recurso da rede.
- **Baseline de Configuração:** Estabelecer padrões mínimos: Aplicações autorizadas, antivírus, logs do sistema e nomenclatura de dispositivos.
- **Topologia Atualizada:** Manter o mapa da rede ***(físico e lógico)*** sempre em dia para facilitar auditorias e resposta a incidentes.

## Segurança de redes: Tecnologias

A tecnologia deve apoiar os processos e **proteger** as pessoas. A implementação de múltiplas camadas de defesa (Defesa em profundidade) é essencial para mitigar riscos cibernéticos modernos.

- Segmentação de Rede (VLANS)
- Firewalls e Roteadores Filtrantes
- SIEM (Correlação de Logs)
- Modelo Zero Trust
- Rotinas de Backups

- Zonas de Segurança (DMZ)
- IDS /IPS (Detecção e Prevenção)
- NTP (Sincronização de tempo)
- Criptografia e VPN
- Restrição de Protocolos (RDP, SMB)

## Segurança de redes: Infraestrutura

A segurança da infraestrutura física é o nível base da "Defesa em Profundidade". Se o acesso físico aos equipamentos for comprometido, todas as camadas lógicas de segurança podem ser contornadas. Uma rede confiável depende de proteção ambiental, controle de acesso físico e monitoramento constante.

### 🛡️ Proteção Física e Controle de Acesso
- Barreiras Físicas: Uso de cercas, guaritas, portões, portas blindadas e racks trancados para impedir acesso direto aos dispositivos.
- Monitoramento: CFTV e sensores de presença para vigilância 24/7 de áreas críticas.
- Controle de Acesso: Autenticação por crachás ou leitores biométricos em salas técnicas.

### 🌡️ Continuidade e Proteção Ambiental
- Ambiente: Monitoramento de temperatura, umidade, fumaça e proteção contra inundações.
- Energia: Fontes redundantes e geradores para garantir disponibilidade operacional.

### 📦 Ativos e Governança
- Inventário: Mapear e classificar todos os ativos (hardware, software e dados) pelo seu nível de criticidade.
- Topologia: Manter mapas de rede (físicos e lógicos) sempre atualizados para auditorias e resposta a incidentes.

<img width="1920" height="809" alt="image" src="https://github.com/user-attachments/assets/ea06903d-528d-4291-bda5-728638d8b331" />


---

## 🔐 Criptografia

Processo de **converter** um texto legível (*texto claro*) para algo ilegível (*texto cifrado*), garantindo a **confidencialidade** dos dados armazenados e transmitidos.

- A **cifra** é o algoritmo usado para criptografar a informação.
- O acesso aos dados originais é possível somente para quem possui autorização (**chave**).

**Princípio de Kerckhoffs:** *”Um sistema de criptografia deve ser seguro mesmo que tudo nele seja público, **exceto a chave.**”*

### 1. Criptografia simétrica

Utiliza **uma única chave** tanto para cifrar (bloquear) quanto para decifrar (desbloquear) a informação.

- **Vantagem**: É extremamente rápida, ideal para grande volumes de dados. Amplamente utilizada em softwares de **compactação de arquivos** (como ZIP, RAR, discos rígidos, arquivos locais ou bancos de dados).
- **Desafio**: O maior problema é a distribuição: Se você precisa enviar a chave para outra pessoa, corre o risco de ela ser interceptada no caminho.

### 2. Criptografia assimétrica

Utiliza um **par de chaves:** Uma **Chave Pública** (que pode ser compartilhada com qualquer pessoa) e uma **Chave Privada** (que deve ser mantida em segredo absoluto).

- **Como funciona**: Se alguém quiser te enviar uma mensagem, usa sua Chave Pública para cifrá-la. Apenas você, com sua Chave Privada, consegue decifrá-la.
- **Vantagem:** Resolve o problema de troca de chaves, pois você nunca vai precisar enviar sua chave secreta pela rede.
- **Desafio:** É um processo computacionalmente mais lento que a simétrica.
- **Aplicações:** Base para certificados digitais, protocolos HTTPS (SSL/TLS), SSH e transações bancárias seguras.

### 3. Hashing

O objetivo principal é a **integridade** e **verificação**. O hashing foi feito para ser **irreversível**.

- **Definição:** Um hash é uma **sequência de caracteres gerada por um algoritmo matemático**.
    - **ex:** `c0fc3c713f09a43384ac08f7d91fca430dcbc6466fff9284ce4571bdc2c8f9f9`
- **Como funciona:** Ele transforma qualquer quantidade de dados em uma “impressão digital” (hash) de tamanho fixo. Não existe uma chave para “desfazer” um hash e voltar ao arquivo original. Se você altera um único bit no dado original, o hash gerado será completamente diferente.
- **Uso prático:** Armazenar senhas de usuários (o sistema guarda apenas o hash, não a senha real), verificar se um arquivo baixada não foi corrompido ou alterado durante o download.

### Interceptação HTTP x HTTPS

- **HTTP (Inseguro):** Dados trafegam em texto claro. Senhas e dados pessoais podem ser interceptados.
- **HTTPS (Seguro):** Implementa uma camada de segurança (SSL/TLS) sobre o HTTP. Utiliza criptografia assimétrica e simétrica, sendo o padrão obrigatório na internet moderna para garantir a confidencialidade e a autenticidade do servidor.

<img width="1913" height="758" alt="image" src="https://github.com/user-attachments/assets/653940be-098e-4e04-bcad-997a73d831db" />


---

## Soluções de Segurança

### 1. Firewall

Um Firewall é um sistema ou grupo de sistemas que aplica uma política de **controle de acesso** entre redes, decidindo o que pode entrar ou sair com base em regras pré-definidas.

| Tipo de Firewall | Nível de inspeção | Características |
| --- | --- | --- |
| Packet Filtering | Camada 3 e 4 | Filtragem básica (Stateless) baseada em IP e Portas. |
| Stateful Inspection | Fluxo de Conexão | Monitora o estado real das conexões ativas e sessões. |
| Application Firewall | Camada 7 | Analisa o conteúdo real das aplicações (HTTP, FTP, etc). |

<img width="1913" height="688" alt="image" src="https://github.com/user-attachments/assets/774c4605-5b74-480b-9dd5-9d0e5df192cd" />


### 2. IDS (DETECTION)

- **Monitoramento Passivo:** Analisa o tráfego e gera alertas sobre atividades suspeitas.
- **Implementação:** Geralmente Out-of-band (cópia do tráfego).
- **Foco:** Visibilidade e detenção precoce sem interromper o fluxo de rede.

### 3. IPS (PREVENTION)

- **Monitoramento Ativo:** Detecta e bloqueia automaticamente ameaças em tempo real.
- **Implementação:** Instalado In-line (tráfego passa por ele).
- **Foco:** Proteção imediata e mitigação de ataques complexos.

### 4. SIEM (Security Information and Event Management)

Sistema de Gerenciamento de Eventos e Informações, é uma solução de segurança que centraliza, analisa e correlaciona dados de logs de múltiplos dispositivos de TI.

- **Visibilidade total:** Monitoramento contínuo para detecção precoce de incidentes e ações tempestivas.
- **Métricas de performance:** Acompanhamento de latência, largura de banda e disponibilidade dos serviços.
- **Análise de logs:** Coleta e análise sistemática de registros de sistemas, aplicações e dispositivos de rede.
- **Detecções de ameaças:** Uso de IDS/IPS para analisar comportamento e conteúdo do tráfego malicioso.

---

## Proteção de estações de trabalho

A proteção dos endpoints vai além do antivírus tradicional, exigindo uma camada de defesa baseada em Hardening e monitoramento ativo.

## Conceito de Hardening

É o processo de **”endurecimento”** de um sistema ou dispositivo, focado na redução da **superfície de ataque** para diminuir a probabilidade de sucesso de uma ameaça.

- **Simplificação:** Desativar tudo o que é desnecessário para o funcionamento básico.
- **Restrição:** Limitar privilégios e acessos ao estritamente necessário.
- **Blindagem:** Aplicar correções e configurações de segurança robustas.

### Ações de Hardening

- **Remover Bloatware:** Desinstalar aplicações e jogos pré-instalados de fábrica sem utilidade profissional.
- **Desativar serviços ociosos:** Desligar recursos não usados: Bluetooth, Xbox, Compartilhamento, Portas USB.
- **Atualizações críticas:** Configurar patches automáticos e imediatos para o SO e aplicações de terceiros.
- **Fechar portas lógicas:** Bloquear portas de redes desnecessárias (como RDP ou SMB) para conexões externas.
- **Remover direitos de ADMIN:** Garantir que o usuário comum utilize conta padrão para mitigar a instalação de malware.
- **Aplicação Allowlist:** Permitir apenas a execução de programas autorizados, bloqueando executáveis desconhecidos.
- **Criptografia de disco:** Ativar BitLocker (Windows) ou FileVault (macOS) para proteção em caso de extravio.
- **Políticas de senhas fortes:** Exigir complexidade, bloqueio por inatividade e limite de tentativas de login.

## Soluções de Segurança

| **Solução** | **Finalidade Principal** | **Baseado em Assinatura?** | **Baseado em Comportamento?** | **Detecta Fileless?** | **Tipo de Ameaça Alvo** | **Ação Principal** |
| --- | --- | --- | --- | --- | --- | --- |
| **Antivírus Tradicional** | Bloquear vírus conhecidos antes da sua execução no disco. | Sim | Não (ou muito básico) | Não | Vírus antigos, Cavalos de Troia comuns, Worms | Apaga ou coloca o arquivo em quarentena. |
| **Anti-Spyware** | Detectar e remover programas focados em espionagem e roubo de dados. | Sim | Sim (Apenas heurística simples) | Raro | *Keyloggers*, Adware (anúncios), cookies maliciosos | Limpa o sistema após varrimento. |
| **Anti-Spam** | Filtrar o correio eletrônico corporativo contra lixo e fraudes. | Não | Não | Não | E-mails publicitários em massa, links de *Phishing* | Desvia e-mails para a pasta de Lixo |
| **Bloqueador de Pop-up** | Impedir janelas e scripts intrusivos durante a navegação web. | Não | Não | Não | Anúncios abusivos, scripts maliciosos de rastreio (browsers) | Oculta ou impede a execução do código da página |
| **EDR (Endpoint Detection & Response)** | Monitorar, detectar e responder a ameaças avançadas focadas no dispositivo | Sim (Secundário) | Sim (Foco total) | Sim | Ataques *Zero-Day*, invasões ativas no dispositivo, *Ransomware*. | Bloqueia processos, isola a máquina da rede e gera telemetria do host. |
| **XDR (Extended Detection & Response)** | Fornecer uma defesa unificada cruzando dados do *endpoint*, rede, e-mail e nuvem em um painel | Sim (Secundário) | Sim (Foco total) | Sim | Ataques complexos, movimentos laterais na rede, roubo de credenciais. | Bloqueia o host, revoga acessos à nuvem e apaga e-mails maliciosos em massa. |

---
### 📚 Materiais de Apoio: 

Recomendo o canal **[Dicionário de Informática](https://www.youtube.com/@dicionariodeinformatica)**. O conteúdo é excelente para fixação, pois explica conceitos de forma didática e resolve questões de concursos, sendo um ótimo preparador para provas.

* [Zero day attacks e o ataque do dia zero](https://youtu.be/K1G4233FR4g)
* [APRENDA de uma vez por todas o que é SIEM](https://youtu.be/tPND-5dVAU4)
