# Guia de Instalação - EducareOne

## Pré-requisitos

Antes de começar, certifique-se de ter instalado:

- **Node.js** (versão 18 ou superior)
- **npm** ou **yarn**
- **PostgreSQL** (versão 12 ou superior)
- **Git** (opcional)

## Passo a Passo

### 1. Instalar Dependências

```bash
npm install
```

### 2. Configurar Banco de Dados

1. Crie um banco de dados PostgreSQL chamado `educareone`:
```sql
CREATE DATABASE educareone;
```

2. Crie um arquivo `.env` na raiz do projeto:
```env
DATABASE_URL="postgresql://seu_usuario:sua_senha@localhost:5432/educareone?schema=public"
```

**Importante**: Substitua `seu_usuario` e `sua_senha` pelas suas credenciais do PostgreSQL.

### 3. Configurar Prisma

1. Gere o cliente Prisma:
```bash
npm run db:generate
```

2. Aplique o schema ao banco de dados:
```bash
npm run db:push
```

### 4. Iniciar o Servidor de Desenvolvimento

```bash
npm run dev
```

### 5. Acessar a Aplicação

Abra seu navegador e acesse:
- **URL**: http://localhost:3000

## Comandos Disponíveis

- `npm run dev` - Inicia o servidor de desenvolvimento
- `npm run build` - Cria uma build de produção
- `npm run start` - Inicia o servidor de produção
- `npm run lint` - Executa o linter
- `npm run db:generate` - Gera o cliente Prisma
- `npm run db:push` - Aplica mudanças do schema ao banco
- `npm run db:studio` - Abre o Prisma Studio (interface visual do banco)

## Estrutura de Rotas

Após a instalação, você terá acesso às seguintes rotas:

- `/` - Página inicial
- `/login` - Área do cliente / Login
- `/escola` - Módulo Escola
- `/saude` - Módulo Saúde
- `/cursos` - Módulo Cursos
- `/viagem` - Módulo Viagem
- `/juridico` - Módulo Jurídico

## Troubleshooting

### Erro de conexão com o banco de dados

- Verifique se o PostgreSQL está rodando
- Confirme que as credenciais no `.env` estão corretas
- Verifique se o banco de dados `educareone` foi criado

### Erro ao executar `npm install`

- Certifique-se de estar usando Node.js 18+
- Tente limpar o cache: `npm cache clean --force`
- Delete a pasta `node_modules` e o arquivo `package-lock.json`, depois execute `npm install` novamente

### Porta 3000 já está em uso

- Altere a porta no arquivo `package.json`:
  ```json
  "dev": "next dev -p 3001"
  ```

## Próximos Passos

Após a instalação bem-sucedida:

1. Explore a página inicial
2. Navegue pelos diferentes módulos
3. Verifique o schema do banco de dados no Prisma Studio: `npm run db:studio`
4. Comece a desenvolver novas funcionalidades!

