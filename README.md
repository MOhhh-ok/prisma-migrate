# Prisma Migrate

A lightweight utility for managing database migrations with Prisma.

## Features

Automatic migration in code.

## Installation

```bash 
npm install @masa-dev/prisma-migrate
```

## Usage

```ts
import { prismaMigrate } from 'prisma-migrate-helper';
import { PrismaClient } from '@prisma/client';

const prisma = new PrismaClient();

await prismaMigrate({
  prisma,
  migrationsPath: './prisma/migrations'
});
```

## Migration Directory Structure

```
migrations**/
  ├── 20240301_initial/
  │   └── migration.sql
  ├── 20240302_add_users/
  │   └── migration.sql
  └── 20240303_add_posts/
      └── migration.sql;
```

## License

MIT