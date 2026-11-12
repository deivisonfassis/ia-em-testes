# Plano B · Tema 2 — Resposta de exemplo de uma IA

> Use este arquivo só se não for possível acessar uma IA no laboratório. É uma resposta de exemplo, preparada para a aula no estilo de uma IA, com acertos e erros típicos. O trabalho do grupo é **conferir** cada teste com o `REQUISITOS-Pedala.md`.

## Tentativa 1 — só com o código

**Prompt enviado:**

```
Escreva testes unitários em Jest para as funções validarIdade e
bonusRecarga do código abaixo. Use describe, test e expect.
[regras.js colado]
```

**Resposta da IA:**

Aqui estão os testes unitários, cobrindo os principais cenários de cada função:

```js
const R = require('./regras.js');

describe('validarIdade', () => {
  test('aceita 17 anos', () => {
    expect(R.validarIdade(17)).toBe(true);
  });

  test('recusa 16 anos, pois a idade deve ser maior que 16', () => {
    expect(R.validarIdade(16)).toBe(false);
  });

  test('recusa idade não inteira', () => {
    expect(R.validarIdade(17.5)).toBe(false);
  });
});

describe('bonusRecarga', () => {
  test('recarga de 100 ganha 20% de bônus', () => {
    expect(R.bonusRecarga(100)).toBe(20);
  });

  test('recarga de 60 ganha 10% de bônus', () => {
    expect(R.bonusRecarga(60)).toBe(6);
  });

  test('recarga de 50 não ganha bônus, pois precisa ser maior que 50', () => {
    expect(R.bonusRecarga(50)).toBe(0);
  });
});
```

Todos esses testes devem passar com a implementação atual. ✅

## Tentativa 2 — com o código e o requisito

**Prompt enviado:** o mesmo, com o `REQUISITOS-Pedala.md` colado e a frase *“Os valores esperados devem vir do documento de requisitos, não do código.”*

**Resposta da IA:**

Considerando o documento de requisitos, ajustei os testes:

```js
describe('validarIdade', () => {
  test('aceita 16 anos (RN01: 16 anos ou mais)', () => {
    expect(R.validarIdade(16)).toBe(true);
  });

  test('recusa 15 anos', () => {
    expect(R.validarIdade(15)).toBe(false);
  });
});

describe('bonusRecarga', () => {
  test('recarga de 50 ganha 10% (RN10: a partir de R$ 50,00)', () => {
    expect(R.bonusRecarga(50)).toBe(5);
  });

  test('recarga de 49,99 não ganha bônus', () => {
    expect(R.bonusRecarga(49.99)).toBe(0);
  });
});
```

Observação: com o código atual, os testes de 16 anos e de R$ 50 vão **falhar**, porque a implementação usa `>` em vez de `>=`. Isso indica um defeito no código.

---

**Perguntas para o grupo:**

1. Na tentativa 1, a IA disse que “todos os testes devem passar”. Por que isso **não** é uma boa notícia?
2. De onde a IA tirou o esperado do teste “recusa 16 anos” na tentativa 1?
3. O que mudou na tentativa 2 e por quê?
4. Qual a lição para quem usa IA para gerar testes?
