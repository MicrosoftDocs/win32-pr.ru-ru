---
description: Свойство Примарикэйс объекта Database возвращает объект Record, содержащий имя таблицы в поле 0, и имена столбцов (содержащие первичные ключи) в полях, соответствующих их номерам столбцов.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Свойство Database. Примарикэйс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669350"
---
# <a name="databaseprimarykeys-property"></a>Свойство Database. Примарикэйс

Свойство **примарикэйс** объекта [**Database**](database-object.md) возвращает объект [**Record**](record-object.md) , содержащий имя таблицы в поле 0, и имена столбцов (содержащие первичные ключи) в полях, соответствующих их номерам столбцов. Число полей в записи равно числу столбцов первичного ключа.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a>Значение свойства

Обязательное имя существующей таблицы. Если таблица не существует, возникает ошибка.

## <a name="remarks"></a>Комментарии

Свойство **примарикэйс** не может использоваться с [ \_ таблицей таблиц](-tables-table.md) или [ \_ столбцами](-columns-table.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




