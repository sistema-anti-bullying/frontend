# 🔧 Configuração do Frontend - Sistema Anti-Bullying

## ❌ Erros Atuais

Você está vendo erros de 404 porque:

```
api/apps/null/entities/User/me - Failed to load resource: 404
api/apps/null/integration-endpoints/Core/UploadFile - Failed to load resource: 404
Manifest fetch failed - code 404
```

O `appId` está **null** porque faltam as credenciais da Base44.

---

## ✅ Como Resolver - Guia Passo a Passo

### 📌 PASSO 1: Acessar Base44

1. Abra seu navegador
2. Acesse: **https://app.base44.com**
3. Faça login com suas credenciais (ou crie uma conta se não tiver)

### 📌 PASSO 2: Encontrar o Projeto

1. Na tela inicial, você verá uma lista de projetos
2. Selecione o projeto **"Sistema Anti-Bullying"** (ou crie um novo com esse nome)
3. Clique para entrar no projeto

### 📌 PASSO 3: Localizar as Credenciais

**Procure por:**
- Menu lateral esquerdo: procure por **"Settings"**, **"Configurações"** ou **"API"**
- OU no topo da página procure por um ícone de ⚙️ (engrenagem)

**Você deve encontrar uma seção com:**
- **App ID** (também pode chamar "Application ID" ou "Client ID")
- **Workspace ID** ou **Organization ID**
- **Functions Version** (número, ex: "1" ou "v1")
- **Base URL** ou **App Base URL** (exemplo: `https://app.base44.com` ou `https://api.base44.com`)

### 📌 PASSO 4: Copiar as Credenciais

1. Abra o arquivo `.env.local` em:
   ```
   c:\Users\jarde\OneDrive\Desktop\frontend-repo\.env.local
   ```

2. Substitua os valores vazios:
   ```env
   # Antes (errado):
   VITE_BASE44_APP_ID=
   VITE_BASE44_FUNCTIONS_VERSION=
   VITE_BASE44_APP_BASE_URL=http://localhost:5173

   # Depois (correto):
   VITE_BASE44_APP_ID=abc123xyz456
   VITE_BASE44_FUNCTIONS_VERSION=1
   VITE_BASE44_APP_BASE_URL=https://app.base44.com
   ```

3. **Exemplo Real:**
   ```env
   VITE_BASE44_APP_ID=f7a3c2b1e9d4k5m0
   VITE_BASE44_FUNCTIONS_VERSION=2
   VITE_BASE44_APP_BASE_URL=https://base44.com
   ```

### 📌 PASSO 5: Salvar e Reiniciar

1. Salve o arquivo `.env.local` (Ctrl+S)
2. Volte para o terminal onde está rodando `npm run dev`
3. Pressione **Ctrl+C** para parar o servidor
4. Digite novamente: `npm run dev`
5. Abra/recarregue a página: **http://localhost:5173**

### ✅ Pronto!

Se as credenciais estiverem corretas, os erros 404 desaparecerão e você verá:
- ✅ Login funcionando
- ✅ Upload de arquivos funcionando
- ✅ Dashboard carregando dados

---

## 📝 Estrutura do Projeto

- **Frontend**: React + Vite + Tailwind CSS
- **UI Components**: Shadcn/ui
- **Backend**: Express.js (repositório separado: `projeto-anti-bullying`)
- **Database**: Base44 (CMS/Backend-as-a-Service)

---

## 🚀 Scripts Disponíveis

```bash
npm run dev       # Inicia servidor de desenvolvimento
npm run build     # Cria build de produção
npm run preview   # Visualiza build de produção
npm run lint      # Verifica código
npm run lint:fix  # Corrige problemas de lint
npm run typecheck # Verifica tipos TypeScript
```

---

## 📍 Repositórios

- **Frontend**: https://github.com/sistema-anti-bullying/frontend
- **Backend**: https://github.com/sistema-anti-bullying/backend

---

## ⚠️ Nota Importante

Sem as credenciais corretas de Base44:
- ❌ Upload de arquivos não funcionará
- ❌ Autenticação não funcionará
- ❌ Banco de dados não será acessível
- ❌ Requisições à API retornarão 404

Configure as variáveis de ambiente corretamente para usar todas as funcionalidades do aplicativo.
