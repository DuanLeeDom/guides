# Guia Completo de Git

Este é um guia essencial para aprender Git, um sistema de controle de versão distribuído. Aqui estão os principais comandos, explicações simples e exemplos práticos para começar a usar Git com confiança. Criado em 28 de fevereiro de 2025.

---

## O que é Git?
Git é uma ferramenta que rastreia mudanças em arquivos, permitindo gerenciar versões de projetos, colaborar em equipe e manter um histórico seguro.

---

## Índice
1. [Configuração Inicial](#configuração-inicial)
2. [Iniciar ou Clonar um Repositório](#iniciar-ou-clonar-um-repositório)
3. [Gerenciar Arquivos Locais](#gerenciar-arquivos-locais)
4. [Trabalhar com Commits](#trabalhar-com-commits)
5. [Branches](#branches)
6. [Repositório Remoto](#repositório-remoto)
7. [Alterar o Histórico](#alterar-o-histórico)
8. [Resolver Problemas](#resolver-problemas)
9. [Dicas Rápidas](#dicas-rápidas)

---

## Configuração Inicial

Antes de começar, configure sua identidade:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```
- **O que faz**: Define quem você é nos commits.
- **Verifique**: `git config user.name`.

---

## Iniciar ou Clonar um Repositório

### Iniciar um Novo Repositório
```bash
git init
```
- **O que faz**: Cria um repositório Git vazio na pasta atual.
- Exemplo: `cd meu-projeto && git init`.

### Clonar um Repositório
```bash
git clone https://github.com/usuario/exemplo.git
```
- **O que faz**: Copia um repositório remoto para o seu computador.
- **Entrar**: `cd exemplo`.

---

## Gerenciar Arquivos Locais

### Verificar o Estado
```bash
git status
```
- **O que faz**: Mostra o estado atual (arquivos modificados ou novos).
- Exemplo: "modified: index.html".

### Adicionar Arquivos
```bash
git add index.html    # Um arquivo
git add -A            # Todos os arquivos
```
- **O que faz**: Prepara as mudanças para o commit.

---

## Trabalhar com Commits

### Criar um Commit
```bash
git commit -m "Add homepage layout"
```
- **O que faz**: Salva as mudanças no histórico com uma mensagem.

### Ver o Histórico
```bash
git log              # Completo
git log --oneline    # Resumido
```
- **O que faz**: Lista os commits.
- Exemplo: `abc1234 Add homepage layout`.

---

## Branches

### Listar Branches
```bash
git branch
```
- **O que faz**: Mostra os branches locais (ex.: `* main`).

### Criar um Branch
```bash
git branch feature-login
```
- **O que faz**: Cria um branch chamado "feature-login".

### Mudar de Branch
```bash
git checkout feature-login
```
- **O que faz**: Vai para o branch "feature-login".

### Criar e Mudar ao Mesmo Tempo
```bash
git checkout -b feature-login
```
- **O que faz**: Cria e entra no branch "feature-login".

### Mesclar Branches
```bash
git checkout main
git merge feature-login
```
- **O que faz**: Junta as mudanças do "feature-login" no "main".

### Deletar um Branch
```bash
git branch -d feature-login
```
- **O que faz**: Remove o branch "feature-login" (se mesclado).

---

## Repositório Remoto

### Conectar ao Remoto
```bash
git remote add origin https://github.com/usuario/exemplo.git
```
- **O que faz**: Liga o repositório local a um remoto.

### Enviar Mudanças
```bash
git push origin main
```
- **O que faz**: Envia os commits locais para o remoto.

### Puxar Mudanças
```bash
git pull origin main
```
- **O que faz**: Atualiza o local com mudanças do remoto.

### Ver Remotos
```bash
git remote -v
```
- **O que faz**: Lista as URLs remotas.

---

## Alterar o Histórico

### Modificar o Último Commit
```bash
git add style.css
git commit --amend -m "Add styles with fixes"
```
- **O que faz**: Atualiza o último commit.

### Reescrever o Histórico
```bash
git rebase -i HEAD~2    # Últimos 2 commits
git rebase -i --root    # Todos os commits
```
- **O que faz**: Abre o Vim para editar commits.
- **Aviso**: Verifique antes:
  ```bash
  git status  # Sem mudanças pendentes
  git add -A && git commit -m "Temp"  # Se houver mudanças
  ```
- No Vim: `reword` (renomear), `drop` (deletar), `squash` (combinar).

### Voltar no Histórico
```bash
git reset --hard abc1234  # Descarta tudo após abc1234
git reset --soft HEAD~1   # Remove último commit, mantém mudanças
```
- **O que faz**: Ajusta o estado do repositório.

### Forçar Push
```bash
git push -f origin main
```
- **O que faz**: Sobrescreve o remoto após alterações no histórico.

---

## Resolver Problemas

### Guardar Mudanças Temporariamente
```bash
git stash
```
- **O que faz**: Salva mudanças não commitadas.
- **Recuperar**: `git stash pop`.

### Ver Commits Perdidos
```bash
git reflog
```
- **O que faz**: Lista commits recentes do HEAD.
- **Restaurar**: `git reset --hard abc1234`.

### Erro: "Cannot rebase: You have unstaged changes"
- **Solução**:
  ```bash
  git add -A
  git commit -m "Save changes"
  ```
  Ou:
  ```bash
  git stash
  ```

### Erro: "Could not resolve HEAD to a commit"
- **Solução**:
  ```bash
  git reflog           # Encontre um commit
  git reset --hard abc1234
  ```
  Ou commit inicial:
  ```bash
  git add -A
  git commit -m "Initial commit"
  ```

---

## Dicas Rápidas

- **Mensagens claras**: Use "Add", "Update", "Fix" (ex.: "Add new feature").
- **Pratique**:
  ```bash
  git init teste
  cd teste
  echo "Hello" > file.txt
  git add . && git commit -m "First commit"
  ```
- **Evite erros**: Sempre cheque `git status` antes de `rebase` ou `reset`.
- **Backup**: Clone antes de grandes mudanças:
  ```bash
  git clone <URL> backup
  ```

---

## Exemplo Genérico

1. Iniciar e Commitar:
   ```bash
   git init projeto
   cd projeto
   echo "<h1>Site</h1>" > index.html
   git add . && git commit -m "Add initial HTML"
   ```

2. Criar Branch e Mesclar:
   ```bash
   git checkout -b add-css
   echo "body { color: blue; }" > style.css
   git add . && git commit -m "Add CSS styles"
   git checkout main
   git merge add-css
   ```

3. Enviar ao Remoto:
   ```bash
   git remote add origin https://github.com/usuario/projeto.git
   git push origin main
   ```

---

Feito para ensinar Git de forma simples e prática!

---

### **Como Usar**
1. Crie o arquivo no seu repositório:
   ```
   touch README.md
   ```
2. Abra no editor:
   - **Vim**: 
     ```
     vim README.md
     ```
     - Pressione `i`, cole o texto, `Esc`, `:wq`, `Enter`.
   - Ou use um editor gráfico (VS Code, Bloco de Notas).
3. Commit e envie:
   ```
   git add README.md
   git commit -m "Add Git guide to README"
   git push origin main
   ```
