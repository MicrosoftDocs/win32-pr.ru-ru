---
description: Этот класс является классом типа события для выполнения подпрограмм драйвера. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: Класс Дриверкомплетионраутине
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac1329c60f38ebfb4597b85ec251e074babd2c1fde7e58fee2423b6a11be92f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814892"
---
# <a name="drivercompletionroutine-class"></a>Класс Дриверкомплетионраутине

Этот класс является классом типа события для выполнения подпрограмм драйвера.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Члены

Класс **дриверкомплетионраутине** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **дриверкомплетионраутине** имеет следующие свойства.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Pointer
</dt> </dl>

Пакет запроса ввода-вывода.

</dd> <dt>

**Подпрограмма**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Pointer
</dt> </dl>

Адрес вызываемой функции драйвера.

</dd> <dt>

**уникматчид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Идентификатор, который однозначно идентифицирует запрос. Используйте этот идентификатор для сопоставления с другими событиями драйвера, например с событием [**дриверкомплетерекуест**](drivercompleterequest.md) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дискио**](diskio.md)
</dt> </dl>

 

 




