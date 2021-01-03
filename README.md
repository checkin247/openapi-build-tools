# Tools to create and manage OpenApi API's

This repository is the conclusion of the [Blog Post: Document Rest APIs](https://tliebrand.com/19-programming/29-openapi-specification-stoplight)

## Installation

````
npm install
# or
yarn install
````


## Requirements

The following tools are expected to be installed globally:

- prism
- speccy

Optionally:

- openapi2postmanv2

In order to use the lint or resolve script, you must install speccy for node or docker

**Node**

```
npm install speccy -g
# or
yarn global add speccy
```

**Docker**

If you want to use docker, just run the docker command, it will install the containers for you.

### Mock server

You can install prism globally for node or run it with docker

**Node:**

```
npm install -g @stoplight/prism-cli
# or
yarn global add @stoplight/prism-cli
```

**Docker**

`docker run --init --rm -it -v ${PWD}:/tmp -p 84:4010 stoplight/prism:3 mock -h 0.0.0.0 "/tmp/dist/openapi.yml"`

*more options here: https://github.com/stoplightio/prism/blob/master/docs/getting-started/01-installation.md*


## Usage
### Create documentation

Automatically create documentations with the OpenAPI specifications.
Resolve the specifications into one file "dist/openapi.yml"

1. Run `npm run lint`
2. Run `npm run build`

Updated documentation is now "dist/index.html"

### Bundle specification

Bundles all modules and specifications into one single file into "dist/openapi.yml"

1. run `npm run lint`
2. run `npm run build`

### Mock

```
npm run mock
```

