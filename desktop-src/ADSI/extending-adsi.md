---
title: Расширение интерфейсов ADSI
description: С помощью модели расширения ADSI можно связать класс каталога с собственным COM-объектом.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e9f5bd316fc4703cf522e2c5facfd6c32c5236da191668f6ba38ae6a904f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428457"
---
# <a name="extending-adsi"></a>Расширение интерфейсов ADSI

С помощью модели расширения ADSI можно связать класс каталога с собственным COM-объектом. С точки зрения программиста ADSI или модуля записи сценариев расширение станет неотъемлемой частью ADSI. например, когда новый сотрудник присоединяется к Fabrikam, администратор Windows NT создаст объект пользователя в каталоге, и администратору заработной платы потребуется настроить некоторые записи в системах отдела кадров для этого пользователя. С расширением ADSI этот процесс можно упростить, используя один сценарий.


```VB
Dim usr
Dim sUserName

On Error Resume Next

sUserName = InputBox ("Enter the name of the user to add:")

Set usr = ou.Create("user", "CN=" & sUserName)

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

// Insert code to set some attributes

usr.SetInfo

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

usr.AddToPayroll  'this is a custom method from an ADSI Extension

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

Debug.Print "User: " & usr.Name & "has been created"
```



Дополнительные сведения см. в разделе [расширения ADSI](adsi-extensions.md).

 

 




