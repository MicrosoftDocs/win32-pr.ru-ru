---
description: Этот класс является классом типа события для виртуальных событий выделения. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 037d33e0-da94-4834-bc02-814c1cae1d8d
title: Класс PageFault_VirtualAlloc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_VirtualAlloc
- PageFault_VirtualAlloc.BaseAddress
- PageFault_VirtualAlloc.RegionSize
- PageFault_VirtualAlloc.ProcessId
- PageFault_VirtualAlloc.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: fa3dd8eb53e9c1a79cf38edde0d9c4dba93ea85b0994bfb316b97064f211f26e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927574"
---
# <a name="pagefault_virtualalloc-class"></a>\_Класс PageFault VirtualAlloc

Этот класс является классом типа события для виртуальных событий выделения.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{98, 99}, EventTypeName{"VirtualAlloc", "VirtualFree"}]
class PageFault_VirtualAlloc : PageFault_V2
{
  uint32 BaseAddress;
  object RegionSize;
  uint32 ProcessId;
  uint32 Flags;
};
```

## <a name="members"></a>Члены

Класс **PageFault \_ VirtualAlloc** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **PageFault \_ VirtualAlloc** имеет следующие свойства.

<dl> <dt>

**BaseAddress**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Pointer
</dt> </dl>

Начальный адрес, с которого была выделена или освобождена память.

</dd> <dt>

**Флаги**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4), Format ("x")
</dt> </dl>

Тип выполнения выделения памяти. Возможные значения см. в описании параметра *флаллокатионтипе* функции [**виртуалаллоцекс**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) .

</dd> <dt>

**Идентификатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Процесс, который владеет памятью (может отличаться от потока, выполнившего выделение).

</dd> <dt>

**регионсизе**
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), расширение ("size")
</dt> </dl>

Размер выделенной или освобожденной памяти в байтах.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**PageFault \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 
