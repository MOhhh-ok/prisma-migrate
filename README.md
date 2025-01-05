# Prisma Migrate

A lightweight utility for managing database migrations with Prisma.

> **Note**
> This is not a complete migration solution. It only applies pending migrations in order and does not support rollbacks or schema validation.


## Installation

```bash 
npm install @masa-dev/prisma-migrate
```

## Usage

```ts
import { migrate } from '@masa-dev/prisma-migrate';
import { PrismaClient } from '@prisma/client';

const prisma = new PrismaClient();

await migrate({
  prisma,
  migrationsPath: './prisma/migrations'
});
```

## Migration Directory Structure

```
migrations/
  ├── 20240301_initial/
  │   └── migration.sql
  ├── 20240302_add_users/
  │   └── migration.sql
  └── 20240303_add_posts/
      └── migration.sql;
```

## License

MIT