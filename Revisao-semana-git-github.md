# 📘 Git e GitHub – Resumo de Revisão

---

## 🔹 O que é Git?
- Sistema de **controle de versões distribuído**
- Permite:
  - Rastrear mudanças no código
  - Colaborar em equipe
  - Mantém histórico de versões

---

## 🛠️ Instalação do Git

### Windows
- Baixe em: [git-scm.com](https://git-scm.com)
- Siga o instalador
- Verifique com:
  ```bash
  git --version
  ```

### macOS
- No terminal:
  ```bash
  brew install git
  git --version
  ```

### Linux

#### Debian/Ubuntu:
```bash
sudo apt-get install git
```

#### Fedora:
```bash
sudo dnf install git
```

- Verifique:
  ```bash
  git --version
  ```

---

## ⚙️ Configuração Inicial

### Nome e e-mail:
```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```

### Verificar configuração:
```bash
git config --list
```

### Configurar editor (VS Code):
```bash
git config --global core.editor "code --wait"
```

---

## 📁 Começando com Repositórios

### Clonar Repositório
```bash
git clone https://github.com/usuario/repositorio.git
```

### Criar Novo Repositório
```bash
mkdir nome-do-projeto
cd nome-do-projeto
git init
```

---

## 🔄 Estados e Fluxo de Trabalho no Git

### 🧩 Três Estados dos Arquivos
- **Modificado (Modified)** – Arquivo alterado
- **Preparado (Staged)** – Pronto para commit
- **Confirmado (Committed)** – Salvo no repositório local

### 🗂️ Três Áreas no Git
- **Diretório de Trabalho (Working Directory)** – onde arquivos são editados
- **Área de Preparação (Staging Area)** – onde arquivos aguardam confirmação
- **Diretório do Git (Git Directory)** – onde commits são armazenados

---

## 🧰 Comandos Básicos do Fluxo de Trabalho

| Comando                     | Função                                                    |
|----------------------------|------------------------------------------------------------|
| `git status`               | Verifica estado atual dos arquivos                         |
| `git add <arquivo>`        | Move arquivo modificado para a área de preparação          |
| `git commit -m "mensagem"` | Confirma mudanças com uma mensagem                         |
| `git log`                  | Exibe histórico de commits                                 |

---

## ✅ Exemplo de Fluxo de Trabalho

```bash
# Criar/modificar um arquivo
echo "Olá, Git" > arquivo.txt

# Verificar o estado atual
git status

# Preparar o arquivo
git add arquivo.txt

# Confirmar a mudança
git commit -m "Adicionar arquivo de exemplo"

# Ver histórico de commits
git log
```

---

## 🐙 Introdução ao GitHub

### O que é GitHub?
- Plataforma de **desenvolvimento colaborativo baseada em Git**
- Interface web + ferramentas extras de colaboração

### Principais Recursos:
- **Repositórios**: Guardam o projeto e seu histórico
- **Colaboração**: Pull requests, revisões e discussões
- **Integrações**: CI/CD, automações e ferramentas externas
- **GitHub Pages**: Hospedagem gratuita para sites estáticos

---

## 🔁 Controle de Versões com GitHub

### Benefícios:
- Histórico completo de mudanças
- Trabalho em equipe eficiente sem sobrescrever código
- Reversão fácil para versões anteriores
- **Branches** para desenvolvimento paralelo sem conflitos

---

## 🚀 Fluxo de Trabalho Básico no GitHub

### Clonar repositório
```bash
git clone https://github.com/usuario/repositorio.git
```

### Criar um ramo (branch)
```bash
git checkout -b nova-feature
```

### Fazer commits localmente
```bash
git add .
git commit -m "Implementa nova feature"
```

### Enviar para o GitHub (push)
```bash
git push origin nova-feature
```

### Criar um Pull Request
- Solicite a mesclagem no GitHub
- Espere revisão de código

### Revisar e mesclar
- Após aprovação, o PR é mesclado ao branch principal

### Desfazendo commits locais (sem enviar para o repositório remoto):

```bash
git reset --hard HEAD~1:
```

- Desfaz o último commit e remove as alterações do diretório de trabalho. Isso significa que as mudanças feitas no commit serão perdidas. 

```bash
git reset --soft HEAD~1:
```

- Desfaz o último commit, mas mantém as alterações no seu diretório de trabalho. Isso permite que você faça novas modificações e crie um novo commit com as alterações corrigidas. 

```bash
git reset --mixed HEAD~1:
```

- É o padrão do git reset e desfaz o último commit, mantendo as alterações no staging area. Você precisará adicionar as alterações novamente e commitar. 
Desfazendo commits remotos (após enviar para o repositório remoto):
 
>>
Nota: 

git revert <hash_do_commit>: Cria um novo commit que reverte as alterações feitas pelo commit especificado. Isso é mais seguro do que o git reset --hard para commits que já foram compartilhados com outras pessoas. 

---

## 📌 Conclusão

- Git é essencial para controle de versões local.
- GitHub amplia as possibilidades com **colaboração em nuvem**.
- Dominar o fluxo de trabalho e comandos básicos é essencial para o desenvolvimento moderno.
