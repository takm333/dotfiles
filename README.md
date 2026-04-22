# dotfiles
リポジトリのルートで実行してください。

```powershell
git clone https://github.com/takm333/dotfiles.git
cd dotfiles
```

## VSCode設定の復元手順

### 1. settings.jsonのコピー

**Windows**
```powershell
copy vscode\settings.json %APPDATA%\Code\User\settings.json
```

**Mac**
```bash
cp vscode/settings.json ~/Library/Application\ Support/Code/User/settings.json
```

---

### 2. 拡張機能の一括インストール

**Windows（PowerShell）**
```powershell
Get-Content vscode\vscode-extensions.txt | ForEach-Object { code --install-extension $_ }
```

**Mac / Linux**
```bash
cat vscode/vscode-extensions.txt | xargs -L 1 code --install-extension
```
