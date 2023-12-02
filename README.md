# Terraform - LocalStack

Segue uma abordagem de estudo bem interessante para simular serviços da AWS como também realizar uma abordagem com Iac (Terraform) segue os testes.

# LocalStack

https://www.localstack.cloud/

Existe uma documentação para realizar a instação desse emulador:

https://docs.localstack.cloud/getting-started/installation/

## Instalar Docker

Link - https://docs.docker.com/engine/install/ubuntu/
````
 sudo apt-get update
 sudo apt-get install ca-certificates curl gnupg
 sudo install -m 0755 -d /etc/apt/keyrings
 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
 sudo chmod a+r /etc/apt/keyrings/docker.gpg
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
 sudo apt-get update
 sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
````
# Terraform

Para realizar os processos do terraform vai ser preciso instalar e também integração como Docker e realizar o processo abaixo:

````
sudo apt  install awscli  
sudo snap install terraform --classic
aws configure # Conforme a estrutura de chave da AWS dentro do terraform tem que ser igual
terraform init # Dentro da IDE (Example: Visual code) abrir o terminal e executar dentro da pasta de trabalho o código
terraform apply # Realizar o plano de execução
````
