# 🎯 Projeto de Treinamento Git/GitHub - Ada EJ

**Descrição para GitHub:**
> Projeto educacional para membros da empresa júnior Ada praticarem Git, GitHub e Git Flow. Inclui exercícios práticos de versionamento, colaboração e padrões de desenvolvimento profissional.

## 📋 Sobre o Projeto

Este é um projeto de treinamento desenvolvido especificamente para membros da **empresa júnior Ada** aprimorarem seus conhecimentos em:

- **Git**: Controle de versão e comandos essenciais
- **GitHub**: Plataforma de colaboração e hospedagem de código
- **Git Flow**: Metodologia de branching para projetos profissionais
- **Boas práticas**: Padrões de desenvolvimento colaborativo

## 🎯 Objetivos de Aprendizagem

Ao completar este treinamento, você será capaz de:

- [ ] Criar e gerenciar repositórios Git
- [ ] Trabalhar com branches seguindo Git Flow
- [ ] Fazer commits seguindo convenções profissionais
- [ ] Colaborar através de Pull Requests
- [ ] Resolver conflitos de merge
- [ ] Usar issues para organização de tarefas
- [ ] Aplicar tags e releases

## 🚀 Como Começar

### 1. **Fork e Clone**
```bash
# 1. Faça um fork deste repositório DA BRANCH MAIN
# 2. Clone seu fork localmente usando SSH
git clone https://github.com/adaejbr/Curso-Git.git
cd Curso-Git
```

**⚠️ Importante:** Sempre faça o fork da branch `main`, que é a branch de produção estável. A branch `develop` será criada localmente após a inicialização do Git Flow.

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

### 3. **Inicialização do Git Flow**
```bash
# Instale git-flow (se necessário)
# Ubuntu/Debian: sudo apt-get install git-flow
# macOS: brew install git-flow
# Windows: wget -q -O - --no-check-certificate https://github.com/nvie/gitflow/raw/develop/contrib/gitflow-installer.sh | bash

# Inicialize git-flow no projeto (aceite as configurações padrão)
git flow init

# Após git flow init, você terá:
# - main: branch de produção (já existe do fork)
# - develop: branch de desenvolvimento (criada automaticamente)
```

**📝 Fluxo de Trabalho:**
1. **Fork da `main`** → repositório estável
2. **Clone local** → sua cópia de trabalho
3. **`git flow init`** → cria estrutura de branches
4. **Trabalhe na `develop`** → branch para desenvolvimento
5. **Features** → criadas a partir da `develop`

## 📚 Exercícios Práticos

### **Nível Iniciante**
1. **Primeiro Commit**: Adicione seu nome ao arquivo `CONTRIBUTORS.md`
2. **Branching**: Crie uma branch `feature/meu-nome-introducao`
3. **Pull Request**: Abra um PR com sua introdução

### **Nível Intermediário**
4. **Git Flow Feature**: Use `git flow feature start nova-funcionalidade`
5. **Conflitos**: Resolva conflitos intencionais criados
6. **Histórico**: Use `git log`, `git blame` e `git show`

### **Nível Avançado**
7. **Release**: Crie uma release usando Git Flow
8. **Hotfix**: Simule e corrija um bug crítico
9. **Rebase**: Pratique rebase interativo para limpar histórico

## 🛠️ Comandos Essenciais

### **Git Básico**
```bash
git status                 # Ver status do repositório
git add .                  # Adicionar arquivos ao staging
git commit -m "mensagem"   # Fazer commit
git push origin branch     # Enviar para repositório remoto
git pull origin main       # Atualizar branch local
```

### **Git Flow**
```bash
git flow feature start nome-feature    # Iniciar nova feature
git flow feature finish nome-feature   # Finalizar feature
git flow release start v1.0.0          # Iniciar release
git flow hotfix start nome-hotfix       # Iniciar hotfix
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
- [Git Flow Cheatsheet](https://danielkummer.github.io/git-flow-cheatsheet/)
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

**Última atualização:** 05 de agosto de 2025

*Projeto mantido pela empresa júnior Ada para fins educacionais.*
