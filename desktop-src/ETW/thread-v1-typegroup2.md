---
description: Этот класс является классом типа события для событий конца потока. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: c495bf22-04ce-4285-8e7e-152e4ab65823
title: Класс Thread_V1_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup2
- Thread_V1_TypeGroup2.ProcessId
- Thread_V1_TypeGroup2.TThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: d00e2d535cdc0fe14d2ae0f48fb7809f627b24fe19cdaff5d63750ee9b5f2c42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814241"
---
# <a name="thread_v1_typegroup2-class"></a>\_ \_ Класс TypeGroup2 потока v1

Этот класс является классом типа события для событий конца потока.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{2, 4}, EventTypeName{"End", "DCEnd"}]
class Thread_V1_TypeGroup2 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
};
```

## <a name="members"></a>Члены

Класс **Thread \_ v1 \_ TypeGroup2** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Thread \_ v1 \_ TypeGroup2** имеет следующие свойства.

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

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Поток \_ v1**](thread-v1.md)
</dt> </dl>

 

 




