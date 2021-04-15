---
description: Свойство Таблеперсистент объекта Database возвращает состояние сохраняемости таблицы как один из следующих параметров.
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: Свойство Database. Таблеперсистент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669349"
---
# <a name="databasetablepersistent-property"></a>Свойство Database. Таблеперсистент

Свойство **таблеперсистент** объекта [**Database**](database-object.md) возвращает состояние сохраняемости таблицы как один из следующих параметров.



| Состояние таблицы               | Значение | Описание                    |
|---------------------------|-------|--------------------------------|
| мсиевалуатекондитионфалсе | 0     | Таблица является временной.            |
| мсиевалуатекондитионтруе  | 1     | Таблица является постоянной.           |
| мсиевалуатекондитионноне  | 2     | Таблица отсутствует в базе данных.  |
| мсиевалуатекондитионеррор | 3     | Имя таблицы недопустимо или отсутствует. |



 

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a>Значение свойства

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




