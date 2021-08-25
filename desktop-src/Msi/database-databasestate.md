---
description: Свойство Датабасестате объекта Database доступно только для чтения.
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: Свойство Database. Датабасестате
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a44fcc9e082878077533edafcd44c9f5a5f26e76bddd3ddb5619fb2842ec0d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745644"
---
# <a name="databasedatabasestate-property"></a>Свойство Database. Датабасестате

Свойство **датабасестате** объекта [**Database**](database-object.md) доступно только для чтения.

Это свойство возвращает состояние сохраняемости базы данных в виде одного из следующих параметров.



| Состояние базы данных        | Значение | Описание                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| мсидатабасестатереад  | 0     | База данных открывается только для чтения. Изменения постоянных данных не разрешены, а временные данные не сохраняются. |
| мсидатабасестатеврите | 1     | База данных полностью работоспособна для чтения и записи.                                                          |



 

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a>Значение свойства

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




