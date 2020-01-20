---
title: Iniciando com minikube
published: true
---

Bom pessoal nosso objetivo é criar um cluster kubernetes, mas o que é kubernetes ?, em poucas palavras o kubernetes é um software open source mantido pelo google para orquestrar e gerenciar clusters de containers aqui usaremos como engine de containers o docker.

O minikube é uma excelente ferramenta para testar e aprender a trabalhar com o kubernetes

![minikube](assets/minikube-start/minikube_kubernetes_00.png)

a primeira etapa para criarmos um cluster kubernetes é instalar o kubectl, mas o que é kubectl ?, kubectl é o software resposavel por "conversar" com o cluster kubernetes a partir de um computador local

![minikube](assets/minikube-start/minikube_kubernetes_01.png)

dependendo da sua internet isso pode demorar um pouco

![minikube](assets/minikube-start/minikube_kubernetes_02.png)

apos fazer o download vamos torna o binário executável.

![minikube](assets/minikube-start/minikube_kubernetes_03.png)

agora basta movermos para o diretório /usr/local/bin/kubectl com isso terminámos a instalação do kubectl

![minikube](assets/minikube-start/minikube_kubernetes_04.png)

com o comando `kubectl version` podemos ter as informações basicas do kubectl instalado

![minikube](assets/minikube-start/minikube_kubernetes_05.png)

para fazer o cluster vamos usar o projeto open source minikube, o minikube vai um software de virtualização para criar um cluster kubernetes de um no único, aqui vamos usar o virtualbox para este processo, é bom lembrar que o minikube não é recomendado para ser usado em ambiente de produção, ele simula um cluster de no único com tudo o que é necessario já instalado e funcionando.

![minikube](assets/minikube-start/minikube_kubernetes_06.png)

antes de prosseguir vamos conferir se a virtualização esta liberada em nossa maquina com o seguinte comando `egrep -q 'vmx|svm' /proc/cpuinfo && echo yes || echo no`

![minikube](assets/minikube-start/minikube_kubernetes_07.png)

depois que vimos que a virtualização esta habilitada vamos fazer a instalação do minikube

![minikube](assets/minikube-start/minikube_kubernetes_08.png)

apos fazer o processo do download e feita a instalação conseguiremos ver a versão do minikube instalado com o comando `minikube version`

![minikube](assets/minikube-start/minikube_kubernetes_09.png)

com o miniukube instalado vamos informar que iremos usar o virtualbox para virtualização

![minikube](assets/minikube-start/minikube_kubernetes_10.png)

feito isso basta usar o camando `minikube start` para criarmos o cluster, este processo pode demorar um pouco

![minikube](assets/minikube-start/minikube_kubernetes_11.png)

com o cluster instalado e funcionando podemos usar o comando `minikube status` para obter informações do cluster

![minikube](assets/minikube-start/minikube_kubernetes_12.png)

Isso é tudo, ja temos nosso cluster kubernetes local instalado e funcionando

