---
title: "FUN-05 · Função afim"
id: FUN-05
trilha: Funções
nivel: Básico
serie: "1ª"
pre_requisitos: [FUN-04, EF-07]
destrava: [FUN-06, FUN-07, FUN-11, FUN-15, FIN-03, SEQ-02, GAN-02]
rota_calculo: sim
bncc: a confirmar
semestre: S1
description: "Função afim: lei, coeficientes e taxa de variação. Trilha Funções, nível básico, 1ª série do Ensino Médio."
draft: false
tags: [funcoes, basico, rota-calculo, pronto]
---

> [!question] A pergunta
> Um aplicativo de corridas cobra R\$ 5,00 fixos mais R\$ 3,00 por quilômetro (valores fictícios). Quanto custa uma corrida de 12 km? E uma de $x$ km?

## Por que faz sentido
Monte uma tabela:

| km ($x$) | 0 | 1 | 2 | 3 | 4 |
|---|---|---|---|---|---|
| preço ($y$, em R\$) | 5 | 8 | 11 | 14 | 17 |

A cada quilômetro a mais, o preço sobe sempre R\$ 3,00: os degraus são iguais. Com 0 km, sobra só a parte fixa, R\$ 5,00. Então o preço é "3 vezes os quilômetros, mais 5":

$$y = 3x + 5$$

Para 12 km: $3 \cdot 12 + 5 = 41$, ou seja, R\$ 41,00.

No gráfico, cada passo de 1 para a direita sobe sempre 3. Degraus iguais formam uma reta, e é por isso que o gráfico de uma função afim é uma reta.

## Ideia central
Uma função afim tem a forma

$$f(x) = ax + b, \qquad a, b \in \mathbb{R}$$

- $a$ é a **taxa de variação**: quanto $f(x)$ muda quando $x$ aumenta 1. Para quaisquer $x_1 \neq x_2$:
$$a = \frac{f(x_2) - f(x_1)}{x_2 - x_1}$$
- $b = f(0)$ é o **valor inicial**: o ponto em que o gráfico corta o eixo $y$.
- $a > 0$: crescente. $a < 0$: decrescente. $a = 0$: constante (alguns livros não chamam a função constante de afim).
- Se $b = 0$, a função é **linear**: $y$ é proporcional a $x$.

## Exemplo resolvido
Uma função afim tem $f(2) = 7$ e $f(5) = 16$. Qual é a lei?

1. Taxa de variação: $a = \dfrac{16 - 7}{5 - 2} = \dfrac{9}{3} = 3$.
2. Valor inicial: $f(2) = 3 \cdot 2 + b = 7$, logo $b = 1$.
3. Lei: $f(x) = 3x + 1$.
4. Conferência: $f(5) = 3 \cdot 5 + 1 = 16$. ✓

## Erro comum
- **O erro:** achar que, se 2 km custam R\$ 11,00, então 4 km custam R\$ 22,00.
- **Por que acontece:** o aluno trata toda relação crescente como proporcional. Isso só vale quando $b = 0$.
- **Como evitar:** pergunte "quanto custa 0 km?". Se não for zero, dobrar $x$ não dobra $y$. Pela tabela, 4 km custam R\$ 17,00.

## Exercícios
1. (Fácil) Para $f(x) = -2x + 6$, calcule $f(0)$ e $f(3)$. A função é crescente ou decrescente?
2. (Fácil) Uma academia cobra R\$ 80,00 de matrícula e R\$ 120,00 por mês. Escreva o custo total $C(m)$ após $m$ meses e calcule o custo de 6 meses.
3. (Médio) Os pares $(1, 4)$, $(3, 10)$ e $(5, 16)$ podem pertencer a uma mesma função afim? Se sim, qual é a lei?
4. (Médio) Encontre a função afim cujo gráfico passa por $(-1, 5)$ e $(3, -3)$.
5. (Médio) Um reservatório tem 900 L e perde 15 L por hora. Escreva o volume $V(t)$ após $t$ horas e diga em quanto tempo ele esvazia.
6. (Desafio) O plano A cobra R\$ 30,00 fixos mais R\$ 0,50 por minuto; o plano B, R\$ 50,00 fixos mais R\$ 0,30 por minuto. Com quantos minutos os dois custam o mesmo? Depois disso, qual fica mais barato, e por quê?

