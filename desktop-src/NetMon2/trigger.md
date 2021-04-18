---
description: Структура ТРИГГЕРа указывает действие, выполняемое драйвером в указанное время.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Структура ТРИГГЕРа (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674113"
---
# <a name="trigger-structure"></a>Структура ТРИГГЕРа

Структура **триггера** указывает действие, выполняемое драйвером в указанное время.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a>Члены

<dl> <dt>

**тригжерактиве**
</dt> <dd>

Логическое значение, определяющее, должен ли триггер уделять внимание драйверу.

</dd> <dt>

**TriggerType может принимать**
</dt> <dd>

Код Op триггера.

</dd> <dt>

**TriggerAction**
</dt> <dd>

Действие, выполняемое триггером при срабатывании.

</dd> <dt>

**тригжерфлагс**
</dt> <dd>

Флаги триггера.

</dd> <dt>

**тригжерпаттернматч**
</dt> <dd>

Сопоставление шаблона триггера.

</dd> <dt>

**тригжербуфферсизе**
</dt> <dd>

Размер буфера триггера.

</dd> <dt>

**Reserved**
</dt> <dd>

Зарезервировано.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




