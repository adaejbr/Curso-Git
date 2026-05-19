# 🎯 Projeto de Treinamento Git/GitHub - Ada EJ

**Descrição para GitHub:**
> Projeto educacional para membros da empresa júnior Ada praticarem Git, GitHub e Git Flow Next. Inclui exercícios práticos de versionamento, colaboração e padrões de desenvolvimento profissional.

## 📋 Sobre o Projeto

Este é um projeto de treinamento desenvolvido especificamente para membros da **empresa júnior Ada** aprimorarem seus conhecimentos em:

- **Git**: Controle de versão e comandos essenciais
- **GitHub**: Plataforma de colaboração e hospedagem de código
- **Git Flow Next**: Metodologia de branching para projetos profissionais.
- **Boas práticas**: Padrões de desenvolvimento colaborativo

## 🎯 Objetivos de Aprendizagem

Ao completar este treinamento, você será capaz de:

- [ ] Criar e gerenciar repositórios Git
- [ ] Trabalhar com branches usando Git Flow Next
- [ ] Fazer commits seguindo convenções profissionais
- [ ] Colaborar através de Pull Requests
- [ ] Resolver conflitos de merge
- [ ] Usar issues para organização de tarefas
- [ ] Aplicar tags e releases

## 🚀 Como Começar

### 1. **Fork e Clone**
```bash
# 1. Faça um fork deste repositório DA BRANCH MAIN
# 2. Clone seu fork localmente (preferencialmente via SSH)
git clone git@github.com:seu-usuario/Curso-Git.git
cd Curso-Git
```

**⚠️ Importante:** Sempre faça o fork da branch `main`, que é a branch de produção estável. A branch `develop` será criada localmente após a inicialização do Git Flow Next.

### 2. **Configuração Inicial**
```bash
# Configure seu Git (se ainda não fez)
git config --global user.name "Seu Nome"
git config --global user.email "seu.email@exemplo.com"

# Configure SSH para GitHub (se ainda não fez)
# 1. Gere uma chave SSH (se não tiver)
ssh-keygen -t ed25519 -C "seu.email@exemplo.com"

# 2. Adicione a chave ao ssh-agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519

# 3. Copie a chave pública e adicione no GitHub
cat ~/.ssh/id_ed25519.pub
# Vá em GitHub → Settings → SSH and GPG keys → New SSH key
```

### 3. **Instalação e Inicialização do Git Flow Next**

---

### ✅ Pré‑requisitos

Antes de instalar o `git-flow-next`, você precisa ter o **Git** instalado e funcionando no seu Windows.

