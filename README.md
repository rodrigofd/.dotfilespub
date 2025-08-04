# .dotfilespub

## Scoop CLI

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```
## Installed apps

[See the list](installed-apps.md)

As an examnple this command will install VS 2022 Community with the desktop C++ workload.

```powershell
winget install Microsoft.VisualStudio.2022.Community --silent --override "--wait --quiet --add ProductLang En-us --add Microsoft.VisualStudio.Workload.NativeDesktop --includeRecommended"
```

> Note that the above command uses --includeRecommended. You need to specify that to get all of the recmommended components with the workload, if you do not specify that the workload may not be functional. You can also specify --includeOptional which will additionally pull in everything in the workload. Of course you can use additional --add to include specific components in the workload.
