# 🔧 Configuração para GitHub

## ✅ Arquivos Corrigidos

### 1. `.gitignore` Atualizado
- ✅ Removido `next-env.d.ts` da lista de ignorados (deve ser commitado)
- ✅ Adicionadas mais exclusões importantes
- ✅ Configurado corretamente para Next.js

### 2. `.npmrc` Criado
- ✅ Configurações do npm para instalação correta
- ✅ Evita problemas com peer dependencies

### 3. `package.json` Atualizado
- ✅ Adicionado `engines` para especificar versão do Node.js
- ✅ Adicionado script `postinstall` para gerar Prisma Client automaticamente

### 4. Arquivos de Versão do Node
- ✅ `.nvmrc` - Para usuários do nvm
- ✅ `.node-version` - Para outras ferramentas

## 📋 Checklist Antes de Fazer Commit

Antes de enviar para o GitHub, certifique-se de:

- [ ] **Remover pastas duplicadas** (educard/, test/, src/ duplicados)
- [ ] **Manter apenas a estrutura correta na raiz**
- [ ] **Commitar `next-env.d.ts`** (não deve estar no .gitignore)
- [ ] **Commitar `package-lock.json`** (deve estar no repositório)
- [ ] **NÃO commitar `node_modules/`** (deve estar no .gitignore)
- [ ] **NÃO commitar `.env`** (deve estar no .gitignore)

## 🚀 Comandos para GitHub

### 1. Limpar e Preparar

```bash
# Remover node_modules local (será reinstalado)
rm -rf node_modules

# Limpar cache do npm
npm cache clean --force

# Verificar o que será commitado
git status
```

### 2. Adicionar Arquivos

```bash
# Adicionar todos os arquivos (exceto os do .gitignore)
git add .

# Verificar o que será commitado
git status
```

### 3. Commit e Push

```bash
git commit -m "feat: projeto EducareOne otimizado para Next.js"
git push origin main
```

## 🔍 Verificar no GitHub

Após fazer push, verifique:

1. ✅ `package.json` está presente
2. ✅ `package-lock.json` está presente
3. ✅ `next-env.d.ts` está presente
4. ✅ `node_modules/` NÃO está presente
5. ✅ `.env` NÃO está presente

## 🐛 Solução de Problemas

### Erro: "Cannot find module"

**Solução:**
```bash
# No GitHub Actions ou após clonar
npm ci  # Usa package-lock.json exato
# ou
npm install
```

### Erro: "Prisma Client not generated"

**Solução:**
O script `postinstall` no `package.json` já resolve isso automaticamente. Se ainda der erro:

```bash
npm run db:generate
```

### Erro: "Node version mismatch"

**Solução:**
Use Node.js 18 ou superior:

```bash
# Com nvm
nvm use 18
nvm install 18

# Verificar versão
node --version
```

### Erro: "Missing dependencies"

**Solução:**
```bash
# Limpar e reinstalar
rm -rf node_modules package-lock.json
npm install
```

## 📝 Estrutura Correta para GitHub

```
educard/
├── .gitignore          ✅ Deve estar
├── .npmrc              ✅ Deve estar
├── .nvmrc              ✅ Deve estar
├── package.json        ✅ Deve estar
├── package-lock.json   ✅ Deve estar
├── next-env.d.ts       ✅ Deve estar (NÃO ignorar)
├── tsconfig.json       ✅ Deve estar
├── next.config.js      ✅ Deve estar
├── tailwind.config.ts  ✅ Deve estar
├── postcss.config.js    ✅ Deve estar
├── prisma/
│   └── schema.prisma   ✅ Deve estar
├── public/
│   └── images/         ✅ Deve estar
└── src/                ✅ Deve estar
    ├── app/
    ├── components/
    ├── lib/
    └── modules/
```

## ⚠️ Arquivos que NÃO devem estar no GitHub

- ❌ `node_modules/`
- ❌ `.env`
- ❌ `.env.local`
- ❌ `.next/`
- ❌ `out/`
- ❌ `*.log`
- ❌ `.DS_Store`

## 🎯 GitHub Actions (Opcional)

Se quiser configurar CI/CD, crie `.github/workflows/ci.yml`:

```yaml
name: CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    
    steps:
      - uses: actions/checkout@v3
      
      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'
          cache: 'npm'
      
      - name: Install dependencies
        run: npm ci
      
      - name: Generate Prisma Client
        run: npm run db:generate
      
      - name: Build
        run: npm run build
      
      - name: Lint
        run: npm run lint
```

---

**Agora o projeto está pronto para o GitHub!** 🚀

