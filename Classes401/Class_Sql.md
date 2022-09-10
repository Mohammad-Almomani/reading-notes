# Reading SQL database, ORM, Sequelize

## SQL: difference between SQL and NoSQL

There are five main differences

1- SQL databases are relational, NoSQL databases are non-relational.

2- SQL databases use structured query language and have a predefined schema. NoSQL databases have dynamic schemas for unstructured data.

3- SQL databases are vertically scalable, while NoSQL databases are horizontally scalable.

4- SQL databases are table-based, while NoSQL databases are document, key-value, graph, or wide-column stores.

5- SQL databases are better for multi-row transactions, while NoSQL is better for unstructured data like documents or JSON.

reference: https://www.integrate.io/blog/the-sql-vs-nosql-difference/

## Sequelize

What is Sequelize and how to use it with Node js?

Sequelize: is a modern TypeScript and Node.js ORM for Postgres, MySQL, MariaDB, SQLite and SQL Server, and more. Featuring solid transaction support, relations, eager and lazy loading, read replication and more.

Sequelization: is the process of connecting a Node.js application to an Object Relational Mapper for better database synchronization.

now to use Sequelize with node.js, lets have an example:

1. Install dependencies:

```
     npm install sequelize sqlite3
```

2. Define models:

```javascript
    import { Sequelize, Model, DataTypes } from 'sequelize';
    const sequelize = new Sequelize('sqlite::memory:');
    const User = sequelize.define('User', {
    username: DataTypes.STRING,
    birthday: DataTypes.DATE,
    >});
```

3. Persist and query:

```javascript
const jane = await User.create({
  username: "janedoe",
  birthday: new Date(1980, 6, 20),
});

const users = await User.findAll();
```

reference: https://sequelize.org/

## ORM

What is an ORM, how does it work, and how should I use one?

ORM stands for Object to Relational Mapping, ORM is a method that enables object-oriented data manipulation and querying from databases.The term "an ORM" refers to a library that uses the Object-Relational Mapping approach

how does it work:

* The Object part is the one you use with your programming language

* The Relational part is a Relational Database Manager System ( A database that is ) there are other types of databases but the most popular is relational ( you know tables, columns, pk fk etc eg Oracle MySQL, MS-SQL )

* And finally the Mapping part is where you do a bridge between your objects and your tables.

how should I use one:

1. First, run the following commands to start an instance of PostgreSQL locally.

```
mkdir -p ~/data/pg-node-orms
docker run 
  --name pg-node-orms 
  -p 5432:5432 
  -e POSTGRES_PASSWORD=hunter12 
  -e POSTGRES_USER=orm-user 
  -e POSTGRES_DB=orm-db 
  -v ~/data/pg-node-orms:/var/lib/postgresql/data 
  -d 
  postgres
```

2. Now that you’ve got a database running we need to add some tables and data to the database. 

```
docker run 
  -it --rm 
  --link pg-node-orms:postgres 
  postgres 
  psql 
  -h postgres 
  -U orm-user 
  orm-db
```

3. Now that you’re connected, copy and paste the following queries into the prompt and press enter.

```SQL
CREATE TYPE item_type AS ENUM (
  'meat', 'veg', 'spice', 'dairy', 'oil'
);

CREATE TABLE item (
  id    SERIAL PRIMARY KEY,
  name  VARCHAR(64) NOT NULL,
  type  item_type
);

CREATE INDEX ON item (type);

INSERT INTO item VALUES
  (1, 'Chicken', 'meat'), (2, 'Garlic', 'veg'), (3, 'Ginger', 'veg'),
  (4, 'Garam Masala', 'spice'), (5, 'Turmeric', 'spice'),
  (6, 'Cumin', 'spice'), (7, 'Ground Chili', 'spice'),
  (8, 'Onion', 'veg'), (9, 'Coriander', 'spice'), (10, 'Tomato', 'veg'),
  (11, 'Cream', 'dairy'), (12, 'Paneer', 'dairy'), (13, 'Peas', 'veg'),
  (14, 'Ghee', 'oil'), (15, 'Cinnamon', 'spice');

CREATE TABLE dish (
  id     SERIAL PRIMARY KEY,
  name   VARCHAR(64) NOT NULL,
  veg    BOOLEAN NOT NULL
);

CREATE INDEX ON dish (veg);

INSERT INTO dish VALUES
  (1, 'Chicken Tikka Masala', false), (2, 'Matar Paneer', true);

CREATE TABLE ingredient (
  dish_id   INTEGER NOT NULL REFERENCES dish (id),
  item_id   INTEGER NOT NULL REFERENCES item (id),
  quantity  FLOAT DEFAULT 1,
  unit      VARCHAR(32) NOT NULL
);

INSERT INTO ingredient VALUES
  (1, 1, 1, 'whole breast'), (1, 2, 1.5, 'tbsp'), (1, 3, 1, 'tbsp'),
  (1, 4, 2, 'tsp'), (1, 5, 1, 'tsp'),
  (1, 6, 1, 'tsp'), (1, 7, 1, 'tsp'), (1, 8, 1, 'whole'),
  (1, 9, 1, 'tsp'), (1, 10, 2, 'whole'), (1, 11, 1.25, 'cup'),
  (2, 2, 3, 'cloves'), (2, 3, 0.5, 'inch piece'), (2, 13, 1, 'cup'),
  (2, 6, 0.5, 'tsp'), (2, 5, 0.25, 'tsp'), (2, 7, 0.5, 'tsp'),
  (2, 4, 0.5, 'tsp'), (2, 11, 1, 'tbsp'), (2, 14, 2, 'tbsp'),
  (2, 10, 3, 'whole'), (2, 8, 1, 'whole'), (2, 15, 0.5, 'inch stick');
```

You now have a populated database. You can type quit to disconnect from the psql client and get control of your terminal back. If you ever want to run raw SQL commands again you can run that same docker run command again.

4. Finally, you’ll also need to create a file named connection.json containing the following JSON structure. This will be used by the Node applications later to connect to the database.

```json
{
  "host": "localhost",
  "port": 5432,
  "database": "orm-db",
  "user": "orm-user",
  "password": "hunter12"
}
```
reference: https://blog.logrocket.com/why-you-should-avoid-orms-with-examples-in-node-js-e0baab73fa5/
