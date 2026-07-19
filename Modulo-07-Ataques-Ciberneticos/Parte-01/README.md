# Módulo 7: Ataques Cibernéticos (Parte 1) ☣︎

### Objetivo principal

O objetivo desta aula é fornecer uma compreensão sólida sobre a natureza dos ataques cibernéticos, abrangendo desde os conceitos fundamentais e as motivações dos agentes maliciosos até a análise de casos reais, as fases do ciclo de um ataque e as estratégias essenciais para o fortalecimento da segurança e proteção de ativos digitais.

---

## O que é um ataque cibernético?

Qualquer ação maliciosa que visa comprometer a segurança de dados, sistemas ou redes.

- **Pode buscar:**
    - Roubo de informações.
    - Interrupção de serviços (ex: derrubar um site).
    - Modificação não autorizada de dados.
    - Espionagem ou sabotagem.

## A Tríade da Segurança da Informação (CIA)

Os ataques geralmente visam comprometer **um** **ou mais** destes pilares:

| **Pilar** | **Definição** |
| --- | --- |
| **Confidencialidade** | Garantir que apenas pessoas autorizadas acessem os dados. |
| **Integridade** | Garantir que os dados não sejam alterados indevidamente. |
| **Disponibilidade** | Garantir que os sistemas estejam acessíveis quando necessário. |

## Termos Fundamentais ⚠︎

- **Ativo:** Qualquer dado, sistema ou recurso com valor.
- **Ameaça:** Potencial agente causador de danos (ex: hacker, vírus, incêndio).
- **Vulnerabilidade:** Fraqueza que pode ser explorada (ex: sistema desatualizado, senha fraca).
- **Exploit:** Código que aproveita uma vulnerabilidade.
- **Risco:** Probabilidade de exploração x impacto.
- **Incidente:** Evento de segurança real ou suspeito.

### Diferenciando Ameaça, Vulnerabilidade e Risco ☢︎

- **Ameaça:** Qualquer agente ou evento que **pode causar dano** (ex: hacker, vírus, incêndio).
- **Vulnerabilidade:** Uma **fraqueza explorável** (ex: sistema desatualizado, senha fraca).
- **Incidente:** A **materialização da ameaça** explorando a vulnerabilidade (ex: invasão, vazamento).
- **Risco:** **A possibilidade de um incidente ocorrer**, causando impacto (ex: perda de dados, prejuízo financeiro).

## Alvos comuns em um Ataque 

- Sistemas operacionais (Windows, Linux)
- Aplicações Web (Sites, APIs)
- Redes (Firewalls, roteadores, switches)
- Usuários finais (via phishing)
- Infraestrutura crítica (SCADA, IoT)

---

## Motivação dos Atacantes ⚠️

Entender a motivação ajuda a prever o comportamento do atacante e desenhar melhores defesas.

| **Motivo** | **Descrição** | **Exemplo** |
| --- | --- | --- |
| **Financeiro** | Buscam dinheiro via fraude ou extorsão. | Ransomware, roubo de cartão. |
| **Curiosidade / Desafio** | Testar habilidades. | Exploração de vulnerabilidades. |
| **Reputação / Ego** | Ganhar fama. | Deface de sites, vazamentos. |
| **Hacktivismo** | Protesto político/social. | Anonymous, ataques de governos ou empresas. |
| **Espionagem** | Obter dados confidenciais. | Empresas concorrentes, espionagem entre nações. |
| **Sabotagem / Guerra** | Danificar infraestrutura. | Ataques a hospitais, redes elétricas. |

---

## Tipos de Ataques Cibernéticos

Um ataque cibernético pode ocorrer de várias formas diferentes. Alguns atacam **sistemas**, outros exploram **pessoas**, e há os que envolvem **infraestrutura**.

### 1. Engenharia Social (Explora pessoas, não máquinas)

*"A engenharia social funciona porque o elo mais fraco é o ser humano."*

- **Phishing:** E-mail falso para enganar o usuário.
- **Spear Phishing:** Phishing personalizado para uma vítima específica.
- **Smishing:** Phishing via SMS.
- **Vishing:** Golpes por telefone.

### 2. Malware (Software malicioso)

- **Vírus:** Precisa ser executado; infecta arquivos.
- **Worm:** Autônomo; se replica pela rede sem necessidade de ação.
- **Trojan:** Finge ser algo útil, mas é malicioso (ex: “Jogo grátis” que rouba senhas).
- **Spyware:** Espiona o usuário sem que ele perceba.
- **Keylogger:** Registra tudo que o usuário digita.
- **Ransomware:** Sequestra dados e exige pagamento.

### 3. Ataques de Infraestrutura e Rede

- **DoS / DDoS:** Derruba sistemas com excesso de acessos simultâneos.
- **MITM (Man-in-the-Middle):** Intercepta a comunicação entre duas partes.
- **DNS Spoofing:** Redireciona o acesso para sites falsos.
- **Sniffing:** Captura dados que trafegam na rede.

