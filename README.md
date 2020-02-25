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

No exemplo abaixo foi imaginado um cenário serveless onde a api pode ser chamada tanto via lambda, quanto pelo api gateway ou direto em um banco de dados.

![lambda](https://imagesbox.blob.core.windows.net/pictures/lambda.png)

No próximo exemplo utilizamos um backend em Kubernetes.

![kubernetes](https://imagesbox.blob.core.windows.net/pictures/kubernetes.png)

## Resumo

Independente qual for o backend utilizado e forma como a API será exposta para ser consumida, o pipeline de CI/CD seguirá o fluxo apresentado no início apenas será ajustado os processos para build e deploy de acordo com a arquitetura e os testes desejados.

O provisionamento da infra indepente do tipo de arquitetura pode ser feito tanto pelo cloudformation da própria AWS, mas aconselho utilizar o terraform para fazer o IAC (infraestrutura como código) necessário, pois o mesmo pode ser utilizado em outros cloud providers.