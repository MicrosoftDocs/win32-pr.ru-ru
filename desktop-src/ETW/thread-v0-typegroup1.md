---
description: Этот класс является классом типа событий для событий потока. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: cc668fef-48fe-4948-8fe5-4351f7a033d1
title: Класс Thread_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V0_TypeGroup1
- Thread_V0_TypeGroup1.TThreadId
- Thread_V0_TypeGroup1.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 334d3a2cb9560a4968cbbfa8419d44e7c8be8ff836ccf95b6fce819ee77a9900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069484"
---
# <a name="thread_v0_typegroup1-class"></a>\_Класс Thread v0 \_ TypeGroup1

Этот класс является классом типа событий для событий потока.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Thread_V0_TypeGroup1 : Thread_V0
{
  uint32 TThreadId;
  uint32 ProcessId;
};
```

## <a name="members"></a>Члены

Класс **Thread \_ v0 \_ TypeGroup1** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Thread \_ v0 \_ TypeGroup1** имеет следующие свойства.

<dl> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Format ("x")
</dt> </dl>

Идентификатор процесса потока, участвующего в событии.

</dd> <dt>

тсреадид
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Format ("x")
</dt> </dl>

Идентификатор потока, участвующего в событии.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_V0 потока**](thread-v0.md)
</dt> </dl>

 

 




