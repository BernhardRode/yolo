# 🐾 PetStore API Demo with Amazon Q CLI

Welcome to this awesome demo showcasing how to use Amazon Q CLI with the PetStore API! 🚀

## 🎯 What's This About?

This demo shows you how to integrate Amazon Q CLI with the [OpenAPI PetStore API](https://petstore3.swagger.io/) using MCP (Model Context Protocol) servers. You'll be able to chat with Amazon Q and have it interact directly with the PetStore API!

## 🛠️ Prerequisites

Before we start, make sure you have:
- ☁️ An AWS account (for Amazon Q CLI)
- 🐍 Python package manager `uv` installed
- 💻 A terminal/command line interface

## 📦 Installation Steps

### 1. Install Amazon Q CLI 🔧

Choose your preferred installation method:

**Option A: Official AWS Documentation (Recommended)**
```bash
# Follow the official guide
https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-installing.html
```

**Option B: GitHub Repository**
```bash
# Check out the GitHub repo for latest instructions
https://github.com/aws/amazon-q-developer-cli
```

### 2. Install UV Package Manager 📋

```bash
# Install uv using the standalone installer
curl -LsSf https://astral.sh/uv/install.sh | sh
```

For more installation options: https://docs.astral.sh/uv/getting-started/installation/#standalone-installer

### 3. Login to Amazon Q 🧠

```bash
q login
```

💡 **Note**: You'll need to create a Builder ID if you don't have one. The usage is largely free!

### 4. Checkout this Repo 🧳

```bash
git clone https://github.com/BernhardRode/yolo.git
```

### 4. YOLO Mode 🚀

Go into the `mcp-server-demo` folder.

```bash
q chat --trust-all-tools
```

The first thing it does is loading the MCP Server, then you should see somethhing like this:

```bash
 q chat --trust-all-tools
✓ awslabsopenapi_mcp_server loaded in 4.93 s


    ⢠⣶⣶⣦⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢀⣤⣶⣿⣿⣿⣶⣦⡀⠀
 ⠀⠀⠀⣾⡿⢻⣿⡆⠀⠀⠀⢀⣄⡄⢀⣠⣤⣤⡀⢀⣠⣤⣤⡀⠀⠀⢀⣠⣤⣤⣤⣄⠀⠀⢀⣤⣤⣤⣤⣤⣤⡀⠀⠀⣀⣤⣤⣤⣀⠀⠀⠀⢠⣤⡀⣀⣤⣤⣄⡀⠀⠀⠀⠀⠀⠀⢠⣿⣿⠋⠀⠀⠀⠙⣿⣿⡆
 ⠀⠀⣼⣿⠇⠀⣿⣿⡄⠀⠀⢸⣿⣿⠛⠉⠻⣿⣿⠛⠉⠛⣿⣿⠀⠀⠘⠛⠉⠉⠻⣿⣧⠀⠈⠛⠛⠛⣻⣿⡿⠀⢀⣾⣿⠛⠉⠻⣿⣷⡀⠀⢸⣿⡟⠛⠉⢻⣿⣷⠀⠀⠀⠀⠀⠀⣼⣿⡏⠀⠀⠀⠀⠀⢸⣿⣿
 ⠀⢰⣿⣿⣤⣤⣼⣿⣷⠀⠀⢸⣿⣿⠀⠀⠀⣿⣿⠀⠀⠀⣿⣿⠀⠀⢀⣴⣶⣶⣶⣿⣿⠀⠀⠀⣠⣾⡿⠋⠀⠀⢸⣿⣿⠀⠀⠀⣿⣿⡇⠀⢸⣿⡇⠀⠀⢸⣿⣿⠀⠀⠀⠀⠀⠀⢹⣿⣇⠀⠀⠀⠀⠀⢸⣿⡿
 ⢀⣿⣿⠋⠉⠉⠉⢻⣿⣇⠀⢸⣿⣿⠀⠀⠀⣿⣿⠀⠀⠀⣿⣿⠀⠀⣿⣿⡀⠀⣠⣿⣿⠀⢀⣴⣿⣋⣀⣀⣀⡀⠘⣿⣿⣄⣀⣠⣿⣿⠃⠀⢸⣿⡇⠀⠀⢸⣿⣿⠀⠀⠀⠀⠀⠀⠈⢿⣿⣦⣀⣀⣀⣴⣿⡿⠃
 ⠚⠛⠋⠀⠀⠀⠀⠘⠛⠛⠀⠘⠛⠛⠀⠀⠀⠛⠛⠀⠀⠀⠛⠛⠀⠀⠙⠻⠿⠟⠋⠛⠛⠀⠘⠛⠛⠛⠛⠛⠛⠃⠀⠈⠛⠿⠿⠿⠛⠁⠀⠀⠘⠛⠃⠀⠀⠘⠛⠛⠀⠀⠀⠀⠀⠀⠀⠀⠙⠛⠿⢿⣿⣿⣋⠀⠀
 ⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠈⠛⠿⢿⡧

╭─────────────────────────────── Did you know? ────────────────────────────────╮
│                                                                              │
│     You can resume the last conversation from your current directory by      │
│                        launching with q chat --resume                        │
│                                                                              │
╰──────────────────────────────────────────────────────────────────────────────╯

/help all commands  •  ctrl + j new lines  •  ctrl + s fuzzy search
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

All tools are now trusted (!). Amazon Q will execute tools without asking for confirmation.
Agents can sometimes do unexpected things so understand the risks.

Learn more at https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-chat-security.html#command-line-chat-trustall-safety

🤖 You are chatting with claude-4-sonnet
```

Enter:

```bash
YOLO!
```

You can see the one shot output of my try in the output folder ;)

