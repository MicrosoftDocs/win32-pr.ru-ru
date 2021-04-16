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
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652105"
---
# <a name="stringlistitem-property"></a>Стринглист. Item, свойство

Свойство **Item** является свойством, предназначенным только для чтения и возвращающим строку в коллекции [**объектов стринглист**](stringlist-object.md) .

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>Значение свойства

Номер индекса элемента с коллекцией строк. Этот параметр обязателен.

## <a name="remarks"></a>Комментарии

Клиент должен убедиться, что [**объект стринглист**](stringlist-object.md) существует и не пуст, прежде чем ссылаться на свойство **Item** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ истринглист определен как 000C1095-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




