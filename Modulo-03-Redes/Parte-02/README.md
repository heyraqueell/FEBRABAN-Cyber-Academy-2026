# Aula 3.2: Principais Protocolos de Rede

### Objetivo Principal
Compreender o conceito de protocolos de comunicação, a estrutura de encapsulamento e desencapsulamento de dados, bem como o mapeamento e as funções das camadas dos modelos de referência OSI e TCP/IP.

---

## 📜 O que são Protocolos de Comunicação?

Protocolos são regras ou padronizações que permitem que os dados sejam transmitidos e entendidos corretamente por diferentes dispositivos e sistemas em uma rede. 

Eles determinam o formato (a estrutura), o tamanho, o tempo, a codificação, o encapsulamento e o padrão das mensagens. Esses padrões são desenvolvidos, publicados e mantidos por diversas organizações internacionais para garantir a interoperabilidade global.

---

## 🧱 Modelos de Referência: OSI vs. TCP/IP

Para organizar como a comunicação ocorre, a tecnologia utiliza modelos divididos em camadas:

* **Modelo OSI (Open Systems Interconnection):** É uma abstração teórica com 7 camadas. Funciona como uma referência didática fundamental para entender o papel de cada etapa na construção de redes, protocolos e ferramentas de segurança.
* **Modelo TCP/IP:** É um modelo funcional prático composto por 4 camadas principais que agrupam funções do modelo OSI. É o padrão de fato que move a Internet atual e serve de base para as implementações modernas.
<details>
<summary><b>Entendendo o Modelo OSI e TCP/IP</b></summary>

O modelo de camadas é como um <b>sistema de correios</b> para dados digitais. Ele organiza a comunicação em etapas independentes para garantir que, quando você acessa um site, a informação saia do seu computador, atravesse o mundo e chegue ao destino de forma organizada.

### Por que usar camadas?
* **Padronização:** Permite que dispositivos de diferentes marcas (Apple, Dell, Cisco) se comuniquem perfeitamente.
* **Manutenção:** Se a rede falha, você consegue isolar o problema (ex: se o cabo está rompido, o problema é na Camada 1, sem afetar o software).
* **Modularidade:** Podemos melhorar ou mudar uma camada (como trocar um cabo de cobre por fibra óptica) sem precisar mudar o funcionamento das camadas superiores (aplicações).
<img width="1748" height="666" alt="image" src="https://github.com/user-attachments/assets/72ad6281-1f7f-4fc3-bf53-b0e236d0f814" />

</details>

---

## 📐 Encapsulamento de Dados

O encapsulamento é o processo de colocar um formato de mensagem (como uma carta) dentro de outro formato de transporte (como um envelope) à medida que ele desce pelas camadas da rede.


### Estrutura Básica de uma PDU (Protocol Data Unit)
Cada camada adiciona suas próprias informações de controle ao dado original, criando uma unidade chamada PDU, dividida em:
* **Cabeçalho (Header):** Contém as **informações de controle** e direcionamento exigidas pelo protocolo daquela camada.
* **Payload (Carga Útil):** Armazena os **dados reais** vindos da camada anterior que precisam trafegar entre os hosts.

<img width="1018" height="756" alt="image" src="https://github.com/user-attachments/assets/ba7eba4d-85a7-4575-af70-3b68823594d8" />


---

## 🗂️ Mapeamento e Funções das Camadas

Abaixo está a divisão combinada dos modelos OSI e TCP/IP, especificando o nome da unidade de dados (PDU) e as funções de cada nível:

| Camada OSI | Nome da Camada | PDU | Função Principal | Common Protocols |
| :---: | :--- | :--- | :--- | :--- |
| **7** | Aplicação | Dado (*Data*) | Serviços de rede para aplicações finais (e-mail, web, transferência de arquivos). | HTTP, SMTP, DHCP, DNS |
| **6** | Apresentação | Dado (*Data*) | Formatação de dados, compressão, criptografia e tradução de códigos. | ASCII, JPEG, MP3, SSL |
| **5** | Sessão | Dado (*Data*) | Estabelecimento, gerenciamento e encerramento de sessões entre aplicações. | RPC, NetBIOS, SMB |
| **4** | Transporte | Segmento / Datagrama | Entrega ponta a ponta, controle de fluxo, portas e tratamento de erros. | TCP, UDP |
| **3** | Rede | Pacotes (*Packets*) | Endereçamento lógico (IP) e determinação da melhor rota (roteamento). | IPv4, IPv6, ARP, ICMP |
| **2** | Link de Dados | Quadros (*Frames*) | Endereçamento físico (MAC) e controle de acesso ao meio físico. | Ethernet, PPP |
| **1** | Física | Bits | Transmissão de bits brutos sobre o meio físico (cabos de cobre, rádio, fibra). | RJ-45, RS-232, USB |

---

## Protocolo de Internet (IP) 🌐
O IP é o protocolo fundamental da família TCP/IP, responsável pelo endereçamento lógico na Camada de Rede.

