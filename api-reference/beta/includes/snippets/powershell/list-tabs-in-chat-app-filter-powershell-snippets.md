---
description: "Automatically generated file. DO NOT MODIFY"
---

```powershell

Import-Module Microsoft.Graph.Teams

Get-MgChatTab -ChatId $chatId -ExpandProperty "teamsApp" -Filter "teamsApp/id eq 'com.microsoft.teamspace.tab.web'"  -OutFile $outFileId

```