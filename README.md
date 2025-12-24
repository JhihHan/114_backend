# 網頁程式設計fastapi
> ssh private/public key
```bash
ssh-keygen -t ed25519 -C "xx@gmail.com"
```
> Python virtual environment 
```bash
python -m venv venv
.\venv\Scripts\activate
python -m pip install --upgrade pip
```
Package import/export
```bash
# filename can change
pip freeze > requirements.txt
pip install -r requirements.txt
```
> Change Execution Policy
```bash
.\venv\Scripts\activate : 因為這個系統上已停用指令碼執行，所以無法載入 C:\Users\USER\Documents\114_backend\venv\Scr
ipts\Activate.ps1 檔案。如需詳細資訊，請參閱 about_Execution_Policies，網址為 https:/go.microsoft.com/fwlink/?LinkI
D=135170。
位於 線路:1 字元:1
+ .\venv\Scripts\activate
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : SecurityError: (:) [], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess
```
```bash
Get-ExecutionPolicy
# select one
Set-ExecutionPolicy RemoteSigned
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
# Revert default
Set-ExecutionPolicy Restricted
```
> FastAPI download with start
```bash
pip install "fastapi[standard]"
fastapi dev main.py

uvicorn app.main:app --reload
```
> Exit venv
```bash
deactivate
```
