# Orquestra_Conteiner
Estudo e prática sobre Containers e Kubernetes.

## Comando Basicos

#### Verificação da instalação do kind
`kind`

#### Verificação da instalação do kubectl
`kubectl`

#### Criando nosso cluster Kubernetes utilizando o Kind
`kind create cluster`

#### Conectar o cluster nas configuração do Kubernetes para o contexto do kind
`kubectl cluster-info --context kind-kind`

#### Verificando os nós disponíveis utilizando o kubectl
`kubectl get nodes`

#### Deleteando o cluster kind com apenas um nó
`kind delete cluster --name=kind`

#### Cria um cluster Kubernetes local, com base em um arquivo de configuração customizado
`kind create cluster --config=<caminho-arquivo-config>.yaml --name=<nome-do-cluster>`

#### Cria o secret utilizando o arquivo de configuração .yaml
`kubectl apply -f secrets.yaml`

#### Cria o pod utilizando o arquivo de configuração .yaml
`kubectl apply -f pod.yaml`

#### Verificando a situação atual do pod criado
`kubectl get pods`

#### Verificando as informações do pod utilizando o comando kubectl describe
`kubectl describe pod <nome-do-pod>`

#### Verificando os logs do pod utilizando o comando kubectl logs
`kubectl logs -f <nome-do-pod>`

#### Fazendo um proxy-forward para acessar a porta do pod
`kubectl port-forward pod/<nome-do-pod> 8000:8000`

#### Excluir o pod criado
`kubectl delete pod <nome-do-pod>`

#### Verifica o replicaset criado
`kubectl get replicaset`

#### Verifica os services ativos
`kubectl get services`

#### Verifica os services ativos utilizando o atalho svc
`kubectl get svc`

#### Deleta  o servido do tipo ClusterIP do servidor-python
`kubectl delete svc servidor-python-service`

#### Redireciona a porta 8000 do host local para a porta 80 do serviço Kubernetes especificado
`kubectl port-forward svc/<nome-do-serviço> <porta-local>:<porta-do-serviço>`

#### Configura o ingress-nginx com todos os seus componentes no cluster kubernetes
`kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml`

#### Aguarda os componentes do ingress-nginx ficarem ativos
`kubectl wait --namespace ingress-nginx --for=condition=ready pod --selector=app.kubernetes.io/component=controller --timeout=90s`

#### Lista os autoscalers (HPA) configurados no cluster
`kubectl get hpa`

#### deletar todos os recursos que foram criados
`kubectl delete all --all`

#### deletar o cluster kind e todos os seus nós
`kind delete cluster --name=k8s-cluster`
