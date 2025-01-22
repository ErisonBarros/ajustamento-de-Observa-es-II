---
description: Prof. Erison Barros
icon: rectangles-mixed
---

# Introdução ao Git e GitHub

\---

#### **Conteúdo Programático:**

**1. Introdução ao Controle de Versão**

* O que é controle de versão?
* Benefícios do controle de versão em projetos colaborativos.

**2. O que é o Git?**

* Definição e história do Git.
* Principais características (distribuído, rápido, eficiente).

**3. Configuração Inicial do Git**

* Instalação do Git (Windows, macOS, Linux).
* Configuração básica (`git config`, nome de usuário e e-mail).

**4. Comandos Básicos do Git**

* Criar um repositório local (`git init`).
* Adicionar arquivos para controle (`git add`).
* Salvar mudanças no repositório (`git commit`).
* Visualizar o histórico de commits (`git log`).

**5. Introdução ao GitHub**

* O que é o GitHub e por que utilizá-lo?
* Criar uma conta no GitHub.
* Conceitos básicos: repositórios, issues, pull requests.

**6. Trabalhando com Repositórios Remotos**

* Conectar repositórios locais ao GitHub (`git remote`).
* Enviar mudanças para o GitHub (`git push`).
* Clonar repositórios existentes (`git clone`).
* Atualizar o repositório local com mudanças do remoto (`git pull`).

**7. Colaboração com GitHub**

* Forks e pull requests.
* Gerenciamento de branches.
* Revisão de código em equipe.

**8. Integração e Automação**

* Utilização de `.gitignore`.
* Introdução a GitHub Actions para automação.

**9. Boas Práticas**

* Escrever mensagens de commit claras.
* Organização de branches e repositórios.
* Contribuindo para projetos open-source.

````markdown
// Markdonw
## **Conteúdo Programático**

### **1. Introdução ao Controle de Versão**
- O que é controle de versão?
- Benefícios do controle de versão em projetos colaborativos.

### **2. O que é o Git?**
- Definição e história do Git.
- Principais características (distribuído, rápido, eficiente).

### **3. Configuração Inicial do Git**
- Instalação do Git (Windows, macOS, Linux).
- Configuração básica:
  ```bash
  git config --global user.name "Seu Nome"
  git config --global user.email "seuemail@exemplo.com"
  ```

### **4. Comandos Básicos do Git**
- Criar um repositório local:
  ```bash
  git init
  ```
- Adicionar arquivos para controle:
  ```bash
  git add <arquivo>
  ```
- Salvar mudanças no repositório:
  ```bash
  git commit -m "Mensagem do commit"
  ```
- Visualizar o histórico de commits:
  ```bash
  git log
  ```

### **5. Introdução ao GitHub**
- O que é o GitHub e por que utilizá-lo?
- Criar uma conta no GitHub.
- Conceitos básicos:
  - Repositórios.
  - Issues.
  - Pull Requests.

### **6. Trabalhando com Repositórios Remotos**
- Conectar repositórios locais ao GitHub:
  ```bash
  git remote add origin <url-do-repositorio>
  ```
- Enviar mudanças para o GitHub:
  ```bash
  git push -u origin main
  ```
- Clonar repositórios existentes:
  ```bash
  git clone <url-do-repositorio>
  ```
- Atualizar o repositório local com mudanças do remoto:
  ```bash
  git pull
  ```

### **7. Colaboração com GitHub**
- Forks e pull requests.
- Gerenciamento de branches:
  ```bash
  git branch <nome-da-branch>
  git checkout <nome-da-branch>
  ```
- Revisão de código em equipe.

### **8. Integração e Automação**
- Utilização de `.gitignore`.
- Introdução a GitHub Actions para automação.

### **9. Boas Práticas**
- Escrever mensagens de commit claras.
- Organização de branches e repositórios.
- Contribuindo para projetos open-source.

---

## **Materiais de Apoio**
- [Documentação Oficial do Git](https://git-scm.com/doc)
- [Documentação do GitHub](https://docs.github.com/)
- Cheatsheet do Git: [link](https://education.github.com/git-cheat-sheet-education.pdf)

---

## **Atividade Prática**
1. Criar um repositório local:
   ```bash
   git init
   ```
2. Criar um arquivo `README.md` e adicioná-lo ao repositório:
   ```bash
   echo "# Meu Projeto" > README.md
   git add README.md
   git commit -m "Adiciona README.md"
   ```
3. Criar um repositório no GitHub e conectar ao repositório local:
   ```bash
   git remote add origin <url-do-repositorio>
   git push -u origin main
   ```
4. Criar uma branch, realizar mudanças e fazer merge:
   ```bash
   git checkout -b feature/novidade
   echo "Nova funcionalidade" >> README.md
   git add README.md
   git commit -m "Adiciona nova funcionalidade"
   git checkout main
   git merge feature/novidade
   ```
5. Colaborar em um repositório compartilhado (fork, pull request).

````
