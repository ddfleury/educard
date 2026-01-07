# EducareOne - Plataforma Modular de Serviços

Uma plataforma full-stack moderna que integra múltiplos serviços em um único ecossistema: Educação (Escola e Cursos), Saúde, Viagem e Jurídico.

## 🚀 Tecnologias

- **Frontend**: Next.js 14 (App Router), React, TypeScript, Tailwind CSS
- **Backend**: Next.js API Routes
- **Database**: PostgreSQL com Prisma ORM
- **Ícones**: Lucide React

## 📁 Estrutura do Projeto

```
educareone/
├── prisma/
│   └── schema.prisma          # Schema do banco de dados
├── src/
│   ├── app/                   # Rotas do Next.js (App Router)
│   │   ├── page.tsx          # Página inicial
│   │   ├── login/            # Página de login
│   │   ├── escola/           # Módulo Escola
│   │   ├── saude/            # Módulo Saúde
│   │   ├── cursos/           # Módulo Cursos
│   │   ├── viagem/           # Módulo Viagem
│   │   └── juridico/         # Módulo Jurídico
│   ├── components/           # Componentes React reutilizáveis
│   │   ├── Layout.tsx
│   │   ├── Header.tsx
│   │   ├── Hero.tsx
│   │   ├── ValueProposition.tsx
│   │   ├── ServiceCard.tsx
│   │   └── MobileApp.tsx
│   └── modules/              # Lógica de negócio modular
│       ├── escola/
│       ├── saude/
│       ├── cursos/
│       ├── viagem/
│       └── juridico/
└── package.json
```

## 🛠️ Instalação

1. **Clone o repositório** (ou navegue até a pasta do projeto)

2. **Instale as dependências**:
```bash
npm install
```

3. **Configure o banco de dados**:
   - Crie um arquivo `.env` na raiz do projeto
   - Adicione a variável `DATABASE_URL` com a conexão do PostgreSQL:
   ```
   DATABASE_URL="postgresql://user:password@localhost:5432/educareone?schema=public"
   ```

4. **Configure o Prisma**:
```bash
npx prisma generate
npx prisma db push
```

5. **Inicie o servidor de desenvolvimento**:
```bash
npm run dev
```

6. **Acesse a aplicação**:
   - Abra [http://localhost:3000](http://localhost:3000) no navegador

## 📋 Funcionalidades

### Página Inicial
- Hero section com call-to-action
- Barra de proposta de valor (Integração Total, Segurança de Dados, Otimização de Tempo)
- Grid de cards com os 5 módulos principais
- Seção do aplicativo móvel

### Módulos Disponíveis

1. **Escola** (`/escola`)
   - Gestão escolar completa
   - Acompanhamento acadêmico
   - Comunicação com a escola

2. **Saúde** (`/saude`)
   - Telemedicina
   - Acesso a resultados de exames
   - Acompanhamento médico

3. **Cursos** (`/cursos`)
   - Trilhas de aprendizagem
   - Cursos online
   - Certificações

4. **Viagem** (`/viagem`)
   - Turismo pedagógico
   - Roteiros educacionais
   - Planejamento de viagens

5. **Jurídico** (`/juridico`)
   - Assessoria legal
   - Consultoria jurídica
   - Gestão de processos

## 🗄️ Modelo de Dados

O schema Prisma inclui models para:
- `User`: Usuários do sistema
- `Student`: Alunos (módulo Escola)
- `Patient`: Pacientes (módulo Saúde)
- `Course` e `CourseEnrollment`: Cursos e matrículas
- `TravelBooking`: Reservas de viagem
- `LegalClient` e `LegalCase`: Clientes e processos jurídicos

## 🎨 Design System

O projeto utiliza Tailwind CSS com cores personalizadas:
- **Azul** (`primary-blue`): Módulo Escola
- **Verde** (`primary-green`): Módulo Saúde
- **Laranja** (`primary-orange`): Módulo Cursos
- **Roxo** (`primary-purple`): Módulo Viagem
- **Cinza Escuro** (`primary-dark`): Módulo Jurídico

## 📱 Responsividade

O design é totalmente responsivo, adaptando-se a:
- Desktop (1024px+)
- Tablet (768px - 1023px)
- Mobile (< 768px)

## 🔐 Autenticação

A página de login está disponível em `/login`. A implementação completa de autenticação pode ser adicionada usando NextAuth.js ou outra solução de autenticação.

## 🚧 Próximos Passos

- [ ] Implementar autenticação completa
- [ ] Criar API Routes para cada módulo
- [ ] Adicionar testes unitários e de integração
- [ ] Implementar dashboard para cada módulo
- [ ] Adicionar sistema de notificações
- [ ] Integrar pagamentos
- [ ] Desenvolver aplicativo móvel

## 📝 Licença

Este projeto é privado e proprietário da EducareOne.

## 👥 Desenvolvimento

Desenvolvido com foco em:
- Arquitetura modular e escalável
- Código limpo e manutenível
- Performance e otimização
- Experiência do usuário (UX)