> [!note]- Gabarito comentado
> 1. $f(0) = 6$ e $f(3) = -6 + 6 = 0$. Decrescente, porque $a = -2 < 0$.
> 2. $C(m) = 120m + 80$. $C(6) = 720 + 80 = 800$, ou seja, R\$ 800,00.
> 3. Sim. As taxas $\frac{10 - 4}{3 - 1} = 3$ e $\frac{16 - 10}{5 - 3} = 3$ são iguais. De $4 = 3 \cdot 1 + b$, vem $b = 1$: $y = 3x + 1$. Conferência: $3 \cdot 5 + 1 = 16$.
> 4. $a = \frac{-3 - 5}{3 - (-1)} = \frac{-8}{4} = -2$. De $5 = -2 \cdot (-1) + b$, vem $b = 3$: $f(x) = -2x + 3$. Conferência: $f(3) = -6 + 3 = -3$.
> 5. $V(t) = 900 - 15t$. Esvazia quando $V(t) = 0$: $15t = 900$, logo $t = 60$ horas.
> 6. $A(x) = 30 + 0{,}5x$ e $B(x) = 50 + 0{,}3x$. Custam o mesmo quando $0{,}2x = 20$, ou seja, com 100 minutos (R\$ 80,00 cada). Depois disso, B fica mais barato: sua taxa de variação (R\$ 0,30 por minuto) é menor, então cada minuto extra pesa menos.

## Já domino?
1. Uma corrida custa $y = 3x + 5$ reais, com $x$ em km. Uma corrida de 2 km custa R\$ 11,00. Quanto custa uma de 4 km?
   a) R\$ 22,00  b) R\$ 17,00  c) R\$ 12,00  d) R\$ 23,00
2. Em $f(x) = -4x + 2$, o que o $-4$ indica?
   a) O gráfico corta o eixo $y$ em $-4$.
   b) Cada aumento de 1 em $x$ diminui $f(x)$ em 4.
   c) A função é crescente.
   d) O gráfico corta o eixo $x$ em $-4$.
3. Os pontos $(0, 3)$ e $(2, 7)$ estão no gráfico de uma função afim. Qual é a lei?
   a) $f(x) = 2x + 3$  b) $f(x) = 3x + 2$  c) $f(x) = 0{,}5x + 3$  d) $f(x) = 4x + 3$

> [!note]- Respostas e o que cada erro revela
> 1. **b**. (a) dobrou o preço de 2 km, como se fosse proporcional; (c) esqueceu a parte fixa; (d) trocou os papéis de $a$ e $b$ ($5 \cdot 4 + 3$).
> 2. **b**. (a) confundiu $a$ com $b$; (c) ignorou o sinal; (d) confundiu a taxa com o zero da função (o zero é $x = 0{,}5$).
> 3. **a**. (b) trocou $a$ e $b$; (c) calculou a taxa invertida, $\frac{\Delta x}{\Delta y}$; (d) usou só $\Delta y = 4$, sem dividir por $\Delta x$.

## Conexões
- **Depende de:** [[FUN-04|Gráfico de uma função e leitura de gráficos]] · [[EF-07|Equações do 1º grau]]
- **Destrava:** [[FUN-06|Zero, sinal e inequações do 1º grau]] · [[FUN-07|Modelagem com função afim]] · [[FUN-11|Funções definidas por partes e função modular]] · [[FUN-15|Taxa de variação média (ponte para o Cálculo)]] · [[FIN-03|Juros simples]] · [[SEQ-02|Progressão aritmética: termo geral]] · [[GAN-02|Equação da reta e coeficiente angular]]

## Para ir além
- [Portal da Matemática (OBMEP)](https://portaldaobmep.impa.br/): videoaulas de funções da 1ª série do Ensino Médio.

%% Autor: troque o link acima pelo link direto do vídeo escolhido. Opcional: gravar um vídeo próprio de 3 a 5 min sobre por que uma taxa de variação constante gera uma reta. Questões de ENEM/OBMEP: selecionar e conferir antes de incluir. %%
