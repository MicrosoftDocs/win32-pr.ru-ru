---
description: Этот класс является классом типа события для событий трассировки стека.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: Класс StackWalk_Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 672d8fc609c14a43ca2692b5cf8a46356a00cccb9c06371e515bc102706c3638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069704"
---
# <a name="stackwalk_event-class"></a>\_Класс событий стакквалк

Этот класс является классом типа события для событий трассировки стека.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a>Члены

Класс **\_ событий стакквалк** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ событий стакквалк** имеет следующие свойства.

<dl> <dt>

**евенттиместамп**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1)
</dt> </dl>

Метка времени исходного события из заголовка события. Используйте эту отметку времени, чтобы сопоставить стек с событием.

</dd> <dt>

**Stack1**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4), Pointer
</dt> </dl>

Адрес вызова.

</dd> <dt>

**Stack192**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (195), Pointer
</dt> </dl>

Адрес вызова.

</dd> <dt>

**стаккпроцесс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Format ("x")
</dt> </dl>

Идентификатор процесса исходного события.

</dd> <dt>

**стакксреад**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Идентификатор потока исходного события.

</dd> </dl>

## <a name="remarks"></a>Remarks

Обратите внимание, что в классе не отображаются все свойства **Stack * n***, существующие между **Stack1** и **Stack192**. Используйте размер события, чтобы определить, сколько свойств **Stack * n*** содержит допустимые адреса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



 

 




