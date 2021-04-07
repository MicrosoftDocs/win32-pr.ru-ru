---
title: Метод Путекс
description: Метод IADs Путекс использует имя свойства для сохранения свойства с одним или несколькими значениями в кэше свойств.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- Путекс ADSI, сведения
- ADSI ADSI, пример кода Visual Basic, использование метода Путекс
- свойства ADSI, сохранение одного или нескольких значений свойства в кэше свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea698c2dd14f3ddf8f3ad97459fad598006db22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887476"
---
# <a name="the-putex-method"></a>Метод Путекс

Метод [**iAds::P утекс**](/windows/desktop/api/Iads/nf-iads-iads-putex) использует имя свойства для сохранения свойства с одним или несколькими значениями в кэше свойств. Это перезаписывает все значения, находящиеся в кэше свойств. Значения в кэше не записываются в базовую службу каталогов до тех пор, пока не будет вызвано значение [**iAds:: сетинфо**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . Первый аргумент **путекс** указывает, нужно ли заменить или добавить к любому существующему значению для свойства. В следующем примере любые существующие значения атрибута **Description** удаляются в кэше при вызове **путекс** и удаляются на сервере при вызове **сетинфо** .


```VB
Dim x As IADs
Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
'----------------------------------------------
' Assume the otherHomePhoneNumber has the following values:
' 111-1111, 222-2222
'----------------------------------------------
x.PutEx ADS_PROPERTY_APPEND, "OtherhomePhone", Array("333-3333" )  
x.SetInfo              'Now the values are 111-1111,222-222,333-3333.
 
x.PutEx ADS_PROPERTY_DELETE, "OtherHomePhone", Array("111-1111", "222-2222")
x.SetInfo              'Now the values are 333-3333.
x.PutEx ADS_PROPERTY_UPDATE, "OtherHomePhone", Array("888-8888", "999-9999")
x.SetInfo              'Now the values are 888-8888,999-9999.
x.PutEx ADS_PROPERTY_CLEAR, "OtherHomePhone",  vbNull
x.SetInfo              'Now the property has no value.
```



 

 