### Características Principais
* **Independência:** Possui as versões v4 e v6, que coexistem para garantir a conectividade global.
* **Não Confiável:** Não garante a entrega, integridade ou correção de pacotes.
* **Sem Conexão:** Não estabelece sessão prévia; pacotes podem seguir caminhos diferentes ou chegar duplicados.
* **Endereçamento:** Atribui um endereço lógico ao dispositivo. Divide-se em duas partes: **Rede** e **Host**.
* **Protocolo Auxiliar:** Precisa ser associado ao **TCP** (confiabilidade) ou **UDP** (velocidade).
* **TTL (Time to Live) / Limite de Salto:** Indicador no cabeçalho que define por quantos roteadores um pacote pode passar antes de ser descartado, evitando *loops* infinitos.

## 🌐 Diferenças do IPv4 e IPv6

Devido ao esgotamento do padrão original (IPv4), o IPv6 foi desenvolvido para suportar a expansão global de dispositivos.

### IPv4 (Internet Protocol version 4)

- **Exemplo:** `192.168.1.10`
- **Estrutura:** Baseado em 32 bits, dividido em quatro octetos.
- **Representação:** Utiliza valores decimais (de 0 a 255 por octeto).
- **Capacidade:** Aproximadamente 4,3 bilhões de endereços únicos.
- **Limitação:** O esgotamento de endereços disponíveis é o seu maior desafio, motivando a transição para o IPv6;

### IPv6 (Internet Protocol version 6)

- **Exemplo:** `2001:0db8:85a3:0000:0000:8a2e:0370:7334`
- **Estrutura:** Baseado em **128** **bits.**
- **Representação:** Utiliza valores **hexadecimais**.
- **Capacidade:** Aproximadamente **340 undecilhões** de endereços. Essencial para o crescimento massivo de dispositivos IoT.
- **Vantagens:** Além da vasta capacidade, oferece recursos nativos de segurança e melhor rastreabilidade.

---

## Protocolo ICMP (Internet Control Message Protocol)
Atua na Camada de Rede como auxiliar do IP, sendo crucial para o diagnóstico da rede.

* **Função:** Notifica erros quando roteadores ou servidores encontram problemas ao processar/entregar pacotes.
* **Diagnóstico:** Base para ferramentas de verificação de conectividade, como **Ping** (testa se o destino é alcançável) e **Traceroute** (mede latência e caminhos).

---

## Distribuição de endereços IP no mundo
<img width="656" height="403" alt="image" src="https://github.com/user-attachments/assets/78e29e54-1754-4457-9411-0e4c1536d0c8" />

---
## Camada de Transporte: TCP vs. UDP

### TCP (Transmission Control Protocol)
Focado na **confiabilidade**.

* **Orientado a Conexão:** Estabelece e mantém a conexão entre cliente e servidor (*Three-Way Handshake*).
* **Entrega Confiável:** Reenvia informações não recebidas e mantém a ordem correta.
* **Controle de Fluxo:** Gerencia a velocidade de transmissão para evitar sobrecarga.
* **Alto processamento:** Exige maior carga computacional devido aos mecanismos de verificação e confirmação.
<img width="1876" height="684" alt="image" src="https://github.com/user-attachments/assets/52ef9510-95d5-46d5-a39c-60bad6ca5cb6" />


**Three-Wat Handshake**: Processo de três etapas para estabelecer uma conexão segura e sincronizada.

### UDP (User Datagram Protocol)
Focado na **velocidade**.

- **Sem conexão:** Envia dados diretamente, sem estabelecer sessão prévia.
- **Baixa sobrecarga:** Cabeçalho simples com apenas 4 campos, exigindo pouco processamento do sistema.
- **Sem confirmação:** Não exige confirmação de recebimento (ACK) e não realiza reenvio de pacotes perdidos.
- **Uso típico:** Transmissões em tempo real, onde a latência é crítica (Streaming de vídeo, VoIP, jogos, Consultas DNS).

---

## Portas e *Sockets*
As portas permitem que um computador execute múltiplas aplicações simultaneamente, direcionando o tráfego para o serviço correto. Um **Socket** é a combinação do Endereço IP + Porta.

| **Grupo** | **Intervalo** | **Descrição** |
| --- | --- | --- |
| **Portas Bem Conhecidas** | 0 a 1023 | Reservadas para serviços **comuns** (Web, E-mail, Acesso Remoto). Permitem que clientes identifiquem facilmente o serviço associado necessário ao servidor. |
| **Portas Registradas** | 1024 a 49151 | Atribuídas pela IANA a processos ou aplicativos específicos instalados pelo usuário. |
| **Privadas / Dinâmicas** | 49152 a 65535 | Conhecidas como **portas efêmeras**. Atribuídas dinamicamente pelo sistema operacional para identificar o cliente na sessão. |

---

## Camada de Aplicação

### DNS (Domain Name System)
Serviço fundamental que traduz nomes de domínios (amigáveis para humanos) em endereços IP (usados pelas máquinas).

### HTTP e HTTPS
* **HTTP:** Protocolo da web. Transmite dados de forma clara (não criptografada).
* **HTTPS:** Versão segura do HTTP, utilizando criptografia.
* **Principais Métodos:**
    * `GET`: Recupera arquivos/recursos.
    * `POST`: Envia/cria novos recursos.
    * `PUT`: Atualiza recursos existentes.
    * `DELETE`: Remove recursos.

---
📚 Materiais de Apoio
* Professora Nattane: https://www.youtube.com/watch?v=gMzka2WM80k&list=WL&index=21&t=740s 
