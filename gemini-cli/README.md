# Gemini CLI

## Installation via npm

Gemini CLI is available as an npm package. Follow these steps to install it on different operating systems:

### Linux/macOS
1. Ensure that Node.js and npm are installed on your system. You can check by running:
   ```bash
   node -v
   npm -v
   ```
   If not installed, download and install Node.js from the official website: [https://nodejs.org/](https://nodejs.org/).

2. Install Gemini CLI globally using npm:
   ```bash
   npm install -g gemini-cli
   ```

3. Verify the installation by running:
   ```bash
   gemini --version
   ```

### Windows
1. Download and install Node.js from the official website: [https://nodejs.org/](https://nodejs.org/).

2. Open a terminal (e.g., PowerShell or Command Prompt) and check that Node.js and npm are installed:
   ```bash
   node -v
   npm -v
   ```

3. Install Gemini CLI globally using npm:
   ```bash
   npm install -g gemini-cli
   ```

4. Verify the installation by running:
   ```bash
   gemini --version
   ```

## Configuration

1. Copy the example `settings.json` file to the `.gemini` directory in your home directory:
   - Linux/macOS: `~/.gemini/settings.json`
   - Windows: `%USERPROFILE%\.gemini\settings.json`

2. Edit the `settings.json` file and replace `{OPENAPI_TOKEN}` with a valid token generated via [openapi.com](https://openapi.com):
   ```json
   {
     "mcpServers": {
       "OpenapiMcpServer": {
         "httpUrl": "https://mcp.openapi.com",
         "headers": {
           "Authorization": "Bearer YOUR_TOKEN"
         }
       }
     }
   }
   ```

3. Save the file and verify that Gemini CLI is correctly configured by running:
   ```bash
   gemini --help
   ```

## Quick Test

If you want to perform a quick test, you can directly modify the example `settings.json` file located in the `.gemini` directory of this repository. There is no need to copy it to your home directory. Make sure to replace `{OPENAPI_TOKEN}` with a valid token generated via [openapi.com](https://openapi.com):

```json
{
  "mcpServers": {
    "OpenapiMcpServer": {
      "httpUrl": "https://mcp.openapi.com",
      "headers": {
        "Authorization": "Bearer YOUR_TOKEN"
      }
    }
  }
}
```

After modifying the file, you can run the `gemini` command directly from this directory to verify that the MCP of openapi.com is enabled.

## Usage Example

### List available commands
Run the following command to start Gemini CLI and view the list of available commands:

```bash
gemini --help
```

### Start in CLI mode and authenticate
To start the client in CLI mode, simply run the command:
```bash
gemini
```
The client will start, and the first time you will be prompted to authenticate:
```bash

 ███            █████████  ██████████ ██████   ██████ █████ ██████   █████ █████
░░░███         ███░░░░░███░░███░░░░░█░░██████ ██████ ░░███ ░░██████ ░░███ ░░███
  ░░░███      ███     ░░░  ░███  █ ░  ░███░█████░███  ░███  ░███░███ ░███  ░███
    ░░░███   ░███          ░██████    ░███░░███ ░███  ░███  ░███░░███░███  ░███
     ███░    ░███    █████ ░███░░█    ░███ ░░░  ░███  ░███  ░███ ░░██████  ░███
   ███░      ░░███  ░░███  ░███ ░   █ ░███      ░███  ░███  ░███  ░░█████  ░███
 ███░         ░░█████████  ██████████ █████     █████ █████ █████  ░░█████ █████
░░░            ░░░░░░░░░  ░░░░░░░░░░ ░░░░░     ░░░░░ ░░░░░ ░░░░░    ░░░░░ ░░░░░

Tips for getting started:
1. Ask questions, edit files, or run commands.
2. Be specific for the best results.
3. /help for more information.
╭─────────────────────────────────────────────────────────────────────────────────────────╮
│                                                                                         │
│ Get started                                                                             │
│                                                                                         │
│ How would you like to authenticate for this project?                                    │
│                                                                                         │
│ ● 1. Login with Google                                                                  │
│   2. Use Gemini API Key                                                                 │
│   3. Vertex AI                                                                          │
│                                                                                         │
│ Authentication timed out. Please try again.                                             │
│                                                                                         │
│ (Use Enter to select)                                                                   │
│                                                                                         │
│ Terms of Services and Privacy Notice for Gemini CLI                                     │
│                                                                                         │
│ https://github.com/google-gemini/gemini-cli/blob/main/docs/tos-privacy.md               │
│                                                                                         │
╰─────────────────────────────────────────────────────────────────────────────────────────╯
~/Openapi/McpGeminiCli     no sandbox (see /docs)        gemini-2.5-pro (100% context left)
```
Refer to the documentation for authentication methods.

Once authentication is complete, it will not be required again.

Now we are ready:
```bash

 ███            █████████  ██████████ ██████   ██████ █████ ██████   █████ █████
░░░███         ███░░░░░███░░███░░░░░█░░██████ ██████ ░░███ ░░██████ ░░███ ░░███
  ░░░███      ███     ░░░  ░███  █ ░  ░███░█████░███  ░███  ░███░███ ░███  ░███
    ░░░███   ░███          ░██████    ░███░░███ ░███  ░███  ░███░░███░███  ░███
     ███░    ░███    █████ ░███░░█    ░███ ░░░  ░███  ░███  ░███ ░░██████  ░███
   ███░      ░░███  ░░███  ░███ ░   █ ░███      ░███  ░███  ░███  ░░█████  ░███
 ███░         ░░█████████  ██████████ █████     █████ █████ █████  ░░█████ █████
░░░            ░░░░░░░░░  ░░░░░░░░░░ ░░░░░     ░░░░░ ░░░░░ ░░░░░    ░░░░░ ░░░░░
```

### Verify connection to mcp.openapi.com
Notice the notification "1 MCP server (ctrl+t to view)" in the client's welcome screen.
Pressing the suggested combination will execute the command:
```bash
/mcp desc 
```
which will display the context provided by the MCP server, and pressing it again will show the list of available tools on the MCP server, i.e., the output of the command:
```bash
/mcp nodesc

  🟢 OpenapiMcpServer - Ready (29 tools)
    Tools:
    - check_email_advanced
    - check_email_start
    - check_ip_advanced
    - check_IT_fiscal_code
    - check_license_plate
    - check_mobile_advanced
    - check_mobile_start
    - check_url_advanced
    - find_IT_istat_by_comune_name
    - find_IT_municipalities_by_zip
    - find_IT_municipality_by_istat
    - geocode
    - get_company_IT_advanced
    - get_company_IT_full
    - get_company_IT_legal_forms_list
    - get_company_IT_search
    - get_company_IT_start
    - get_company_WW_top
    - get_IT_metropolitan_cities_list
    - get_IT_provinces_list
    - get_IT_regions_list
    - get_italian_company_official_document
    - get_italian_company_official_documents_list
    - get_risk_IT_creditscore_top
    - get_suppressed_italian_municipalities
    - get_today_exchange_rates
    - post_risk_WW_kyc_full
    - reverse_geocode
    - send_sms
```
### Try the service
If the token provided is valid, you can start "talking" naturally with the integrated services of openapi.com through the selected language model. In this demonstration, gemini-2.5-pro is selected; refer to the client's documentation for more details on available models, their costs, and availability.
Let's ask the model a simple question:
```bash
╭──────────────────────────────────────────────────────────╮
│  > I have 12 euros in my pocket, how much are they worth in dollars today?  │
╰──────────────────────────────────────────────────────────╯
```
Shortly after, the model will select the correct service to answer the question accurately, avoiding hallucinations.
```bash
 ╭─────────────────────────────────────────────────────────────────────────────────────────╮
 │ ?  get_today_exchange_rates (OpenapiMcpServer MCP Server) get_today_exchange_rates … ←  │
 │                                                                                         │
 │   MCP Server: OpenapiMcpServer                                                          │
 │   Tool: get_today_exchange_rates                                                        │
 │                                                                                         │
 │ Allow execution of MCP tool "get_today_exchange_rates" from server "Openap…             │
 │                                                                                         │
 │ ● 1. Yes, allow once                                                                    │
 │   2. Yes, always allow tool "get_today_exchange_rates" from server "Openap…             │
 │   3. Yes, always allow all tools from server "OpenapiMcpServer"                         │
 │   4. No, suggest changes (esc)                                                          │
 │                                                                                         │
╰─────────────────────────────────────────────────────────────────────────────────────────╯
⠏ Waiting for user confirmation...
```
Authorization is requested to execute the specific MCP tool call to mcp.openapi.com (in this case, "get_today_exchange_rates"), which can be one-time or permanent.
```bash

 ╭────────────────────────────────────────────────────────────────────────────────────────────╮
 │ ✔ get_today_exchange_rates (OpenapiMcpServer MCP Server) get_today_exchange_rates (Open…  │
 │                                                                                            │
 │    {"AED":4.2876,"AFN":79.895,"ALL":97.6738,"AMD":447.1099,"ANG":2.0895,"AOA":1            │
 │    070.58,"ARS":1557.4466,"AUD":1.7884,"AWG":2.1044,"AZN":1.9893,"BAM":1.9574,"            │
 │    BBD":2.353,"BDT":142.0463,"BGN":1.9551,"BHD":0.4401,"BIF":3484.6563,"BMD":1.            │
 │    1675,"BND":1.4992,"BOB":8.0724,"BRL":6.3205,"BSD":1.1683,"BTC":0,"BTN":102.2            │
 │    776,"BWP":15.6977,"BYN":3.971,"BYR":22882.6273,"BZD":2.3496,"CAD":1.6055,"CD            │
 │    F":3350.6701,"CHF":0.9363,"CLF":0.0288,"CLP":1130.4954,"CNY":8.3521,"CNH":8.            │
 │    3127,"COP":4700.9206,"CRC":589.7536,"CUC":1.1675,"CUP":30.9382,"CVE":110.355            │
 │    4,"CZK":24.5288,"DJF":207.4851,"DKK":7.4644,"DOP":73.5102,"DZD":151.4486,"EG            │
 │    P":56.6193,"ERN":17.5122,"ETB":167.4468,"EUR":1,"FJD":2.6355,"FKP":0.867,"GB            │
 │    P":0.8642,"GEL":3.1464,"GGP":0.867,"GHS":13.3763,"GIP":0.867,"GMD":83.4715,"            │
 │    GNF":10127.2927,"GTQ":8.9546,"GYD":244.4184,"HKD":9.1002,"HNL":30.577,"HRK":            │
 │    7.5343,"HTG":152.8452,"HUF":396.6633,"IDR":19092.9256,"ILS":3.8821,"IMP":0.8            │
 │    67,"INR":102.2618,"IQD":1530.3466,"IRR":49107.1626,"ISK":143.0047,"JEP":0.86            │
 │    7,"JMD":186.3266,"JOD":0.8278,"JPY":171.6559,"KES":151.1535,"KGS":101.9868,"            │
 │    KHR":4682.3154,"KMF":494.4253,"KPW":1050.7094,"KRW":1617.4394,"KWD":0.3568,"            │
 │    KYD":0.9735,"KZT":628.0896,"LAK":25349.3627,"LBP":104614.716,"LKR":353.2516,            │
 │    "LRD":234.2299,"LSL":20.638,"LTL":3.4473,"LVL":0.7062,"LYD":6.3402,"MAD":10.            │
 │    532,"MDL":19.4692,"MGA":5137.7791,"MKD":61.5108,"MMK":2451.3256,"MNT":4199.0            │
 │    784,"MOP":9.3795,"MRU":46.6372,"MUR":53.7158,"MVR":17.963,"MWK":2025.693,"MX            │
 │    N":21.7903,"MYR":4.9233,"MZN":74.6027,"NAD":20.638,"NGN":1795.2117,"NIO":42.            │
 │    9852,"NOK":11.7611,"NPR":163.6446,"NZD":1.9853,"OMR":0.4489,"PAB":1.1683,"PE            │
 │    N":4.1479,"PGK":4.9432,"PHP":66.4151,"PKR":331.2564,"PLN":4.2622,"PYG":8442.            │
 │    9134,"QAR":4.2698,"RON":5.072,"RSD":117.1742,"RUB":93.9839,"RWF":1691.588,"S            │
 │    AR":4.3808,"SBD":9.5854,"SCR":16.5769,"SDG":701.0735,"SEK":11.0666,"SGD":1.4            │
 │    979,"SHP":0.9175,"SLE":27.1905,"SLL":24481.4901,"SOS":667.6411,"SRD":44.9673            │
 │    ,"STD":24164.4992,"STN":24.523,"SVC":10.2214,"SYP":15179.0869,"SZL":20.6368,            │
 │    "THB":37.6866,"TJS":11.0049,"TMT":4.0979,"TND":3.4175,"TOP":2.7344,"TRY":48.            │
 │    0389,"TTD":7.9294,"TWD":35.6133,"TZS":2923.9935,"UAH":48.1546,"UGX":4150.878            │
 │    9,"USD":1.1675,"UYU":46.7493,"UZS":14500.1839,"VES":168.3423,"VND":30792.311            │
 │    ,"VUV":140.0008,"WST":3.1249,"XAF":656.5621,"XAG":0.0299,"XAU":0.0003,"XCD":            │
 │    3.1552,"XCG":2.1055,"XDR":0.8185,"XOF":656.4946,"XPF":119.3317,"YER":280.37,            │
 │    "ZAR":20.6709,"ZMK":10508.7184,"ZMW":27.3652,"ZWL":375.9284,"success":true,"            │
 │    message":"","error":null}                                                               │
 ╰────────────────────────────────────────────────────────────────────────────────────────────╯
✦ Today, 12 euros are worth 14.01 dollars. The exchange rate is 1 EUR = 1.1675 USD.

```
### Something more complex
```bash
╭───────────────────────────────────────────────────────────────────────────────────╮
│  > How many corporations have a turnover above 10 million in the province of Terni?  │
╰───────────────────────────────────────────────────────────────────────────────────╯

 ╭────────────────────────────────────────────────────────────────────────────────────────────╮
 │ ✔ get_company_IT_search (OpenapiMcpServer MCP Server) get_company_IT_search (OpenapiMcp…  │
 │                                                                                            │
 │    {"data":[],"count":27,"cost":0.027,"success":true,"message":"","error":null}            │
 ╰────────────────────────────────────────────────────────────────────────────────────────────╯
✦ With the province set to "TR", there are 27 corporations with a turnover above 10 million.

╭───────────────────────────────────────────────────────╮
│  > Generate an HTML report for OpenAPI S.p.A.  │
╰───────────────────────────────────────────────────────╯

 ╭────────────────────────────────────────────────────────────────────────────────────────────╮
 │ ✔ get_company_IT_search (OpenapiMcpServer MCP Server) get_company_IT_search (OpenapiMcp…  │
 │                                                                                            │
 │    [{"taxCode":"12485671007","vatCode":"12485671007","companyName":"OPENAPI                │
 │    S.P.A.","address":{"registeredOffice":{"town":"ROMA"}},"creationTimestamp":1            │
 │    624358855,"lastUpdateTimestamp":1755789554,"id":"60d1bfc731177b0a092cdfc1"}]            │
 ╰────────────────────────────────────────────────────────────────────────────────────────────╯
 ╭────────────────────────────────────────────────────────────────────────────────────────────╮
 │ ✔ get_company_IT_advanced (OpenapiMcpServer MCP Server) get_company_IT_advanced (Openap…  │
 │                                                                                            │
 │    [{"taxCode":"12485671007","vatCode":"12485671007","companyName":"OPENAPI                │
 │    S.P.A.","address":{"registeredOffice":{"toponym":"VIALE","street":"FILIPPO              │
 │    TOMMASO MARINETTI","streetNumber":"221","streetName":"VIALE FILIPPO TOMMASO             │
 │    MARINETTI                                                                               │
 │    221","town":"ROMA","hamlet":null,"province":"RM","zipCode":"00143","region":            │
 │    {"code":"12","description":"LAZIO"},"townCode":"H501","gps":null}},"activity            │
 │    Status":"ATTIVA","reaCode":"1378273","cciaa":"RM","atecoClassification":{"at            │
 │    eco":{"code":"621","description":"Attivita' di programmazione                           │
 │    informatica"},"ateco2007":{"code":"6201","description":"Produzione di                   │
 │    software non connesso                                                                   │
 │    all'edizione"},"ateco2022":{"code":"6201","description":"Produzione di                  │
 │    software non connesso                                                                   │
 │    all'edizione"}},"detailedLegalForm":{"code":"SP","description":"SOCIETA' PER            │
 │    AZIONI"},"startDate":"2013-10-20","registrationDate":"2013-07-19","endDate":            │
 │    null,"pec":"openapi@legalmail.it","taxCodeCeased":false,"taxCodeCeasedTimest            │
 │    amp":1752166005,"vatGroup":{"vatGroupParticipation":false,"isVatGroupLeader"            │
 │    :false,"registryOk":true},"sdiCode":"USAL8PV","sdiCodeTimestamp":1756386216,            │
 │    "creationTimestamp":1624358855,"lastUpdateTimestamp":1755789554,"balanceShee            │
 │    ts":{"last":{"year":2024,"employees":15,"balanceSheetDate":"2024-12-31","tur            │
 │    nover":3671995,"netWorth":338315,"shareCapital":50000,"totalStaffCost":61742            │
 │    8,"totalAssets":1118403,"avgGrossSalary":41161},"all":[{"year":2025,"balance            │
 │    SheetDate":null,"turnover":null,"netWorth":null,"employees":15,"shareCapital            │
 │    ":50000,"totalStaffCost":null,"totalAssets":null},{"year":2024,"employees":1            │
 │    5,"balanceSheetDate":"2024-12-31","turnover":3671995,"netWorth":338315,"shar            │
 │    eCapital":50000,"totalStaffCost":617428,"totalAssets":1118403,"avgGrossSalar            │
 │    y":41161},{"year":2023,"employees":15,"balanceSheetDate":"2023-12-31","turno            │
 │    ver":3438271,"netWorth":-4710,"shareCapital":50000,"totalStaffCost":565291,"            │
 │    totalAssets":1286998,"avgGrossSalary":37686},{"year":2022,"employees":14,"ba            │
 │    lanceSheetDate":"2022-12-31","turnover":4043407,"netWorth":166491,"shareCapi            │
 │    tal":50000,"totalStaffCost":604997,"totalAssets":1483126,"avgGrossSalary":43            │
 │    214},{"year":2021,"employees":15,"balanceSheetDate":"2021-12-31","turnover":            │
 │    4432761,"netWorth":469366,"shareCapital":50000},{"year":2020,"employees":14,            │
 │    "balanceSheetDate":"2020-12-31","turnover":4192138,"netWorth":170234,"shareC            │
 │    apital":10000},{"year":2019,"employees":14,"balanceSheetDate":"2019-12-31","            │
 │    turnover":1799587,"netWorth":111309,"shareCapital":10000},{"year":2018,"empl            │
 │    oyees":null,"balanceSheetDate":"2018-12-31","turnover":1325358,"netWorth":82            │
 │    6,"shareCapital":null},{"year":2017,"employees":null,"balanceSheetDate":"201            │
 │    7-12-31","turnover":1120176,"netWorth":2928,"shareCapital":null}]},"shareHol            │
 │    ders":[{"companyName":"OPEN HOLDING                                                     │
 │    S.R.L.","name":null,"surname":null,"taxCode":"16935371001","percentShare":10            │
 │    0}],"id":"60d1bfc731177b0a092cdfc1"}]                                                   │
 ╰────────────────────────────────────────────────────────────────────────────────────────────╯
 ╭────────────────────────────────────────────────────────────────────────────────────────────╮
 │ ✔ WriteFile Writing to openapi_report.html                                      │
 │                                                                                  │
 │    ... first 105 lines hidden ...                                                │
 │     44 +   <tr><th>Description</th><td>Produzione di software non connesso       │
 │        all'edizione</td></tr>                                                    │
 │     45 + </table>                                                                │
 │     46                                                                           │
 │    ════════════════════════════════════════════════════════════════════════════  │
 │     57 -         <div class="section">                                           │
 │     58 -             <h2>Struttura Societaria</h2>                               │
 │     59 -             <ul>                                                        │
 │     60 -                 <li>L'azienda è controllata al 100% da <strong>OPEN     │
 │        HOLDING S.R.L.</strong> (C.F. 16935371001).</li>                          │
 │     61 -             </ul>                                                       │
 │     62 -         </div>                                                          │
 │     47 + <h2>Financials</h2>                                                     │
 │     48 + <h3>Balance Sheet</h3>                                                  │
 │     49 + <table>                                                                 │
 │     50 +   <tr>                                                                  │
 │     51 +     <th>Year</th>                                                       │
 │     52 +     <th>Employees</th>                                                  │
 │     53 +     <th>Turnover</th>                                                   │
 │     54 +     <th>Net Worth</th>                                                  │
 │     55 +     <th>Share Capital</th>                                              │
 │     56 +     <th>Total Staff Cost</th>                                           │
 │     57 +     <th>Total Assets</th>                                               │
 │     58 +     <th>Avg Gross Salary</th>                                           │
 │     59 +   </tr>                                                                 │
 │     60 +   <tr>                                                                  │
 │     61 +     <td>2024</td>                                                       │
 │     62 +     <td>15</td>                                                         │
 │     63 +     <td>3671995</td>                                                    │
 │     64 +     <td>338315</td>                                                     │
 │     65 +     <td>50000</td>                                                      │
 │     66 +     <td>617428</td>                                                     │
 │     67 +     <td>1118403</td>                                                    │
 │     68 +     <td>41161</td>                                                      │
 │     69 +   </tr>                                                                 │
 │     70 +   <tr>                                                                  │
 │     71 +     <td>2023</td>                                                       │
 │     72 +     <td>15</td>                                                         │
 │     73 +     <td>3438271</td>                                                    │
 │     74 +     <td>-4710</td>                                                      │
 │     75 +     <td>50000</td>                                                      │
 │     76 +     <td>565291</td>                                                     │
 │     77 +     <td>1286998</td>                                                    │
 │     78 +     <td>37686</td>                                                      │
 │     79 +   </tr>                                                                 │
 │     80 +   <tr>                                                                  │
 │     81 +     <td>2022</td>                                                       │
 │     82 +     <td>14</td>                                                         │
 │     83 +     <td>4043407</td>                                                    │
 │     84 +     <td>166491</td>                                                     │
 │     85 +     <td>50000</td>                                                      │
 │     86 +     <td>604997</td>                                                     │
 │     87 +     <td>1483126</td>                                                    │
 │     88 +     <td>43214</td>                                                      │
 │     89 +   </tr>                                                                 │
 │     90 +     <tr>                                                                │
 │     91 +     <td>2021</td>                                                       │
 │     92 +     <td>15</td>                                                         │
 │     93 +     <td>4432761</td>                                                    │
 │     94 +     <td>469366</td>                                                     │
 │     95 +     <td>50000</td>                                                      │
 │     96 +     <td></td>                                                           │
 │     97 +     <td></td>                                                           │
 │     98 +     <td></td>                                                           │
 │     99 +   </tr>                                                                 │
 │    100 +     <tr>                                                                │
 │    101 +     <td>2020</td>                                                       │
 │    102 +     <td>14</td>                                                         │
 │    103 +     <td>4192138</td>                                                    │
 │    104 +     <td>170234</td>                                                     │
 │    105 +     <td>10000</td>                                                      │
 │    106 +     <td></td>                                                           │
 │    107 +     <td></td>                                                           │
 │    108 +     <td></td>                                                           │
 │    109 +   </tr>                                                                 │
 │    110 +     <tr>                                                                │
 │    111 +     <td>2019</td>                                                       │
 │    112 +     <td>14</td>                                                         │
 │    113 +     <td>1799587</td>                                                    │
 │    114 +     <td>111309</td>                                                     │
 │    115 +     <td>10000</td>                                                      │
 │    116 +     <td></td>                                                           │
 │    117 +     <td></td>                                                           │
 │    118 +     <td></td>                                                           │
 │    119 +   </tr>                                                                 │
 │    120 +     <tr>                                                                │
 │    121 +     <td>2018</td>                                                       │
 │    122 +     <td></td>                                                           │
 │    123 +     <td>1325358</td>                                                    │
 │    124 +     <td>826</td>                                                        │
 │    125 +     <td></td>                                                           │
 │    126 +     <td></td>                                                           │
 │    127 +     <td></td>                                                           │
 │    128 +     <td></td>                                                           │
 │    129 +   </tr>                                                                 │
 │    130 +     <tr>                                                                │
 │    131 +     <td>2017</td>                                                       │
 │    132 +     <td></td>                                                           │
 │    133 +     <td>1120176</td>                                                    │
 │    134 +     <td>2928</td>                                                       │
 │    135 +     <td></td>                                                           │
 │    136 +     <td></td>                                                           │
 │    137 +     <td></td>                                                           │
 │    138 +     <td></td>                                                           │
 │    139 +   </tr>                                                                 │
 │    140 + </table>                                                                │
 │    141                                                                           │
 │     64 -         <div class="section">                                           │
 │     65 -             <h2>Grafici Dati Storici</h2>                               │
 │     66 -             <div class="chart-container">                               │
 │     67 -                 <h3>Fatturato Annuale</h3>                              │
 │     68 -                 <canvas id="turnoverChart"></canvas>                    │
 │     69 -             </div>                                                      │
 │     70 -             <div class="chart-container">                               │
 │     71 -                 <h3>Numero Dipendenti</h3>                              │
 │     72 -                 <canvas id="employeesChart"></canvas>                   │
 │     73 -             </div>                                                      │
 │     74 -             <div class="chart-container">                               │
 │     75 -                 <h3>Patrimonio Netto</h3>                               │
 │     76 -                 <canvas id="netWorthChart"></canvas>                    │
 │     77 -             </div>                                                      │
 │     78 -         </div>                                                          │
 │    ════════════════════════════════════════════════════════════════════════════  │
 │    142 + <h2>Shareholders</h2>                                                   │
 │    143 + <table>                                                                 │
 │    144 +   <tr><th>Company Name</th><th>Tax Code</th><th>Share</th></tr>         │
 │    145 +   <tr><td>OPEN HOLDING S.R.L.</td><td>16935371001</td><td>100%</td></   │
 │        tr>                                                                       │
 │    146 + </table>                                                                │
 │    147                                                                           │
 │     81 -     <script>                                                            │
 │     82 -         const historicalData = [                                        │
 │     83 -                                                                         │
 │        {"year":2025,"balanceSheetDate":null,"turnover":null,"netWorth":null,"em  │
 │        ployees":15,"shareCapital":50000,"totalStaffCost":null,"totalAssets":nul  │
 │        l},                                                                       │
 │     84 -                                                                         │
 │        {"year":2024,"employees":15,"balanceSheetDate":"2024-12-31","turnover":3  │
 │        671995,"netWorth":338315,"shareCapital":50000,"totalStaffCost":617428,"t  │
 │        otalAssets":1118403,"avgGrossSalary":41161},                              │
 │     85 -                                                                         │
 │        {"year":2023,"employees":15,"balanceSheetDate":"2023-12-31","turnover":3  │
 │        438271,"netWorth":-4710,"shareCapital":50000,"totalStaffCost":565291,"to  │
 │        talAssets":1286998,"avgGrossSalary":37686},                               │
 │     86 -                                                                         │
 │        {"year":2022,"employees":14,"balanceSheetDate":"2022-12-31","turnover":4  │
 │        043407,"netWorth":166491,"shareCapital":50000,"totalStaffCost":604997,"t  │
 │        otalAssets":1483126,"avgGrossSalary":43214},                              │
 │     87 -                                                                         │
 │        {"year":2021,"employees":15,"balanceSheetDate":"2021-12-31","turnover":4  │
 │        432761,"netWorth":469366,"shareCapital":50000},                           │
 │     88 -                                                                         │
 │        {"year":2020,"employees":14,"balanceSheetDate":"2020-12-31","turnover":4  │
 │        192138,"netWorth":170234,"shareCapital":10000},                           │
 │     89 -                                                                         │
 │        {"year":2019,"employees":14,"balanceSheetDate":"2019-12-31","turnover":1  │
 │        799587,"netWorth":111309,"shareCapital":10000},                           │
 │     90 -                                                                         │
 │        {"year":2018,"employees":null,"balanceSheetDate":"2018-12-31","turnover"  │
 │        :1325358,"netWorth":826,"shareCapital":null},                             │
 │     91 -                                                                         │
 │        {"year":2017,"employees":null,"balanceSheetDate":"2017-12-31","turnover"  │
 │        :1120176,"netWorth":2928,"shareCapital":null}                             │
 │     92 -         ];                                                              │
 │     93 -                                                                         │
 │     94 -         // Filter out future years or entries with null data for        │
 │        charts and sort by year                                                   │
 │     95 -         const filteredData = historicalData.filter(d => d.year <= new   │
 │        Date().getFullYear() && d.turnover !== null && d.employees !== null &&    │
 │        d.netWorth !== null)                                                      │
 │     96 -                                            .sort((a, b) => a.year -     │
 │        b.year);                                                                  │
 │     97 -                                                                         │
 │     98 -         const years = filteredData.map(d => d.year);                    │
 │     99 -         const turnoverData = filteredData.map(d => d.turnover);         │
 │    100 -         const employeesData = filteredData.map(d => d.employees);       │
 │    101 -         const netWorthData = filteredData.map(d => d.netWorth);         │
 │    102 -                                                                         │
 │    103 -         // Chart for Turnover                                           │
 │    104 -         new Chart(document.getElementById('turnoverChart'), {           │
 │    105 -             type: 'line',                                               │
 │    106 -             data: {                                                     │
 │    107 -                 labels: years,                                          │
 │    108 -                 datasets: [{                                            │
 │    109 -                     label: 'Fatturato (€)',                             │
 │    110 -                     data: turnoverData,                                 │
 │    111 -                     borderColor: 'rgb(75, 192, 192)',                   │
 │    112 -                     tension: 0.1                                        │
 │    113 -                 }]                                                      │
 │    114 -             },                                                          │
 │    115 -             options: {                                                  │
 │    116 -                 responsive: true,                                       │
 │    117 -                 scales: {                                               │
 │    118 -                     y: {                                                │
 │    119 -                         beginAtZero: true                               │
 │    120 -                     }                                                   │
 │    121 -                 }                                                       │
 │    122 -             }                                                           │
 │    123 -         });                                                             │
 │    124 -                                                                         │
 │    125 -         // Chart for Employees                                          │
 │    126 -         new Chart(document.getElementById('employeesChart'), {          │
 │    127 -             type: 'bar',                                                │
 │    128 -             data: {                                                     │
 │    129 -                 labels: years,                                          │
 │    130 -                 datasets: [{                                            │
 │    131 -                     label: 'Numero Dipendenti',                         │
 │    132 -                     data: employeesData,                                │
 │    133 -                     backgroundColor: 'rgba(153, 102, 255, 0.6)',        │
 │    134 -                     borderColor: 'rgb(153, 102, 255)',                  │
 │    135 -                     borderWidth: 1                                      │
 │    136 -                 }]                                                      │
 │    137 -             },                                                          │
 │    138 -             options: {                                                  │
 │    139 -                 responsive: true,                                       │
 │    140 -                 scales: {                                               │
 │    141 -                     y: {                                                │
 │    142 -                         beginAtZero: true,                              │
 │    143 -                         stepSize: 1                                     │
 │    144 -                     }                                                   │
 │    145 -                 }                                                       │
 │    146 -             }                                                           │
 │    147 -         });                                                             │
 │    148 -                                                                         │
 │    149 -         // Chart for Net Worth                                          │
 │    150 -         new Chart(document.getElementById('netWorthChart'), {           │
 │    151 -             type: 'line',                                               │
 │    152 -             data: {                                                     │
 │    153 -                 labels: years,                                          │
 │    154 -                 datasets: [{                                            │
 │    155 -                     label: 'Patrimonio Netto (€)',                      │
 │    156 -                     data: netWorthData,                                 │
 │    157 -                     borderColor: 'rgb(255, 99, 132)',                   │
 │    158 -                     tension: 0.1                                        │
 │    159 -                 }]                                                      │
 │    160 -             },                                                          │
 │    161 -             options: {                                                  │
 │    162 -                 responsive: true,                                       │
 │    163 -                 scales: {                                               │
 │    164 -                     y: {                                                │
 │    165 -                         beginAtZero: false // Net worth can be          │
 │        negative                                                                  │
 │    166 -                     }                                                   │
 │    167 -                 }                                                       │
 │    168 -             }                                                           │
 │    169 -         });                                                             │
 │    170 -     </script>                                                           │
 │    148   </body>                                                                 │
 │    149   </html>                                                                 │
╰──────────────────────────────────────────────────────────────────────────────────╯
✦ I have generated the report in HTML format, you can find it here:
  ~/Openapi/McpGeminiCli/openapi_report.html
```