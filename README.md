
# Pipeline para website front-end 

Contrução de uma Pipeline para um front-end de website.


## Roadmap

- [X] Criar bucket s3 e deixar publico  
- [ ] Entregar o site buildado para bucket ao realizar push  
- [ ] Vincular dominio proprio ao bucket  
- [ ] Vincular ao CloudFront


## Stack

* AWS CLI
* Terraform




## Variaveis locais

Para utilização da criação dos recursos, necessario criar um arquivo chamado: "terraform.tfvars" na raiz do projeto, contendo as variaveis:

* aws_region
* site_domain


## Scripts Uteis

Scripts usados para testes e criação da pipeline:

Enviar conteudo da pasta "website" para o bucket s3:
```bash
  aws s3 cp website/ s3://$(terraform output -raw website_bucket_name)/ --recursive
```

Comandos uteis para testes e aplicações dos recursos
```bash
  terraform init
  terraform validate
  terraform plan
  terraform apply
  terraform show
  terraform state list
```


    
