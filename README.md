# Setup Project

Create .env file

```
DATABASE_URL="sqlserver://localhost;database=restful_api_typescript;user=db-user;password=db-password;trustServerCertificate=true"
```

```shell

npm install

npx prisma migrate dev

npx prisma generate

npm run build

npm run start

```
