# 🏁 Desafio de Código: Detecção de Brute Force

Este desafio prático simula um mecanismo de segurança real: o monitoramento de tentativas de login para prevenir ataques de força bruta, bloqueando o acesso após um limite de falhas consecutivas.

## 📝 Enunciado
O objetivo é analisar uma lista cronológica de tentativas de autenticação ("sucesso" ou "falha") e determinar o status da conta.

* **Regra de Negócio:** Se houver **3 ou mais falhas consecutivas**, a conta deve ser bloqueada. 
* **Reset de Contador:** Uma tentativa de "sucesso" reseta o contador de falhas seguidas.

---

# 📝 Desafio 1

## 💻 Implementação Técnica (Python)

A solução utiliza um laço de repetição `for` com uma estrutura `else` (específica do Python), que só é executada se o loop terminar sem atingir um `break`.

```python
entrada = input().strip()  

# Processa a entrada para uma lista de strings
tentativas = [item.strip().lower() for item in entrada.split(',')]

falhas_consecutivas = 0

for tentativa in tentativas:
    if tentativa == "falha":
        falhas_consecutivas += 1
        
        # Verifica se atingiu o limite de segurança
        if falhas_consecutivas >= 3:
            print("Conta Bloqueada")
            break
    else:
        # Reset do contador em caso de sucesso
        falhas_consecutivas = 0  
else:
    # Caso o loop termine sem o 'break' (menos de 3 falhas seguidas)
    print("Acesso Normal")
```

---
### 🧠 Lógica e Cibersegurança
Este desafio exercita o pilar de Reconhecimento de Padrões do pensamento computacional:

* **Iteração**: Analisamos cada evento sequencialmente.
* **Estado**: Mantemos uma variável (falhas_consecutivas) para rastrear o estado atual da segurança.
* **Resposta a Incidentes**: O break simula a ação imediata de bloqueio assim que uma ameaça (padrão de brute force) é detectada.

---
# 📝 Desafio 2: Detecção de Injeção de Comando
O objetivo deste desafio foi criar um filtro de segurança para identificar caracteres especiais frequentemente utilizados por atacantes para encadear comandos maliciosos em sistemas vulneráveis.

Caracteres Monitorados:
* `;` (Ponto e vírgula): Usado para separar comandos.
* `&` (E comercial): Usado para execução em segundo plano ou encadeamento.
* `|` (Pipe): Redireciona a saída de um comando para a entrada de outro.
* `$` (Cifrão): Frequentemente usado para acessar variáveis de ambiente ou substituição de comandos.

## 💻 Implementação Técnica (Python)
A solução percorre os caracteres suspeitos definidos e verifica sua presença na string fornecida pelo usuário:

```Python
def verificar_comando(comando):
    # Lista de caracteres frequentemente usados em injeção de comandos
    caracteres_suspeitos = [';', '&', '|', '$']
    
    # Verifica se algum caractere da lista está presente na string do comando
    for char in caracteres_suspeitos:
        if char in comando:
            return "Comando Suspeito"
    
    # Se nenhum caractere for encontrado após percorrer toda a lista
    return "Comando Seguro"

# Entrada do usuário
comando_usuario = input()

# Exibe o resultado da verificação
print(verificar_comando(comando_usuario))
```

## 🛡️ Relação com Cibersegurança
Este desafio exemplifica a importância da validação de inputs. Em ataques reais, um usuário mal-intencionado poderia tentar algo como `cat file.txt; rm -rf /`. Sem essa verificação, o sistema leria o arquivo e, em seguida, tentaria apagar o diretório raiz.

A detecção desses "metacaracteres" é o primeiro passo para construir aplicações robustas e seguras contra explorações de injeção.

---
*Este desafio conclui as atividades práticas de Fundamentos de Pentest.*