---
description: Регистрирует поставщики методов с помощью инструментария WMI.
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: Класс __MethodProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: dd59a88c9c0ff7b4b6726b58ce69f879eb3893ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703015"
---
# <a name="__methodproviderregistration-class"></a>\_\_Класс Месодпровидеррегистратион

Системный класс **\_ \_ месодпровидеррегистратион** регистрирует поставщиков методов с помощью инструментария WMI.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ месодпровидеррегистратион** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ месодпровидеррегистратион** имеет следующие свойства.

<dl> <dt>

**поставщики**
</dt> <dd> <dl> <dt>

Тип данных: **\_ \_ поставщик**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр [**\_ \_ поставщика**](--provider.md) , представляющий путь к объекту поставщика метода. Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ \_ месодпровидеррегистратион** является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md). Только администраторы могут зарегистрировать или удалить поставщик метода, создав экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и **\_ \_ месодпровидеррегистратион**.

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

[Регистрация поставщика методов](registering-a-method-provider.md)
</dt> </dl>

 

