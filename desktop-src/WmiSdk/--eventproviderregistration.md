---
description: используется для регистрации поставщиков событий с помощью инструментарий управления Windows (WMI) (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: Класс __EventProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: ce973f05aec0a1c859598c558ef8c2cc637a8faec22fd1d7f2ad2aaf383bd201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557948"
---
# <a name="__eventproviderregistration-class"></a>\_\_Класс Евентпровидеррегистратион

класс system **\_ \_ евентпровидеррегистратион** используется для регистрации поставщиков событий с помощью инструментарий управления Windows (WMI) (WMI).

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ евентпровидеррегистратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ евентпровидеррегистратион** имеет следующие свойства.

<dl> <dt>

**евенткуерилист**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

один или инструментарий управления Windows (WMI) несколько запросов языка запросов (WQL), описывающих события, поддерживаемые поставщиком событий.

</dd> <dt>

**поставщики**
</dt> <dd> <dl> <dt>

Тип данных: **\_ \_ поставщик**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к объекту поставщика событий. Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Только администраторы могут регистрировать или удалять поставщик событий, создавая экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и [**\_ \_ евентпровидеррегистратион**](--eventconsumerproviderregistration.md). Класс **\_ \_ евентпровидеррегистратион** является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md).

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

[Регистрация поставщика событий](registering-an-event-provider.md)
</dt> <dt>

[Создание поставщика событий](writing-an-event-provider.md)
</dt> </dl>

 

