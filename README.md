# Zynx Wallet - Documentação Mintlify

Documentação completa da API Zynx Wallet construída com Mintlify.

## 📁 Estrutura do Projeto

```
zynx-docs/
├── docs/
│   ├── introduction.mdx              # Página inicial
│   ├── getting-started/              # Guias de introdução
│   │   ├── overview.mdx
│   │   ├── authentication.mdx
│   │   ├── rate-limiting.mdx
│   │   └── errors.mdx
│   ├── api-reference/                # Referência da API
│   │   ├── introduction.mdx
│   │   ├── payments/
│   │   ├── withdrawals/
│   │   ├── transfers/
│   │   └── account/
│   ├── webhooks/                     # Documentação de webhooks
│   │   ├── overview.mdx
│   │   ├── events.mdx
│   │   └── testing.mdx
│   ├── guides/                       # Guias práticos
│   │   ├── pix-integration.mdx
│   │   ├── qr-code.mdx
│   │   ├── webhook-integration.mdx
│   │   ├── security-best-practices.mdx
│   │   └── error-handling.mdx
│   └── resources/                    # Recursos adicionais
│       ├── faq.mdx
│       ├── glossary.mdx
│       └── changelog.mdx
├── public/                           # Arquivos estáticos
│   └── logo/
├── mint.json                         # Configuração Mintlify
└── README.md                         # Este arquivo
```

## 📊 Conteúdo

### Páginas Criadas: 28

- **1** página de introdução
- **4** páginas de guia de início
- **1** página de introdução da API
- **12** páginas de referência da API (Pagamentos, Saques, Transferências, Conta)
- **3** páginas de webhooks
- **5** guias práticos
- **3** páginas de recursos (FAQ, Glossário, Changelog)

## 🚀 Como Implantar no Mintlify

### Opção 1: Usando Mintlify CLI (Recomendado)

#### 1. Instalar Mintlify CLI

```bash
npm install -g mintlify
```

#### 2. Fazer Login

```bash
mintlify login
```

#### 3. Implantar

```bash
cd /tmp/zynx-docs
mintlify deploy
```

#### 4. Acessar Documentação

A documentação será implantada em: `https://zynxwallet.mintlify.app` (ou seu domínio customizado)

### Opção 2: Usando GitHub (Recomendado para Produção)

#### 1. Criar Repositório GitHub

```bash
# Criar novo repositório
# Nome: zynx-wallet-docs
# Descrição: Documentação da API Zynx Wallet
# Visibilidade: Public
```

#### 2. Fazer Push do Código

```bash
cd /tmp/zynx-docs

# Inicializar git
git init

# Adicionar arquivos
git add .

# Commit
git commit -m "Initial documentation"

# Adicionar remote
git remote add origin https://github.com/seu-usuario/zynx-wallet-docs.git

# Push
git branch -M main
git push -u origin main
```

#### 3. Conectar ao Mintlify

