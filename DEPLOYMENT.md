# Guia de Implantação - Zynx Wallet Documentação

## 🚀 Implantação Rápida

### Pré-requisitos

- Node.js 16+ instalado
- Git instalado
- Conta GitHub
- Conta Mintlify

### Passo 1: Preparar Repositório GitHub

```bash
# Clonar ou criar novo repositório
git init

# Adicionar todos os arquivos
git add .

# Commit inicial
git commit -m "Initial Zynx Wallet documentation"

# Criar repositório no GitHub
# https://github.com/new
# Nome: zynx-wallet-docs
# Descrição: Documentação da API Zynx Wallet

# Adicionar remote
git remote add origin https://github.com/seu-usuario/zynx-wallet-docs.git

# Push
git branch -M main
git push -u origin main
```

### Passo 2: Implantar no Mintlify

#### Opção A: Via Mintlify CLI (Mais Rápido)

```bash
# Instalar Mintlify CLI
npm install -g mintlify

# Fazer login
mintlify login

# Implantar
mintlify deploy

# Acessar: https://zynxwallet.mintlify.app
```

#### Opção B: Via Dashboard Mintlify (Recomendado para Produção)

1. Acesse https://dashboard.mintlify.app
2. Clique em "New Project"
3. Selecione seu repositório GitHub (zynx-wallet-docs)
4. Configure:
   - Root Directory: `/`
   - Branch: `main`
5. Clique em "Deploy"
6. Aguarde a implantação (2-5 minutos)

### Passo 3: Configurar Domínio Customizado (Opcional)

1. No Mintlify Dashboard, vá para "Settings"
2. Clique em "Custom Domain"
3. Insira: `docs.zynxwallet.com.br`
4. Siga as instruções para configurar DNS:
   ```
   CNAME: docs.zynxwallet.com.br -> zynxwallet.mintlify.app
   ```
5. Aguarde propagação DNS (até 24 horas)

## 📝 Atualizar Documentação

### Fazer Alterações

```bash
# Editar arquivos .mdx conforme necessário
# Exemplo: docs/guides/novo-guia.mdx

# Testar localmente (opcional)
mintlify dev
# Acesse http://localhost:3000
```

### Publicar Alterações

```bash
# Commit
git add .
git commit -m "Atualizar documentação: [descrição das mudanças]"

# Push
git push origin main

# Mintlify implanta automaticamente em alguns segundos
```

## 🔍 Validação

### Verificar Implantação

1. Acesse https://zynxwallet.mintlify.app (ou seu domínio)
2. Verifique:
   - [ ] Página inicial carrega
   - [ ] Navegação funciona
   - [ ] Links internos funcionam
   - [ ] Código está formatado corretamente
   - [ ] Imagens carregam (se houver)

### Testar Links

```bash
# Instalar linkchecker (opcional)
pip install linkchecker

# Verificar links
linkchecker https://zynxwallet.mintlify.app
```

## 🐛 Troubleshooting

### Problema: Documentação não aparece

**Solução:**
1. Verifique se o repositório é público
2. Verifique se mint.json está na raiz
3. Verifique se os arquivos .mdx existem
4. Tente fazer novo push

### Problema: Páginas não carregam

**Solução:**
1. Verifique se os caminhos em mint.json estão corretos
2. Verifique se os arquivos .mdx têm frontmatter válido
3. Verifique o console do navegador para erros

### Problema: Domínio customizado não funciona

**Solução:**
1. Verifique se o CNAME está configurado corretamente
2. Aguarde propagação DNS (até 24 horas)
3. Limpe cache do navegador (Ctrl+Shift+Delete)

## 📊 Monitoramento

### Acessar Estatísticas

1. Vá para Mintlify Dashboard
2. Clique em seu projeto
3. Vá para "Analytics"
4. Veja:
   - Visitantes
   - Páginas mais acessadas
   - Tempo de permanência
   - Origem do tráfego

## 🔐 Segurança

### Proteger com Senha (Opcional)

1. Vá para Mintlify Dashboard
2. Clique em "Settings"
3. Ative "Password Protection"
4. Configure a senha
5. Compartilhe a senha com usuários autorizados

## 🎯 Próximas Etapas

- [ ] Implantar no Mintlify
- [ ] Configurar domínio customizado
- [ ] Configurar analytics
- [ ] Adicionar SEO metadata
- [ ] Integrar com sistema de feedback
- [ ] Configurar notificações de erro
- [ ] Manter documentação atualizada

## 📞 Suporte

### Mintlify

- Documentação: https://mintlify.com/docs
- Discord: https://discord.gg/mintlify
- Email: support@mintlify.com

### Zynx Wallet

- Email: suporte@zynxwallet.com.br
- Telegram: @zynxwallet_support

---

**Última atualização**: 10 de Fevereiro de 2024
**Versão**: 1.0.0
