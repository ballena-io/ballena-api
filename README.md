# ballena-api

Serverless API for [ballena.io](https://ballena.io).

## Dependencies

- [Vercel CLI](https://vercel.com/download)
  - Required to emulate local environment (serverless functions).

# Development

## Install requirements

```shell
yarn global add vercel
```

## Build

```shell
# Install dependencies
yarn

# Build project
vercel dev
```

Endpoints are based on folder/filename inside the `api/` folder.

```shell
# api/v1/time.ts
curl -X GET 'localhost:3000/v1/time'

# ...
```

# Production

## Deploy

Deployments to production should be triggered by a webhook when a commit, or a pull-request is merged to `master`.

If you need to force a deployment, use the following command:

```shell
vercel --prod
```
