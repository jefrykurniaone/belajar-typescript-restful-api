# Setup Project

Create .env file

```dotenv
DATABASE_URL="sqlserver://localhost;database=restful_api_typescript;user=your-db-user;password=your-db-password;trustServerCertificate=true"
```

```shell

npm install

npx prisma migrate dev

npx prisma generate

npm run build

npm run start

```
