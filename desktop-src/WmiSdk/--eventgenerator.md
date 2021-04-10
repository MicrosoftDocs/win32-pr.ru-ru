---
description: Выступает в качестве родительского класса для классов, управляющих созданием событий, например событий таймера.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: Класс __EventGenerator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b40524405c3b284e7ec61414e36448cb37afeab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272921"
---
# <a name="__eventgenerator-class"></a>\_\_Класс Евентженератор

Класс System **\_ \_ евентженератор** является абстрактным базовым классом, который служит родительским классом для классов, управляющих созданием событий, таких как [события таймера](receiving-a-timed-or-repeating-event.md).

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a>Члены

Класс **\_ \_ евентженератор** не определяет никаких членов.

## <a name="remarks"></a>Комментарии

Класс **\_ \_ евентженератор** является производным от [**\_ \_ индикатионрелатед**](--indicationrelated.md), у которого нет свойств.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_индикатионрелатед**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> </dl>

 

