# 타입스크립트+리액트 설치 
```
npx create-react-app 이름 --template typescript 
```

## react에서 타입오류 계속 뜰때 
```
npm install --save @types/react @types/react-dom
```

## 기본 모듈
```
npm i --save-dev @types/react-router-dom
npm i --save-dev @types/styled-components
npm install axios
npm install node-sass
//버전 6이 맞지 않아 5로 낮춰 install
npm uninstall node-sass 
npm install node-sass@5.0.0
```

## index.html
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <!-- <link rel="icon" href="%PUBLIC_URL%/favicon.ico" /> -->
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="theme-color" content="#000000" />
    <!-- <meta
      name="description"
      content="Web site created using create-react-app"
    /> -->
    <!-- <link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" /> -->
    <link rel="manifest" href="%PUBLIC_URL%/manifest.json" />
    <title>React App</title>
  </head>
  <body>
    <div id="root"></div>
  </body>
</html>

```

## App.tsx
```
import React from 'react';

function App() {
  return (
    <div className="App">
      APP
    </div>
  );
}

export default App;

```

## index.tsx
```
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);
```
## tsconfig.json
<a href="https://www.typescriptlang.org/docs/handbook/tsconfig-json.html">타입스크립트 tsconfig 핸드북</a>
```
{
  "compilerOptions": {
    "target": "es5",
    "lib": [
      "dom",
      "dom.iterable",
      "esnext"
    ],
    "allowJs": true,
    "skipLibCheck": true,
    "esModuleInterop": true,
    "allowSyntheticDefaultImports": true,
    "strict": true,
    "forceConsistentCasingInFileNames": true,
    "noFallthroughCasesInSwitch": true,
    "module": "esnext",
    "moduleResolution": "node",
    "resolveJsonModule": true,
    "isolatedModules": true,
    "noEmit": true,
    "jsx": "react-jsx"
  },
  "include": [
    "src"
  ]
}

```
## 상대 경로 축약 사용 
```
[jsconfig.json]

{
  "compilerOptions": {
    "baseUrl": "src"
  },
  "include": [
    "src"
  ]
}
```

## git에 공유 안하는 파일 
```
[.gitignore]

# lock
package-lock.json
yarn.lock

```


## redux-toolkit 적용해보기
<a href="https://kyounghwan01.github.io/blog/React/redux/redux-toolkit/#reselect">예제 참고</a>
```
//첫 셋팅 시: 리액트 + 타입스크립트 + 리덕스 설치 
npx create-react-app my-app --template redux-typescript

//리덕스 타입스크립트 설치 
npm install @types/react-redux

// 리덕스 툴킷 설치 
npm install @reduxjs/toolkit react-redux
```

