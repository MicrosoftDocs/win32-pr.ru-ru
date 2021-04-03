---
title: Расширение интерфейсов ADSI
description: С помощью модели расширения ADSI можно связать класс каталога с собственным COM-объектом.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e597d4b2dd2cf6a3b4a81f1fff3515289418b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772962"
---
# <a name="extending-adsi"></a>Расширение интерфейсов ADSI

С помощью модели расширения ADSI можно связать класс каталога с собственным COM-объектом. С точки зрения программиста ADSI или модуля записи сценариев расширение станет неотъемлемой частью ADSI. Например, когда новый сотрудник присоединяется к Fabrikam, администратор Windows NT создает объект пользователя в каталоге, и администратору заработной платы потребуется настроить некоторые записи в системах отдела кадров для этого пользователя. С расширением ADSI этот процесс можно упростить, используя один сценарий.


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

 

 




