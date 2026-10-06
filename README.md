# Projeto Conceitual de Banco de Dados - E-commerce

Refinamento de um modelo conceitual de e-commerce, feito no MySQL Workbench para o desafio da DIO.

## Diagrama

## Objetivo do desafio
Refinar o modelo acrescentando:
- *Cliente PJ e PF:* uma conta pode ser PJ ou PF, mas não pode ter as duas informações.
- *Pagamento:* pode ter mais de uma forma de pagamento cadastrada.
- *Entrega:* possui status e código de rastreio.

## Como foi resolvido
- *Cliente PF/PJ:* a tabela Cliente guarda os dados comuns e o campo Tipo_cliente ('PF' ou 'PJ'). Cliente_PF (CPF) e Cliente_PJ (CNPJ e razão social) se ligam a ela em relação 1:1, com Cliente_idCliente único. Assim, cada cliente é de um só tipo.
- *Pagamento:* relação 1:N com Cliente, então um cliente pode ter várias formas de pagamento.
- *Entrega:* relação 1:N com Pedido, com Status e Codigo_de_Rastreio.
