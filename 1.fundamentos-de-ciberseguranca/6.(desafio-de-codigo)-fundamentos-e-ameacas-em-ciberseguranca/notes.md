# 🏁 Desafios de Código: Fundamentos e Ameaças

Este diretório contém a resolução de dois desafios práticos focados em consolidar os conceitos de controle de acesso e identificação de ameaças cibernéticas através de lógica de programação.

---

## 📝 Desafio 1: Autenticação e Autorização
O objetivo foi criar um sistema de consulta que associa conceitos de controle de acesso às suas definições técnicas.

### Conceitos Mapeados:
* **Autenticação:** Verificação da identidade de um usuário.
* **Autorização:** Permissão para acessar recursos específicos.
* **MFA:** Verificação usando múltiplos fatores de segurança.
* **OAuth:** Padrão aberto para delegar acesso sem compartilhar senha.

---

## 📝 Desafio 2: Tipos de Ataques Cibernéticos
Neste desafio, o foco foi identificar e descrever os vetores de ataque mais comuns enfrentados por profissionais de segurança.

### Ameaças Mapeadas:
* **Phishing:** Enganar usuários para roubar informações sensíveis.
* **DDoS:** Atacar um serviço com muitos acessos para derrubá-lo.
* **Malware:** Software malicioso projetado para causar danos.
* **Engenharia Social:** Manipulação psicológica para obter acesso ou dados.

---

## 💻 Implementação Técnica (Python)

Abaixo, a solução consolidada utilizando estruturas condicionais para o mapeamento das descrições:

```python
# Entrada do usuário
entrada = input()

# Função para descrever conceitos de acesso (Desafio 1)
def descrever_conceito(conceito):
    if conceito == "Autenticação":
        return "Verificação da identidade de um usuário"
    elif conceito == "Autorização":
        return "Permissão para acessar recursos específicos"
    elif conceito == "MFA":
        return "Verificação usando múltiplos fatores de segurança"
    elif conceito == "OAuth":
        return "Padrão aberto para delegar acesso sem compartilhar senha"

# Função para descrever tipos de ataque (Desafio 2)
def descrever_ataque(ataque):
    if ataque == "Phishing":
        return "Enganar usuários para roubar informações sensíveis"
    elif ataque == "DDoS":
        return "Atacar um serviço com muitos acessos para derrubá-lo"
    elif ataque == "Malware":
        return "Software malicioso projetado para causar danos"
    elif ataque == "Engenharia Social":
        return "Manipulação psicológica para obter acesso ou dados"

# Execução (conforme o contexto do desafio atual)
print(descrever_conceito(entrada))
print(descrever_ataque(entrada))