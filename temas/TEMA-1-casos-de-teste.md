# Tema 1 — IA gerando casos de teste a partir de requisitos

**Missão:** descobrir se a IA consegue transformar um documento de requisitos em bons casos de teste, e o que ela deixa passar.

## Pesquisa (10 min)

1. O que é um caso de teste e quais campos ele precisa ter?
2. O que são as técnicas de **partição de equivalência** e **valor limite**?
3. Que ferramentas ou empresas já usam IA para gerar casos de teste? Cite uma.

## Experimento (15 min)

**Material:** `materiais/pedala/REQUISITOS-Pedala.md`

1. Abra a IA e envie o **prompt inicial**, colando o documento inteiro no lugar indicado:

   ```
   Você é um analista de testes de software. Abaixo está o documento de
   requisitos do sistema Pedala. Gere casos de teste para as regras RN01,
   RN07 e RN10. Responda numa tabela com: ID, regra, entrada, resultado
   esperado. Use a técnica de valor limite. Não invente regras que não
   estão no documento.

   [COLE AQUI O DOCUMENTO]
   ```

2. Registre a resposta no registro do grupo.
3. **Tentativa 2:** peça para a IA mostrar a **conta** de cada resultado esperado da RN07.
4. **Tentativa 3:** melhore o prompt para corrigir o que estava fraco (ex.: “inclua exatamente o valor do limite, um abaixo e um acima”).

## Conferir (10 min)

- A IA testou **exatamente** os limites? Idade **16** (e 15)? Recarga de **R$ 50** (e R$ 49,99)? Recarga de R$ 100?
- Os resultados esperados batem com o requisito? Refaça as contas da RN07 com o teto: estudante, 100 minutos.
- A IA inventou alguma regra que não está no documento?

## Mostrar na apresentação

- O caso de teste mais útil que a IA criou.
- Um limite que ela esqueceu ou uma conta que ela errou, com a prova no requisito.
