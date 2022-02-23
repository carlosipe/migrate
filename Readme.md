# Migrate

## Usage

```sh
export DATABASE_URL=postgres://john:doe@localhost:5432/db_name
export MIGRATIONS_DIR=/home/whoever/project_one/migrations
migrate
```

Given a migrations directory with two migration files like:
```sql
-- migrations/1234_create_users.sql
create table users(id bigint);
```

```sql
-- migrations/1789_create_orders.sql
create table orders(price bigint);
```

```sh
$ migrate
Migrating 1234_create_users.sql
Migrating 1789_create_orders.sql
```
