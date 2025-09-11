# GitHub Copilot VS Code
In questa documentazione sono raccolti degli esempi e dei rapidi consigli per configurare il server mcp.openapi.com
all'interno di GitHub Copilot VS Code.

## 📋 Prerequisiti

- **Visual Studio Code** (versione recente)
- **GitHub Copilot Chat** (estensione installata e attiva)
- **Token OpenAPI** (ottenibile da [openapi.com](https://openapi.com))

## 🚀 Quick Start

Per un rapido test possibile eseguire vscode da questa directory (copilot-vscode):

**Windows:**
```cmd
> code .
```


**macOS/Linux:**
```bash
$ code .
```
---

## ⚙️ Installazione "permanente"

### 1. Localizza la Directory di Configurazione

Naviga alla cartella di configurazione di Copilot Chat:

**Windows:**
```cmd
%USERPROFILE%\.vscode\copilot-chat
```

**macOS/Linux:**
```bash
~/.vscode/copilot-chat
```

> 💡 Se la cartella `copilot-chat` non esiste, creala manualmente

### 2. Crea il File di Configurazione

Crea il file `mcp.json` nella cartella identificata:

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

### 3. Riavvia VS Code

**Questo passaggio è fondamentale**. Chiudi completamente Visual Studio Code e riaprilo. In questo modo l'estensione di Copilot Chat caricherà il tuo nuovo file di configurazione.

---

## Come Utilizzarlo

Una volta riavviato VS Code, la configurazione sarà attiva.

1.  Apri la chat di GitHub Copilot (solitamente con `Ctrl+Alt+I` o `Cmd+Option+I`).
2.  Nella chat, digita `@` e dovresti vedere il nuovo servizio `@openapi.com` tra le opzioni disponibili.
3.  Selezionalo e scrivi la tua richiesta. Ad esempio: `@openapi.com get my user details`.
4.  Alla prima richiesta, VS Code mostrerà un campo di input in alto, chiedendoti di inserire il token (`Insert a valid Openapi.com Token`). Grazie a `"password": true`, l'input sarà mascherato mentre digiti.
5.  Inserisci il token e premi Invio. Copilot userà questo token per autenticare la sua richiesta al servizio `https://mcp.openapi.com/` e ti mostrerà il risultato. ✨