---
description: Представляет системное событие.
ms.assetid: 84099483-03e4-4c21-b680-f0975b18c1f6
ms.tgt_platform: multiple
title: Класс __SystemEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 445b84e8b692283693c0849c43f603678cdbabde8fc6c313c4da973e3921a4e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110171"
---
# <a name="__systemevent-class"></a>\_\_Класс Системевент

Системный класс **\_ \_ системевент** представляет системное событие.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __SystemEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ системевент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ системевент** имеет следующие свойства.

<dl> <dt>

**\_дескриптор безопасности**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие. Это свойство наследуется от [**\_ \_ события**](--event.md).

> [!Note]  
> **Пустой** список управления доступом (ACL) в [**\_ дескрипторе безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет всем всем времени неограниченный доступ. Дополнительные сведения см. в разделе [Создание дескриптора безопасности для нового объекта](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**ВРЕМЯ \_ создания**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальное значение, указывающее время создания события. Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г. Эти сведения находятся в формате всеобщего скоординированного времени (UTC). Это свойство наследуется от [**\_ \_ события**](--event.md).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **\_ \_ системевент** является производным от класса [**\_ \_ екстринсицевент**](--extrinsicevent.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_\_екстринсицевент**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> </dl>

 

