# Tema 4 — IA analisando a segurança do código

**Missão:** descobrir se a IA encontra uma falha de segurança real num código, e se ela também aponta “falhas” que não existem.

## Pesquisa (10 min)

1. O que é **XSS** (cross-site scripting)? Como ele acontece num site?
2. Qual a diferença entre `innerHTML` e `textContent` em JavaScript?
3. Que ferramentas analisam a segurança do código automaticamente (com ou sem IA)? Cite uma.

## Experimento (15 min)

**Material:** `materiais/lermais/app.js` e `materiais/lermais/REQUISITOS-LerMais.md` (veja a RNF03)

1. **Tentativa 1.** Envie:

   ```
   Você é um especialista em segurança de aplicações web. Analise o código
   JavaScript abaixo e liste as vulnerabilidades de segurança. Para cada
   uma, informe: a linha, o risco, um exemplo de ataque e a correção.

   [COLE AQUI O app.js]
   ```

2. A IA encontrou a falha da **linha 286** (`saudacao`)? Anote.
3. **Tentativa 2:** se a IA apontou vários usos de `innerHTML`, pergunte: *“Quais desses usos de innerHTML são realmente perigosos e quais são seguros? Explique cada um.”*
4. **Tentativa 3:** teste o ataque de verdade. Abra o Ler+ (se o grupo tiver o `lermais-testes`) e entre com o nome `<b>Ana</b>`. A saudação ficou em negrito?

## Conferir (10 min)

- `lista.innerHTML = ''` só **apaga** o conteúdo. Isso é perigoso? A IA disse que era?
- A linha 286 coloca o **nome digitado pelo usuário** dentro do HTML. Essa é a falha real.
- A correção sugerida pela IA funciona? Ela muda só o necessário?

## Mostrar na apresentação

- A falha verdadeira que a IA achou, com a linha e a correção.
- Um falso alarme da IA, se houve, e por que ele não é um risco.
