# Plano B · Tema 3 — Resposta de exemplo de uma IA

> Use este arquivo só se não for possível acessar uma IA no laboratório. É uma resposta de exemplo, preparada para a aula no estilo de uma IA, com acertos e erros típicos. O trabalho do grupo é **marcar tudo o que a IA inventou**, comparando com o `materiais/relato-ruim.md`.

**Prompt enviado (só a mensagem do testador):**

```
Transforme a mensagem abaixo num relatório de defeito completo, com:
título, regra violada, ambiente, pré-condições, passos para reproduzir,
dados usados, resultado esperado, resultado obtido e severidade.
"oi gente, o desconto de estudante ta errado, fiz uma viagem longa e
cobrou mais do que devia. arruma ai pfv"
```

**Resposta da IA:**

### [BUG] Desconto de estudante não aplicado em viagens longas

**Regra violada:** RN05 — Desconto de estudante

**Ambiente:**
- Sistema: Pedala v2.3
- Navegador: Google Chrome 118
- Sistema operacional: Windows 11

**Pré-condições:** usuário cadastrado como estudante, com saldo de R$ 50,00 e a bicicleta BK0457 disponível na Estação Central.

**Passos para reproduzir:**
1. Acessar o Pedala e fazer login com a conta de estudante.
2. Desbloquear a bicicleta BK0457 na Estação Central.
3. Pedalar por 75 minutos.
4. Devolver a bicicleta na Estação Praça da Sé.
5. Verificar o valor cobrado no histórico.

**Dados usados:** viagem avulsa de 75 minutos, estudante.

**Resultado esperado:** valor com 50% de desconto: R$ 20,25.

**Resultado obtido:** o sistema cobrou R$ 40,50, sem o desconto.

**Severidade:** Crítica. O defeito impede o uso do sistema por estudantes.

---

**Perguntas para o grupo:**

1. Liste **tudo** o que a IA escreveu e que não estava na mensagem nem nos fatos da equipe.
2. A regra violada é mesmo a RN05? Confira no `REQUISITOS-Pedala.md`.
3. Os valores de esperado e obtido são reais ou inventados? Quais são os verdadeiros, pelos fatos da equipe e pela RN07?
4. A severidade “Crítica” faz sentido? O sistema fica inutilizável?
5. Como vocês mudariam o prompt para a IA parar de inventar?
