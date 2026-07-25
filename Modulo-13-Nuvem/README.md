# ☁️ Módulo 13: Nuvem e Segurança Cibernética ☁️

### Objetivo principal

Compreender os fundamentos da computação em nuvem, seus modelos de serviços e as principais práticas de segurança, riscos e governança.

---

## O que é Computação em Nuvem?

É o fornecimento de recursos de computação pela internet, como *servidores*, *armazenamento*, *banco de dados*, *redes* e *software*. Ao invés de armazenar dados e **rodar** aplicativos no seu computador pessoal, você usa servidores remotos acessíveis via internet.

### **Pirâmide de Serviços em Nuvem:**

A apresentação detalha as camadas arquiteturais divididas em:

- **Infraestrutura:** Computação, Armazenamento, Rede.
- **Plataforma:** Identidade, Armazenamento de Objetos, Motores de Execução, Bancos de Dados.
- **Aplicação:** Monitorização, Conteúdo, Colaboração, Finanças e Desktops.

<img width="940" height="851" alt="image" src="https://github.com/user-attachments/assets/4b436bf2-598e-4b02-9aa8-9735870137e9" />


## Vantagens Estratégicas da Nuvem

- **Acessibilidade Global:** Gestão de infraestrutura de qualquer lugar do mundo via internet, desde que protegida por autenticação robusta.
- **Escalabilidade:** Capacidade automatizada de expandir ou contrair recursos computacionais conforme a oscilação da demanda.
- **Otimização de Custos (*OPEX vs. CAPEX*):** Eliminação de investimentos iniciais pesados em hardware físico, substituídos por despesas operacionais proporcionais ao uso real.
- **Economia:** Pague **apenas** pelo o que usar.
- **Compliance e Governança:** Facilidade na implementação de padrões rígidos de segurança, como o **PCI-DSS** para transações com cartão de crédito, por meio de contas isoladas e automação via Infraestrutura como Código (*IaC*).

## Desvantagens, Riscos e Desafios Operacionais

- **Dependência de Fornecedor:** Embora o conceito de *multicloud* seja amplamente discutido, na prática as empresas acabam atrelando a maioria de seus serviços críticos a um único provedor predominante (como AWS no setor privado e Azure em órgãos governamentais).
- **Complexidade de Preços e FinOps:** A estrutura de custos é altamente complexa (cobranças por hora, minuto, segundo ou número de requisições), dando origem à profissão especializada em Gestão Financeira na Nuvem (**FinOps**).
- **Custos de Egressão de Dados:** Taxas adicionais incidentes sobre o tráfego de dados que sai do ambiente em nuvem.
- **Modelo de Segurança Compartilhada:** Ambiguidade recorrente entre as equipes sobre quais camadas de segurança são de responsabilidade do provedor de nuvem (*cloud provider*) e quais pertencem ao cliente.
- **Perda de Flexibilidade e Customização:** Restrições impostas pelos serviços gerenciados dos provedores, dificultando ajustes finos profundos em comparação a ambientes locais (*on-premises*).

---

## Principais tecnologias

- Virtualização
- Containers
- Redes definidas por software
- Armazenamento distribuídos

## Provedores de Nuvem (Mais conhecidos)

- Amazon Web Services (AWS)
- Microsoft Azure
- Google Cloud Platform (GCP)
- Outros: IBM Cloud, Oracle Cloud, etc.

<img width="895" height="254" alt="image" src="https://github.com/user-attachments/assets/f9b336a5-64d5-47d8-8090-d045fb64ebb7" />


## Modelos de Serviços em Nuvem ⚙️

| **Modelo** | **O que é fornecido?** | Exemplo |
| --- | --- | --- |
| **IaaS** (**Infraestrutura** como Serviço) | Servidores, redes, armazenamento | AWS EC2 |
| **PaaS** (**Plataforma** como Serviço) | Ambiente para desenvolvimento de apps | Google Ap Engine |
| **SaaS** (**Software** como Serviço) | Aplicativos prontos para uso | Gmail, Netflix, Office 365 |

