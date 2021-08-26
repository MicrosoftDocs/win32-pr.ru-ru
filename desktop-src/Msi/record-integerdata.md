---
description: Это свойство IntegerData объекта Record. Это свойство, доступное для чтения и записи, передает 32-разрядные целочисленные данные в указанное поле в записи или из него. Если значение поля не может быть преобразовано в целое число, возвращается Мсидатабасенуллинтежер.
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: Свойство Record. IntegerData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3593f31d8f8cea6278346e8c99bb9c9b880aed273ae7ab70614ade112cd8c8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912924"
---
# <a name="recordintegerdata-property"></a>Свойство Record. IntegerData

Это свойство **IntegerData** объекта [**Record**](record-object.md) . Это свойство, доступное для чтения и записи, передает 32-разрядные целочисленные данные в указанное поле в записи или из него. Если значение поля не может быть преобразовано в целое число, возвращается Мсидатабасенуллинтежер.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a>Значение свойства

Обязательный номер поля значения в записи, 1.

## <a name="remarks"></a>Remarks

Чтобы задать для поля записи целое значение null, используйте Мсидатабасенуллинтежер. Возвращенное значение несуществующего поля — Мсидатабасенуллинтежер. Попытка сохранить значение в несуществующем поле приводит к ошибке.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ирекорд определен как 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




