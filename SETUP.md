# 🔧 Configuração do Frontend - Sistema Anti-Bullying

## ❌ Erros Atuais

Você está vendo erros de 404 porque:

```
api/apps/null/entities/User/me - Failed to load resource: 404
api/apps/null/integration-endpoints/Core/UploadFile - Failed to load resource: 404
```

O `appId` está **null** porque faltam as credenciais da Base44.

---

## ✅ Como Resolver

### 1. Obtenha as Credenciais da Base44

1. Acesse **https://app.base44.com**
2. Faça login ou crie uma conta
3. Crie um novo projeto (se não tiver)
4. Vá para **Settings** ou **API Keys**
5. Copie:
   - **App ID**
   - **Functions Version**
   - **App Base URL** (geralmente algo como `https://api.base44.com` ou similar)

### 2. Configure o `.env.local`

Edite o arquivo `.env.local` nesta pasta:

```env
VITE_BASE44_APP_ID=seu_app_id_aqui
VITE_BASE44_FUNCTIONS_VERSION=seu_version_aqui
VITE_BASE44_APP_BASE_URL=sua_url_aqui
```

### 3. Reinicie o Servidor

```bash
npm run dev
```

O servidor recarregará automaticamente e os erros 404 desaparecerão.

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
