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
ms.openlocfilehash: 99404c8e9fc48e0ab85b956dd84af39b11eb87b22c87b4f9a232bd5b72d32143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363022"
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



 

 




