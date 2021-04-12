---
description: Выступает в качестве родительского класса для классов регистрации для различных типов поставщиков.
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: Класс __ProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7359f3d5cdcfb2447b724fd6d369a1029d8fcd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156618"
---
# <a name="__providerregistration-class"></a>\_\_Класс Провидеррегистратион

Абстрактный системный класс **\_ \_ провидеррегистратион** выступает в качестве родительского класса для классов регистрации для различных типов поставщиков.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ провидеррегистратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ провидеррегистратион** имеет следующие свойства.

<dl> <dt>

**поставщики**
</dt> <dd> <dl> <dt>

Тип данных: **\_ \_ поставщик**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр [**\_ \_ поставщика**](--provider.md) , представляющий путь к объекту поставщика.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ \_ провидеррегистратион** является производным от [**\_ \_ системкласс**](--systemclass.md), у которого нет свойств.

Экземпляры класса System **\_ \_ провидеррегистратион** не создаются. Классы, используемые поставщиками для создания экземпляров для регистрации, наследуются прямо или косвенно от этого класса. Ниже приведены классы:

[**\_\_класспровидеррегистратион**](--classproviderregistration.md)

[**\_\_евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md)

[**\_\_евентпровидеррегистратион**](--eventproviderregistration.md)

[**\_\_инстанцепровидеррегистратион**](--instanceproviderregistration.md)

[**\_\_месодпровидеррегистратион**](--methodproviderregistration.md)

[**\_\_обжектпровидеррегистратион**](--objectproviderregistration.md)

[**\_\_пропертипровидеррегистратион**](--propertyproviderregistration.md)

Только администраторы могут зарегистрировать или удалить поставщик, создав экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и зарегистрировав его.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_системкласс**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> <dt>

[Регистрация поставщика](registering-a-provider.md)
</dt> </dl>

 

