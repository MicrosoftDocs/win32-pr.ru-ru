---
title: начало работы со сценариями для ADSI
description: Сценарии удобно использовать для системных администраторов, желающих создавать пакетные скрипты для часто используемых задач.
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- начало работы со сценариями для ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a83da0194fb03cdb31430f389dbfbf64327806b1b142be3b9c1c5813696548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839957"
---
# <a name="getting-started-with-scripting-for-adsi"></a>начало работы со сценариями для ADSI

Сценарии удобно использовать для системных администраторов, желающих создавать пакетные скрипты для часто используемых задач.

для запуска сценариев с помощью ADSI необходимо иметь компьютер, на котором работает Windows или входить в домен, содержащий данные для учетных записей компьютеров в каталоге.

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a>Простой пример создания сценариев: Поиск имен и расположения учетных записей компьютеров

Создайте новый текстовый файл с помощью текстового редактора. В следующем примере кода показано, как найти имена и расположения учетных записей компьютеров.


```VB
'---------------------------------------------------------------
' Returns the name and location for all the computer accounts in 
' Active Directory.
'--------------------------------------------------------------- 
Const ADS_SCOPE_SUBTREE = 2
Set objConnection = CreateObject("ADODB.Connection")
Set objCommand =   CreateObject("ADODB.Command")
objConnection.Provider = "ADsDSOObject"
objConnection.Open "Active Directory Provider"
Set objCommand.ActiveConnection = objConnection
objCommand.CommandText = "Select Name, Location from 'LDAP://DC=fabrikam,DC=com' " & "where objectClass='computer'"  
objCommand.Properties("Page Size") = 1000
objCommand.Properties("Timeout") = 30 
objCommand.Properties("Searchscope") = ADS_SCOPE_SUBTREE 
objCommand.Properties("Cache Results") = False 
Set objRecordSet = objCommand.Execute
objRecordSet.MoveFirst
Do Until objRecordSet.EOF
    Wscript.Echo "Computer Name: " & objRecordSet.Fields("Name").Value
    Wscript.Echo "Location: " & objRecordSet.Fields("Location").Value
    objRecordSet.MoveNext
Loop
```



Сохраните файл как First.vbs. Измените строку, которая начинается с "Обжкомманд. CommandText", чтобы изменить путь к домену. в командной строке введите **cscript First.vbs** для командной строки или First.vbs для Windows сценариев. Результаты должны возвращаться в командной строке.

Дополнительные сведения о скриптах для ADSI см. в разделе [Active Directorying Service Interfaces Scripting](adsi-scripting-tutorial.md).

 

 




