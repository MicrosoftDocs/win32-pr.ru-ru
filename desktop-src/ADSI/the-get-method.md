---
title: Метод Get
description: Метод IADs Get используется для получения отдельных именованных атрибутов из объекта каталога.
ms.assetid: e3754663-fe31-46f3-9dc1-a9c96ed53fde
ms.tgt_platform: multiple
keywords:
- Получение ADSI с помощью команды IADs Get
- ADSI ADSI, использование с помощью метода IADs Get
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11590fda2cfd207315453323fa3d0999f298103d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654096"
---
# <a name="the-get-method"></a>Метод Get

Метод [**iAds:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) используется для получения отдельных именованных атрибутов из объекта каталога.

В следующем примере кода метод [**iAds:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) используется для получения именованного атрибута из объекта.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.Get("distinguishedName")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



В языках автоматизации доступ к именованным атрибутам также можно получить напрямую с помощью точечной нотации. Например, **Object. Get ("distinguishedName")** идентичен **объекту Object. distinguishedName**.

Следующий пример кода идентичен предыдущему примеру за исключением того, что доступ к атрибуту **distinguishedName** осуществляется с помощью точечной нотации.


```VB
Dim MyUser as IADs
Dim MyDistinguishedName as String

On Error GoTo Cleanup
 
' Bind to a specific user object.
set MyUser = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
MyDistinguishedName = MyUser.distinguishedName

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set MyUser = Nothing
```



Если для объекта не задано значение, метод [**iAds:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) возвратит ошибку "свойство не найдено в кэше".

 

 




