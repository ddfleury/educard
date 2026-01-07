# 🚀 Guia Rápido - Como Rodar o Sistema

## Passo 1: Instalar Dependências

Abra o terminal na pasta do projeto e execute:

```bash
npm install
```

Isso vai instalar todas as dependências necessárias (Next.js, React, Prisma, etc.)

## Passo 2: Configurar Banco de Dados (Opcional para começar)

**Opção A - Sem banco de dados (para testar o frontend):**
Você pode rodar o sistema sem configurar o banco primeiro. O frontend funcionará normalmente.

**Opção B - Com banco de dados (recomendado):**

1. Crie um arquivo `.env` na raiz do projeto com:
```
DATABASE_URL="postgresql://usuario:senha@localhost:5432/educareone?schema=public"
```

2. Execute os comandos do Prisma:
```bash
npm run db:generate
npm run db:push
```

## Passo 3: Rodar o Sistema

Execute o comando:

```bash
npm run dev
```

## Passo 4: Acessar no Navegador

Abra seu navegador e acesse:

**http://localhost:3000**

## ✅ Pronto!

O sistema estará rodando e você poderá:
- Ver a página inicial
- Navegar pelos módulos (Escola, Saúde, Cursos, Viagem, Jurídico)
- Acessar a página de login

## 📝 Comandos Úteis

- `npm run dev` - Inicia o servidor de desenvolvimento
- `npm run build` - Cria build de produção
- `npm run start` - Inicia servidor de produção
- `npm run db:studio` - Abre interface visual do banco (Prisma Studio)

## ⚠️ Problemas Comuns

**Erro: "Cannot find module"**
- Execute `npm install` novamente

**Porta 3000 ocupada**
- O Next.js vai perguntar se quer usar outra porta (ex: 3001)

**Erro de banco de dados**
- Se não configurou o banco, ignore os erros do Prisma por enquanto
- O frontend funcionará normalmente sem o banco

