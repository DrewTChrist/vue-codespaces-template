# Vue Codespace Template

### Usage
* Create a repository from template
* Select this repository as the template
* Create a new codespace
* Select the previously created repository

### Defaults

Project Name: vue-project

Includes:
* vue-router 
* pinia 
* eslint 
* eslint-with-prettier 

### devcontainer.json

```json
{
	"name": "vue-project",
	"image": "mcr.microsoft.com/devcontainers/javascript-node:1-22-bookworm",
    "customizations": {
		"vscode": {
			"extensions": [
				"Vue.volar"
			]
		}
    },
    "forwardPorts": [5173],
	"postCreateCommand": "npm create vue@latest -y -- vue-project --vue-router --pinia --eslint --eslint-with-prettier && mv vue-project/{.,}* . && rm -r vue-project && npm install",
    "postAttachCommand": "npm run dev"
}
```
