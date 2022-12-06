## :dart: Objetivo
Praticar a criação e implementação de uma Infraestrutura como Código (IaC) na Cloud Azure, usando o Modelo ARM (Azure Resource Manager) em formato .json.
- Implementar um modelo JSON do ARM usando o Visual Studio Code;
- Declarar recursos e adicionar flexibilidade ao modelo adicionando parâmetros e saídas.


## :pushpin: Descrição
Os modelos JSON do ARM (modelos do Azure Resource Manager) permitem especificar a infraestrutura de seu projeto de modo declarativo e reutilizável, tratando sua infraestrutura como código. Tratar sya infraestrutura como código permite que você controle as alterações em seus requisitos de infraestrutura e torna suas implantações mais consistentes e reproduzíveis. Os modelos podem ter controle de versão e ser salvos no mesmo controle do código-fonte do projeto de desenvolvimento. Este é apenas uma das formas, existe outras como Terraform, Ansible, Bicep e ARM. 


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
- Este exemplo foi realizado a partir da Trilha de Estudo para certificação: AZ-104: pré-requisitos para administradores do Azure [Microsoft Learn](https://learn.microsoft.com/pt-br/training/modules/create-azure-resource-manager-template-vs-code/7-summary)


### :bookmark: Notas
- Necessário alterar o nome do Storage Account, onde os nomes devem ser Únicos na plataforma Azure;
- Com a extensão ARM instalada dotada do recurso de Intelli Sense, basta digitar " que para cada parâmetro ele já irá sugerir as opções.
