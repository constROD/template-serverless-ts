# Template Serverless TypeScript

## Prerequisites

- Download extension **ESLint** and **Prettier - Code formatter** in your VSCode.
- Install **node** >= 16.13.0
- Install **pnpm** >= 7.17.0
- Install **serverless**
- Install **nodemon**

- **(Required for MacOSX):** Run this to give permission husky to run pre-commit hook.

```bash
$ chmod ug+x .husky/*
$ chmod ug+x .git/hooks/*
```

- **(Optional):** Do this if you are using **nvm**.

```bash
$ nvm use or nvm use 16.13.0
```

- Create `.env` file.
- Create `.aws-config` file.
- Create `.aws-credentials` file.
- Create `.npmrc` and file.
- And refer to the `sample.<secret-file>` for the required variables.

## Without Docker

- Install dependencies.

```bash
$ pnpm i
```

- Run in **development** mode.

```bash
$ pnpm dev
```

## With Docker

- Build container.

```bash
$ docker compose build
```

```bash
$ docker compose build --no-cache # Build with no cache
```

- Run container in **development** mode.

```bash
$ docker compose up
```

```bash
$ docker compose up -d # Run in the background.
```

- Check container's logs.

```bash
$ docker logs <container-name>
```

- Shutdown container.

```bash
$ docker compose down
```

```bash
$ docker compose down -v # Remove including the volumes
```

- If you want to access the container.

```bash
$ docker exec -it <container-name> bash
```
