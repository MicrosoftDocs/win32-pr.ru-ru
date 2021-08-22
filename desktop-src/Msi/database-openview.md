---
description: метод OpenView объекта Database возвращает объект представления, представляющий запрос, заданный SQL строкой.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Метод Database. OpenView (Цертвиев. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ccc37b72dd44064172672d1067dae293da30048853f3ca83f82fb50b0a90cfaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947527"
---
# <a name="databaseopenview-method"></a>Database. OpenView, метод

метод **OpenView** объекта [**Database**](database-object.md) возвращает объект [**представления**](view-object.md) , представляющий запрос, заданный SQL строкой.

## <a name="syntax"></a>Синтаксис


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*sql* 
</dt> <dd>

обязательный SQL строки запроса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

сведения о синтаксисе SQL, реализованном в установщике, см. в разделе [синтаксис SQL](sql-syntax.md).

В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| Заголовок<br/>  | <dl> <dt>Цертвиев. h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>См. также

<dl> <dt>

[**База данных**](database-object.md)
</dt> <dt>

[Синтаксис SQL](sql-syntax.md)
</dt> </dl>

 

 




