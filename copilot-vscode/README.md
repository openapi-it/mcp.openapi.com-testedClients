# GitHub Copilot VS Code
This documentation contains examples and quick tips for configuring the mcp.openapi.com server
within GitHub Copilot VS Code.

## 📋 Prerequisites

- **Visual Studio Code** (recent version)
- **GitHub Copilot Chat** (extension installed and active)
- **OpenAPI Token** (obtainable from [openapi.com](https://openapi.com))

## 🚀 Quick Start

For a quick test, you can run VS Code from this directory (copilot-vscode):

**Windows:**
```cmd
> code .
```

**macOS/Linux:**
```bash
$ code .
```
---

## ⚙️ "Permanent" Installation

### 1. Locate the Configuration Directory

Navigate to the Copilot Chat configuration folder:

**Windows:**
```cmd
%USERPROFILE%\.vscode\copilot-chat
```

**macOS/Linux:**
```bash
~/.vscode/copilot-chat
```

> 💡 If the `copilot-chat` folder doesn't exist, create it manually

### 2. Create the Configuration File

Create the `mcp.json` file in the identified folder:

````json
{
  "inputs": [{
    "type": "promptString",
    "id": "OpenapiToken",
    "description": "Insert a valid Openapi.com Token",
    "password": true
  }],
  "servers": {
    "openapi.com": {
      "type": "http",
      "url": "https://mcp.openapi.com/",
      "headers": {
        "Authorization": "Bearer ${input:OpenapiToken}"
      }
    }
  }
}
````

### 3. Restart VS Code

**This step is essential**. Completely close Visual Studio Code and reopen it. This way, the Copilot Chat extension will load your new configuration file.

---

## How to Use It

Once VS Code is restarted, the configuration will be active.

1.  Open the GitHub Copilot chat (usually with `Ctrl+Alt+I` or `Cmd+Option+I`).
2.  In the chat, type `@` and you should see the new `@openapi.com` service among the available options.
3.  Select it and write your request. For example: `@openapi.com get my user details`.
4.  On the first request, VS Code will show an input field at the top, asking you to enter the token (`Insert a valid Openapi.com Token`). Thanks to `"password": true`, the input will be masked while you type.
5.  Enter the token and press Enter. Copilot will use this token to authenticate its request to the `https://mcp.openapi.com/` service and show you the result. ✨