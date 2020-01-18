# Regras de Associação

São métodos de aprendizagem de máquina com objetivo de descobrir relações entre itens em uma grande base de dados. Geralmente são algoritmos simples que basicamente calculam a probabilidade de itens ocorrerem em um mesmo conjunto. 

A vantagem é que essa simplicidade torna esse conjunto de algoritmos mais acessível e transparente para as análises. 

Esses métodos podem ser empregados em diversas áreas, porém são mais utilizados e conhecidos para análise de vendas no varejo, onde nem sempre possível aplicar um modelo mais complexo devido a falta de dados atrelados aos clientes. Descobrir as relações entre itens comprados em conjunto podem ajudar para: Melhoras no layout da loja; Criações de promoções; Marketing; Venda cruzada (Cross-selling).

## Conceitos básicos

Antes de entrar nos algoritmos vamos apresentar alguns conceitos básicos utilizados em regras de associação.

### Regra de associação

Uma regra de associação é composta por um *antecendente* e um *consequente*, ambos consistem em conjunto de itens.

Por exemplo: {Pão, Manteiga} => {Leite}

### Suporte

O suporte indica quão frequente um conjunto de itens ocorre na base de dados. Se o suporte desse conjunto é muito pequeno significa que não temos informações suficiente para tirar conclusões dessa relação.

[Colocar fórmula do suporte]

### Confiança

A confiança indica o quão frequente a regra se mostrou válida. Porém a confiança para uma regra com um *consequente* muito frequente sempre será alta, portanto considerar somente o valor da confiança pode levar análises imprecisas sobre o negócio.

[Colocar fórmula do confiança]

### Lift

Representa o aumento em vendas do *consequente* dado o *antecendete*.

[Colocar fórmula do lift]

* Se o lift = 1, significa que não há correlação no conjunto
* Se o lift > 1, significa que há um correlação positiva no conjunto
* Se o lift < 1, significa que há um correlação negativa no conjunto

## Algoritmo

A extração das regras de associação consistem em dois passos:

### Geração dos conjuntos de itens

Nessa etapa procura-se apenas os conjuntos mais frequentes, sendo aqueles com o suporte acima de um limite. Aqui entra o algoritmo *Apriori*, que torna essa busca desses conjuntos mais eficiente.

Exemplo:

{Pão, Leite, Manteiga}, ...

### Geração das regras para cada conjunto

A identificação das regras nos conjuntos é menos custosa, são selecionadas as regras que estão acima de um limite mínimo de confiança.

{Leite, Manteiga -> Pão}

## Mão na massa

Nessa demonstração vamos usar os dados de uma loja online britanica, contendo transações durante o período de 01/12/2010 à 09/12/2011.


# Fontes

https://towardsdatascience.com/market-basket-analysis-978ac064d8c6
https://en.wikipedia.org/wiki/Association_rule_learning
https://towardsdatascience.com/association-rules-2-aa9a77241654
https://www.kaggle.com/carrie1/ecommerce-data