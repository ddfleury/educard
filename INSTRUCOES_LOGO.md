# 📸 Instruções para Adicionar o Logo EducareOne

## ✅ O que foi feito:

1. ✅ Pasta `public/images/` criada
2. ✅ Componente Header atualizado para usar a imagem do logo
3. ✅ Código configurado para carregar `/images/logo.png`

## 📋 O que você precisa fazer:

### Passo 1: Adicionar a imagem do logo

1. Copie a imagem do logo que você tem
2. Cole na pasta: `C:\xampp\htdocs\educard\public\images\`
3. Renomeie o arquivo para: `logo.png`

**Formatos aceitos:**
- `logo.png` (recomendado)
- `logo.svg` (melhor qualidade, se tiver)
- `logo.jpg` ou `logo.jpeg`

### Passo 2: Se usar outro formato

Se sua imagem for `.svg`, `.jpg` ou `.jpeg`, você precisa atualizar o arquivo `src/components/Header.tsx`:

**Linha 14**, altere:
```tsx
src="/images/logo.png"
```

Para:
```tsx
src="/images/logo.svg"  // ou .jpg, .jpeg
```

### Passo 3: Verificar

1. Inicie o servidor: `npm run dev`
2. Acesse: http://localhost:3000
3. O logo deve aparecer no header (topo da página)

## 🎨 Dimensões recomendadas:

- **Largura:** 200-300px
- **Altura:** 50-80px
- **Formato:** PNG com fundo transparente (melhor) ou SVG

## ⚠️ Nota:

Se a imagem não aparecer:
- Verifique se o arquivo está em `public/images/logo.png`
- Verifique se o nome do arquivo está correto (case-sensitive)
- Limpe o cache do navegador (Ctrl + F5)
- Verifique o console do navegador para erros

## 📁 Estrutura de arquivos:

```
educard/
└── public/
    └── images/
        └── logo.png  ← Coloque sua imagem aqui
```


