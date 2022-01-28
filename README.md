# Realm Web and GraphQL Tutorial

Follow along at https://docs.mongodb.com/realm/tutorial/web-graphql/

## Troubleshooting

- Be sure to **check the logs in Realm UI** for more information as well as the console in your app.
- Be sure to **deploy your changes** in the Realm UI.

## Issues & Pull Requests

If you find an issue or have a suggestion, please let us know using the feedback
widget on the [docs site](http://docs.mongodb.com/realm/tutorial).

This repo is automatically derived from our main docs repo. If you'd like to
submit a pull request -- thanks! -- please feel free to do so at
https://github.com/mongodb/docs-realm/ (see the tutorial/ subdirectory).

# Additional NPM modules installed to reduce errors

```java
npm install node-polyfill-webpack-plugin
npm install stream --save
npm install util --save
```

# Errors running nmp run start

```java
npm run start
```

Output

```java
WARNING in ./node_modules/@apollo/client/version.js
Module Warning (from ./node_modules/source-map-loader/dist/cjs.js):
Failed to parse source map from '/mnt/volume_nyc1_01/realm-tutorial-web/node_modules/@apollo/src/version.ts' file: Error: ENOENT: no such file or directory, open '/mnt/volume_nyc1_01/realm-tutorial-web/node_modules/@apollo/src/version.ts'
 @ ./node_modules/@apollo/client/core/ApolloClient.js 5:0-40 87:19-26
 @ ./node_modules/@apollo/client/core/index.js 1:0-49 1:0-49
 @ ./node_modules/@apollo/client/index.js 1:0-32 1:0-32
 @ ./src/graphql/RealmApolloProvider.js 8:0-87 11:19-27 29:20-33 30:13-25 47:42-56
 @ ./src/App.js 9:0-64 52:38-57
 @ ./src/index.js 7:0-24 16:36-39

WARNING in ./node_modules/bson/dist/bson.browser.esm.js 2196:26-55
Module not found: Error: Can't resolve 'crypto' in '/mnt/volume_nyc1_01/realm-tutorial-web/node_modules/bson/dist'

BREAKING CHANGE: webpack < 5 used to include polyfills for node.js core modules by default.
This is no longer the case. Verify if you need this module and configure a polyfill for it.

If you want to include a polyfill, you need to:
        - add a fallback 'resolve.fallback: { "crypto": require.resolve("crypto-browserify") }'
        - install 'crypto-browserify'
If you don't want to include a polyfill, you can use an empty module like this:
        resolve.fallback: { "crypto": false }
 @ ./src/graphql/useTaskMutations.js 6:0-32 102:19-27
 @ ./src/graphql/useTasks.js 5:0-50 18:6-22 28:32-48
 @ ./src/components/ProjectScreen.js 9:0-43 113:6-14 281:10-18
 @ ./src/TaskApp.js 10:0-55 37:39-52
 @ ./src/App.js 8:0-32 59:38-45
 @ ./src/index.js 7:0-24 16:36-39

93 warnings have detailed information that is not shown.
Use 'stats.errorDetails: true' resp. '--stats-error-details' to show it.

webpack 5.67.0 compiled with 93 warnings in 2195 ms
```
