# v0.1.0版本

## 套件
### vite-tsconfig-paths 
> 如果有使用 TypeScript 的話，可以直接搭配使用 vite-tsconfig-paths，然後就會讀取 tsconfig 中的設置自動為vite配置路徑。
* 安裝：`npm install --save-dev vite-tsconfig-paths `
* 基礎配置：
  ```
  import tsconfigPaths from 'vite-tsconfig-paths';
  
  export default defineConfig({
    plugins: [tsconfigPaths()],
  });
  ```

### eslint-plugin-import
> 用於檢查ES Module 的導入和導出代碼，防止文件路徑和導入名稱拼寫錯誤的問題。
* 安裝：`npm i -D eslint-plugin-import `
* 基礎配置：
  ```
    "extends" :  [ "plugin:import/recommended" ] ,
    plugins" :  "eslint-plugin-import" 
  ```

### eslint-import-resolver-typescript
> 由於 ESLint 並不會自動去讀 tsconfig.json 的檔案，這時候可以使用 eslint-import-resolver-typescript，然後在 .eslintrc 中使用。
* 安裝：`npm install --save-dev eslint-import-resolver-typescript `
* 基礎配置：`settings.import/resolver.typescript` 設定至少為 `{}`，以免解析 import/module 位置錯誤
  ```
  {
   "settings": {
      "import/resolver": {
        "typescript": {}
      },
    },
  }
  ```
* 路徑配置：map 的路徑是相對專案根目錄的，如果.eslintrc 不在根目錄下，改用js來配置絕對路徑( path.resolve(__dirname, 'src'))。
  ```
  {
   "settings" : {
     "import/resolver" : {
       "alias" : {
         "map" : [[ "@" , "./src" ]],
         "extensions" : [ ".js" , ".jsx" ]
        }
      }
    }
  }
  ```


## 配置參考
* [eslint-plugin-import Unable to resolve path to module](https://github.com/zhbhun/blog/issues/1)
