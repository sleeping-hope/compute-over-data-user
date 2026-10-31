# 🚀 Compute-Over-Data (CoD) - User Repository

**Your personal workspace for Compute-Over-Data system integration and customization**

[![GitHub](https://img.shields.io/badge/GitHub-sleeping--hope%2Fcompute--over--data--user-blue)](https://github.com/sleeping-hope/compute-over-data-user)
[![Status](https://img.shields.io/badge/Status-Ready-brightgreen)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

---

## 📋 Quick Overview

This is a **user-specific fork** of the main [Compute-Over-Data](https://github.com/sleeping-hope/Compute-Over-Data-CoD) system with:

- ✅ **Global code** (shared, version controlled) → committed to GitHub
- ✅ **Local secrets** (your API keys) → gitignored, stays on your computer only
- ✅ **Complete documentation** (2.7MB offline bundle)
- ✅ **MCP server** for Claude Desktop integration
- ✅ **nBlock AI Memory** system for autonomous learning

---

## 📁 Directory Structure

```
compute-over-data-user/
├── global/                         (Shared code)
│   └─ Symlink to shared resources
│
├── local/                          (Your secrets - gitignored)
│   ├── config/
│   │   └── .env.local             ← Add your API key here
│   ├── personal/
│   │   └── user-specific data
│   └── storage/logs/
│       └── application logs
│
├── .env.local                      (Secrets file - NEVER commit)
├── LOCAL.md                        (Setup guide)
├── STORAGE_SYSTEMS_INTEGRATION.md  (Architecture & metadata)
└── README.md                       (This file)
```

---

## 🚀 Getting Started

### 1. **Setup Local Environment**

```bash
# Clone this repo (already done!)
cd /home/user/compute-over-data-user

# Install MCP dependencies
cd mcp/servers/spacerouter
npm install
```

### 2. **Add Your API Key**

```bash
# Edit your local secrets (never pushed to GitHub)
nano .env.local
```

Add your Anthropic API key:
```env
ANTHROPIC_API_KEY=sk-ant-xxxxxxxxxxxxxxxx
```

### 3. **Configure Claude Desktop**

Create or update: `~/.claude/claude_desktop_config.json`

```json
{
  "mcpServers": {
    "spacerouter-privacy": {
      "command": "node",
      "args": ["$(pwd)/mcp/servers/spacerouter/index.js"],
      "env": {
        "SOCKS5_HOST": "127.0.0.1",
        "SOCKS5_PORT": "1080",
        "NODE_ENV": "production"
      }
    }
  }
}
```

### 4. **Run MCP Server**

```bash
cd mcp/servers/spacerouter
npm start
```

---

## 📚 Documentation

Start with one of these guides:

| Document | Purpose | Time |
|----------|---------|------|
| [LOCAL.md](./LOCAL.md) | Setup your local environment | 5 min |
| [STORAGE_SYSTEMS_INTEGRATION.md](./STORAGE_SYSTEMS_INTEGRATION.md) | Complete architecture & metadata | 10 min |
| [Agent SDK Quickstart](./storage/systems/nblock/data/AI_memory/ai_nblock_sdk/Agent_SDK_Quickstart.md) | Get started with Agent SDK | 15 min |
| [nBlock Index](./storage/systems/nblock/data/AI_memory/ai_nblock_sdk/NBLOCK_INDEX.md) | Complete knowledge base navigation | Reference |

---

## 🔐 Security

**Your secrets stay safe!**

```yaml
✅ Committed to GitHub:
   - Code & implementations
   - Documentation
   - Configuration templates
   - Installation scripts

❌ Never committed (gitignored):
   - .env.local (API keys)
   - local/ folder (personal data)
   - Logs & temporary files
```

See [.gitignore](./.gitignore) for complete protection rules.

---

## 🔗 Integration Points

### Claude Desktop
MCP server connects to Claude for autonomous tool execution.

### nBlock AI Memory
2.7MB offline documentation bundle with:
- Agent SDK complete API reference
- Installation & setup guides
- Quick start examples
- Loop mechanics documentation

### SOCKS5 Privacy Network
Optional privacy layer for SpaceRouter integration.

---

## 📊 What's Included

```
📦 Complete Package:
├── 🖥️  MCP Server (400+ lines)
├── 📚 Documentation (2.7MB)
├── ⚙️  Configuration system
├── 🔐 Security templates
├── 🚀 Installation automation
└── 💾 nBlock integration
```

---

## 🎯 Use Cases

- **Personal Development**: Customize agents for your workflow
- **Team Collaboration**: Share code via GitHub, keep secrets local
- **Production Deployment**: Secure configuration management
- **Learning**: Complete offline documentation for reference

---

## 🔄 Sync with Main Repository

Keep your fork updated:

```bash
# Fetch latest from main repo
git fetch upstream main

# Merge updates into your branch
git merge upstream/main

# Push your branch
git push origin main
```

---

## 📋 System Requirements

- **Node.js 18+** (for MCP server)
- **2GB disk space** (for documentation)
- **Claude Desktop** (optional, for full integration)
- **Windows/Linux/Mac** (supports all platforms)

---

## 🐛 Troubleshooting

### MCP Server Won't Start
```bash
# Check Node.js
node --version

# Install dependencies
npm install

# Check config file syntax
npm start
```

### API Key Issues
- Ensure `.env.local` is in `.gitignore`
- API key should be in `.env.local`, not `.env`
- Never commit API keys

### Claude Desktop Integration
- Verify `~/.claude/claude_desktop_config.json` syntax
- Restart Claude Desktop after config changes
- Check MCP server logs

---

## 📝 Contributing

This is your personal workspace! Feel free to:
- ✅ Create branches for experiments
- ✅ Customize agent implementations
- ✅ Push code improvements back to GitHub
- ✅ Keep secrets local only

---

## 🔗 Related Resources

- **Main Repository**: [sleeping-hope/Compute-Over-Data-CoD](https://github.com/sleeping-hope/Compute-Over-Data-CoD)
- **Claude Code Docs**: https://code.claude.com/docs
- **Agent SDK**: https://code.claude.com/docs/en/agent-sdk

---

## 📜 License

Same as main repository (MIT assumed)

---

## ✅ Status

- **Repository**: ✅ Ready for use
- **Documentation**: ✅ Complete (2.7MB)
- **MCP Server**: ✅ Implemented
- **Security**: ✅ Production-ready
- **Integration**: ✅ Claude Desktop compatible

---

**Last Updated**: 2026-10-31  
**Version**: 1.0  
**Owner**: sittiwatnueangwongsa  

**Ready to build with Compute-Over-Data!** 🚀