---
description: Этот класс является классом типа событий для событий конфигурации ЦП.
ms.assetid: 5a24be04-9e5e-4ba9-baaf-b58b79ad947b
title: Класс SystemConfig_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_CPU
- SystemConfig_CPU.MHz
- SystemConfig_CPU.NumberOfProcessors
- SystemConfig_CPU.MemSize
- SystemConfig_CPU.PageSize
- SystemConfig_CPU.AllocationGranularity
- SystemConfig_CPU.ComputerName
- SystemConfig_CPU.DomainName
- SystemConfig_CPU.HyperThreadingFlag
api_type:
- NA
api_location: ''
ms.openlocfilehash: d08d0eeac9aa2287576bbb6dfe0e8ce41f116e8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985696"
---
# <a name="systemconfig_cpu-class"></a>\_Класс ЦП системконфиг

Этот класс является классом типа событий для событий конфигурации ЦП.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_CPU : SystemConfig
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
  uint32 HyperThreadingFlag;
};
```

## <a name="members"></a>Участники

Класс **\_ ЦП системконфиг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ ЦП системконфиг** имеет следующие свойства.

<dl> <dt>

**аллокатионгрануларити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (5)
</dt> </dl>

Степень гранулярности, с которой выделяется виртуальная память.

</dd> <dt>

**ИмяКомпьютера**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (6), **Max** (256), **Format ("s")**
</dt> </dl>

Имя компьютера.

</dd> <dt>

**Имя_домена**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (7), **Max** (132), **Format ("s")**
</dt> </dl>

Имя домена, членом которого является компьютер.

</dd> <dt>

**хиперсреадингфлаг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (8), Pointer
</dt> </dl>

Указывает, включен ли параметр Hyper-Threading для процессора. Каждый бит отражает состояние ЦП компьютера на уровне Hyper-Threading.

</dd> <dt>

**мемсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (3)
</dt> </dl>

Общий объем физической памяти, доступной операционной системе.

</dd> <dt>

**Частоты**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (1)
</dt> </dl>

Максимальная скорость процессора в мегагерцах.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (2)
</dt> </dl>

Количество процессоров на компьютере.

</dd> <dt>

**PageSize**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (4)
</dt> </dl>

Размер страницы переключения в байтах.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**системконфиг**](systemconfig.md)
</dt> </dl>

 

 




