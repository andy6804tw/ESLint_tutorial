# ESLint教學
> ESLint支援ES6與JSX語法，具高度設定彈性與擴充性的檢查語法工具，可提供程式開發者在語法上的錯誤警告，這邊我所使用的是Airbnb的規範，簡單來說ESLint就是可以規範整個開發團隊中的coding style

# Usage
1. clone the repository
```
$ git clone https://github.com/andy6804tw/ESLint_tutorial.git
```
2. install package
```
$ npm install
$ cd ESLint_tutorial
```

## 教學
1. 初始化node
```
$ npm init -y
```
這邊會產出一個package.json,這個檔案專門管理node的各種套件

2. 安裝eslint與babel-eslint 
```
$ npm install eslint babel-eslint --save-dev
```

3. 使用eslint-airbnb-base
這邊可以參考至Airbnb的[GitHub](es6+的eslint-rules)
```
$ npm install eslint-config-airbnb-base eslint-plugin-import eslint --save-dev
```

4. 建立.eslintrc檔案並貼上下列程式
```js
{
  "parser": "babel-eslint", //parser: 指的是剖析器，如果你有用babel編譯器，就是設定"babel-eslint"
  "env": {
    "browser": true,
    "node": true
  },
  "extends": "airbnb-base",
  "rules": {
    "semi": [2, "never"],
    "arrow-body-style": ["error", "always"],
    "comma-dangle": ["error", "never"], //該規則強制使用對象和數組文字中的逗號
    "no-console": 0 //關掉console.log()錯誤
  }
}
```
> 最後執得一提的是筆者開發環境是使用VScode記得安裝ESLint的擴充套件才會即時顯示錯誤哦，裡面分別有兩隻js檔index.js是錯誤並且跳出警示的寫法，correct.js是依照規範修改後正確的寫法

## MIT License
```
Copyright (c) 2017 Yi Lin Tsai 

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```