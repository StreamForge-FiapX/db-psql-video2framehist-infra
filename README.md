# Infraestrutura RDS PostgreSQL - Video2FrameHist

Este repositório contém a configuração Terraform para provisionar um banco de dados PostgreSQL no Amazon RDS para a aplicação Video2FrameHist.

## Recursos Provisionados

- Banco de dados PostgreSQL 15.10 no Amazon RDS
- Security Group permitindo acesso na porta 5432
- Credenciais armazenadas no AWS Secrets Manager

## Pré-requisitos

- Terraform instalado
- Credenciais AWS configuradas
- Bucket S3 para armazenar o estado do Terraform

## Configuração

O banco de dados é configurado com:

- Instance class: db.t3.micro
- Storage: 10GB GP2
- Nome do banco: video2framehistdb
- Acesso público habilitado
- Backup final desabilitado

As credenciais do banco são geradas automaticamente e armazenadas de forma segura no AWS Secrets Manager.

## Deploy

O deploy é realizado automaticamente via GitHub Actions quando há push na branch main.