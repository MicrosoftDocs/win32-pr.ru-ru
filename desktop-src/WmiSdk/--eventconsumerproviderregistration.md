---
description: Регистрирует поставщиков объектов-получателей событий с помощью инструментария WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: Класс __EventConsumerProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911975"
---
# <a name="__eventconsumerproviderregistration-class"></a>\_\_Класс Евентконсумерпровидеррегистратион

Системный класс **\_ \_ евентконсумерпровидеррегистратион** регистрирует поставщиков потребителей событий с помощью WMI.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ евентконсумерпровидеррегистратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ евентконсумерпровидеррегистратион** имеет следующие свойства.

<dl> <dt>

**консумеркласснамес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Массив имен логических классов потребителей, поддерживаемых поставщиком объектов событий.

</dd> <dt>

**поставщики**
</dt> <dd> <dl> <dt>

Тип данных: **\_ \_ поставщик**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к объекту поставщика. Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ \_ евентконсумерпровидеррегистратион** является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_провидеррегистратион**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> <dt>

[Регистрация поставщика событий-получателя](registering-an-event-consumer-provider.md)
</dt> <dt>

[Создание поставщика объектов событий](writing-an-event-consumer-provider.md)
</dt> </dl>

 

