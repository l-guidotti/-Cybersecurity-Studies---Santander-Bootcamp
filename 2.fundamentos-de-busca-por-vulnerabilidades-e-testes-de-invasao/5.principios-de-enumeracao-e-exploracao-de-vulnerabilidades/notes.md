# 🔍 Princípios de Enumeração e Exploração

A enumeração é a fase onde o auditor estabelece conexões ativas com o alvo para descobrir informações detalhadas sobre a infraestrutura. Diferente da varredura geral, a enumeração busca dados específicos que possam ser usados diretamente em um ataque.

## 🎯 Objetivos da Enumeração
* **Usuários e Grupos:** Identificar nomes de contas válidas no sistema. 
* **Compartilhamentos de Rede:** Localizar pastas e recursos compartilhados (SMB/NFS).
* **Tabelas de Roteamento:** Entender como a rede interna está estruturada.
* **Serviços de Diretório:** Extrair informações de Active Directory ou LDAP.

---

## 🛠️ Serviços Comuns para Enumeração

Cada protocolo de rede oferece diferentes oportunidades de extração de dados:

### 1. SMB (Server Message Block) - Portas 139/445
Muito comum em ambientes Windows, permite enumerar usuários e compartilhamentos. 
* **Ferramentas:** `enum4linux`, `smbclient`, `nbtscan`.

### 2. SNMP (Simple Network Management Protocol) - Porta 161
Se mal configurado (com strings de comunidade padrão como "public"), pode revelar informações sobre hardware e softwares instalados. 

### 3. HTTP/HTTPS - Portas 80/443
Enumeração de diretórios e arquivos ocultos para encontrar painéis administrativos ou backups.
* **Ferramentas:** `Dirb`, `Gobuster`, `Wfuzz`.

---

## 🚀 Exploração de Vulnerabilidades

Após a enumeração, o auditor busca por falhas conhecidas (CVEs) que correspondam às versões de software encontradas.


### Pontuação de Gravidade (CVSS)
As vulnerabilidades são classificadas pelo **Common Vulnerability Scoring System (CVSS)**, variando de 0 a 10:
* **Baixa/Média:** Exige condições específicas ou acesso físico.
* **Alta/Crítica:** Pode permitir execução remota de código (RCE) sem autenticação.

### O Framework Metasploit
A ferramenta mais utilizada para automação de explorações. Ela organiza o ataque em:
1. **Exploit:** O código que aproveita a falha.
2. **Payload:** O que será executado no alvo após a invasão (ex: uma Reverse Shell).
3. **Auxiliary:** Módulos de varredura e enumeração.

---

## ⚠️ Pós-Exploração e Ética
O objetivo do Pentest não é apenas "invadir", mas provar o impacto. Após ganhar acesso, o auditor deve verificar:
* Quais dados estão acessíveis?
* É possível realizar movimentação lateral para outros servidores?

**Lembre-se:** Toda ação deve estar dentro do escopo do contrato.

---
*Anotações baseadas nas aulas de Enumeração e Exploração - DIO / Santander Bootcamp.*