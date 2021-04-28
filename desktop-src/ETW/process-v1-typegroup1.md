---
description: Process_V1_TypeGroup1 класс — этот класс является классом типа события для событий процесса. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Класс Process_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V1_TypeGroup1
- Process_V1_TypeGroup1.PageDirectoryBase
- Process_V1_TypeGroup1.ProcessId
- Process_V1_TypeGroup1.ParentId
- Process_V1_TypeGroup1.SessionId
- Process_V1_TypeGroup1.ExitStatus
- Process_V1_TypeGroup1.UserSID
- Process_V1_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d7f4426f34a97ff79dc41806f1e0070013528d2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106332"
---
# <a name="process_v1_typegroup1-class"></a>\_ \_ Класс TypeGroup1 процесса v1

Этот класс является классом типа события для событий процесса.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V1_TypeGroup1 : Process_V1
{
  uint32 PageDirectoryBase;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a>Члены

Класс **Process \_ v1 \_ TypeGroup1** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Process \_ v1 \_ TypeGroup1** имеет следующие свойства.

<dl> <dt>

ExitStatus
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5)
</dt> </dl>

Состояние завершения остановленного процесса.

</dd> <dt>

имажефиленаме
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (7), Стрингтерминатион ("NullTerminated")
</dt> </dl>

Путь к исполняемому файлу процесса.

</dd> <dt>

пажедиректорибасе
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Pointer
</dt> </dl>

Зарезервировано.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3)
</dt> </dl>

Уникальный идентификатор процесса, который создает этот процесс. Идентификаторы процессов используются повторно, поэтому они определяют только процесс времени существования этого процесса. Возможно, процесс, идентифицированный Парентпроцессид, завершается, поэтому Парентпроцессид может не ссылаться на выполняющийся процесс. Также возможно, что Парентпроцессид неправильно ссылается на процесс, который повторно использует идентификатор процесса.

**Windows Server 2003:** Включает квалификатор Format ("x").

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2)
</dt> </dl>

Глобальный идентификатор процесса, который можно использовать для идентификации процесса. Значение допустимо с момента создания процесса до его завершения.

**Windows Server 2003:** Включает квалификатор Format ("x").

</dd> <dt>

SessionId
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4)
</dt> </dl>

Уникальный идентификатор, создаваемый операционной системой при создании нового сеанса. Сеанс охватывает период времени от входа до выхода из определенной системы.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Тип данных: **объект**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (6), Extension ("sid")
</dt> </dl>

Идентификатор безопасности (SID) для пользовательского контекста, в котором происходит событие.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Процесс \_ v1**](process.md)
</dt> <dt>

[**Процесс \_ v1**](process-v1.md)
</dt> </dl>

 

 




