---
description: Представляет класс типа событий для событий обработчиков объектов, связанных с началом и концом сбора данных.
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: Класс Обхандлерундовневент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985720"
---
# <a name="obhandlerundownevent-class"></a>Класс Обхандлерундовневент

Представляет класс типа событий для событий обработчиков объектов, связанных с началом и концом сбора данных. Это событие включает в себя перечисление всех дескрипторов при выполнении очистки.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a>Участники

Класс **обхандлерундовневент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **обхандлерундовневент** имеет следующие свойства.

<dl> <dt>

**Дескриптор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Объектный обработчик.

</dd> <dt>

**Объект**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Формат**](event-tracing-mof-qualifiers.md) ("x"), [**указатель**](event-tracing-mof-qualifiers.md), [**вмидатаид**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Объект.

</dd> <dt>

**ObjectName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**Стрингтерминатион**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Имя объекта.

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Тип объекта.

</dd> <dt>

**Идентификатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (2)
</dt> </dl>

Идентификатор процесса.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |



 

 




