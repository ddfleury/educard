# 🚀 Como Rodar o Sistema EducareOne

## ⚠️ IMPORTANTE: Política de Execução do PowerShell

Se você receber um erro sobre "execução de scripts foi desabilitada", siga um destes métodos:

### Método 1: Usar CMD (Prompt de Comando) ao invés de PowerShell

1. Abra o **Prompt de Comando** (CMD) como Administrador
2. Navegue até a pasta do projeto:
   ```
   cd C:\xampp\htdocs\educard
   ```
3. Execute os comandos normalmente

### Método 2: Habilitar Scripts no PowerShell (Recomendado)

1. Abra o PowerShell como **Administrador**
2. Execute este comando:
   ```
   Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
   ```
3. Digite `S` para confirmar
4. Agora você pode usar `npm` normalmente

### Método 3: Usar Terminal Integrado do VS Code/Cursor

1. Abra o terminal integrado do seu editor
2. Execute os comandos normalmente

---

## 📋 Passo a Passo Completo

### 1️⃣ Instalar Dependências

No terminal (CMD, PowerShell ou Terminal Integrado), execute:

```bash
npm install
```

**Tempo estimado:** 2-5 minutos

Isso vai instalar:
- Next.js
- React
- TypeScript
- Tailwind CSS
- Prisma
- Lucide React (ícones)
- E todas as outras dependências

### 2️⃣ Configurar Banco de Dados (OPCIONAL)

**Você pode pular este passo se quiser apenas testar o frontend!**

O sistema funciona sem banco de dados para visualizar as páginas.

Se quiser configurar o banco:

1. **Crie o arquivo `.env`** na raiz do projeto (`C:\xampp\htdocs\educard\.env`)

2. **Adicione esta linha** (ajuste usuário e senha):
   ```
   DATABASE_URL="postgresql://postgres:senha@localhost:5432/educareone?schema=public"
   ```

3. **Execute os comandos do Prisma:**
   ```bash
   npm run db:generate
   npm run db:push
   ```

### 3️⃣ Rodar o Sistema

Execute:

```bash
npm run dev
```

Você verá uma mensagem como:
```
▲ Next.js 14.0.4
- Local:        http://localhost:3000
- ready started server on 0.0.0.0:3000
```

### 4️⃣ Acessar no Navegador

Abra seu navegador e acesse:

**👉 http://localhost:3000**

## ✅ O que você verá:

- **Página Inicial** com hero section, cards dos módulos e seção mobile
- **Header** com navegação e botão de login
- **Links funcionais** para todos os módulos

## 🎯 Rotas Disponíveis:

- `/` - Página inicial
- `/login` - Área do cliente / Login
- `/escola` - Módulo Escola
- `/saude` - Módulo Saúde  
- `/cursos` - Módulo Cursos
- `/viagem` - Módulo Viagem
- `/juridico` - Módulo Jurídico

## 🛑 Para Parar o Servidor

No terminal, pressione: **Ctrl + C**

## 🔧 Comandos Úteis:

```bash
npm run dev          # Inicia servidor de desenvolvimento
npm run build        # Cria build de produção
npm run start        # Inicia servidor de produção
npm run lint         # Verifica erros de código
npm run db:studio    # Abre interface visual do banco (Prisma Studio)
```

## ❓ Problemas Comuns:

### "Porta 3000 já está em uso"
- O Next.js vai perguntar se quer usar outra porta (ex: 3001)
- Ou feche o programa que está usando a porta 3000

### "Cannot find module"
- Execute `npm install` novamente
- Delete a pasta `node_modules` e execute `npm install` novamente

### Erros do Prisma
- Se não configurou o banco, ignore esses erros
- O frontend funciona normalmente sem banco de dados

### "npm não é reconhecido"
- Instale o Node.js: https://nodejs.org/
- Reinicie o terminal após instalar

## 📞 Precisa de Ajuda?

Verifique:
1. ✅ Node.js está instalado? (`node --version`)
2. ✅ Está na pasta correta? (`cd C:\xampp\htdocs\educard`)
3. ✅ Dependências instaladas? (`npm install`)
4. ✅ Servidor rodando? (`npm run dev`)

---

**🎉 Pronto! Seu sistema está rodando!**


