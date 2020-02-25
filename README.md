# Herospark

## Objetivo

Descrever o pipeline completo de CI/CD para uma api.

## Pré Requisito

Processo de pipeline deve utilizar o cloud provider AWS.

## Pipeline

![pipeline](https://imagesbox.blob.core.windows.net/pictures/aws_code_pipeline.png)

## Possíveis utilizações do pipeline

Temos um exemplo abaixo da api armazenada em um elastic beanstalk e o processo de deploy da nova versão até o backend.

![elasticbeanstalk](https://imagesbox.blob.core.windows.net/pictures/elasticbeabstalk.png)

No exemplo abaixo foi imaginado um cenário serverless onde a api pode ser chamada tanto via lambda, quanto pelo api gateway ou direto em um banco de dados.

![lambda](https://imagesbox.blob.core.windows.net/pictures/lambda.png)

No próximo exemplo utilizamos um backend em Kubernetes.

![kubernetes](https://imagesbox.blob.core.windows.net/pictures/kubernetes.png)

## Resumo

Independente qual for o backend utilizado e forma como a API será exposta para ser consumida, o pipeline de CI/CD seguirá o fluxo apresentado no início apenas será ajustado os processos para build e deploy de acordo com a arquitetura e os testes unitários desejados.

O provisionamento da infra pode ser feito tanto pelo cloudformation da própria AWS quanto pelo terraform, caso exista a possibilidade de utilizar outros provedores de cloud no futuro, optar pelo uso do terraform para o IAC (infraestrutura como código) da arquitetura, pois o mesmo aceita diferentes providers.
