---
description: Метод OpenView объекта Database возвращает объект представления, представляющий запрос, заданный строкой SQL.
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
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652255"
---
# <a name="databaseopenview-method"></a>Database. OpenView, метод

Метод **OpenView** объекта [**Database**](database-object.md) возвращает объект [**представления**](view-object.md) , представляющий запрос, заданный строкой SQL.

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

Обязательная строка запроса SQL.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Сведения о синтаксисе SQL, реализованном в установщике, см. в разделе [синтаксис SQL](sql-syntax.md).

В случае сбоя метода можно получить расширенные сведения об ошибке с помощью метода [**ластерроррекорд**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| Header<br/>  | <dl> <dt>Цертвиев. h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ идатабасе определяется как 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**База данных**](database-object.md)
</dt> <dt>

[Синтаксис SQL](sql-syntax.md)
</dt> </dl>

 

 