### 4. Ataques às Aplicações Web

- **SQL Injection:** Comando malicioso inserido em campos de formulário.
- **XSS (Cross-site Scripting):** Injeção de scripts maliciosos em páginas web.
- **CSRF:** Ação maliciosa disfarçada como legítima.

### 5. Ataques modernos e complexos

- **APT (Threat Persistente Avançada):** Invasão problongada e sofisticada, geralmente por governos.
- **Ataque à Cadeia de Suprimentos:** Compromete um fornecedor para atacar clientes.
- **Ataques a IoT/Smart Services:** Invade câmeras, lâmpadas, roteadores e outros dispositivos.

### Classificação dos ataques

| **Tipo de Classificação** | **Exemplos** |
| --- | --- |
| Interno x Externo | Funcionário mal-intencionado vs. hacker |
| Ativo x Passivo | Modifica dados vs. apenas espiona |
| Direcionado x Oportunista | Um alvo específico vs. qualquer vítima |
| Manual x Automatizado | Feito por uma pessoa vs. via scripts |

---

## Exemplos de Ataques Reais

É fundamental entender o passado para se proteger no futuro.

Casos reais mostram como os ataques realmente acontecem:

- Revelam erros **humanos**, **falhas técnicas** e **brechas na organização**
- Mostram que **ninguém** está 100% seguro, nem grandes empresas.

*“Quem não conhece seus inimigos, perde a guerra antes de lutar.”* 

— Sun Tzu, A Arte da Guerra.

### 1. WannaCry (2017)

- **Tipo:** Ransomware global. Se espalhou no mundo em **poucas horas**.
- **Falha:** Explorava o *EternalBlue* (SMBv1), falha já corrigida pela Microsoft.
- **Cenário:** Mais de **200 mil computadores** foram infectados em **150 países**.
    - Hospitais no Reino Unido **cancelaram cirurgias** e **atendimentos**.
    - Empresas como **Telefônica (Espanha)** e **Renault (França)** interromperam operações.
- **Prejuízo:** Estimado em **U$ 4 Bilhões**.
- **Lição:** Manter sistemas atualizados é crítico.

### 2. SolarWinds (2020)

- **Tipo:** Ataque à cadeia de suprimentos (Supply Chain).
- **Método:** Invasão ao código de uma ferramenta de monitoramento confiável (Orion).
- **Impacto:** Afetou agências do governo dos EUA e grandes empresas (Microsoft, FireEye). Um update malicioso enviado para mais de **18.000** clientes.
- **Objetivo:** Espionagem avançada e acesso sigiloso a redes críticas.

### 3. Colonial Pipeline (2021)

- **Tipo:** Ransomware.
- **Cenário:** O grupo **DarkSide** invadiu a rede da **maior operadora de dutos de combust**í**vel dos EUA**.
    - A empresa suspendeu as operações por **quase uma semana**.
- **Impacto:** Interrupção do abastecimento de combustível nos EUA.
    - Filas Enormes em postos de gasolinas em vários estados.
    - **Aumento dos preços** dos combustível.
    - Desabastecimento temporário em alguns locais.
- **Custo:** Pagamento de US$ 4,4 milhões em criptomoedas.

### 4. **TSE** (Brasil, 2020)

- **Tipo:** Vazamento de Dados.
- **Impacto:** Divulgação de dados administrativos de servidores e ex-ministros.
- **Objetivo:** Deslegitimar o processo eleitoral e gerar desinformação.

### Outros casos

| **Caso** | **Tipo de ataque** | **Impacto** |
| --- | --- | --- |
| Facebook (2019) | Vazamento de dados | 533 milhões de contas |
| Yahoo (2013-2014) | Invasão + roubo de dados | 3 bilhões de contas |
| iFood (2021) | Engenharia Social | Golpes e pedidos indevidos |
| Descomplica (2023) | Exploração de API | Acesso a dados de usuários |

---

## Conclusões e Lições Aprendidas

1. **Segurança não é apenas problema técnico:** É estratégico e cultural.
2. **Não existe 100% seguro:** Nem grandes empresas nem órgãos públicos.
3. **Preparação e Prevenção:** São os melhores remédios.
4. **Cuidado com a negligência:** Falhas simples (como falta de atualização ou senhas fracas) são os vetores mais comuns.
5. **Reflexão:** "Quem não conhece seus inimigos, perde a guerra antes de lutar." (Sun Tzu). "Segurança começa com conhecimento."

---

### Material de Apoio 📚
* [O Ataque Hacker que Parou o Mundo | WannaCry](https://www.youtube.com/watch?v=Irwhxliiq30)
* [The Biggest Hack in US History: SolarWinds Hack (Ativar legendas)](https://www.youtube.com/watch?v=Eq6ATHhBezw)
* [Colonial Pipeline: como um ataque hacker paralisou um dos maiores oleodutos dos EUA](https://www.youtube.com/watch?v=L4qqFre-RxE)
