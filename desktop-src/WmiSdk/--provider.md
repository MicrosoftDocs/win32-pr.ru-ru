---
description: Выступает в качестве родительского класса для \_ \_ системного класса Win32Provider.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: Класс __Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712123"
---
# <a name="__provider-class"></a>\_\_Класс поставщика

Класс системы **\_ \_ поставщика** является абстрактным базовым классом, который служит родительским классом для системного класса [**\_ \_ Win32Provider**](--win32provider.md) .

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ поставщика** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ поставщика** имеет следующие свойства.

<dl> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [ **ключ**](standard-qualifiers.md)
</dt> </dl>

Строка, не зависящая от языка, которая уникально идентифицирует поставщик. Для предотвращения конфликтов имен рекомендуется следующий формат:

\|версия поставщика \| поставщика

Например, это имя поставщика представляет версию 1,0 Microsoft Тестпровидер:

«Microsoft \| тестпровидер \| v 1.0»

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ \_ поставщика** является производным от [**\_ \_ системкласс**](--systemclass.md), у которого нет свойств.

Поставщики создают экземпляры [**\_ \_ Win32Provider**](--win32provider.md) , чтобы указать сведения о своей физической реализации.

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

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 

