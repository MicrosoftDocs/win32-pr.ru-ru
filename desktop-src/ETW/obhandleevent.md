---
description: Представляет класс типа события для событий создания или закрытия обработчика.
ms.assetid: 39d27cdf-fa51-4fb1-8998-7150ca627eff
title: Класс Обхандливент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleEvent
- ObHandleEvent.Handle
- ObHandleEvent.Object
- ObHandleEvent.ObjectName
- ObHandleEvent.ObjectType
api_type:
- NA
api_location: ''
ms.openlocfilehash: eec4e0eb00f7c821e3977f448d9c1af7e286d72a21a0a1b9473a6d3cd8fa3451
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083224"
---
# <a name="obhandleevent-class"></a>Класс Обхандливент

Представляет класс типа события для событий создания или закрытия обработчика.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, EventType{32,33}, EventTypeName{CreateHandle,CloseHandle}]
class ObHandleEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
};
```

## <a name="members"></a>Члены

Класс **обхандливент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **обхандливент** имеет следующие свойства.

<dl> <dt>

**Дескриптор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (2)
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

Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**Стрингтерминатион**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Имя объекта.

</dd> <dt>

**ObjectType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Тип объекта.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |



 

 




