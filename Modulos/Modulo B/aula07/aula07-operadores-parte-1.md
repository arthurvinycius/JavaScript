# Aula 07: Operadores (Parte 1)

Curso de JavaScript do CursoemVideo (Gustavo Guanabara).

## Operadores aritméticos

| Operador | Nome | Exemplo (5 e 2) |
|---|---|---|
| `+` | soma | `5 + 2` → 7 |
| `-` | subtração | `5 - 2` → 3 |
| `*` | multiplicação | `5 * 2` → 10 |
| `/` | divisão real | `5 / 2` → 2.5 |
| `%` | resto da divisão inteira | `5 % 2` → 1 |
| `**` | potência | `5 ** 2` → 25 |

- O `%` **não calcula porcentagem**, ele dá o resto da divisão inteira.

## Ordem de precedência (aritméticos)

1. Parênteses `( )`
2. Potência `**`
3. `*`, `/` e `%` (mesmo nível, da esquerda para a direita)
4. `+` e `-`

Exemplos:

- `5 + 3 / 2` → **6.5** (a divisão é feita primeiro)
- `(5 + 3) / 2` → **4** (os parênteses mudam a ordem)

O JavaScript só acusa erro de **sintaxe**. Uma conta pode estar errada e não dar erro nenhum.

## Atribuição

- O `=` **não é "igual", é "recebe"**. `a = 5 + 3` significa "a recebe 8".
- Uma variável guarda um valor por vez. O novo valor apaga o antigo.

Exercício resolvido na aula (passo a passo):

```js
var a = 5 + 3          // 8
var b = a % 5          // 3
var c = 5 * b ** 2     // 45
var d = 10 - a / 2     // 6
var e = 6 * 2 / d      // 2
var f = b % e + 4 / e  // 3
```

## Auto-atribuição (forma curta)

| Longa | Curta |
|---|---|
| `n = n + 4` | `n += 4` |
| `n = n - 5` | `n -= 5` |
| `n = n * 4` | `n *= 4` |
| `n = n / 2` | `n /= 2` |
| `n = n ** 2` | `n **= 2` |
| `n = n % 5` | `n %= 5` |

- Só vale quando a variável da esquerda é a mesma que aparece na conta.

## Incremento e decremento

- `x++` soma 1 e `x--` tira 1.
- **Depois** da variável (`n++`): mostra o valor antigo e depois atualiza.
- **Antes** da variável (`++n`): atualiza e depois mostra.

## Dicas do professor

- Use nomes coerentes: `nome`, `idade`, `salario`. Evite `a`, `b`, `c` e `n1`, `n2`.
- Pratique no Node: abra com `node`, saia com `.exit` e limpe a tela com `Ctrl+L`.
