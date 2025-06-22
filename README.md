# Start React.js

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

