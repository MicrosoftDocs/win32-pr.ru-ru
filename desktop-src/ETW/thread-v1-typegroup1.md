---
description: Этот класс является классом типа события для событий запуска потока. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Класс Thread_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 90d8f4afe9d78cc774dea3159a728ccc6d4db52314e692594d026f7e4fe2161c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069444"
---
# <a name="thread_v1_typegroup1-class"></a>\_ \_ Класс TypeGroup1 потока v1

Этот класс является классом типа события для событий запуска потока.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a>Члены

Класс **Thread \_ v1 \_ TypeGroup1** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Thread \_ v1 \_ TypeGroup1** имеет следующие свойства.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1)
</dt> </dl>

Идентификатор процесса потока, участвующего в событии.

**Windows Server 2003:** Содержит квалификатор формата ("x").

</dd> <dt>

стаккбасе
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3), Pointer
</dt> </dl>

Базовый адрес стека потока.

</dd> <dt>

стакклимит
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4), Pointer
</dt> </dl>

Ограничение стека потока.

</dd> <dt>

стартаддр
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (7), Pointer
</dt> </dl>

Адрес памяти, с которого начинается трассировка.

</dd> <dt>

тсреадид
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2)
</dt> </dl>

Идентификатор потока, участвующего в событии.

**Windows Server 2003:** Содержит квалификатор формата ("x").

</dd> <dt>

усерстаккбасе
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5), Pointer
</dt> </dl>

Базовый адрес стека пользовательского режима потока.

</dd> <dt>

усерстакклимит
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (6), Pointer
</dt> </dl>

Ограничение стека пользовательского режима потока.

</dd> <dt>

ваитмоде
</dt> <dd> <dl> <dt>

Тип данных: **sint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (9), Format ("c")
</dt> </dl>

Не используется.

</dd> <dt>

Win32StartAddr
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (8), Pointer
</dt> </dl>

Начальный адрес функции, которая будет выполнена этим потоком.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Поток \_ v1**](thread-v1.md)
</dt> </dl>

 

 