<img width="1200" height="627" alt="image" src="https://github.com/user-attachments/assets/48e96562-6740-4bd9-8c52-356551f020db" />


## Responsabilidade Compartilhada

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0ada7145-32fc-437e-8710-806c8c3d1543" />


Eu: Azul x Nuvem: Verde

- **IaaS (Infrastructure as a Service):** O provedor gerencia o **hardware físico** e a **virtualização**. O usuário tem total controle e responsabilidade sobre o sistema operacional (**SO**), runtime, middleware, dados e código da aplicação. *Exemplo:* **AWS EC2**.
- **PaaS (Platform as a Service):** O provedor gerencia a infraestrutura e o ambiente de execução (**runtime**, servidores web como Apache ou Tomcat). O desenvolvedor foca exclusivamente no **código da aplicação** e nos dados. *Exemplo:* **Google App Engine**, **Heroku**.
- **SaaS (Software as a Service):** O provedor é responsável por praticamente toda a pilha tecnológica, desde o hardware até a entrega da interface pronta para uso. O usuário final gerencia apenas suas credenciais de acesso e configurações de perfil. *Exemplos:* **Gmail, Netflix, Microsoft 365**.
- **Modelos Intermediários:** Destacam-se também o **CaaS** (Containers as a Service) e o **FaaS** (Function as a Service / Serverless, como AWS Lambda e Google Cloud Functions), onde a abstração da infraestrutura é ainda maior.

## Principais Ameaças e Riscos na Nuvem 🛡️

A segurança em ambientes de nuvem apresenta vulnerabilidades críticas, muitas vezes decorrentes de falhas humanas ou de projeto:

- **Vazamento de Dados:** Exposição acidental ou criminosa de dados sensíveis devido a buckets de armazenamento (como **AWS S3** ou blobs) configurados com acesso público generalizado.
- **Ataques de Ransomware e Extorsão Dupla:** Ciber criminosos que invadem ambientes, criptografam arquivos produtivos e exfiltram cópias dos dados, exigindo resgates financeiros sob ameaça de vazamento público.
- **Configurações Incorretas (*Security Misconfigurations*):** O clássico erro de deixar "portas abertas" (como instâncias EC2 expostas na internet com a porta SSH `22` liberada sem autenticação baseada em chaves seguras).
- **Acesso Não Autorizado:** Uso de credenciais fracas, vazamento de chaves de API e tokens de acesso em repositórios públicos (como commits acidentais no **GitHub**).
- **Ataques Internos:** Ações mal-intencionadas de colaboradores ou falhas decorrentes de desatenção (engenharia social e *phishing*).

<details>
<summary>O estudo oficial do <b>CSA (Cloud Security Alliance - Top Threats to Cloud Computing 2024)</b> categoriza as 11 principais ameaças atuais:</summary>

1. Configuração incorreta e controle de alterações inadequado.
2. Gerenciamento de Identidade e Acesso (<b>IAM</b>) deficiente.
3. Interfaces e <b>APIs</b> inseguras.
4. Seleção e implementação inadequada da estratégia de segurança.
5. Recursos de terceiros inseguros (dependências e bibliotecas vulneráveis).
6. Desenvolvimento de software inseguro.
7. Divulgação acidental de dados na nuvem.
8. Vulnerabilidades sistêmicas e falhas de software (<b>CVEs</b>).
9. Visibilidade e observabilidade limitadas.
10. Compartilhamento de recursos não autenticado.
11. <b>APTs</b> (Ameaças Persistentes Avançadas).
</details>

---

## O Framework MITRE ATT&CK Aplicado à Nuvem ⚔️

O **MITRE ATT&CK** é uma base de conhecimento globalmente reconhecida que cataloga **táticas**, **técnicas** e **procedimentos** (**TTPs**) reais utilizados por atacantes cibernéticos. 

O framework possui matrizes específicas adaptadas para **Enterprise Cloud** e **Containers**. As táticas analíticas mapeadas cobrem todo o ciclo de vida de uma intrusão:

