# 🔐 Local Configuration (Your Computer Only)

This `local/` folder is **NOT committed to GitHub** and stays on your computer only.

## 📁 Structure

```
local/
├── config/              # Your personal .env files
│   └── .env.local       # Your API keys, secrets
├── personal/            # Your personal data & configs
│   └── .env.example     # Template for personal settings
└── storage/
    └── logs/            # Application logs (local only)
```

---

## 🔑 **Setup Instructions**

### 1. Create Your .env.local

Copy template and add your secrets:

```bash
# Create your local config
cp .env.local local/config/.env.local

# Edit with your API keys
nano local/config/.env.local
```

### 2. Add Your API Key

In `local/config/.env.local`:

```env
ANTHROPIC_API_KEY=sk-ant-xxxxxxxxxx
```

### 3. Personal Settings

```env
USER_NAME=Your Name
USER_EMAIL=your@email.com
WORKSPACE_NAME=My Workspace
```

---

## ✅ Security Checklist

- ✅ `.env.local` is in `.gitignore`
- ✅ `local/` folder is in `.gitignore`
- ✅ Never commit API keys
- ✅ Keep secrets local only
- ✅ Don't sync to cloud (OneDrive, Dropbox, etc.)

---

## 🌐 Global vs Local

| Item | Global (GitHub) | Local (Computer Only) |
|------|-----------------|----------------------|
| Code & scripts | ✅ Commit | ❌ Keep local |
| Documentation | ✅ Commit | ❌ Keep local |
| API keys | ❌ Never | ✅ `.env.local` |
| Secrets | ❌ Never | ✅ `.env.local` |
| Personal configs | ❌ Never | ✅ `local/config/` |
| Logs | ❌ Never | ✅ `local/storage/logs/` |

---

## 🚀 Next Steps

1. ✅ Create `.env.local` with your API key
2. ✅ Run MCP server: `cd mcp/servers/spacerouter && npm install && npm start`
3. ✅ Use with Claude Desktop

Your secrets stay safe on your computer! 🔐
