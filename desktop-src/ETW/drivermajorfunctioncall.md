---
description: Этот класс является классом типа события для событий вызова основной функции драйвера. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: Класс Дривермажорфунктионкалл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: b69012ae3d9dd46d2dd54c3859895288b9113fa89c772172e3f66a730b058d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070244"
---
# <a name="drivermajorfunctioncall-class"></a>Класс Дривермажорфунктионкалл

Этот класс является классом типа события для событий вызова основной функции драйвера.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Члены

Класс **дривермажорфунктионкалл** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **дривермажорфунктионкалл** имеет следующие свойства.

<dl> <dt>

**Закрыт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4), Pointer
</dt> </dl>

Сопоставьте значение этого указателя со значением указателя **FileObject** в событии [**дискио \_ TypeGroup1**](diskio-typegroup1.md) , чтобы определить тип операции ввода-вывода.

</dd> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5), Pointer
</dt> </dl>

Пакет запроса ввода-вывода.

</dd> <dt>

**мажорфунктион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1)
</dt> </dl>

Код, определяющий вызываемую основную функцию.

</dd> <dt>

**минорфунктион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2)
</dt> </dl>

Код, иденитифиес вызываемую вспомогательную функцию.

</dd> <dt>

**раутинеаддр**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3), Pointer
</dt> </dl>

Адрес вызываемой функции драйвера.

</dd> <dt>

**уникматчид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (6)
</dt> </dl>

Идентификатор, который однозначно идентифицирует запрос. Используйте этот идентификатор для сопоставления с другими событиями драйвера, например с событием [**дриверкомплетерекуест**](drivercompleterequest.md) .

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**дискио**](diskio.md)
</dt> </dl>

 

 