*   **Git para Windows**: Baixe a versão mais recente no [site oficial](https://git-scm.com/downloads/win). Durante a instalação, recomenda‑se manter as opções padrão, que incluem o **Git Bash**.
*   **Verifique a instalação**: Abra um terminal (**PowerShell**, **Prompt de Comando** ou **Git Bash**) e execute:
    ```bash
    git --version
    ```
    Se o comando retornar a versão do Git (ex: `git version 2.47.1.windows.1`), você está pronto para seguir.

---

## 🎯 Instalação usando o Winget (Gerenciador de Pacotes Nativo do Windows)

O Winget é o gerenciador de pacotes oficial da Microsoft. É a forma mais simples e recomendada pela equipe do `git-flow-next` para usuários Windows.

### 1. Instale o Winget (geralmente já vem com o Windows 10/11)
Caso não tenha, baixe o [App Installer](https://apps.microsoft.com/detail/9nblggh4nns1) da Microsoft Store.

### 2. Instale o `git-flow-next`
Abra o **PowerShell** (como usuário comum, não precisa ser administrador) e execute:
```powershell
winget install GitTower.GitFlowNext
```
Este comando baixará e instalará automaticamente a versão mais recente do `git-flow-next`.

### 3. Verifique a instalação
Após a conclusão, feche e reabra o terminal (ou inicie uma nova sessão do PowerShell) e execute:
```bash
git flow version
```
Se tudo ocorreu bem, você verá a versão do `git-flow-next`.

### 4. Inicie no seu repositório
Entre no repositório onde deseja usar o Git Flow e execute:
```bash
git flow init
```
Siga as instruções interativas para configurar os nomes das branches (ou aceite os padrões).

---

## 🧪 Verificação da Instalação e Primeiros Passos

Independentemente do método escolhido, após a instalação você pode confirmar que o `git-flow-next` está funcionando corretamente.

1. **Teste o comando principal:**
   ```bash
   git flow version
   ```
   Exemplo de saída esperada:
   ```
   git-flow-next version 0.9.1
   ```

2. **Inicialize o Git Flow em um repositório:**
   ```bash
   git flow init
   ```
   O comando irá perguntar sobre os nomes das branches principais (`main` e `develop`). Você pode aceitar os valores padrão pressionando `Enter`.

3. **Crie sua primeira feature:**
   ```bash
   git flow feature start minha-feature
   ```
   Isso criará e trocará automaticamente para a branch `feature/minha-feature` baseada na `develop`.

Se você encontrar a mensagem `'git flow' is not a git command`, significa que o executável `git-flow.exe` não foi encontrado. Verifique:
*   Se você está usando um terminal novo após a instalação.
*   Se o diretório onde `git-flow.exe` foi colocado está realmente na variável `PATH`.
*   No caso da instalação manual, certifique‑se de que o arquivo foi renomeado para `git-flow.exe`.

---

**📝 Fluxo de Trabalho:**
1. **Fork da `main`** → repositório estável.
2. **Clone local** → sua cópia de trabalho.
3. **`git flow init`** → cria a estrutura de branches.
4. **Trabalhe na `develop`** → branch principal para desenvolvimento.
5. **Features, Releases, Hotfixes** → criadas a partir da `develop`.

## 📚 Exercícios Práticos

### **Nível Iniciante**
1. **Primeiro Commit**: Adicione seu nome ao arquivo `CONTRIBUTORS.md`
2. **Branching**: Crie uma branch `feature/meu-nome-introducao`
3. **Pull Request**: Abra um PR com sua introdução

### **Nível Intermediário**
4. **Git Flow Next Feature**: Use `git flow feature start minha-funcionalidade` para criar uma nova feature.
5. **Conflitos**: Resolva conflitos intencionais criados.
6. **Histórico**: Use `git log`, `git blame` e `git show`.

### **Nível Avançado**
7. **Release**: Crie uma release usando `git flow release start v1.0.0` e depois finalize com `git flow release finish v1.0.0`.
8. **Hotfix**: Simule e corrija um bug crítico com `git flow hotfix start correcao-urgente`.
9. **Comandos Abreviados (Shorthands)**: Pratique comandos como `git flow finish` que, em uma branch `feature`, executam `git flow feature finish` automaticamente.

## 🛠️ Comandos Essenciais

### **Git Básico**
```bash
git status                 # Ver status do repositório
git add .                  # Adicionar arquivos ao staging
git commit -m "mensagem"   # Fazer commit
git push origin branch     # Enviar para repositório remoto
git pull origin main       # Atualizar branch local
```

### **Git Flow Next**
```bash
# Inicialização
git flow init                         # Inicialização interativa padrão
git flow init --defaults              # Inicialização com valores padrão (não-interativo)
git flow init --preset=classic        # Inicializar com o preset 'Classic GitFlow'

# Gerenciamento de Branches
git flow feature start nome-feature   # Iniciar nova feature
git flow feature finish nome-feature  # Finalizar feature
git flow release start v1.0.0         # Iniciar release
git flow hotfix start nome-hotfix     # Iniciar hotfix

# Comandos Abreviados (Shorthands) - Detectam automaticamente o tipo da branch atual
git flow finish                       # Finaliza a branch atual (feature, release ou hotfix)
git flow update                       # Atualiza a branch atual a partir de sua branch pai
git flow publish                      # Publica a branch atual no repositório remoto
```

## 📝 Convenções do Projeto

### **Commits**
Use o padrão conventional commits:
```
feat: adiciona nova funcionalidade
fix: corrige bug específico
docs: atualiza documentação
style: formatação e estilo
refactor: refatoração de código
test: adiciona ou corrige testes
```

### **Branches**
- `main`: Branch principal (produção)
- `develop`: Branch de desenvolvimento
- `feature/nome-da-feature`: Novas funcionalidades
- `release/vX.X.X`: Preparação para release
- `hotfix/nome-do-fix`: Correções críticas

### **Pull Requests**
- Título claro e descritivo
- Descrição detalhada das mudanças
- Referencie issues relacionadas
- Solicite review de pelo menos 1 pessoa

## 🏆 Desafios Extras

1. **Configurar GitHub Actions** para CI/CD básico
2. **Criar templates** para issues e PRs
3. **Implementar branch protection rules**
4. **Usar GitHub Projects** para organização
5. **Configurar webhooks** para integrações

## 📖 Recursos de Estudo

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [git-flow-next Official Site](https://git-flow.sh/)
- [git-flow-next Commands Reference](https://git-flow.sh/docs/commands)
- [Conventional Commits](https://www.conventionalcommits.org/)

## 🤝 Como Contribuir

1. Fork o projeto
2. Crie uma branch para sua feature (`git flow feature start minha-feature`)
3. Commit suas mudanças (`git commit -m 'feat: adiciona minha feature'`)
4. Push para a branch (`git push origin feature/minha-feature`)
5. Abra um Pull Request

## 📞 Suporte

- **Issues**: Use para dúvidas, bugs ou sugestões
- **Discussions**: Para discussões gerais sobre Git/GitHub
- **Wiki**: Documentação adicional e tutoriais

---

**Bom treinamento! 🚀**

**Última atualização:** 18 de maio de 2026

*Projeto mantido pela empresa júnior Ada para fins educacionais.*
