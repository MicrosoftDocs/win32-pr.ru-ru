---
description: Свойство Item является свойством, предназначенным только для чтения и возвращающим строку в коллекции объектов Стринглист.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: Стринглист. Item, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 85962aac5e841c929518a7a37fdada647ce4c74baa69be23048f26f5470c91fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142022"
---
# <a name="stringlistitem-property"></a>Стринглист. Item, свойство

Свойство **Item** является свойством, предназначенным только для чтения и возвращающим строку в коллекции [**объектов стринглист**](stringlist-object.md) .

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>Значение свойства

Номер индекса элемента с коллекцией строк. Это обязательный параметр.

## <a name="remarks"></a>Remarks

Клиент должен убедиться, что [**объект стринглист**](stringlist-object.md) существует и не пуст, прежде чем ссылаться на свойство **Item** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ истринглист определен как 000C1095-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




