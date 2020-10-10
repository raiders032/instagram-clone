# instagram-clone

instagram-clone



### 1.0 Setting up the project

```shell
yarn init
yarn add graphql-yoga
yarn add nodemon -D
yarn add babel-node
yarn add babel-cli
```

### nodemon

- 파일을 저장할 때마다 실행을 해주는 도구



___



### 1.1 Creating GraphQL Server

```shell
yarn add dotenv
yarn add @babel/node
yarn add @babel/preset-env
yarn add @babel/core
```



dotenv

* .env파일을 읽는다.
* 모든 설정 값들을 env에 추가하는게 좋다.



babel

```
{
  "presets": ["@babel/preset-env"]
}
```



error

```
Error: Requires Babel "^7.0.0-0", but was loaded with "6.26.3". If you are sure you have a compatible version of @babel/core, it is likely that something in your build process is loading the wrong version. Inspect the stack trace of this error to look for the first entry that doesn't mention "@babel/core" or "babel-core" to see what is calling Babel. (While processing preset: "/Users/yeongsamno/Desktop/dev/project/instagram-clone/node_modules/@babel/preset-env/lib/index.js")
,,,
```



해결

```
1. package.json 에서 babel-cli 지우기
2. node_moldules 지우기
3. yarn add @babel/cli
```



___



### 1.2 Setting Up the Server like the Pros

```
yarn add morgan
```



morgan

* 로깅 모듈

graphQLServer

* Express 서버가 내장되어 있다.

```javascript
const server = new GraphQLServer({ typeDefs, resolvers });

#GraphQLServer룰 통해 express에 접근 할 수 있다.
#미들웨어 morgan을 추가한다.
server.express.use(logger("dev"));
```



```shell
yarn add graphql-tools merge-graphql-schemas
```



























