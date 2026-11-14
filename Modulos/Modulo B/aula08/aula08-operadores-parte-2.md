# Aula 08: Operadores (Parte 2)

Curso de JavaScript do CursoemVideo (Gustavo Guanabara).

## Operadores relacionais

O resultado é sempre `true` ou `false`.

| Operador | Significado |
|---|---|
| `>` | maior |
| `<` | menor |
| `>=` | maior ou igual |
| `<=` | menor ou igual |
| `==` | igual (compara só o **valor**) |
| `!=` | diferente |

- **Macete:** divida o símbolo ao meio. Se parecer um 4, é o menor. Se parecer um 7, é o maior.
- `=` é atribuição. `==` é comparação.
- Em expressões mistas, primeiro os aritméticos e depois os relacionais.
  Exemplo com `a = 8` e `b = 15`: `a <= b - 10` → `8 <= 5` → `false`.

## Operadores de identidade

| Operador | O que compara |
|---|---|
| `==` | só o valor: `5 == '5'` → `true` |
| `===` | valor **e** tipo: `5 === '5'` → `false` |
| `!=` | diferente em valor |
| `!==` | diferente em valor **ou** tipo |

Teste feito no Node:

```js
var x = 5      // number
var y = '5'    // string
x == y         // true
x === y        // false
x != y         // false
x !== y        // true
```

## Operadores lógicos

| Operador | Nome | Regra |
|---|---|---|
| `!` | não | inverte `true` e `false` |
| `&&` | e | só dá `true` se os **dois** forem verdadeiros |
| `\|\|` | ou | dá `true` se **pelo menos um** for verdadeiro |

- `&&`: `true && true` → true. Qualquer outra combinação → false.
- `||`: `false || false` → false. Qualquer outra combinação → true.
- Analogia da aula: "uma caneta azul **e** uma vermelha" (preciso das duas) contra "azul **ou** vermelha" (basta uma).

Exemplos com `a = 5` e `b = 8`:

```js
a > b && b % 2 == 0      // false
a <= b || b / 2 == 2     // true
```

## Ordem de precedência completa

1. **Aritméticos:** parênteses, `**`, depois `*`, `/` e `%`, depois `+` e `-`
2. **Relacionais:** da esquerda para a direita
3. **Lógicos:** primeiro `!`, depois `&&`, depois `||`
4. **Ternário:** é sempre o último a ser resolvido

## Exemplos para ler em português

```js
idade >= 15 && idade <= 17          // idade entre 15 e 17 (incluindo)
estado == 'RJ' || estado == 'SP'    // mora no Rio ou em São Paulo
salario > 1500 && sexo != 'M'       // ganha mais de 1500 e não é do sexo M
```

## Operador ternário

Formato: `teste ? valor_se_verdadeiro : valor_se_falso`

```js
media >= 7 ? "APROVADO" : "REPROVADO"
var res = x % 2 == 0 ? 5 : 9
var r = idade >= 18 ? "MAIOR" : "MENOR"
```

- Na aula, o exemplo da idade aparece com `<=`, mas "maior de idade" é `>= 18`. Teste no Node para conferir.
- Para praticar: abra o Node com `node`, faça a conta de cabeça antes de apertar Enter e confira o resultado.
