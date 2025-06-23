# Package install

- Scoop 설치
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -scope CurrentUser
```
```powershell
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```

- git, aria2 설치
```powershell
scoop install git aria2
```

- node.js 설치
```powershell
scoop install nodejs-lts
node -v
> v22.16.0
```

- vscode 설치
```powershell
scoop bucket add extras
scoop install vscode

cd C:\scoop\apps\vscode\current
./install-context.reg
```

- touch, chrome 설치
```powershell
scoop install touch
```
```powershell
scoop install googlechrome
chrome
```

<br>

# VSCode Extension
- Korean Language Pack
- Prettier
- Tailwind CSS
- Headwind
- PostCSS

<br>

# Typescript

- 컴파일러 설치
```powershell
npm i -g typescript ts-node
tsc -v
> Version 5.8.3
ts-node -v
> v10.9.2
```

- 파일 생성, 컴파일
```powershell
mkdir ch01/ch01_4/src
touch ch01/ch01_4/src/index.ts
cd ch01/ch01_4
```
> index.ts
> ```typescript
> console.log("Hello world!");
> ```
```powershell
ts-node src/index.ts
> Hello World!
```

- 프리티어 설정
> setting.json에 다음 내용 추가
> ```js
> {
>   "editor.defaultFormatter": "esbenp.prettier-vscode",
>   "editor.formatOnSave": true,
>   "[typescript]": {
>     "editor.formatOnPaste": true,
>     "editor.formatOnSave": true,
>     "editor.defaultFormatter": "esbenp.prettier-vscode"
>   },
>   "workbench.editor.empty.hint": "hidden"
> }
> ```
```powershell
touch .prettierrc.js
```
```js
module.exports = {
  singleQuote: true,
  semi: false,
}
```
> n행에 다음 코드를 추가하면 n+1행에는 프리티어가 동작 안함
> ```typescript
> // prettier-ignore
> ```
> 주의 : typescript의 타입 체크를 무력화하므로 개발이 끝난 코드에 대해서만 적용

<br>

# Project
- npx : 패키지의 최신버전 찾아내 `npm i -g`로 설치
```powershell
npx create-react-app new_project --template typescript
cd new_project
```
- 실행
```powershell
npm run start
npm run build
```
- serve 설치
```
npm install -g serve
serve -s build
```
> Ctrl+C로 동작 중인 서버 중지

- 코드 공유 시 node_modules 디렉터리, package-lock.json 파일 삭제
```powershell
rm -r force node_modules
rm package-lock.json
```
