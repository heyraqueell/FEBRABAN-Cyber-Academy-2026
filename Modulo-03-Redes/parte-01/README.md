# 📂 Módulo 03: Redes de Computadores e Segurança Cibernética (Parte 1)

### Objetivo Principal
Compreender os conceitos fundamentais que definem uma rede de computadores, identificando seus componentes estruturais, os principais termos técnicos associados à comunicação digital e as classificações de abrangência geográfica e interligação.

---

## 🌐 O que são rede de computadores?

- É uma **coleção de dispositivos interconectados que compartilham recursos e informações.** Esses dispositivos podem incluir *computadores*, *servidores*, *impressoras* e *outros hardwares*.
- A troca de informações caracteriza-se por qualquer envio ou recepção de dados. O compartilhamento de recursos ocorre quando uma máquina pode utilizar partes do hardware de outra, como HD, CD-ROM, drivers de disquete, impressoras etc.

## Componentes de uma Rede

A infraestrutura e os elementos conectados em uma arquitetura de rede dividem-se em quatro categorias básicas:

- **Dispositivos Finais, Intermediários e Mídias:** Dispositivos de uso direto do utilizador final como tablets, computadores, smartphones e portáteis.
- **Dispositivos de Infraestrutura:** Elementos essenciais para o direcionamento e segurança do tráfego, englobando servidores, roteadores, switches e firewalls.
- **Dispositivos de Escritório e Trabalho:** Hardwares utilitários integrados ao ambiente corporativo como desktops, impressoras de rede, câmeras de segurança, alarmes e sensores.
- **Dispositivos Pessoais e Domésticos (IoT):** Tecnologias do dia a dia conectadas à internet, incluindo televisores, eletrodomésticos (geladeiras, cafeteiras), carros conectados e centrais de ar-condicionado.

---

## 🧠 Definições Técnicas Iniciais

- **Mídia (Meio de transmissão):** **O caminho físico ou lógico pelo qual os dados trafegam.** Pode ser guiado/com fio *(cabos elétricos de cobre, cabos ópticos)* ou não guiado/sem fio *(radiofrequência, infravermelho e micro-ondas).*
- **Servidor:** Máquina ou programa que **oferece** um serviço ou recurso.
- **Cliente:** Máquinas ou aplicações que **utilizam** os serviços oferecidos e disponibilizados pelos servidores.
- **Host:** Qualquer máquina ou dispositivo computacional ativamente existente em uma rede que possua um endereço lógico, atuando como cliente ou servidor (Possui endereço de IP).
    - Exemplos de Host: PC’s, Notebooks, Smartphones, tablets…
- **Hostname:** O **apelido** ou **nome de identificação** amigável atribuído a uma máquina para **facilitar sua localização humana** sem a necessidade de decorar números.
- **NIC (Network Interface Card):** A placa de interface de rede. É o componente de hardware responsável por conectar o dispositivo à rede.
  <details>
  <summary>Clique aqui para ver exemplos de NIC (Integrada vs. Dedicada) 📸 </summary>
  <br>
  <p align="center">
    <img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/cc670c99-fb77-45dd-a3c9-87fc9c87d40b" />
    <br>
    <em>Comparação entre placas de rede integradas à placa-mãe (chipset) e placas de rede dedicadas (placas de expansão PCI).</em>
  </p>
  </details>
    

## Métricas de Performance e Tráfego

- **Bit:** Abreviação de **"dígito binário"** (0 ou 1). Representa a menor unidade de informação processada por um computador.
- **Largura de Banda (Bandwidth):** A **capacidade máxima teórica** de dados que podem fluir de um **ponto para outro** em um determinado intervalo de tempo. Ex:
    - Milhares de bits por segundo (Kbps - Kgbits por segundo).
    - Milhões de bits por segundo (Mbps - Megabits por segundo).
    - Bilhões de bits por segundo (Gbps - Gigabits por segundo).
- **Latência:** O tempo necessário para os dados viajarem de um ponto para o outro, incluindo todos os atrasos de processamento e propagação.
    - Ex: Quando assistimos um jogo de futebol e está atrasado.
- **Taxa de Transferência (Throughput):** A **quantidade real de bits transmitidos** com sucesso em um determinado período de tempo. Geralmente, a taxa real não corresponde à largura de banda máxima devido a interferências.
- **Protocolos:** Regras que definem estritamente como será a comunicação, o comportamento e o funcionamento de uma rede, evento ou serviço.

