# Plano B · Tema 1 — Resposta de exemplo de uma IA

> Use este arquivo só se não for possível acessar uma IA no laboratório. É uma resposta de exemplo, preparada para a aula no estilo de uma IA, com acertos e erros típicos. O trabalho do grupo é **conferir** cada linha com o `REQUISITOS-Pedala.md`.

**Prompt enviado:**

```
Você é um analista de testes de software. Abaixo está o documento de
requisitos do sistema Pedala. Gere casos de teste para as regras RN01,
RN07 e RN10. Responda numa tabela com: ID, regra, entrada, resultado
esperado. Use a técnica de valor limite. Não invente regras que não
estão no documento.
[documento colado]
```

**Resposta da IA:**

Claro! Aqui estão os casos de teste para as regras solicitadas, aplicando a técnica de valor limite:

| ID | Regra | Entrada | Resultado esperado |
| --- | --- | --- | --- |
| CT01 | RN01 | Idade 18 | Aceito |
| CT02 | RN01 | Idade 15 | Recusado |
| CT03 | RN01 | Idade 10 | Recusado |
| CT04 | RN01 | Idade 60 | Aceito |
| CT05 | RN07 | Estudante, avulsa, 20 minutos | R$ 6,50 |
| CT06 | RN07 | Estudante, avulsa, 100 minutos | R$ 26,50 |
| CT07 | RN07 | Estudante, plano mensal, 60 minutos | R$ 3,00 (50% de desconto sobre R$ 6,00) |
| CT08 | RN10 | Recarga de R$ 30,00 | Sem bônus |
| CT09 | RN10 | Recarga de R$ 60,00 | Bônus de R$ 6,00 |
| CT10 | RN10 | Recarga de R$ 100,00 | Bônus de R$ 20,00 |
| CT11 | RN10 | Recarga de R$ 150,00 | Bônus de R$ 30,00 |
| CT12 | RN11 | 4ª viagem no mesmo dia | Recusada (limite de 3 viagens diárias) |

**Observações:** os casos CT01 a CT04 cobrem a faixa de idade válida e inválida, e os casos CT08 a CT11 cobrem as faixas de bônus. Todos os valores foram calculados conforme a tabela de preços do documento.

---

**Perguntas para o grupo:**

1. Os testes da RN01 usam valor limite de verdade? Qual idade deveria estar na tabela e não está?
2. E na RN10, qual valor de recarga é o limite e ficou de fora?
3. Refaça a conta do CT06 com a RN06 e a RN07. Está certo?
4. O CT07 obedece a RN07? Leia a última frase da regra.
5. De onde veio a RN11?
