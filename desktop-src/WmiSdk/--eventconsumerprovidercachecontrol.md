---
description: Определяет, когда WMI должен освободить поставщик потребителей событий.
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: Класс __EventConsumerProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703319"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a>\_\_Класс Евентконсумерпровидеркачеконтрол

Класс System **\_ \_ евентконсумерпровидеркачеконтрол** определяет, когда WMI должен освободить поставщик потребителей событий. Класс **\_ \_ евентконсумерпровидеркачеконтрол** является Singleton-классом. Он расположен только в \\ корневом пространстве имен.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ евентконсумерпровидеркачеконтрол** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ евентконсумерпровидеркачеконтрол** имеет следующие свойства.

<dl> <dt>

**клеарафтер**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Интервал времени, по истечении которого WMI освобождает поставщик потребителей событий. Интервал, указанный для выгрузки поставщика, может занять вдвое больше времени. Время указано в [формате интервала](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ \_ евентконсумерпровидеркачеконтрол** является производным от [**\_ \_ CacheControl**](--cachecontrol.md). Дополнительные сведения об использовании этого класса см. [в разделе выгрузка поставщика](unloading-a-provider.md).

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

 

 




