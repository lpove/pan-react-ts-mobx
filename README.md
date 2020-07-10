## 目标

[] 添加 mobx 支持
[] 添加 scss 支持
[] 添加 react-router-dom 支持
[] 添加函数式编程，hooks
[] 添加主要应用 use 等

## webpack 启动说明

```bash
- cnpm install
- npm run dev
```

## package.json 说明

```js
{
    "name": "pan-dev-react",
    "version": "1.0.0",
    "description": "",
    "main": "index.js",
    "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1",
        "dev": "webpack-dev-server --mode development",
        "build": "webpack --mode production"
    },
    "author": "",
    "license": "ISC",
    "devDependencies": {
        "@types/react": "^16.9.41",
        "@types/react-dom": "^16.9.8",
        "awesome-typescript-loader": "^5.2.1",
        "html-webpack-plugin": "^4.3.0",
        "typescript": "^3.9.6",
        "webpack": "^4.43.0",
        "webpack-cli": "^3.3.12",
        "webpack-dev-server": "^3.11.0"
    }
}
```

-   "dev": "webpack-dev-server --mode development",
    -   node_modules/.bin/webpack-dev-server --mode development
-   "build": "webpack --mode production"
