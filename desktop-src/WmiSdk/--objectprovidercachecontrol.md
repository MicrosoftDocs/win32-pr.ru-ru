---
description: Определяет, когда выгружается поставщик класса или экземпляра.
ms.assetid: 4cbeb820-8a65-4fab-97f1-2a973b2a4310
ms.tgt_platform: multiple
title: Класс __ObjectProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderCacheControl
- Root.__ObjectProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 53cfaa69afead4f436879f128a4d42e50d36fe67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703012"
---
# <a name="__objectprovidercachecontrol-class"></a>\_\_Класс Обжектпровидеркачеконтрол

Класс системы **\_ \_ обжектпровидеркачеконтрол** определяет, когда выгружается поставщик класса или экземпляра. Он расположен только в \\ корневом пространстве имен.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[singleton]
class __ObjectProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ обжектпровидеркачеконтрол** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ обжектпровидеркачеконтрол** имеет следующие свойства.

<dl> <dt>

**клеарафтер**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Интервал времени, после которого WMI освобождает экземпляр, класс или поставщик метода. Время указано в [формате интервала](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ \_ обжектпровидеркачеконтрол** является производным от [**\_ \_ CacheControl**](--cachecontrol.md). Дополнительные сведения об использовании этого класса см. [в разделе выгрузка поставщика](unloading-a-provider.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Root<br/>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_CacheControl**](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> <dt>

[Получение событий в любое время](receiving-events-at-all-times.md)
</dt> </dl>

 

