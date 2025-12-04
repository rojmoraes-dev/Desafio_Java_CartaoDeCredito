# Desafio: Controle de Compras com Cartão de Crédito 💳

Projeto prático para implementar um sistema simples de registro de compras em um cartão de crédito utilizando **Java**.

## Objetivo do Projeto

Criar uma aplicação console que permita ao usuário:
- Definir o limite do cartão de crédito
- Registrar compras enquanto houver saldo disponível
- Visualizar o resultado de cada tentativa de compra
- Ao final, exibir o saldo restante e a lista de compras realizadas ordenada por valor

## Requisitos Funcionais Implementados

### 1. Classe `Compra`
- Representa uma compra realizada
- Atributos:
  - `String descricao`
  - `double valor`
- Construtor que recebe descrição e valor
- Getters necessários
- Implementado `Comparable<Compra>` para ordenação por valor

### 2. Classe `CartaoCredito`
- Representa o cartão de crédito
- Atributos:
  - `double limite`
  - `double saldo` (inicia com o valor do limite)
  - `List<Compra> compras`
- Construtor que recebe o limite inicial
- Método `lancarCompra(Compra compra)` que:
  - Verifica se há saldo suficiente
  - Se sim: adiciona a compra à lista e subtrai do saldo → retorna `true`
  - Se não: não altera nada → retorna `false`

### 3. Classe `Principal` (com método `main`)
Deve seguir exatamente esta sequência:

1. Solicitar o limite do cartão ao usuário
2. Instanciar o `CartaoCredito` com o limite informado
3. Entrar em um loop enquanto o usuário quiser continuar comprando:
   - Pedir descrição da compra
   - Pedir valor da compra
   - Criar objeto `Compra`
   - Tentar registrar a compra no cartão
   - Exibir mensagem: **"Compra realizada!"** ou **"Saldo insuficiente!"**
4. Quando o usuário decidir parar:
   - Exibir mensagem de encerramento
   - Mostrar o **saldo restante** do cartão
   - Listar todas as compras realizadas **ordenadas por valor (crescente)**

## Observações:
- Utilizada a classe Scanner para fazer a leitura das informações do usuário;
- Utilizado construtores nas classes para passar as informações ao instanciar um objeto.
