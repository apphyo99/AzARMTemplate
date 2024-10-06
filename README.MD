<H1> ARM project includes: <H1>

AzureARMProject/
├── templates/
│   └── mainTemplate.json
├── parameters/
│   └── dev.parameters.json
├── README.md
└── .gitignore


Install Azure CLI:

Windows: Download the installer from the Azure CLI installation page.
macOS: Use Homebrew:

```brew install azure-cli```

Verify Installation: Open a terminal and run:

```az --version```
You should see the installed Azure CLI version.

Sign In to Azure:

```az login```
This command will open a browser window for authentication. Complete the sign-in process.

<H2> Validate and Test Your Templates </H2>
Before deploying, it's crucial to validate your templates to catch any syntax or configuration errors.


create a Resource Group (if you don't have one):
az group create --name MyResourceGroup --location eastus


<H3>1. Using Azure CLI </H3>
Open the integrated terminal in VS Code (Ctrl+`` or Cmd+`` on macOS) and navigate to your project directory.

Run the validation command:

```
az deployment group validate \
  --resource-group <YourResourceGroupName> \
  --template-file templates/mainTemplate.json \
  --parameters parameters/dev.parameters.json
```

Run the create command:
```
az deployment group create \
  --resource-group az-group-rg \
  --template-file mainTemplate.json \
  --parameters parameters.json
  ```
