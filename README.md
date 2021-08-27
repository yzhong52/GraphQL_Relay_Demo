- [GraphQL_Relay_Demo](#graphql_relay_demo)
  - [Frontend](#frontend)
    - [Step by Steps](#step-by-steps)
    - [Configure Relay Compiler](#configure-relay-compiler)
  - [Backend](#backend)
  - [References](#references)


# GraphQL_Relay_Demo

## Frontend

GraphQL Relay Demo Todo App

### Step by Steps

```
yarn create react-app graphql-relay-demo
```

```
yarn start
```

We should now be able to open the application in http://localhost:3000.

### Configure Relay Compiler

Placeholder graphql schema file:
```
cd graphql-relay-demo
curl https://raw.githubusercontent.com/relayjs/relay-examples/main/issue-tracker/schema/schema.graphql > schema.graphql
```

Update scripts:

```
// your-app-name/package.json
{
  ...
  "scripts": {
    ...
    "start": "yarn run relay && react-scripts start",
    "build": "yarn run relay && react-scripts build",
    "relay": "yarn run relay-compiler --schema schema.graphql --src ./src/ --watchman false $@"
    ...
  },
  ...
}
```

## Backend

## References

- [Step-by-step Guide](https://relay.dev/docs/getting-started/step-by-step-guide/)
- [Build A TODO App with Relay 1 - useQueryLoader | JSer - Learning Relay](https://www.youtube.com/watch?v=Vo2HX86gGL8&list=PLvx8w9g4qv_oIjs-sNY5MX3tcM7Spa8qP&index=1&ab_channel=JSer)
