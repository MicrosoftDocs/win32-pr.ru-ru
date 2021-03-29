---
description: Управляет кэшем при выгрузке поставщика свойств.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: Класс __PropertyProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264803"
---
# <a name="__propertyprovidercachecontrol-class"></a>\_\_Класс Пропертипровидеркачеконтрол

Класс **\_ \_ пропертипровидеркачеконтрол** управляет кэшем при выгрузке поставщика свойств. Этот класс существует только в \\ корневом пространстве имен.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ пропертипровидеркачеконтрол** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ пропертипровидеркачеконтрол** имеет следующие свойства.

<dl> <dt>

**клеарафтер**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Интервал времени после освобождения WMI поставщиком свойств. Время указано в формате интервала.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ \_ пропертипровидеркачеконтрол** является производным от [**\_ \_ CacheControl**](--cachecontrol.md). Дополнительные сведения см. [в разделе выгрузка поставщика](unloading-a-provider.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> </dl>

 

 




