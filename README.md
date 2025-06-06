**Resposta para a Questão Ponderada - Módulo IN02**

---

# 1. ITEM 1 – ZEROS DE FUNÇÕES

## a) Gráfico da Função e Estimativa Visual do Mínimo

Gráfico desenhado com GeoGebra.

Visualmente, o ponto mínimo ocorre aproximadamente em:

**f(1) ≈ 1,83**

---

## b) Derivada da Função f(x)

Função:

```math
f(x) = x e^{-0.5x} + \sin(x) + 2
```

Derivada $f'(x)$:

```math
e^{-0.5x} \rightarrow e^{-0.5x} \cdot (-0.5) = -0.5 e^{-0.5x}
```

```math
\sin(x) \rightarrow \cos(x)
```

Resultado:

```math
f'(x) = e^{-0.5x} - 0.5 x e^{-0.5x} + \cos(x)
```

---

## c) Método de Newton-Raphson

Fórmula utilizada:

```math
x_n = x - \dfrac{e^{-0.5x} - 0.5x e^{-0.5x} + \cos(x)}{e^{-0.5x} - 0.5 e^{-0.5x} - 0.5 x e^{-0.5x} - \sin(x)}
```

**Resultado:**

Utilizando Google Sheets, chegou-se a $|x_{n+2} - x_n| < 10^{-4}$ em **3 iterações**, com o **mínimo da função ≈ 1.8330**.

---

# 2. ITEM 2 – INTEGRAL INDEFINIDA, DEFINIDA E INTEGRAÇÃO NUMÉRICA

## a) Integral Indefinida

Função:

```math
f(x) = x e^{-0.5x} + \sinh(x) + 2
```

Integração por partes:

```math
u = x
```

```math
dv = e^{-0.5x} dx \Rightarrow v = \dfrac{1}{-0.5} e^{-0.5x} = -2 e^{-0.5x}
```

```math
\int u dv = u v - \int v du
```

```math
\int x e^{-0.5x} dx = -2x e^{-0.5x} - 2 \int e^{-0.5x} dx
```

```math
= -2x e^{-0.5x} - 4 e^{-0.5x}
```

Resposta final:

```math
\int f(x) dx = -2x e^{-0.5x} - 4 e^{-0.5x} - \cosh(x) + 2x + C
```

---

## b) Integral Definida no Intervalo \[1, 6]

Cálculo da integral definida:

```math
-2 \cdot 6 e^{-0.5 \cdot 6} - 4 e^{-0.5 \cdot 6} - \cosh(6) + 12 + C
```

```math
-2 \cdot 1 e^{-0.5 \cdot 1} - 4 e^{-0.5 \cdot 1} - \cosh(1) + 2 + C
```

Resultado:

```math
10.2x - [-2.173] = 12.47
```

---

## c) Integração Numérica – Newton-Cotes de Ordem 2

```math
H = \dfrac{6 - 1}{2} = 2.5
```

Pontos:

```math
x_0 = 1, x_1 = 3.5, x_2 = 6
```

Cálculos:

```math
f(1) = 3.788
```

```math
f(3.5) = 2.257
```

```math
f(6) = 2.079
```

Resultado:

```math
\dfrac{2.5}{3} [3.788 + 4(2.257) + 2.079] = 12.07
```

---

## d) Integração Numérica – Newton-Cotes de Ordem 4

```math
h = \dfrac{6 - 1}{4} = 1.25
```

Pontos:

```math
x_0 = 1, x_1 = 2.25, x_2 = 3.5, x_3 = 4.75, x_4 = 6
```

Cálculos:

```math
f(1) = 3.788
```

```math
f(2.25) = 3.508
```

```math
f(3.5) = 2.257
```

```math
f(4.75) = 1.872
```

```math
f(6) = 2.079
```

Resultado:

```math
\dfrac{2.5}{45} [7(3.788) + 32(3.508) + 12(2.257) + 32(1.872) + 7(2.079)] = 12.73
```

---

## e) Cálculo dos Erros Relativos

**Erro relativo entre (b) e (c):**

```math
\left| \dfrac{12.07 - 12.47}{12.47} \right| \times 100 = 2.739\% 
```

**Erro relativo entre (b) e (d):**

```math
\left| \dfrac{12.73 - 12.47}{12.47} \right| \times 100 = 0.761\%
```

**Conclusão:**

Podemos observar que o método de ordem 4 tem uma porcentagem de erro bem menor que o método de ordem 2. Isso significa que a ordem 4 é mais precisa, devido ao seu maior número de pontos.
