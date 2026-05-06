# 📋 README - Sistema Anti-Bullying (Frontend)

## 🎯 O que é este projeto?

Sistema web para registrar e acompanhar denúncias de bullying em escolas, com:
- 📝 Formulário seguro de denúncias
- 🔍 Rastreamento de protocolo de denúncia
- 👨‍💼 Painel administrativo para gerenciar denúncias
- 📊 Estatísticas e relatórios
- 🔐 Autenticação segura

---

## 🚀 Início Rápido

### Requisitos
- Node.js 16+
- npm ou yarn
- Credenciais de Base44

### 1. Clone e Instale

```bash
git clone https://github.com/sistema-anti-bullying/frontend.git
cd frontend
npm install
```

### 2. Configure as Variáveis de Ambiente

**Copie o arquivo de exemplo:**
```bash
cp .env.example .env.local
```

**Edite `.env.local` com suas credenciais de Base44:**

```env
VITE_BASE44_APP_ID=seu_app_id_aqui
VITE_BASE44_FUNCTIONS_VERSION=1
VITE_BASE44_APP_BASE_URL=https://seu-url-base44.com
```

### 3. Inicie o Servidor

```bash
npm run dev
```

Acesse: **http://localhost:5173**

---

## 🔴 Resolvendo Erros de 404

### ❌ Erro: "Failed to load resource: 404"

**Causa:** Credenciais de Base44 não configuradas

**Solução:**

1. **Você precisa de credenciais Base44**
   - Se não tiver, crie em: https://app.base44.com
   - Se já tiver, entre com suas credenciais

2. **Copie as 3 informações:**
   - App ID
   - Functions Version  
   - App Base URL

3. **Cole em `.env.local`:**
   ```env
   VITE_BASE44_APP_ID=f7a3c2b1
   VITE_BASE44_FUNCTIONS_VERSION=1
   VITE_BASE44_APP_BASE_URL=https://base44.com
   ```

4. **Reinicie o servidor:**
   ```bash
   npm run dev
   ```

5. **Recarregue a página:** http://localhost:5173

---

## 📁 Estrutura do Projeto

```
frontend/
├── src/
│   ├── pages/           # Páginas principais
│   │   ├── Landing.jsx       # Página inicial
│   │   ├── ReportForm.jsx    # Formulário de denúncia
│   │   ├── TrackReport.jsx   # Rastreamento de denúncia
│   │   └── admin/            # Páginas administrativas
│   ├── components/      # Componentes React
│   ├── lib/             # Utilitários e contextos
│   └── main.jsx         # Entrada da aplicação
├── .env.local           # Variáveis de ambiente (criar)
├── .env.example         # Template de variáveis
└── SETUP.md             # Guia de configuração
```

---

## 🛠️ Comandos Disponíveis

```bash
npm run dev      # Desenvolvimento local (http://localhost:5173)
npm run build    # Build para produção
npm run preview  # Visualizar build de produção
npm run lint     # Verificar código
npm run lint:fix # Corrigir problemas de código
```

---

## 🔐 Variáveis de Ambiente

### Obrigatórias:
- `VITE_BASE44_APP_ID` - ID da aplicação Base44
- `VITE_BASE44_FUNCTIONS_VERSION` - Versão das funções
- `VITE_BASE44_APP_BASE_URL` - URL base da API

### Onde Encontrar:

1. Acesse **https://app.base44.com**
2. Faça login
3. Vá para **Projeto → Settings/Configurações**
4. Procure a seção "API Keys" ou "Developer"
5. Você verá:
   ```
   App ID: f7a3c2b1e9d4k5m0
   Functions Version: 1
   App Base URL: https://base44.com
   ```

---

## 🌐 URLs Importantes

| Recurso | URL |
|---------|-----|
| Frontend Local | http://localhost:5173 |
| Frontend Produção | https://antibullying123.netlify.app |
| Base44 Console | https://app.base44.com |
| GitHub Frontend | https://github.com/sistema-anti-bullying/frontend |
| GitHub Backend | https://github.com/sistema-anti-bullying/backend |

---

## 🆘 Problemas Comuns

### Erro: "Cannot find package '@base44/sdk'"
**Solução:** `npm install`

### Erro: "appId is null"
**Solução:** Configure `.env.local` com credenciais Base44

### Erro: "Port 5173 is already in use"
**Solução:** 
```bash
# Matar processo:
npx kill-port 5173
# Ou iniciar em outra porta:
npm run dev -- --port 3000
```

### Upload de arquivos não funciona
**Solução:** Verifique se `VITE_BASE44_APP_ID` está preenchido em `.env.local`

---

## 📞 Suporte

- Issues: https://github.com/sistema-anti-bullying/frontend/issues
- Base44 Docs: https://base44.com/docs
- Base44 Support: https://base44.com/support

---

## 📝 Arquivos Importantes

| Arquivo | Descrição |
|---------|-----------|
| `.env.local` | **COPIE ESTE ARQUIVO** - Suas credenciais pessoais |
| `.env.example` | Template - não edite, copie para `.env.local` |
| `SETUP.md` | Guia de configuração passo a passo |
| `vite.config.js` | Configuração do Vite |
| `package.json` | Dependências do projeto |

---

## ✅ Checklist de Setup

- [ ] Node.js instalado
- [ ] Repositório clonado
- [ ] `npm install` executado
- [ ] `.env.local` criado
- [ ] Credenciais Base44 preenchidas
- [ ] `npm run dev` em execução
- [ ] Acesso http://localhost:5173 funciona
- [ ] Sem erros 404 no console

Se tudo está ✅, você está pronto para desenvolver!
