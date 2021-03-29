---
title: Изменение объекта ADSI из ADO
description: ADSI для Windows 2000 и клиент DS включают в себя поставщик OLE DB только для чтения. Это означает, что вы не можете в настоящее время выполнить инструкцию UPDATE в диалекте SQL.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Изменение объекта ADSI из ADO ADSI
- Интерфейс ADSI объектов данных ActiveX, изменение объекта ADSI из ADO
- ADSI ADSI, пример кода C/C++, изменение объекта ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7291088915a537231077e1d75161b57684caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772944"
---
# <a name="modifying-an-adsi-object-from-ado"></a>Изменение объекта ADSI из ADO

ADSI для Windows 2000 и клиент DS включают в себя поставщик OLE DB только для чтения. Это означает, что вы не можете в настоящее время выполнить инструкцию UPDATE в диалекте SQL.

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



 

 




