---
title: Изменение объекта ADSI из ADO
description: ADSI для Windows 2000 и клиент DS включают в себя поставщик OLE DB только для чтения. это означает, что вы не можете в настоящее время выполнить инструкцию UPDATE в диалекте SQL.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Изменение объекта ADSI из ADO ADSI
- ActiveX объектов data adsi, изменение объекта adsi из ADO
- ADSI ADSI, пример кода C/C++, изменение объекта ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4562e67043ea168a0b158088ffe3c2772f3ae28a0a2fa8881e102574cf2eb97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839454"
---
# <a name="modifying-an-adsi-object-from-ado"></a>Изменение объекта ADSI из ADO

ADSI для Windows 2000 и клиент DS включают в себя поставщик OLE DB только для чтения. это означает, что вы не можете в настоящее время выполнить инструкцию UPDATE в диалекте SQL.

**Изменение объекта, возвращаемого запросом ADO**

1.  Запросите значение **ADsPath** при указании имени атрибута, как в «SELECT ADsPath,...».
2.  Выполните запрос и получите атрибут **ADsPath** .
3.  Выполните привязку к набору записей с помощью **ADsPath** и измените атрибуты.

В следующем примере кода показано, как изменить объект ADSI после выполнения шагов, описанных в предыдущем примере.


```VB
Dim Con As New Connection
Dim rs As New Recordset
Dim command As New Command
Dim usr As IADsUser

' Replace department for all users in OU=sales.
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
 
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = con
 
command.CommandText = "SELECT AdsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=com' WHERE objectClass = 'user'"
 
command.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Set rs = command.Execute
While Not rs.EOF
    Set usr = GetObject(rs.Fields("AdsPath").Value)
    usr.Put "department", "1001"
    usr.SetInfo
    rs.MoveNext
Wend
```



 

 