- **Initial Access:** Como o atacante obtém acesso (ex: exploração de aplicações públicas vulneráveis, contas válidas comprometidas).
- **Execution & Persistence:** Comandos executados no ambiente e mecanismos para garantir a permanência do acesso.
- **Privilege Escalation & Defense Evasion:** Técnicas para elevar privilégios dentro do cluster e burlar ferramentas de monitoramento.
- **Credential Access & Discovery:** Varredura e roubo de credenciais/chaves de acesso armazenadas na nuvem.
- **Lateral Movement, Collection & Exfiltration:** Movimentação entre nós (ex: pods em Kubernetes), coleta de dados sensíveis e expropriação de informações.
- **Impact:** Ações destrutivas, como **Data Destruction** e ataques de negação de serviço (**DDoS**).

<img width="1707" height="651" alt="image" src="https://github.com/user-attachments/assets/6ec802bf-f7e3-47c5-9d14-034ebe316fca" />


---

# Mecanismos Básicos e Boas Práticas de Proteção 🛡️

- **Autenticação Multifator (MFA):** O princípio fundamental de que **não se deve confiar apenas na senha**. O uso de **hardware tokens (ex: YubiKey)** é citado como a opção mais robusta e segura em comparação a tokens baseados em SMS ou aplicativos autenticadores baseados em software.
- **Criptografia:** Essencial para proteger dados tanto **em trânsito** (com o uso obrigatório de **HTTPS**) quanto **em repouso** (armazenados em bancos de dados e storages).
- **Backups:** Manutenção constante de **cópias de segurança** isoladas para garantir rápida recuperação e mitigação de impactos em ataques de **ransomware** ou corrupção de dados.
- **Controle de Acesso:** Aplicação rigorosa do **Princípio do Menor Privilégio**, garantindo que apenas usuários e sistemas com necessidade real tenham acesso aos recursos.
- **Atualizações e Patches:** Manutenção contínua do sistema operacional e das aplicações atualizadas para fechar brechas de segurança conhecidas.
- **Monitoramento Contínuo:** Implementação de sistemas de **logs** e monitoramento em tempo real para detectar comportamentos anômalos ou tentativas de exploração (*Brute Force*, varreduras de portas) desde o início.

## Roteiro de Maturidade de Segurança da AWS (CAF v2) 🗺️

1. **Inventário:** Saber exatamente o que está rodando no ambiente.
2. **Ter backups:** Garantir cópias de segurança confiáveis.
3. **Visibilidade e correção inicial:** Monitorar serviços e corrigir falhas básicas.
4. **Detecção:** Identificar anomalias e problemas precocemente.
5. **Acesso seguro ao IAM:** Gerenciamento rígido de identidades e acessos.
6. **Reduzir superfície de ataque:** Desativar serviços e portas desnecessárias.
7. **Reprodutibilidade e propriedade:** Utilizar **infraestrutura como código (IaC)** para recriar ambientes do zero.
8. **Refinamento de privilégios mínimos:** Ajustar finamente as permissões de usuários e aplicações.
9. **Comunicações de rede seguras:** Isolação e criptografia rigorosa de tráfego.
10. **Preparação para incidentes:** Elaboração e testes de planos de **disaster recovery** e resposta a crises.

As capacidades são gerenciadas através de domínios como **Governança de Segurança**, **Gestão de Identidade e Acesso (IAM)**, **Proteção de Dados**, **Detecção de Ameaças** e divididas em quatro grandes fases de maturidade: **Quick Wins**, **Fundação**, **Eficiência** e **Otimização**.

<img width="1800" height="711" alt="image" src="https://github.com/user-attachments/assets/b4d58067-0525-4852-a443-fa2e75cba078" />


---

## Conclusão

A computação em nuvem transforma a forma como usamos tecnologia, mas também traz novas responsabilidades. Entender os conceitos básicos e adotar medidas simples de segurança pode fazer toda a diferença para proteger seu dados e sua privacidade.

