# Plano B · Tema 4 — Resposta de exemplo de uma IA

> Use este arquivo só se não for possível acessar uma IA no laboratório. É uma resposta de exemplo, preparada para a aula no estilo de uma IA, com acertos e erros típicos. O trabalho do grupo é **conferir** cada item com o `materiais/lermais/app.js`.

**Prompt enviado:**

```
Você é um especialista em segurança de aplicações web. Analise o código
JavaScript abaixo e liste as vulnerabilidades de segurança. Para cada
uma, informe: a linha, o risco, um exemplo de ataque e a correção.
[app.js colado]
```

**Resposta da IA:**

Encontrei as seguintes vulnerabilidades no código:

**1. XSS na saudação do usuário — linha 286 · Risco: alto**
O nome digitado pelo usuário é inserido com `innerHTML`. Um atacante pode cadastrar o nome `<img src=x onerror=alert(document.cookie)>` e o código será executado.
**Correção:** `document.getElementById('saudacao').textContent = 'Olá, ' + usuario.nome;`

**2. XSS na lista da conta — linha 282 · Risco: alto**
`lista.innerHTML = ''` permite a injeção de HTML malicioso.
**Correção:** usar `textContent`.

**3. XSS no catálogo — linha 318 · Risco: alto**
`area.innerHTML = ''` também é vulnerável a injeção.
**Correção:** usar `textContent`.

**4. XSS no painel do bibliotecário — linhas 362 e 388 · Risco: alto**
Mesmo problema dos itens 2 e 3.

**5. Senhas guardadas no localStorage sem criptografia · Risco: crítico**
O sistema guarda os dados do usuário, incluindo a senha, no `localStorage`, que pode ser lido por qualquer script da página.
**Correção:** nunca guardar senhas no navegador; usar autenticação no servidor.

**6. Matrícula sem validação · Risco: médio**
A matrícula digitada não é validada antes de ser usada.
**Correção:** validar o formato da matrícula.

---

**Perguntas para o grupo:**

1. O item 1 é uma falha real? Confira a linha 286 e a RNF03 do Ler+.
2. Os itens 2, 3 e 4 colocam algum texto do usuário no HTML, ou só apagam o conteúdo (`= ''`)? São falhas de verdade?
3. O Ler+ tem senha? Procure no código. O item 5 existe?
4. A matrícula é validada em algum lugar? Procure `validarMatricula` no `app.js`.
5. Quantas das 6 “vulnerabilidades” são reais?
