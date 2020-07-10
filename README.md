## 目标

-   [x] 添加 eslint 和 prettier，husky(commitlint) 配置
-   [x] 添加 react-router-dom 支持(https://segmentfault.com/q/1010000015912149/)
-   [x] 添加 mobx 支持
-   [x] 添加 scss 支持
-   [x] 添加函数式编程，hooks
-   [x] 添加主要应用 use 等
-   [x] 加入了 eslint 以后电脑内存吃紧

## webpack 启动说明

```bash
- cnpm install
- npm run dev
```

## eslint&prettier 配置说明

### 安装和初始化 `eslint`

```bash
sudo npm  i eslint -g
eslint --init
```

-   配置

```
module.exports = {
  parser: {},  // 解析器
  extends: [], // 继承的规则 [扩展]
  plugins: [], // 插件
  rules: {}    // 规则
};
```

### 安装和初始化 prettier

```bash
npm i prettier eslint-config-prettier eslint-plugin-prettier -D
```

```js
// .eslintrc.js
 "extends": [
        "eslint:recommended",
        "plugin:react/recommended",
        "plugin:@typescript-eslint/recommended",
        'plugin:prettier/recommended',
    ],
```

### husky 配置提交检测

```bash
cnpm i husky -D
```

-   有了 `husky` 我们如果要验证我们每次的 `git commit` 的话，可以安装 `commitlint`

```js
 "husky": {
        "hooks": {
            "commit-msg": "commitlint -e $HUSKY_GIT_PARAMS"
        }
    },
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
