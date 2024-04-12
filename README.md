# Find My Hip Hop

[Preview the project](http://hiato.fly.dev)

<a alt="Nx logo" href="https://nx.dev" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/nrwl/nx/master/images/nx-logo.png" width="45"></a>

✨ **This workspace has been generated by [`create-nextup-platforms`](https://github.com/dcat23/nextup)** ✨


## Features

- [nextup](#nextup-plugin)

### Built with

- [Nx](https://nx.dev)
- [Docker](https://docs.docker.com/get-docker/)
- [Next.js](https://nextjs.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [TanStack Query](https://tanstack.com/query/latest)
- [NextAuth.js](https://next-auth.js.org/)
- [Prisma](https://www.prisma.io/)
- [Zustand](https://zustand.surge.sh/)
- [Socket.io](https://socket.io/)
- [zod](https://github.com/colinhacks/zod)
- [Upstash Redis](https://upstash.com/)
- [Framer motion](https://www.framer.com/motion/)
- [Tailwind CSS](https://tailwindcss.com/)

## Getting started

FindMyHipHop uses [pnpm](https://pnpm.io) as a package manager, so make sure to [install](https://pnpm.io/installation) it first.

### Installation

```bash
pnpm i
```

### Environment Variables

Before running the development server, make sure to create `.env` file in the root directory
of the project and add the required environment variables.

You can use the example provided in the repository as a starting point.

```bash
cp .env.example .env
```

Create a `NEXTAUTH_SECRET`
```bash
openssl rand -base64 32
```

GitHub OAuth secrets for auth & login [here](https://github-client-generator.vercel.app/)
- `AUTH_GITHUB_ID`
- `AUTH_GITHUB_SECRET`


### Setting Database

FindMyHipHop uses [Prisma](https://www.prisma.io/) as an ORM to interact with the database.

Spin up database locally from [docker-compose.yml](./docker-compose.yml)
```bash
docker compose up -d
```

Access the database from [localhost:5050](http://localhost:5050)


Before running the development server, make sure to generate the Prisma client by
pushing the [initial schema](./prisma/init.sql)

```bash
npx prisma db push
```

If using an existing postgres db, pull existing changes if necessary.
add `public` or other schema name used into [`schemas`](./prisma/schema.prisma)

```bash
npx prisma db pull
```

Generate @prisma/client
```bash
npx prisma generate
```

After generating the Prisma client, make sure to also push any changes to the database schema by running:

```bash
npx prisma db push
```

### Development

Run the dev server
```bash
npx nx dev
```

This ensures that the local database is up-to-date with any changes made to the schema in the codebase.

## Contributing

- Missing something or found a bug? [Report here](https://github.com/dcat23/FindMyHipHop/issues).
- Want to contribute? Check out the [contribution guide](https://github.com/dcat23/FindMyHipHop/blob/main/CONTRIBUTING.md).

## License

Distributed under the [MIT License](https://github.com/dcat23/FindMyHipHop/blob/main/LICENSE).

## Acknowledgments

- [Docker](https://www.docker.com/)
- [Fly.io](https://fly.io/)
- [Supabase](https://supabase.com/)