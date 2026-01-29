# 🌐 Fundamentos de Redes de Computadores

Redes de computadores são sistemas de dispositivos interconectados que trocam dados e compartilham recursos entre si através de protocolos de comunicação. Em cibersegurança, entender redes é essencial para identificar como as ameaças se propagam e como bloqueá-las.

## 📡 Classificação de Redes (Abrangência)

As redes são classificadas pela sua escala geográfica:
* **PAN (Personal Area Network):** Dispositivos de uso pessoal (ex: Bluetooth).
* **LAN (Local Area Network):** Redes locais em residências ou escritórios.
* **MAN (Metropolitan Area Network):** Conecta redes dentro de uma cidade.
* **WAN (Wide Area Network):** Redes de longa distância, como a própria Internet.

---

## 🏗️ Topologias de Rede

A topologia define como os dispositivos estão conectados fisicamente ou logicamente:
* **Barramento (Bus):** Todos os nós conectados a um cabo central (backbone).
* **Anel (Ring):** Cada dispositivo tem dois vizinhos, formando um círculo.
* **Estrela (Star):** Todos os nós se conectam a um hub ou switch central (a mais comum em redes modernas).
* **Malha (Mesh):** Dispositivos conectados entre si, oferecendo alta redundância.

---

## 📑 Protocolos e Endereçamento

Os protocolos são as "regras" da comunicação. Os principais citados no curso são:

### Endereço IP (Internet Protocol)
É o rótulo numérico atribuído a cada dispositivo em uma rede:
* **IPv4:** Formato de 32 bits (ex: 192.168.0.1).
* **IPv6:** Formato de 128 bits, criado para suprir a escassez de endereços IPv4.
* **Máscara de Sub-rede:** Define qual parte do IP refere-se à rede e qual refere-se ao host.

### Protocolos de Aplicação
* **HTTP/HTTPS:** Navegação web (HTTPS utiliza criptografia).
* **FTP:** Transferência de arquivos.
* **SMTP/POP3/IMAP:** Protocolos de e-mail.
* **DNS:** Traduz nomes de domínios (google.com) em endereços IP.

---

## 🔒 Privacidade e Segurança na Rede

Para proteger a identidade e os dados durante o tráfego, utilizamos:

### 1. Proxy
Um servidor intermediário que faz requisições em nome do cliente.
* **Uso em Segurança:** Esconde o IP real do usuário e pode filtrar conteúdo malicioso.

### 2. VPN (Virtual Private Network)
Cria um túnel criptografado entre o dispositivo e a internet.
* **Vantagem:** Impede que atacantes "escutem" a transmissão (Sniffing) e oculta o tráfego do Provedor de Internet (ISP).

---

## 🔍 Exemplo Prático de Cibersegurança
Uma técnica comum de ataque em redes é o **Man-in-the-Middle (MitM)**, onde o atacante se posiciona entre a vítima e o roteador para interceptar dados. O uso de **VPNs** e o protocolo **HTTPS** são as defesas primárias contra esse tipo de interceptação.

---
*Anotações baseadas nas aulas de Cassiano Peres - DIO / Santander Bootcamp.*