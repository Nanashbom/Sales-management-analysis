# Sales-management-analysis
Criação de um jupyter notebook com ênfase em analisar as vendas, de produtos tecnológicos, dos gerentes de cada loja.

## Objetivo
O que você quer descobrir (ex.: vendas por mês, melhores produtos, desempenho por vendedor).

## Dados
De onde vêm os dados (arquivo CSV, planilha, etc.).

## Ferramentas
Python, pandas, matplotlib (ou o que for usar).

## Como rodar
Passos rápidos para executar o projeto.


## Como editar o arquivo e atualizar ele no main
Aqui vai o passo a passo pelo terminal (o do VS Code serve também, ou o Git Bash no Windows).

**0. Baixar o repositório pro seu computador (só na primeira vez)**

```bash
git clone https://github.com/SEU-USUARIO/sales-analysis.git
cd sales-analysis
```

Troque pelo link do seu repositório (botão verde **Code** no GitHub).

**1. Criar uma branch nova e entrar nela**

```bash
git checkout -b minha-branch
```

Dá pra usar também `git switch -c minha-branch`, que faz a mesma coisa. Escolha um nome que diga o que você vai fazer, como `analise-inicial` ou `limpeza-dados`.

Para ver em qual branch você está:

```bash
git branch
```

**2. Fazer suas alterações**

Crie ou edite arquivos normalmente (notebook, script, README etc.).

**3. Ver o que mudou**

```bash
git status
```

**4. Adicionar os arquivos ao commit**

```bash
git add .
```

O ponto adiciona tudo que mudou. Como a pasta `data/` está no `.gitignore`, ela não vai junto. Se preferir adicionar só um arquivo: `git add nome-do-arquivo.py`.

**5. Fazer o commit**

```bash
git commit -m "Adiciona análise inicial de vendas"
```

A mensagem deve descrever o que você fez, de forma curta.

**6. Enviar pro GitHub (push)**

Na primeira vez que você envia uma branch nova:

```bash
git push -u origin minha-branch
```

Nas próximas vezes nessa mesma branch, basta:

```bash
git push
```

**7. Juntar a branch na principal (opcional)**

Quando terminar o trabalho, você pode:

- **Pelo GitHub:** abrir um Pull Request e clicar em **Merge**.
- **Pelo terminal:**

```bash
git checkout main
git merge minha-branch
git push
```

Se o seu repositório usa `master` em vez de `main`, troque o nome nos comandos.

**Resumo do dia a dia:**

```bash
git status
git add .
git commit -m "mensagem"
git push
```

Como o repositório é só seu e é um projeto básico, você pode trabalhar direto na `main` sem criar branch. Branches ficam mais úteis quando você quer testar algo sem mexer no que já funciona, ou quando trabalha em equipe.
