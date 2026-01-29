# 💻 Sistemas Operacionais e Virtualização

Sistemas Operacionais (SO) são softwares que atuam como intermediários entre o usuário e o hardware do computador. Em cibersegurança, dominar diferentes SOs é vital para realizar análises forenses e testes de invasão.

## 🏗️ Estrutura e Componentes de um SO

Para executar tarefas, os sistemas operacionais dependem de dois componentes principais:

* **Shell:** Camada mais externa que gerencia a interação entre o usuário e o sistema, tratando entradas e saídas.
* **Kernel:** Núcleo central do SO que atua como interface direta entre o sistema e o hardware, gerenciando CPU, memória e dispositivos


### Funções Essenciais
* **Gerenciamento de Processos:** Execução e escalonamento de aplicativos.
* **Gerenciamento de Memória:** Controle de cache, memória primária e secundária.
* **Segurança:** Implementação de recursos nativos para proteção de dados e detecção de erros.

---

## 🖥️ Microsoft Windows vs. 🐧 Linux

### Microsoft Windows
* Padrão global para computadores domésticos e empresariais.
* Baseado em Interface Gráfica (GUI) e escrito majoritariamente em C/C++.
* **Alvo Crítico:** Devido à sua popularidade, é o principal alvo de ameaças cibernéticas.

### Linux (O Núcleo da Segurança)
* Sistema *Open Source* baseado no Kernel originalmente escrito por Linus Torvalds.
* **Distribuições (Distros):** Diversas variações criadas para fins específicos (ex: Debian, Ubuntu, Mint).
* **Análise de Risco:** Vulnerabilidades são rastreadas pelo **CVSS** (Common Vulnerability Scoring System), que atribui pontuações de 0 a 10 conforme a gravidade.

---

## ☁️ Virtualização com VirtualBox

A virtualização consiste em executar um sistema operacional isolado sobre outro SO, consumindo recursos de hardware de forma controlada.


### Por que usar VMs em Cybersecurity?
1.  **Isolamento:** Execução de malwares ou ferramentas de hacking em um ambiente "Sandbox", sem risco ao sistema anfitrião.
2.  **Laboratórios:** Criação de redes internas para simular ataques e defesas.
3.  **Kali Linux:** O padrão para testes de invasão e pentest, contendo ferramentas nativas como **Nmap**, **Metasploit** e **Wireshark**.
---
<br>

*Anotações baseadas nas aulas de Cassiano Peres - DIO / Santander Bootcamp.*