## ⚙️ MCP Server Configuration

### 1. Create MCP Configuration File 📝

Create or edit the file at `~/.amazonq/mcp.json`:

Get all the details <https://awslabs.github.io/mcp/servers/openapi-mcp-server>.

```json
{
  "mcpServers": {
    "awslabs.openapi-mcp-server": {
      "command": "uvx",
      "args": ["awslabs.openapi-mcp-server@latest"],
      "env": {
        "API_NAME": "PetStore",
        "API_BASE_URL": "https://petstore3.swagger.io/api/v3",
        "API_SPEC_URL": "https://petstore3.swagger.io/api/v3/openapi.json"
      }
    }
  }
}
```

### 2. Understanding the Configuration 🧠

- **API_NAME**: Friendly name for your API
- **API_BASE_URL**: Base URL where the API is hosted
- **API_SPEC_URL**: URL to the OpenAPI specification

## 🚀 Usage

Once everything is set up, you can start Amazon Q CLI:

```bash
q chat
```

Now you can ask Amazon Q to interact with the PetStore API! Try commands like:

- 🐕 "Show me all available pets"
- 🔍 "Find pets by status 'available'"
- ➕ "Add a new pet to the store"
- 📊 "Get the store inventory"

## Getting Help:

- Type `/quit` to exit Amazon Q CLI
- Run `q --help` for usage instructions
- Check the logs for detailed error messages

## 🎊 Ready to Go!

You're all set! Start chatting with Amazon Q and explore the PetStore API. Have fun building amazing things! 🌟

## 🔗 Useful Links

- 📚 [MCP Server Documentation](https://awslabs.github.io/mcp/servers/openapi-mcp-server)
- 🛠️ [Amazon Q CLI MCP Configuration Guide](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-mcp-understanding-config.html)
- 🐾 [PetStore API Documentation](https://petstore3.swagger.io/)

## 🔄 Alternative CLI Tools

If you want to explore other AI CLI tools:

- 💻 [OpenCode AI](https://github.com/opencode-ai/opencode)
- 🤖 [Google Gemini CLI](https://github.com/google-gemini/gemini-cli)

---

*Happy coding! 🚀*
