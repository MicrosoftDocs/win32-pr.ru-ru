---
description: Process_V0_TypeGroup1 класс — этот класс является классом типа события для событий процесса. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Класс Process_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0d42ed4704eafcbb335b29c2c2d8d83e2ea82591c75855a6da096cb1e11a7572
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394440"
---
# <a name="process_v0_typegroup1-class"></a>\_Класс Process v0 \_ TypeGroup1

Этот класс является классом типа события для событий процесса.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a>Члены

Класс **Process \_ v0 \_ TypeGroup1** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Process \_ v0 \_ TypeGroup1** имеет следующие свойства.

<dl> <dt>

имажефиленаме
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4), Стрингтерминатион ("NullTerminated")
</dt> </dl>

Путь к исполняемому файлу процесса.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Pointer
</dt> </dl>

Уникальный идентификатор процесса, который создает процесс. Идентификаторы процессов используются повторно, поэтому они определяют только процесс времени существования этого процесса. Возможно, процесс, идентифицированный Парентпроцессид, завершается, поэтому Парентпроцессид может не ссылаться на выполняющийся процесс. Также возможно, что Парентпроцессид неправильно ссылается на процесс, который повторно использует идентификатор процесса.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Pointer
</dt> </dl>

Глобальный идентификатор процесса, который можно использовать для идентификации процесса. Значение допустимо с момента создания процесса до его завершения.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3), Extension ("sid")
</dt> </dl>

Идентификатор безопасности (SID) для пользовательского контекста, в котором происходит событие.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Обработка \_ v0**](process-v0.md)
</dt> </dl>

 

 




