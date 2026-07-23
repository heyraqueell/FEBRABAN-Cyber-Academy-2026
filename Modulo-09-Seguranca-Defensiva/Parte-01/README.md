# Módulo 09: Segurança Cibernética Defensiva (Parte 01)

### Objetivo principal

Demonstrar que a Segurança Cibernética Defensiva moderna não se baseia na ilusão de impedir 100% dos ataques, mas sim na implementação de uma arquitetura resiliente fundamentada em múltiplas camadas de proteção (Defesa em Profundidade), confiança zero (Zero Trust), políticas e normas estruturadas e controles práticos priorizados (como o CIS Controls).

---

## Contexto e Ideia Central

Esqueça a ilusão de que um sistema perfeitamente seguro é aquele que **bloqueia 100% dos ataques**. No cenário tecnológico atual, potencializado pelo uso de inteligência artificial por grupos criminosos, acreditar que barreiras intransponíveis existem é um erro perigoso.

O verdadeiro objetivo da **Segurança Defensiva** não é impedir o impensável, mas sim:

- **Reduzir riscos:** Dificultar ataques e limitar a superfície exposta.
- **Detectar e responder rapidamente** a desvios antes que virem catástrofes;
- **Preservar evidências, restaurar operações** com o mínimo de dano possível e **aprender continuamente** com cada incidente para que o erro não se repita.

## A Importância das Atividades Defensivas

Defender sistemas vai muito além de proteger computadores ou servidores isolados; trata-se de garantir a **sobrevivência da própria empresa**.

O que protegemos?

- **Pessoas:** Funcionários, clientes e usuários.
- **Dados críticos:** Financeiros, operacionais e confidenciais amparados por leis como a **LGPD.**
- **Reputação:** Que leva anos para ser construída e segundos para desmoronar.
- **Continuidade dos negócios**.

Em um ambiente digital moderno, a pergunta central deixou de ser *"Será que vamos sofrer um incidente?"* para se tornar *"Quando sofreremos um incidente?"*.

---

## A Anatomia dos Ataques em Cadeia (Kill Chain)

Os ataques cibernéticos graves não acontecem por acaso; eles seguem uma **trilha lógica em formato de cadeia**. Se a defesa atua logo no início, o estrago é mínimo. Se atua tarde demais, o impacto é devastador. As **8 fases** de um ataque típico são:

1. **Reconhecimento**: O atacante estuda o alvo.
2. **Exploração**: Identifica brechas técnicas.
3. **Obtenção de Credenciais**: Rouba senhas ou chaves de acesso.
4. **Movimentação Lateral**: Navega por dentro da rede da empresa.
5. **Elevação de Privilégios**: Consegue acessos de administrador.
6. **Persistência**: Garante que continuará com acesso mesmo se o sistema for reiniciado.
7. **Exfiltração**: Rouba e extrai os dados para fora da empresa.
8. **Impacto na Organização**: O dano é concretizado (ex: sequestro de dados por ransomware).

---

## Segurança Proativa vs. Segurança Reativa

- **Segurança Proativa (Prevenção)**: Atua **antes** do problema. Envolve **corrigir** vulnerabilidades, mapear riscos, criar diretrizes e testar sistemas constantemente. É a "medicina preventiva": mais barata, planejada e segura.
- **Segurança Reativa (Resposta)**: Atua **depois** que o incidente acontece. Envolve **conter** o estrago, estancar vazamentos e investigar a causa raiz. É o "pronto-socorro": uma crise operacional cara e estressante.

***Regra de Ouro*:** Ambas são vitais, mas viver apenas apagando incêndios (reativo) é um caminho caro e arriscado.

---

## 🛡️ Defesa em Profundidade e Zero Trust

**Defesa em Profundidade**: Arquitetura baseada na metáfora da cebola, combinando múltiplas camadas de proteção independentes. Se uma camada falhar, a seguinte reduz o dano, atrasa o invasor e possibilita a detecção e resposta. Se o atacante passar pelo firewall, encontrará barreiras no endpoint, na rede, na aplicação e nas credenciais.

<img width="1643" height="400" alt="image" src="https://github.com/user-attachments/assets/b141880c-3915-4157-8333-91d5a11909d4" />


### As 8 Camadas de Defesa em Profundidade

<details>
  <summary><strong>1. Governança e Políticas</strong></summary>

Estabelece as regras do jogo na empresa. Define diretrizes de comportamento, limites de uso para funcionários (quais sites podem ser acessados, como usar dispositivos corporativos) e atribui responsabilidades claras sobre a segurança.

</details>

<details>
  <summary><strong>2. Gestão de Identidades</strong></summary>

Controla o acesso de pessoas e sistemas. Utiliza autenticação forte (MFA), cofres de senhas, revogação imediata de acessos de funcionários desligados e proteção contra ataques de roubo de credenciais.

</details>

<details>
  <summary><strong>3. Proteção de Endpoint</strong></summary>

Foca na segurança de dispositivos finais (computadores, celulares e servidores). Envolve o endurecimento (hardening) de máquinas, desativação de serviços desnecessários e uso de antivírus ou EDRs modernos.

</details>

<details>
  <summary><strong>4. Proteção de Rede</strong></summary>

Protege o tráfego de dados da organização. Aplica firewalls robustos e realiza a segmentação de redes (separando setores e níveis de privilégio para impedir que um invasor navegue livremente pela empresa).

</details>

<details>
  <summary><strong>5. Segurança de Aplicações</strong></summary>

Garante que os softwares e sistemas desenvolvidos ou utilizados sejam seguros. Envolve testes de código, análise de vulnerabilidades, uso de WAF (Web Application Firewall) e revisão de bibliotecas de terceiros.

</details>

<details>
  <summary><strong>6. Proteção de Dados</strong></summary>

