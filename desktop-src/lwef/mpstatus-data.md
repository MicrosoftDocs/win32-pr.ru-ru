---
title: Структура MPSTATUS_DATA (Мпклиент. h)
description: Содержит данные о текущем состоянии компонента продукта.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- MPSTATUS_DATA структуры устаревшие функции среды Windows
- Функции PMPSTATUS_DATA указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPSTATUS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5da4ea9c8c51d8ee74d3242e5020df23f758228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802878"
---
# <a name="mpstatus_data-structure"></a>\_Структура данных мпстатус

Содержит данные о текущем состоянии компонента продукта.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPSTATUS_DATA {
  MPCOMPONENT_ID ComponentID;
  BOOL           fEnable;
  union {
    PMPSTATUS_DATAEX_UNUSED p1;
    PMPSTATUS_DATAEX_UNUSED p2;
    PMPSTATUS_DATAEX_UNUSED p3;
    PMPSTATUS_DATAEX_UNUSED p4;
    PMPSTATUS_DATAEX_UNUSED p5;
    PMPSTATUS_DATAEX_UNUSED p6;
    PMPSTATUS_DATAEX_UNUSED p7;
    PMPSTATUS_DATAEX_UNUSED p8;
    PMPSTATUS_DATAEX_UNUSED p9;
    PMPSTATUS_DATAEX_UNUSED pa;
    PMPSTATUS_DATAEX_UNUSED pb;
  } ComponentStatus;
} MPSTATUS_DATA, *PMPSTATUS_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**ComponentID**
</dt> <dd>

Тип: **[ **мпкомпонент \_ ID**](mpcomponent-id.md)**

</dd> <dd>

Конкретный идентификатор компонента, для которого сообщается состояние.

</dd> <dt>

**фенабле**
</dt> <dd>

Тип: **bool** .

</dd> <dd>

Состояние, запрошенное для компонента. **hResult** в данных обратного вызова обозначает успешность или неудачу запроса.

</dd> <dt>

**компонентстатус**
</dt> <dd>

Дополнительные данные о состоянии в зависимости от значения **ComponentID**.

> [!Note]  
> В настоящее время приводится указатель на фиктивную структуру для всех возможных значений **компонента ComponentID**.

 

<dl> <dt>

**ниже**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

Когда **ComponentID**  ==  **мпкомпонент \_ в качестве \_ сигнатуры**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> <dt>

**–**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

При   ==  **\_ \_ сигнатуре ComponentID мпкомпонент AV**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> <dt>

**–**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

При   ==  **\_ \_ мониторе ComponentID мпкомпонент в режиме реального времени**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> <dt>

**P4**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

Когда **ComponentID**  ==  **мпкомпонент \_ \_ защиты доступа**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> <dt>

**P5**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

Когда **ComponentID**  ==  **мпкомпонент \_ защиту ioav \_ Protection**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> <dt>

**архитектур**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

При   ==  **\_ \_ мониторе поведения ComponentID мпкомпонент**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> <dt>

**P7**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

При   ==  **\_ автоматическом \_ сканировании ComponentID мпкомпонент**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> <dt>

**P8**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

Когда **ComponentID**  ==  **мпкомпонент \_ Auto \_ сигупдате**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> <dt>

**P9**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

Когда **ComponentID**  ==  **мпкомпонент \_ IPC**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> <dt>

**pa**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

Когда **ComponentID**  ==  **мпкомпонент \_ NIS**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> <dt>

**МС**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

Когда **ComponentID**  ==  **мпкомпонент \_ ELAM**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_идентификатор мпкомпонент**](mpcomponent-id.md)
</dt> <dt>

[**МПСТАТУС \_ датаекс не \_ используется**](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





