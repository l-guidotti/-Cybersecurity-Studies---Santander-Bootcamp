# 📡 Conceitos e Técnicas de Varredura de Rede

A varredura de rede (ou *Scanning*) é o processo de identificação de hosts ativos, portas abertas e serviços disponíveis em uma rede. É uma etapa de reconhecimento ativo que visa encontrar vetores de ataque exploráveis.

## 🎯 Objetivos da Varredura
* **Identificar Hosts Ativos:** Descobrir quais dispositivos estão ligados e respondendo na rede.
* **Mapeamento de Portas:** Verificar quais portas (TCP/UDP) estão abertas, fechadas ou filtradas por firewalls.
* **Fingerprinting de SO:** Identificar qual sistema operacional e versão estão sendo utilizados pelo alvo.
* **Enumeração de Serviços:** Listar os softwares e versões que rodam em cada porta (ex: Apache 2.4.41 na porta 80).

---

## 🛠️ O Protocolo ICMP e Varredura
O ICMP (*Internet Control Message Protocol*) é frequentemente utilizado para verificar a conectividade inicial.
* **Ping Scan:** Utiliza mensagens *Echo Request* e *Echo Reply* para determinar se um host está "vivo".
* **Limitação:** Muitos firewalls modernos bloqueiam o ICMP para evitar esse tipo de descoberta.

---

## 🛡️ Nmap: A Ferramenta Definitiva
O **Nmap (Network Mapper)** é a ferramenta padrão da indústria para varreduras. Ela permite desde verificações rápidas até mapeamentos complexos que burlam sistemas de detecção.



### Comandos Comuns e Técnicas:
* **TCP Connect Scan (`-sT`):** Realiza o *Three-Way Handshake* completo. É mais lento e fácil de detectar.
* **SYN Stealth Scan (`-sS`):** Conhecido como "meio-aberto". Não completa a conexão, tornando-o mais silencioso.
* **UDP Scan (`-sU`):** Utilizado para identificar serviços como DNS, DHCP e SNMP.
* **Varredura de Versão (`-sV`):** Interage com a porta para descobrir a versão exata do serviço.
* **Identificação de SO (`-O`):** Tenta adivinhar o Sistema Operacional baseado na resposta do stack TCP/IP.

---

## ⚠️ Detecção e IDS/IPS
Varreduras agressivas podem ser facilmente detectadas por sistemas de:
* **IDS (Intrusion Detection System):** Monitora o tráfego e alerta sobre atividades suspeitas.
* **IPS (Intrusion Prevention System):** Além de detectar, pode bloquear automaticamente o IP que está realizando a varredura.

**Boas Práticas:** Em um Pentest ético, ajuste o "timing" da varredura (`-T0` a `-T5` no Nmap) para evitar sobrecarregar o sistema do cliente ou ser bloqueado precocemente.

---
*Anotações baseadas nas aulas de Varredura de Rede - DIO / Santander Bootcamp.*