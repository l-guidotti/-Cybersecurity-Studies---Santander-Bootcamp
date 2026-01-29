# 🔍 Coleta e Análise de Segurança Cibernética

A coleta de informações, também conhecida como **Footprinting** ou **Reconhecimento**, é a primeira etapa ativa de um Teste de Invasão. O objetivo é criar um mapa detalhado da infraestrutura, pessoas e tecnologias do alvo.

## 📡 OSINT (Open Source Intelligence)

A **Inteligência de Fontes Abertas** consiste na coleta de dados a partir de fontes públicas e acessíveis a qualquer pessoa
* **Fontes de Dados:** Redes sociais, registros de domínios, fóruns, documentos públicos e motores de busca.
* **Aplicações:** Identificar nomes de funcionários, e-mails corporativos, tecnologias utilizadas no site e subdomínios que possam estar esquecidos ou desprotegidos.

---

## 🏗️ Metodologias de Coleta

Existem duas abordagens principais para coletar dados de um alvo:

### 1. Reconhecimento Passivo
Consiste em coletar informações sem interagir diretamente com os sistemas do alvo. 
* **Vantagem:** É praticamente impossível de ser detectado pela vítima.
* **Exemplos:** Consultas em sites de busca, Whois e ferramentas de análise de DNS públicas.

### 2. Reconhecimento Ativo
Envolve a interação direta com os servidores e a rede do alvo para obter respostas mais precisas.
* **Risco:** Pode ser detectado por sistemas de monitoramento (IDS/IPS) e logs de servidores.
* **Exemplos:** Varredura de portas (Port Scanning) e enumeração de serviços.

---

## 🛠️ Ferramentas Essenciais no Kali Linux

O Kali Linux oferece um ecossistema completo para esta fase:

* **Nmap:** A ferramenta definitiva para varredura de rede, identificação de portas abertas e versões de serviços.
* **TheHarvester:** Excelente para coletar e-mails, nomes de subdomínios e hosts de diferentes fontes públicas.
* **Whois:** Utilizado para obter informações sobre a propriedade de domínios e faixas de IP.
* **Maltego:** Ferramenta gráfica para mineração de dados e mapeamento de relações entre pessoas, empresas e infraestruturas digitais.

---

## 📊 Análise de Dados
Após a coleta, o analista deve organizar as informações para identificar:
1.  **Vetores de Ataque:** Quais serviços estão mais expostos?
2.  **Superfície de Ataque:** Quantos IPs e domínios respondem pela empresa?
3.  **Falhas de Configuração:** Há serviços antigos ou desnecessários ativos?

---
*Anotações baseadas nas aulas de Coleta e Análise - DIO / Santander Bootcamp.*