---
title: Метод Путекс
description: Метод IADs Путекс использует имя свойства для сохранения свойства с одним или несколькими значениями в кэше свойств.
ms.assetid: fb9a0610-e955-424b-a2b9-da4986d0ba5f
ms.tgt_platform: multiple
keywords:
- Путекс ADSI, сведения
- adsi adsi, пример кода Visual Basic, использование метода путекс
- свойства ADSI, сохранение одного или нескольких значений свойства в кэше свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646c07fad5d22110d345b71a763add5483d7f0be5f6ae2c36557eb7f1563561c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023172"
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



 

 




