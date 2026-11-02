# Painel Bella - Dashboard MongoDB

**[Ler o estudo de caso](https://lariantunez.github.io/painel-contagem-estoque/)** · **[Abrir a demo do painel](https://lariantunez.github.io/painel-contagem-estoque/painel/)**

![Painel Bella com dados fictícios](assets/painel-estoque.jpg)

Dashboard web desenvolvido para automatizar análises comerciais do cliente Bella, transformando consultas antes feitas manualmente em planilhas dinâmicas em um painel com importação, tratamento e indicadores executivos.

O projeto contempla vendas, valor, estoque e rotinas específicas de contagem manual de estoque, com filtros e agregações preparadas para uso pela diretoria comercial.

## Objetivo

Reduzir trabalho manual em Excel e oferecer uma visão recorrente, padronizada e navegável dos principais indicadores de sell out e estoque do cliente Bella.

## Principais recursos

- Importação de dados brutos em CSV/XLSX.
- Tratamento de datas, meses, GTIN/EAN e campos numéricos.
- De/Para de lojas e categorias.
- Dashboard com KPIs de vendas, faturamento, estoque e evolução diária.
- Filtros por período, filial, categoria, família e produto.
- Importação de estoque manual com modelo de planilha.
- Template de contagem de estoque para download.
- Área administrativa com usuários, admins, logs e templates.
- Reset de senha por e-mail.
- Healthcheck e modo somente leitura para deploy/demo.

## Tecnologias

- Node.js
- Express
- MongoDB Atlas
- HTML, CSS e JavaScript puro
- Multer
- XLSX
- csv-parser
- Nodemailer
- Docker

## Estrutura

```text
backend/src/server.js                API, importacoes, autenticacao e agregacoes
frontend/index.html                  Dashboard e administracao
frontend/reset-senha.html            Redefinicao de senha
modelo_contagem_estoque_bella.xlsx Modelo de contagem de estoque com lojas e produtos ficticios
docs/                                Manuais de uso e manutencao
README_DEPLOY.md                     Notas de deploy
Dockerfile                           Build da aplicacao
```

## Variáveis de ambiente

Use `.env.example` como referência para criar o `.env` local. O `.env` não deve ser publicado.

```env
PORT=3000
DB_NAME=bella_dashboard
MONGODB_URI=mongodb+srv://USUARIO:SENHA@HOST/?appName=Cluster0
ADMIN_USER=usuario-admin
ADMIN_PASSWORD=senha-admin
ADMIN_EMAIL=email@dominio.com
EMAIL_USER=
EMAIL_PASS=
READ_ONLY=false
```

## Como executar

```bash
npm install
npm start
```

## Demo estática

Este repositório também possui uma demo do painel real em `docs/index.html`, criada para GitHub Pages e portfólio. Ela usa dados fictícios e uma API simulada no navegador, sem depender de MongoDB, backend ou variáveis de ambiente.

## Cuidados de portfólio

O repositório deve permanecer sem bases reais, credenciais, uploads e planilhas operacionais. Apenas o modelo vazio de contagem de estoque é mantido para demonstrar a funcionalidade.

## Status

Projeto funcional, com rotinas de importação, dashboard analítico, administração e deploy via Docker.
