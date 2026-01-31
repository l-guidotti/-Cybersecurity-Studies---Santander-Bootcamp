# 🛡️ Projeto Prático: Simulação de Brute Force com Medusa

Este projeto documenta a execução de testes de intrusão controlados, simulando ataques de força bruta contra serviços comuns (FTP e SSH) para validar a robustez de políticas de autenticação.

## 🛠️ Ambiente de Laboratório
Para garantir a segurança e a ética, o teste foi realizado em um ambiente isolado[cite: 161]:
* **Atacante:** Kali Linux (VM).
* **Alvo:** Metasploitable 2 (VM vulnerável).
* **Rede:** Host-only (Interna) para evitar tráfego externo.



---

## 🚀 Passo a Passo da Execução

### 1. Reconhecimento (Scanning)
Antes do ataque, utilizei o **Nmap** para identificar os serviços ativos no alvo:
```bash
nmap -sV -p 21,22,80,445,139 192.168.56.101 [IP_DO_ALVO]
```

*Identificado: Porta 21 (FTP), Porta 22 (SSH) abertas, Porta 80  (HTTP) e Porta 445 (SMB)*

---

### 2. Preparação de Wordlists
Criei listas simplificadas de usuários e senhas para o teste:

* ```users.txt```: msfadmin, user, nroot, nadmin.

* ```pass.txt```: 123456, npassword, msfadmin, nqwerty.

---

### 3. Ataque de Força Bruta com Medusa
O Medusa é uma ferramenta de login modular, rápida e paralela. Utilizei o seguinte comando para testar o serviço FTP:

```Bash
medusa -h [IP_DO_ALVO] -U users.txt -P pass.txt -M ftp -t 6
```
Parâmetros utilizados:

```-h```: Endereço IP do host alvo.

```-U```: Caminho para o arquivo de lista de usuários.

```-P```: Caminho para o arquivo de lista de senhas.

```-M```: Módulo do protocolo a ser testado (ftp, ssh, smb, etc).

```-t```: Quantaidade de conexões/threads simultâneas o programa vai ser usado contra o alvo.

---

## 📊 Resultados e Validação

Durante os testes, o Medusa identificou credenciais válidas (ACCOUNT FOUND). O sucesso do ataque demonstra que o uso de senhas fracas ou padrões de fábrica é uma das maiores vulnerabilidades de um sistema.

--- 
## 🛡️ Recomendações de Mitigação
Para prevenir ataques de força bruta, recomendo as seguintes medidas:

1. **Políticas de Senhas Fortes**: Exigir complexidade mínima (letras, números e símbolos).
2. **Bloqueio de Conta (Account Lockout)**: Bloquear temporariamente o acesso após X tentativas falhas.
3. **Implementação de MFA**: Adicionar um segundo fator de autenticação.
4. **Uso de Fail2Ban**: Ferramenta que monitora logs e bane IPs que apresentam comportamento suspeito de brute force.

---
*Este projeto faz parte do Bootcamp Santander Cibersegurança - DIO.*