# Tema 2 — IA gerando testes unitários com Jest

**Missão:** descobrir se os testes que a IA escreve conseguem achar defeitos, ou se eles só confirmam o que o código já faz.

## Pesquisa (10 min)

1. O que é um teste unitário? O que é o Jest?
2. Que ferramentas usam IA para gerar testes unitários automaticamente? Cite uma.
3. O que significa dizer que um teste deve ser escrito a partir do **requisito**, e não do **código**?

## Experimento (15 min)

**Material:** `materiais/pedala/regras.js` e `materiais/pedala/REQUISITOS-Pedala.md`

1. **Tentativa 1, só com o código.** Envie:

   ```
   Escreva testes unitários em Jest para as funções validarIdade e
   bonusRecarga do código abaixo. Use describe, test e expect.

   [COLE AQUI O regras.js]
   ```

2. Observe: qual valor esperado a IA colocou para `validarIdade(16)` e para `bonusRecarga(50)`?
3. **Tentativa 2, com o requisito.** Envie o mesmo pedido, mas cole também o `REQUISITOS-Pedala.md` e acrescente: *“Os valores esperados devem vir do documento de requisitos, não do código.”*
4. **Tentativa 3:** pergunte à IA: *“Os testes da tentativa 1 e da tentativa 2 têm valores esperados diferentes. Qual está certo e por quê?”*

## Conferir (10 min)

- A RN01 diz “16 anos **ou mais**”. A RN10 diz “**a partir de** R$ 50,00”. O que os testes da tentativa 1 esperavam?
- Um teste que espera o comportamento errado **passa** e esconde o defeito. Isso aconteceu?
- A IA percebeu sozinha a diferença entre o código e o requisito?

## Mostrar na apresentação

- Os dois testes lado a lado: o que veio só do código e o que veio do requisito.
- A conclusão: o que acontece quando a IA tira o esperado do próprio código.
