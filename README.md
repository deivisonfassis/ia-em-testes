# IA nos testes — seminário

A inteligência artificial já escreve casos de teste, gera código de teste, revisa relatórios e procura falhas de segurança. **Mas ela acerta sempre?** Hoje cada grupo investiga um uso da IA em testes, faz um experimento de verdade e conta para a turma onde a IA ajuda e onde ela erra.

## O que tem neste repositório

```
ia-nos-testes/
├── README.md                          ← este arquivo
├── temas/                             ← um cartão de missão por grupo
│   ├── TEMA-1-casos-de-teste.md
│   ├── TEMA-2-testes-unitarios.md
│   ├── TEMA-3-relato-de-defeito.md
│   ├── TEMA-4-seguranca.md
│   ├── TEMA-5-ferramentas.md
│   └── TEMA-6-riscos-e-etica.md
├── materiais/                         ← o que vocês vão dar para a IA
│   ├── pedala/                        ← requisitos e regras do Pedala
│   ├── lermais/                       ← requisitos e código do Ler+
│   └── relato-ruim.md                 ← um relato de defeito mal escrito
├── modelos/
│   └── REGISTRO-PROMPTS-modelo.md     ← onde vocês registram o experimento
├── plano-b/                           ← respostas de IA prontas, se a IA não abrir
└── entregas/                          ← o registro do grupo vai aqui
```

## Passo a passo (45 minutos)

| Tempo | O que fazer |
| --- | --- |
| 0–5 min | Um integrante cria o repositório do grupo: **Use this template** → `ia-nos-testes-grupo-N`. Todos leem o cartão do tema em `temas/`. |
| 5–15 min | **Pesquisar:** respondam às perguntas-guia do cartão. Anotem as fontes (site e link). |
| 15–30 min | **Experimentar:** façam o experimento do cartão com uma IA (ChatGPT, Gemini, Copilot ou outra). Registrem cada prompt e cada resposta no registro. |
| 30–40 min | **Conferir:** comparem a resposta da IA com o requisito ou com o código. Onde ela acertou? Onde errou? |
| 40–45 min | **Preparar a apresentação** com o roteiro abaixo. Commit e push do registro. |

## A receita do bom prompt

Um prompt fraco: *“faz uns testes pra esse sistema”*.

Um prompt bom tem cinco partes:

| Parte | Exemplo |
| --- | --- |
| **Papel** | “Você é um analista de testes de software.” |
| **Contexto** | “Abaixo está o documento de requisitos do sistema Pedala.” (e cole o documento) |
| **Tarefa** | “Gere casos de teste para as regras RN01 a RN10.” |
| **Formato** | “Responda numa tabela com: ID, regra, entrada, resultado esperado.” |
| **Critério** | “Use valor limite. Não invente regras que não estão no documento.” |

## Roteiro da apresentação (5 minutos, igual para todos os grupos)

1. **A pergunta** (30 s): qual era o tema e o que vocês queriam descobrir.
2. **Como funciona** (1 min): o que a pesquisa mostrou, com uma fonte.
3. **O experimento** (1 min 30 s): o prompt usado e o melhor trecho da resposta. Mostrem na tela.
4. **Onde a IA errou** (1 min): pelo menos um erro, com a prova (o requisito, o código ou a conta).
5. **A recomendação do grupo** (1 min): “Use IA para… Não confie na IA para…”.

Pode apresentar direto do registro na tela ou com até 4 slides.

## Regras

- **Nunca** colem na IA dados pessoais reais, senhas ou código de uma empresa. Aqui só usamos os materiais fictícios da pasta `materiais/`.
- Toda afirmação da IA precisa ser **conferida**: no requisito, no código ou numa fonte confiável.
- A IA pode errar com muita confiança. Achar o erro dela vale mais do que copiar o acerto.

## Entrega

1. `entregas/REGISTRO-PROMPTS-grupo-N.md` preenchido (copie de `modelos/`).
2. Commit e push: `git commit -m "docs: registro do experimento com IA"`.
3. Apresentação no fim da aula.

## A IA não abriu no laboratório?

Usem a pasta `plano-b/`: ela tem respostas de exemplo, no estilo de uma IA, para os temas 1 a 4, com acertos e erros típicos. O trabalho do grupo vira **analisar** essa resposta: onde ela acertou e onde errou. Os temas 5 e 6 seguem só com a pesquisa na internet.
