---
title: Метод info
description: Метод IADs info загружает все значения атрибутов объекта ADSI в локальный кэш из базовой службы каталогов.
ms.assetid: b29f1156-7c38-4f5a-a88c-578ae6167758
ms.tgt_platform: multiple
keywords:
- Info ADSI, использование команды IADs info
- ADSI ADSI с использованием с помощью метода IADs info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b374791e7fd7ff787c1b825827f410a9c15b551b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772908"
---
# <a name="the-getinfo-method"></a>Метод info

Метод [**iAds:: info**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) загружает все значения АТРИБУТОВ объекта ADSI в локальный кэш из базовой службы каталогов. Метод [**iAds:: жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) используется для загрузки конкретных значений атрибутов в локальный кэш. Дополнительные сведения об использовании метода **iAds:: жетинфоекс** см. в разделе [Оптимизация с помощью жетинфоекс](optimization-using-getinfoex.md).

ADSI сделает неявный вызов метода [**iAds::**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get) или [**iAds:: жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) для конкретного атрибута, и в локальном кэше значение не найдено. При вызове метода **iAds::-info** неявный вызов не повторяется. Если значение уже существует в кэше свойств, то при вызове метода **iAds:: Get** или **iAds:: жетекс** без предварительного вызова функции **iAds::-info** будет получено кэшированное значение, а не самое последнее значение из базового каталога. Это может привести к перезаписанию обновленных значений атрибутов, если локальный кэш был изменен, но значения не были зафиксированы в базовой службе каталогов с помощью вызова метода [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . Чтобы избежать проблем с кэшированием, следует зафиксировать изменения значений атрибутов, вызвав метод **iAds:: сетинфо** перед вызовом метода **iAds::** OutAttribute.


```VB
Dim usr As IADs

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' This code example assumes that the property description has a single value in the directory.
' Be aware that this will IMPLICITLY call GetInfo because at this point GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's title is " + usr.Get("title")

' Change the attribute value in the local cache.
usr.Put "title", "Vice President"
Debug.Print "User's title is " + usr.Get("title")

' Call GetInfo, which will overwrite the updated value because SetInfo has not 
' been called.
usr.GetInfo
Debug.Print "User's title is " + usr.Get("title")
```



Некоторые службы каталогов не возвращают значения атрибутов объекта в ответ на вызов метода [**iAds::**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) GetResponse. В этих случаях для загрузки этих значений в локальный кэш используйте метод [**iAds:: жетинфоекс**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) .

 

 




