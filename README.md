# @xinliang/scp

> Encapsulated [node-scp](https://www.npmjs.com/package/node-scp), uploading files to the server is more convenient.

## 0. install

```shell
npm i @xinliang/scp -D
```

## 1. init `scp.config.json` file

> The clientConfig configuration should be consistent with node-scp. If you expect more freedom of control, you should use [node-scp](https://www.npmjs.com/package/node-scp) directly

```json
{
  "clientConfig": {
    "host": "www.google.com",
    "port": 22,
    "username": "root"
  },
  "uploadPath": "./dist",
  "remotePath": "project/workspace"
}
```

## 2. add `scripts` for `package.json`

```diff
  ...
  "scripts": {
+    "push": "scp",
  },
  ...
```
