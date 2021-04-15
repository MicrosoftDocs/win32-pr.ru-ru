---
description: Класс является абстрактным базовым классом для классов, которые используются для определения того, когда WMI должен освободить объект модели COM.
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: Класс __CacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fe5358630a7ac5eb48751135d39c2fd998196bf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683706"
---
# <a name="__cachecontrol-class"></a>\_\_Класс CacheControl

Класс System **\_ \_ CacheControl** является абстрактным базовым классом для классов, которые используются для определения того, когда WMI должен освободить объект модели COM. Экземпляры этого класса никогда не создаются. Класс **\_ \_ CacheControl** расположен только в корневом пространстве имен. Дополнительные сведения об использовании этого класса см. [в разделе выгрузка поставщика](unloading-a-provider.md).

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a>Члены

Класс **\_ \_ CacheControl** не определяет никаких членов.

## <a name="remarks"></a>Комментарии

Класс **\_ \_ CacheControl** является производным от [**\_ \_ системкласс**](--systemclass.md).

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

[**\_\_евентконсумерпровидеркачеконтрол**](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[**\_\_евентпровидеркачеконтрол**](--eventprovidercachecontrol.md)
</dt> <dt>

[**\_\_евентсинккачеконтрол**](--eventsinkcachecontrol.md)
</dt> <dt>

[**\_\_обжектпровидеркачеконтрол**](--objectprovidercachecontrol.md)
</dt> <dt>

[\_\_пропертипровидеркачеконтрол](--propertyprovidercachecontrol.md)
</dt> <dt>

[Выгрузка поставщика](unloading-a-provider.md)
</dt> </dl>

 

