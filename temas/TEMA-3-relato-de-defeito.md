# Tema 3 — IA revisando relatórios de defeito

**Missão:** descobrir se a IA consegue transformar um relato ruim numa Issue completa, e se ela inventa informações que ninguém deu.

## Pesquisa (10 min)

1. Quais seções um bom relatório de defeito precisa ter?
2. O que é **alucinação** em IA? Dê um exemplo.
3. Que ferramentas de bugtracker (Jira, GitHub, Azure DevOps…) já têm IA para escrever ou resumir defeitos? Cite uma.

## Experimento (15 min)

**Material:** `materiais/relato-ruim.md` e `materiais/pedala/REQUISITOS-Pedala.md`

1. **Tentativa 1, só a mensagem.** Envie:

   ```
   Transforme a mensagem abaixo num relatório de defeito completo, com:
   título, regra violada, ambiente, pré-condições, passos para reproduzir,
   dados usados, resultado esperado, resultado obtido e severidade.

   "oi gente, o desconto de estudante ta errado, fiz uma viagem longa e
   cobrou mais do que devia. arruma ai pfv"
   ```

2. Marque **tudo** o que a IA escreveu e que **não estava** na mensagem (navegador, valores, passos, datas…).
3. **Tentativa 2:** envie de novo, agora com os fatos da seção “O que a equipe sabe” do `relato-ruim.md` e o texto da RN07. Acrescente: *“Use só as informações fornecidas. Onde faltar informação, escreva A CONFIRMAR.”*
4. **Tentativa 3:** peça: *“Calcule o resultado esperado pela RN07 e mostre a conta.”*

## Conferir (10 min)

- Quantas informações a IA **inventou** na tentativa 1?
- Na tentativa 3, a conta está certa? Pela RN07: 3 + 100 × 0,50 = 53 → teto de R$ 40,00 → 50% de desconto. Qual deveria ser o valor?
- A severidade que a IA escolheu faz sentido?

## Mostrar na apresentação

- A tentativa 1 com as invenções destacadas.
- A tentativa final e o que mudou no prompt para a IA parar de inventar.