- ---

## 🗺️ Classificação das Redes: Abrangência Geográfica

As redes são tipificadas conforme o espaço territorial que conseguem cobrir:

| Tipo | Abrangência | Exemplos Práticos |
| :--- | :--- | :--- |
| **LAN** *(Local Area Network)* | Rede local de **curta** distância | Redes domésticas, escritórios, empresas e condomínios. |
| **MAN** *(Metropolitan Area Network)* | Rede metropolitana de **média** abrangência | Redes que interconectam diferentes filiais/sedes em uma mesma cidade ou região. |
| **WAN** *(Wide Area Network)* | Rede **global** de **grande** abrangência | Estruturas que cobrem países ou continentes inteiros. O maior exemplo é a Internet. |
<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/d1699256-ac94-474f-8dcb-b9279c5c1a15" alt="Redes LAN MAN WAN" width="580"></td>
    <td><img src="https://github.com/user-attachments/assets/0d17de40-0375-4cdd-a38a-c7251d4d22f4" alt="Esquema de Redes" width="600"></td>
  </tr>
</table>

---

## 🔗 Formas de Interligação de Redes

Dependendo do nível de acesso e privacidade, as redes organizam-se em:

* **Intranet:** Rede restrita a uma organização específica. Somente pessoas e computadores devidamente autorizados e autenticados possuem acesso aos servidores e informações internas.
* **Extranet:** Parte da intranet estendida e tornada acessível com restrições a um público externo controlado, tais como fornecedores, parceiros comerciais ou clientes estratégicos.
* **Internet:** A rede mundial de computadores. Consiste na interligação pública e global de milhares de redes de menor porte (intranets, extranets ou redes públicas).

---

## 📐 Topologias de Redes Locais (LAN)

A disposição física e lógica na qual os nós da rede estão interconectados estrutura-se em modelos clássicos:

* **Barramento (Bus):** Todos os dispositivos compartilham um único cabo central de comunicação.
* **Estrela (Star):** O modelo mais comum, onde todos os endpoints conectam-se individualmente a um dispositivo central concentrador (switch ou hub).
* **Anel (Ring):** Cada dispositivo possui duas conexões vizinhas diretas, formando um circuito fechado em formato circular.
* **Malha (Mesh):** Dispositivos interconectados entre si de forma redundante, garantindo que os dados encontrem caminhos alternativos se um link falhar.
* **Árvore (Tree):** Estrutura hierárquica baseada na combinação de várias topologias em estrela ligadas a um barramento central.
* **Híbrido:** Redes complexas que misturam duas ou mais topologias diferentes para atender às necessidades específicas da infraestrutura.
<img width="1408" height="768" alt="image" src="https://github.com/user-attachments/assets/9a2c6125-660c-42ec-be9c-1a8e812ee742" />



---

## 🔀 Classificação dos Fluxos de Transmissão

Os dados movem-se pelos canais de comunicação através de três modos de fluxo:

* **Modo Simplex:** Transmissão estritamente **unidirecional**. Os dados viajam em apenas um sentido, sem retorno. *Exemplo:* Transmissão de televisão ou rádio convencional.
* **Modo Half-Duplex:** Transmissão **bidirecional**, porém não simultânea. Ambos os pontos transmitem e recebem dados, mas apenas um de cada vez. *Exemplo:* Rádio Amador / Walkie-Talkie.
* **Modo Full-Duplex:** Transmissão **bidirecional simultânea**. Ambos os dispositivos podem enviar e receber dados ao mesmo tempo pelo canal. *Exemplo:* Chamada telefônica.

---

## 📢 Métodos de Difusão de Dados

Determina como os pacotes de dados são endereçados aos alvos na rede:

* **Unicast:** A mensagem é transmitida de forma direta e exclusiva de um **único** emissor para um único destinatário específico.
* **Multicast:** A mensagem é direcionada e entregue apenas a um **grupo** específico e selecionado de máquinas associadas àquele serviço.
* **Broadcast:** A mensagem é replicada e transmitida para absolutamente **todos** os dispositivos e hosts conectados naquela mesma rede.

---
## Para não confundir
Fluxo de Transmissão vs. Difusão de Dados

* Fluxo refere-se ao caminho/direção (como os dados viajam).
* Difusão refere-se ao endereçamento/destino (quem recebe os dados).
