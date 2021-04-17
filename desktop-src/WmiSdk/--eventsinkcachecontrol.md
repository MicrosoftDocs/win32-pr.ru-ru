---
description: Используется для определения того, когда инструментарий WMI освобождает указатель Ивбемунбаундобжектсинк поставщиков событий.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: Класс __EventSinkCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693556"
---
# <a name="__eventsinkcachecontrol-class"></a>\_\_Класс Евентсинккачеконтрол

Класс System **\_ \_ евентсинккачеконтрол** используется для определения того, когда WMI освобождает указатель [**ивбемунбаундобжектсинк**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) поставщика событий. Класс **\_ \_ евентсинккачеконтрол** является Singleton-классом. Он расположен только в \\ корневом пространстве имен.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ евентсинккачеконтрол** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ евентсинккачеконтрол** имеет следующие свойства.

<dl> <dt>

**клеарафтер**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Интервал времени, по истечении которого WMI освобождает поставщик событий. Интервал, указанный для выгрузки поставщика, может занять вдвое больше времени. Время указано в [формате интервала](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ \_ евентсинккачеконтрол** является производным от [**\_ \_ CacheControl**](--cachecontrol.md). Дополнительные сведения об использовании этого класса см. [в разделе выгрузка поставщика](unloading-a-provider.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Root<br/>                |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> </dl>

 

 




