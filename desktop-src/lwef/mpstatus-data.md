---
title: Структура MPSTATUS_DATA (Мпклиент. h)
description: Содержит данные о текущем состоянии компонента продукта.
ms.assetid: 6AEF485C-30D1-47DB-92B6-048B8CAA7833
keywords:
- MPSTATUS_DATA структуры устаревшие функции среды Windows
- функции PMPSTATUS_DATA Windows указателя структур в устаревшей среде
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
ms.openlocfilehash: 78989b055e6de79c3da733ff8bc498a3fb6717c5dec226db73b80c4e5c9d899c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887914"
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

**PA**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

Когда **ComponentID**  ==  **мпкомпонент \_ NIS**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> <dt>

**ПБ**
</dt> <dd>

Тип: **пмпстатус \_ датаекс не \_ используется**

</dd> <dd>

Когда **ComponentID**  ==  **мпкомпонент \_ ELAM**. См. раздел [**мпстатус \_ датаекс не \_ используется**](mpstatus-dataex-unused.md).

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_идентификатор мпкомпонент**](mpcomponent-id.md)
</dt> <dt>

[**МПСТАТУС \_ датаекс не \_ используется**](mpstatus-dataex-unused.md)
</dt> </dl>

 

 





