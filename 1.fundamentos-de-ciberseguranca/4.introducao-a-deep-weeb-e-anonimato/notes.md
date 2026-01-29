# 🕶️ Deep Web e Anonimização

Muitas vezes confundidos, os conceitos de Surface, Deep e Dark Web representam diferentes camadas de visibilidade e acesso à informação na rede mundial de computadores.

## 🧊 As Camadas da Internet

A internet pode ser visualizada como um iceberg, dividida pelo seu nível de indexação:

1.  **Surface Web (Web de Superfície):** É a camada que todos acessamos diariamente. Contém sites indexados por motores de busca como Google e Bing (ex: Wikipedia, portais de notícias).
2.  **Deep Web (Web Profunda):** Conteúdo que não é indexado por motores de busca. Isso inclui bases de dados acadêmicas, registros médicos, extratos bancários e páginas protegidas por senhas. É a maior parte da internet.
3.  **Dark Web:** Uma pequena parcela da Deep Web que é intencionalmente oculta e só pode ser acessada através de softwares específicos (como o Tor).

---

## 🛠️ Ferramentas de Anonimato

Para garantir a privacidade e o anonimato nessas camadas, utilizamos tecnologias específicas:

### 1. Tor Browser (The Onion Router)
O Tor funciona através de um sistema de "camadas de cebola", onde o tráfego é roteado por múltiplos servidores (nós) ao redor do mundo, ocultando a origem dos dados.
* **Domínios:** Sites na rede Tor geralmente possuem a extensão `.onion`.
* **Uso Ético:** Utilizado por jornalistas, ativistas e cidadãos em países com censura para garantir a liberdade de expressão.

### 2. Tails Linux (The Amnesic Incognito Live System)
Um sistema operacional focado em segurança e anonimato que pode ser executado via USB ou Máquina Virtual (VM).
* **Amnésico:** Por padrão, o Tails não salva nada no disco rígido; tudo o que você faz é apagado ao desligar o sistema.
* **Tudo via Tor:** Todas as conexões de saída são forçadas a passar pela rede Tor.

---

## 🔒 Práticas de Segurança e Privacidade

Navegar em camadas mais profundas exige cuidados redobrados para evitar a exposição de dados reais:

* **Uso de VPN com Tor:** Embora o Tor oculte o destino, o seu Provedor de Internet (ISP) pode saber que você está usando Tor. Uma VPN mascara esse fato.
* **Anonimização de Proxies:** Uso de servidores intermediários para esconder o endereço IP real.
* **Criptografia:** Essencial para garantir que, mesmo se os dados forem interceptados, não possam ser lidos (Princípio da Confidencialidade).

---

## ⚠️ Mitos e Verdades
* **Mito:** A Deep Web é um lugar exclusivo para crimes.
* **Verdade:** A maioria da Deep Web é composta por dados legítimos, como seus e-mails e arquivos no Drive, que apenas não devem estar abertos ao público geral do Google.

---
*Anotações baseadas nas aulas de Cassiano Peres - DIO / Santander Bootcamp.*