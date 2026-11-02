# Deploy - Painel Bella

## Variáveis de ambiente

Configure estas variáveis no Koyeb:

```env
READ_ONLY=false
PORT=3000
DB_NAME=bella_dashboard
MONGODB_URI=mongodb+srv://USUARIO:SENHA@HOST/?appName=Cluster0
ADMIN_USER=usuario-admin
ADMIN_PASSWORD=SENHA_DO_ADMIN
ADMIN_EMAIL=email@dominio.com
```

`EMAIL_USER` e `EMAIL_PASS` são opcionais e usados apenas para envio de e-mail de redefinição de senha.

## Build

O projeto está preparado para deploy por Dockerfile.

```bash
docker build -t bella-dashboard .
docker run --env-file .env -p 3000:3000 bella-dashboard
```

## Observações

- As bases brutas e modelos `.xlsx`/`.csv` não entram no Git nem no Docker.
- Os dados do painel ficam no MongoDB, banco `bella_dashboard`.
- O arquivo `.env` local contém credenciais e não deve ser commitado.
