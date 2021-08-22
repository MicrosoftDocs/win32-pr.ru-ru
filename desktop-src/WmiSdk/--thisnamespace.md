---
description: Содержит права доступа для пространства имен в виде дескриптора безопасности.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: класс __thisNAMESPACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 02e92bd8cb1c1827af86d23320e7347baa08c395d32def8c9b8adea2fcfd35bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132027"
---
# <a name="__thisnamespace-class"></a>\_\_класс Сиснамеспаце

Класс System **\_ \_ сиснамеспаце** содержит права доступа для пространства имен в форме дескриптора безопасности. Этот класс и один экземпляр находятся во всех пространствах имен.

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a>Члены

Класс **\_ \_ сиснамеспаце** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ сиснамеспаце** имеет следующие свойства.

<dl> <dt>

**\_дескриптор безопасности**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дескриптор безопасности, описывающий, кто имеет доступ к пространству имен и кто может выполнять чтение из пространства имен или запись в него. Это свойство наследуется от [**\_ \_ события**](--event.md). дополнительные сведения о формате дескрипторов безопасности см. в разделе [дескрипторы безопасности](/windows/desktop/SecAuthZ/security-descriptors) раздела безопасность Windows SDK.

</dd> </dl>

## <a name="remarks"></a>Remarks

Одноэлементный экземпляр **\_ \_ сиснамеспаце** доступен только для чтения. Чтобы изменить параметры свойства дескриптора безопасности, используйте методы класса [**\_ \_ системсекурити**](--systemsecurity.md) . Класс **\_ \_ сиснамеспаце** является производным от [**\_ \_ системкласс**](--systemclass.md).

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
</dt> </dl>

 

