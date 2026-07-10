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

## 🔄 Fluxo de Comunicação na Rede

A transferência de dados entre um cliente (Web Client) e um servidor (Web Server) ocorre em duas vias complementares:

### Processo de Encapsulamento (Origem)
O dado gerado pelo usuário na camada de Aplicação desce o modelo recebendo "envelopes" sucessivos:
1. O Dado vira um **Segmento TCP** na camada de Transporte (ganha informações de portas).
2. O Segmento vira um **Pacote IP** na camada de Rede (ganha endereços IP de origem e destino).
3. O Pacote vira um **Quadro Ethernet** na camada de Link de Dados (ganha endereços MAC físicos).
4. O Quadro é convertido em **Bits (0 e 1)** e enviado pelos cabos ou ar na camada Física.

### Processo de Desencapsulamento (Destino)
Ao chegar no host de destino, o processo é invertido: o dispositivo lê a mensagem da camada física para a aplicação, removendo os cabeçalhos de controle camada por camada ("abrindo os envelopes") até entregar o dado puro para o sistema final.
