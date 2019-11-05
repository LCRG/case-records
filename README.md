# case-records
A place to practice capturing CASE records for competencies with API access for visualizing

This example shows how to implement an example **GraphQL server with TypeScript** based on  [Photon JS](https://photonjs.prisma.io/), [apollo-server](https://www.apollographql.com/docs/apollo-server/) and [GraphQL Nexus](https://nexus.js.org/).

## How to use

### 1. Download example & install dependencies

Clone the repository:

```
git clone https://github.com/LCRG/case-records.git
```

Install Node dependencies:

```
cd case-records
npm install
```

Launch Postgres container in Docker:
```
npm run launch
```

### 2. Install the Prisma 2 CLI

To run the example, you need the [Prisma 2 CLI](https://github.com/prisma/prisma2-docs/blob/master/prisma-2-cli.md):

```
npm install -g prisma2
```

### 3. Set up database

The following commands will use your schema.prisma data model to create a database migration and then create the database schema. To set up your database, run:

```
prisma2 lift save --name 'init'
prisma2 lift up
```

You can now use your favorite Postgres client to view and edit your data that was created when you ran `prisma2 lift up`.

### 4. Generate Photon (type-safe database client)

Run the following command to generate [Photon JS](https://photonjs.prisma.io/):

```
prisma2 generate
```

Now you can seed your database using the `seed` script from `package.json`:

```
npm run seed
```

### 5. Start the GraphQL server

Launch your GraphQL server with this command:

```
npm start
```

Navigate to [http://localhost:4000](http://localhost:4000) in your browser to explore the API of your GraphQL server in a [GraphQL Playground](https://github.com/prisma/graphql-playground).

