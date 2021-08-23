---
description: '\_Класс ЦП хвконфиг является классом типа событий для событий конфигурации ЦП. Следующий синтаксис упрощен из MOF-кода.'
ms.assetid: a94714c6-009c-4300-a0a0-b7b3ce94f91e
title: Класс HWConfig_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_CPU
- HWConfig_CPU.MHz
- HWConfig_CPU.NumberOfProcessors
- HWConfig_CPU.MemSize
- HWConfig_CPU.PageSize
- HWConfig_CPU.AllocationGranularity
- HWConfig_CPU.ComputerName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9987095c8c2a1e9b9abbb54eb66816277428e2296c98395d36340297cc541bfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070194"
---
# <a name="hwconfig_cpu-class"></a>\_Класс ЦП хвконфиг

Класс **\_ ЦП хвконфиг** является классом типа событий для событий конфигурации ЦП.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(10), EventTypeName("CPU")]
class HWConfig_CPU : HWConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  string ComputerName;
};
```

## <a name="members"></a>Члены

Класс **\_ ЦП хвконфиг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ ЦП хвконфиг** имеет следующие свойства.

<dl> <dt>

аллокатионгрануларити
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5)
</dt> </dl>

Степень гранулярности, с которой выделяется виртуальная память.

</dd> <dt>

ИмяКомпьютера
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (6), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Имя компьютера.

</dd> <dt>

мемсизе
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Общий объем физической памяти, доступной операционной системе.

</dd> <dt>

Частоты
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1)
</dt> </dl>

Максимальная скорость процессора в мегагерцах.

</dd> <dt>

NumberOfProcessors
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2)
</dt> </dl>

Количество процессоров на компьютере.

</dd> <dt>

PageSize
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4)
</dt> </dl>

Размер страницы переключения в байтах.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                   |



## <a name="see-also"></a>См. также

<dl> <dt>

[**хвконфиг**](hwconfig.md)
</dt> </dl>

 

 




