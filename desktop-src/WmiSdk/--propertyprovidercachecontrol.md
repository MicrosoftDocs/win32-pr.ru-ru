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
ms.openlocfilehash: 33edad107859328e9a81a6c77c3c02e29e2ee3aebbbe411ee20fb438e51517a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110542"
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

### <a name="properties"></a>Элемент Property

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

## <a name="remarks"></a>Remarks

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

 

 




