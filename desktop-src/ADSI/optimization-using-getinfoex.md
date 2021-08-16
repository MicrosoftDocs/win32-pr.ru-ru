---
title: Оптимизация с помощью Жетинфоекс
description: Используется для загрузки конкретных значений атрибутов в локальный кэш из базовой службы каталогов.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Оптимизация с помощью Жетинфоекс ADSI
- Жетинфоекс ADSI, оптимизация с помощью IADs Жетинфоекс
- ADSI ADSI, использование, оптимизация с помощью метода IADs Жетинфоекс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4daf75fa3961a57996d6ae51d237d27835213a25a20c52452b5896c6224964a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838998"
---
# <a name="optimization-using-getinfoex"></a>Оптимизация с помощью Жетинфоекс

Метод [**iAds. жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) используется для загрузки конкретных значений атрибутов в локальный кэш из базовой службы каталогов. Этот метод загружает указанные значения атрибутов в локальный кэш. Метод [**iAds.**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) OutAttribute используется для загрузки всех значений атрибутов в локальный кэш.

Метод [**iAds. жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) получает конкретные текущие значения свойств объекта Active Directory из базового хранилища каталога, обновляя кэшированные значения.

Если значение уже существует в кэше свойств, то при вызове метода [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) или [**iAds. жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) без предварительного вызова функции [**iAds. жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) для этого атрибута будет получено кэшированное значение, а не самое последнее значение из базового каталога. Это может привести к перезаписанию обновленных значений атрибутов, если локальный кэш был изменен, но значения не были зафиксированы в базовой службе каталогов с помощью вызова метода [**iAds. сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . Предлагаемый метод предотвращения проблем с кэшированием заключается в том, чтобы всегда фиксировать изменения значений атрибутов путем вызова метода **iAds. сетинфо** перед вызовом метода [**iAds. info**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a>Получение Active Directory сконструированных атрибутов

В Active Directory большинство сконструированных атрибутов извлекается и кэшируется при вызове метода [**iAds. info**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ([**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) выполняет неявный вызов **iAds.-info** , если кэш пуст). Однако некоторые сконструированные атрибуты не извлекаются автоматически и не кэшируются, поэтому для их извлечения требуется явно вызывать метод [**iAds. жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) . Например, в Active Directory атрибут [**каноникалнаме**](/windows/desktop/ADSchema/a-canonicalname) не извлекается при вызове метода **iAds.** , а метод **iAds. Get** возвратит **\_ свойство E ADS \_ \_ не \_ Найдено**. Для получения атрибута **каноникалнаме** необходимо вызвать метод **iAds. жетинфоекс** . Эти же сконструированные атрибуты также не будут извлекаться с помощью интерфейса [**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) для перечисления атрибутов.

Дополнительные сведения и пример кода, демонстрирующий получение всех значений атрибутов, см. в разделе [пример кода для чтения сконструированного атрибута](example-code-for-reading-a-constructed-attribute.md).

 

 