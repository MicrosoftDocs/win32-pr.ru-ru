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
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985701"
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

## <a name="members"></a>Участники

Класс **\_ событий стакквалк** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ событий стакквалк** имеет следующие свойства.

<dl> <dt>

**EventTimeStamp**
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

## <a name="remarks"></a>Примечания

Обратите внимание, что в классе не отображаются все свойства **Stack * n***, существующие между **Stack1** и **Stack192**. Используйте размер события, чтобы определить, сколько свойств **Stack * n*** содержит допустимые адреса.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



 

 




