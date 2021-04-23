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
# <a name="the-get-method"></a><span data-ttu-id="311e3-105">Метод Get</span><span class="sxs-lookup"><span data-stu-id="311e3-105">The Get Method</span></span>

<span data-ttu-id="311e3-106">Метод [**iAds:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) используется для получения отдельных именованных атрибутов из объекта каталога.</span><span class="sxs-lookup"><span data-stu-id="311e3-106">The [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method is used to retrieve individual named attributes from a directory object.</span></span>

<span data-ttu-id="311e3-107">В следующем примере кода метод [**iAds:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) используется для получения именованного атрибута из объекта.</span><span class="sxs-lookup"><span data-stu-id="311e3-107">The following code example uses the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method to retrieve a named attribute from an object.</span></span>


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



<span data-ttu-id="311e3-108">В языках автоматизации доступ к именованным атрибутам также можно получить напрямую с помощью точечной нотации.</span><span class="sxs-lookup"><span data-stu-id="311e3-108">In Automation languages, named attributes can also be accessed directly using the dot notation.</span></span> <span data-ttu-id="311e3-109">Например, **Object. Get ("distinguishedName")** идентичен **объекту Object. distinguishedName**.</span><span class="sxs-lookup"><span data-stu-id="311e3-109">For example, **object.Get("distinguishedName")** is identical to **object.distinguishedName**.</span></span>

<span data-ttu-id="311e3-110">Следующий пример кода идентичен предыдущему примеру за исключением того, что доступ к атрибуту **distinguishedName** осуществляется с помощью точечной нотации.</span><span class="sxs-lookup"><span data-stu-id="311e3-110">The following code example is identical to the previous example except that the **distinguishedName** attribute is accessed using the dot notation.</span></span>


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



<span data-ttu-id="311e3-111">Если для объекта не задано значение, метод [**iAds:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) возвратит ошибку "свойство не найдено в кэше".</span><span class="sxs-lookup"><span data-stu-id="311e3-111">If a value is not set on the object, the [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) method will return the error "Property not found in cache".</span></span>

 

 




