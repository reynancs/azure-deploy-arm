## :dart: Objetivo
Praticar a criação e implementação de uma Infraestrutura como Código (IaC) na Cloud Azure, usando o Modelo ARM (Azure Resource Manager) em formato .json.
Esta prática é voltada para automação no deploy de recursos em uma cloud, o objetivo final é praticar as principais ferramentas de DevOps na cloud Azure.

- Azure Cloud Provider
- IaC - ARM Model
- Azure CLI


## :pushpin: Descrição

Este exemplo foi realizado a partir da Trilha de Estudo para certificação: AZ-104: pré-requisitos para administradores do Azure, onde foi criado um arquivo em 
formato .json utilizano modelo ARM na cloud Azure, o qual foi criado um recurso do tipo Storage Account e parâmetros do tipo: resources, parameters e output.



## :computer: Como rodar a aplicação
1. Realizar git fork e git clone respectivamente deste arquivo .json para seu repositório local;
2. Instalar a extensão Azure Resource Manager no VS Code para alterar os nomes do Storage Account
4. `Az login` -> Selecione sua subscription da sua conta Azure
5. `az deployment group create --name myResourceGroup --template-file "azuredeploy.json" --parameters storageSKU=Standard_LRS storageName=mystorage06122022`
  - `--name myResourceGroup`: Altere para o nome do seu grupo de recursos;
  - `--template-file "azuredeploy.json"`: Nome do arquivo de modelo ARM;
  - `--parameters storageSKU=Standard_LRS` : Tipo de SKU passando como parâmetro no azure CLI 
  - `--parameters storageName=mystorage06122022` : Nome do seu Storage Account, necessário trocar por um outro que seja <unique-name>

## :triangular_flag_on_post: Pré-Requisitos
- VS Code v1.72.2
- cmdlet = Azure CLI
- Azure Resource Manager extensão instalada no Vs Code
- Conta Free Azure Cloud
- Grupo de Recursos já criado


## :link: Links/Referência
- [Microsoft Learn](https://learn.microsoft.com/pt-br/training/modules/create-azure-resource-manager-template-vs-code/7-summary)

### :bookmark: Notas
- Necessário alterar o nome do Storage Account, onde os nomes devem ser Únicos na plataforma Azure;
- Com a extensão ARM instalada dotada do recurso de Intelli Sense, basta digitar " que para cada parâmetro ele já irá sugerir as opções.
