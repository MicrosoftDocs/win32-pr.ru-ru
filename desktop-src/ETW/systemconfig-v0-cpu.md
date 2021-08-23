---
description: Класс SystemConfig_V0_CPU — этот класс является классом типа событий для событий конфигурации ЦП.
ms.assetid: 9ca77676-ff0e-4c47-ae4e-f8192376d3ca
title: Класс SystemConfig_V0_CPU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_CPU
- SystemConfig_V0_CPU.MHz
- SystemConfig_V0_CPU.NumberOfProcessors
- SystemConfig_V0_CPU.MemSize
- SystemConfig_V0_CPU.PageSize
- SystemConfig_V0_CPU.AllocationGranularity
- SystemConfig_V0_CPU.ComputerName
- SystemConfig_V0_CPU.DomainName
api_type:
- NA
api_location: ''
ms.openlocfilehash: d533eb06aca34ffdb5996bb0c08c7d40645042e7ccab7645cfd3a04adf0db2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069664"
---
# <a name="systemconfig_v0_cpu-class"></a>\_ \_ Класс ЦП системконфиг v0

Этот класс является классом типа событий для событий конфигурации ЦП.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(10), EventTypeName("CPU")]
class SystemConfig_V0_CPU : SystemConfig_V0
{
  uint32 MHz;
  uint32 NumberOfProcessors;
  uint32 MemSize;
  uint32 PageSize;
  uint32 AllocationGranularity;
  char16 ComputerName[];
  char16 DomainName[];
};
```

## <a name="members"></a>Члены

Класс **\_ \_ ЦП системконфиг v0** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ ЦП системконфиг v0** имеет следующие свойства.

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

Квалификаторы: **вмидатаид** (6), **Max** (256)
</dt> </dl>

Имя компьютера.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Тип данных: массив **Char16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмидатаид** (7), **Max** (132)
</dt> </dl>

Имя домена, членом которого является компьютер.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Системконфиг \_ v0**](systemconfig-v0.md)
</dt> </dl>

 

 




