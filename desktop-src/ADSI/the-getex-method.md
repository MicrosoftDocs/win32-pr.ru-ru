---
title: Метод Жетекс
description: Некоторые атрибуты могут хранить одно или несколько значений.
ms.assetid: aaa5fa90-7e60-4668-bd23-1475c2e4d184
ms.tgt_platform: multiple
keywords:
- Жетекс ADSI, использование функции IADs Жетекс
- ADSI ADSI с использованием с помощью метода IADs Жетекс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e656bd6a48830feb725e927f08be1d573e7b0232cf02c16ee87bd7d6a5b2f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690153"
---
# <a name="the-getex-method"></a>Метод Жетекс

Некоторые атрибуты могут хранить одно или несколько значений. Например, атрибут **осертелефоне** объекта пользователя в Active Directory является свойством, которое может иметь ноль, одно или несколько значений. Атрибуты, имеющие несколько значений, называются атрибутами с несколькими значениями. Если метод [**iAds:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) используется для получения атрибута с несколькими значениями, результаты должны обрабатываться иначе, чем если бы атрибут состоять из одного значения. Однако результаты, предоставляемые методом [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) , обрабатываются одинаковым образом независимо от того, имеет ли атрибут одно или несколько значений. В обоих случаях метод **iAds:: жетекс** возвращает значения в массиве.

Метод [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) извлекает свойства из кэша свойств. Если указанное свойство не найдено в кэше, метод **iAds:: жетекс** выполняет неявный вызов метода [**iAds::-info**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .

Метод [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) возвращает массив вариантов типа Variant, независимо от числа возвращаемых сервером значений. Это справедливо, даже если атрибут содержит только одно значение.


```VB
Dim usr As IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
homePhones = usr.GetEx("otherHomePhone")
For each phone in homePhones
    Debug.Print phone
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



Метод [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) можно также использовать для атрибутов с одним значением. Результаты атрибута с одним значением обрабатываются так же, как и результаты для атрибута с несколькими значениями.


```VB
Dim usr as IADs
On Error GoTo Cleanup

Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
sds = usr.GetEx("ntSecurityDescriptor")
For each sd in sds
    Set acl = sd.DiscretionaryACL
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



Если для атрибута не задано значение, функция [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) возвращает ошибку "свойство не найдено в кэше".

 

 