1. Acesse [Mintlify Dashboard](https://dashboard.mintlify.app)
2. Clique em "New Project"
3. Selecione seu repositório GitHub
4. Configure as opções:
   - **Root Directory**: `/` (raiz)
   - **Branch**: `main`
5. Clique em "Deploy"

#### 4. Configurar Domínio Customizado (Opcional)

1. No Mintlify Dashboard, vá para "Settings"
2. Clique em "Custom Domain"
3. Insira seu domínio: `docs.zynxwallet.com.br`
4. Siga as instruções para configurar DNS

### Opção 3: Usando Docker

```bash
# Construir imagem Docker
docker build -t zynx-docs .

# Rodar container
docker run -p 3000:3000 zynx-docs

# Acessar em http://localhost:3000
```

## 🔧 Configuração

### mint.json

O arquivo `mint.json` contém toda a configuração:

```json
{
  "name": "Zynx Wallet",
  "logo": {
    "light": "/logo/light.svg",
    "dark": "/logo/dark.svg"
  },
  "colors": {
    "primary": "#0D9488"
  },
  "navigation": [
    // Estrutura de navegação
  ]
}
```

### Customizar Cores

Edite `mint.json`:

```json
"colors": {
  "primary": "#0D9488",      // Cor primária
  "light": "#07C983",        // Cor clara
  "dark": "#065F46"          // Cor escura
}
```

### Customizar Logo

1. Coloque seus arquivos em `public/logo/`
2. Atualize em `mint.json`:

```json
"logo": {
  "light": "/logo/light.svg",
  "dark": "/logo/dark.svg"
}
```

## 📝 Adicionar Novas Páginas

### 1. Criar Arquivo MDX

```bash
touch docs/guides/novo-guia.mdx
```

### 2. Adicionar Frontmatter

```mdx
---
title: Título da Página
description: Descrição breve
---

# Título da Página

Conteúdo aqui...
```

### 3. Atualizar mint.json

```json
"navigation": [
  {
    "group": "Guias",
    "pages": [
      "guides/novo-guia"
    ]
  }
]
```

## 🎨 Estilo e Formatação

### Elementos Suportados

#### Blockquotes

```markdown
> Esta é uma citação
```

#### Callouts

```markdown
<Note>
  Nota importante
</Note>

<Warning>
  Aviso importante
</Warning>

<Tip>
  Dica útil
</Tip>
```

#### Cards

```markdown
<CardGroup cols={2}>
  <Card
    title="Título"
    icon="icon-name"
    href="/link"
  >
    Descrição
  </Card>
</CardGroup>
```

#### Código

````markdown
```javascript
// Código JavaScript
const api = new Zynx();
```

```python
# Código Python
api = Zynx()
```
````

#### Tabelas

```markdown
| Coluna 1 | Coluna 2 |
|----------|----------|
| Valor 1  | Valor 2  |
```

## 🧪 Testar Localmente

### 1. Instalar Dependências

```bash
npm install
```

### 2. Rodar Servidor de Desenvolvimento

```bash
mintlify dev
```

### 3. Acessar

Abra http://localhost:3000 no navegador

## 📦 Publicar Atualizações

### 1. Fazer Alterações

Edite os arquivos `.mdx` conforme necessário

### 2. Commit e Push

```bash
git add .
git commit -m "Atualizar documentação"
git push origin main
```

### 3. Mintlify Implanta Automaticamente

A documentação será atualizada automaticamente em alguns segundos

## 🔍 SEO e Metadados

Cada página tem metadados para SEO:

```mdx
---
title: Título da Página (aparece no navegador)
description: Descrição (aparece em buscas)
---
```

## 📊 Analytics

Para adicionar analytics:

1. Vá para Mintlify Dashboard
2. Clique em "Settings"
3. Configure Google Analytics ou Mixpanel
4. Obtenha o ID de rastreamento
5. Atualize em `mint.json`:

```json
"analytics": {
  "ga4": {
    "measurementId": "G-XXXXXXX"
  }
}
```

## 🔐 Segurança

### Proteger Documentação

Se desejar proteger com senha:

1. Vá para Mintlify Dashboard
2. Clique em "Settings"
3. Ative "Password Protection"
4. Configure a senha

## 📞 Suporte

### Mintlify Support

- [Documentação Mintlify](https://mintlify.com/docs)
- [Discord Community](https://discord.gg/mintlify)
- [Email Support](mailto:support@mintlify.com)

### Zynx Wallet Support

- Email: [suporte@zynxwallet.com.br](mailto:suporte@zynxwallet.com.br)
- Telegram: [@zynxwallet_support](https://t.me/zynxwallet_support)

## 📄 Licença

Esta documentação é propriedade da Zynx Wallet.

## 🎯 Próximos Passos

1. ✅ Estrutura de documentação criada
2. ✅ Páginas de conteúdo criadas
3. ✅ mint.json configurado
4. ⏭️ Implantar no Mintlify
5. ⏭️ Configurar domínio customizado
6. ⏭️ Adicionar analytics
7. ⏭️ Manter documentação atualizada

## 📝 Checklist de Implantação

- [ ] Repositório GitHub criado
- [ ] Código enviado para GitHub
- [ ] Conta Mintlify criada
- [ ] Projeto conectado ao Mintlify
- [ ] Documentação implantada
- [ ] Domínio customizado configurado
- [ ] Analytics configurado
- [ ] Links testados
- [ ] SEO verificado
- [ ] Documentação publicada

---

**Última atualização**: 10 de Fevereiro de 2024
**Versão**: 1.0.0