Foca na salvaguarda de informações sensíveis (dados pessoais regidos pela LGPD, segredos comerciais e dados financeiros). Utiliza criptografia e ferramentas de prevenção contra vazamento de dados (DLP).

</details>

<details>
  <summary><strong>7. Monitoramento e Logs</strong></summary>

Olhos e ouvidos da segurança. Utiliza softwares de correlação de eventos (SIEM) para registrar, monitorar comportamentos anômalos e disparar alertas operacionais em tempo real.

</details>

<details>
  <summary><strong>8. Backup e Continuidade</strong></summary>

A última linha de defesa para manter o negócio vivo. Consiste em realizar cópias de segurança frequentes e testadas (como a regra 3-2-1), garantindo a rápida restauração dos sistemas após um incidente grave (como um ataque de ransomware).

</details>

**Zero Trust (Confiança Zero)**: O lema definitivo é *"Nunca confie, sempre verifique"*. Nenhuma pessoa, aplicativo ou dispositivo dentro ou fora da rede tem passe livre automático; tudo é rigorosamente autenticado e validado a cada tentativa de acesso.

<img width="1557" height="510" alt="image" src="https://github.com/user-attachments/assets/c379a781-587d-4c5b-ba37-3337de661b0a" />


### Princípios Defensivos Essenciais

- **Menor Privilégio:** Acesso somente ao **extremamente** necessário para a função.
- **Monitoramento contínuo e Autenticação forte:** Visibilidade como base de toda resposta eficaz e verificação robusta de identidade.
- **Redução da superfície de ataque:** Eliminar o que **não é necessário** estar exposto.
- **Resiliência e Melhoria Contínua:** Corrigir, aprender e fortalecer após cada evento.

---

## Políticas de Segurança

- **O que são**: Declarações formais de direção e responsabilidade definidas pela alta administração. Elas determinam **o que** a organização espera, **quem** responde pelas ações, **quais** regras se aplicam e quais controles **devem** existir.
- **Não podem ser enfeite:** De nada adianta criar uma política linda e deixá-la esquecida na intranet. Ela precisa ser um documento vivo, que se atualiza sempre que o mundo digital ou os riscos mudam.
- **O equilíbrio ideal:** Muita segurança trava o trabalho das pessoas; pouca segurança deixa a empresa vulnerável. O segredo é achar o ponto de equilíbrio.
- **As 6 Políticas Essenciais:** Uma empresa madura precisa ter, no mínimo, regras claras sobre: **Segurança da Informação, Controle de Acesso, Classificação de Dados, Backup, Gestão de Vulnerabilidades e Proteção de Dados Pessoais (LGPD)**.

### A Pirâmide das Regras: Políticas, Normas e Procedimentos

Para organizar a casa, a documentação de segurança funciona em três níveis de detalhe:

1. **Política (O Topo - Estratégico)**: É a visão geral da diretoria (a "Constituição"). Exemplo: *"A empresa exige controle de acesso rígido para dados financeiros"*.
2. **Norma (O Meio - Tático)**: Dá mais detalhes práticos. Exemplo: *"Toda senha corporativa deve ter no mínimo 12 caracteres e usar autenticação em dois fatores (MFA)"*.
3. **Procedimento (A Base - Operacional)**: É o passo a passo exato do que fazer na rotina. Exemplo: *"Clique no botão X, preencha o campo Y para cadastrar a nova senha do funcionário novo"*.

---

## 🕹️ Os Controles de Segurança: Como agir na prática?

Os controles são as medidas que a empresa adota para segurar os riscos. Eles se dividem em duas formas principais:

#### **Por Natureza:**

- **Administrativos**: Regras, treinamentos, contratos e políticas.
- **Técnicos**: Firewalls, antivírus, criptografia, sistemas de monitoramento (SIEM).
- **Físicos**: Trancas, catracas, câmeras e segurança do Data Center.

#### Por Objetivo:

- **Preventivos**: Tentam impedir que o problema aconteça (ex: bloqueio de senhas fracas).
- **Detectivos**: Avisam quando algo estranho está rolando (ex: alertas de login em outro país).
- **Corretivos**: Consertam o estrago e trazem o sistema de volta à normalidade após uma crise (ex: restaurar um backup).
- **Dissuasórios**: Desanimam o invasor (ex: avisos de sistemas monitorados).
- **Compensatórios**: Um plano B quando a solução ideal é cara demais ou inviável tecnicamente.

---

## O Framework CIS Controls v8.1

**CIS Controls v8.1**, um guia super prático e famoso no mundo todo (e que inspira programas de segurança do governo brasileiro, como o PPSI). Ele prioriza ações reais para empresas do mundo real, cobrindo desde inventário de hardwares e softwares até a gestão de e-mails, backups e testes de segurança.

<img width="1574" height="383" alt="image" src="https://github.com/user-attachments/assets/d4e8ed79-2c2d-461e-b8df-09cf557a1024" />


---

## A Escala de Maturidade: Do Caos à Organização

A segurança de uma empresa evolui em 6 passos:

1. **Improviso**: Cada um faz do seu jeito; se apagar o incêndio, ótimo.
2. **Controles Básicos**: Tem antivírus ou firewall, mas nada integrado.
3. **Processos Definidos**: As normas começam a ser escritas e documentadas.
4. **Monitoramento Contínuo**: A empresa passa a vigiar ativamente o ambiente com equipes e ferramentas dedicadas (como um SOC).
5. **Governança Baseada em Risco**: As decisões de segurança acompanham os objetivos do negócio.
6. **Melhoria Baseada em Evidências**: O cenário ideal, onde tudo é auditado, medido por métricas reais e aprimorado o tempo todo para evitar que os mesmos erros voltem a acontecer.
