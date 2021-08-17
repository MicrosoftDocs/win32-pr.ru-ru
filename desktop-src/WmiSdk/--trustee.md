---
description: '\_ \_ Абстрактный системный класс доверенного лица представляет доверенное лицо. Можно использовать либо имя, либо идентификатор безопасности (массив байтов).'
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: Класс __Trustee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: ac1e80bceb3dc584a22e342780bbf32660276868e473ff33ff01d6c2ad65d504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131957"
---
# <a name="__trustee-class"></a>\_\_Класс доверенного лица

Абстрактный системный класс [**\_ \_ доверенного лица**](--securitydescriptor.md) представляет [*доверенное лицо*](/windows/desktop/SecGloss/t-gly). Можно использовать либо имя, либо идентификатор безопасности (массив байтов).

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ доверенного лица** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ доверенного лица** имеет эти свойства.

<dl> <dt>

**Доменная**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Доменная часть учетной записи.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Имя части учетной записи.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Идентификатор безопасности доверенного лица в двоичном формате байтового массива.

</dd> <dt>

**сидленгс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Длина SID в байтах.

</dd> <dt>

**сидстринг**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Идентификатор безопасности доверенного лица в строковом формате, например "S-1-1-0".

</dd> <dt>

**ВРЕМЯ \_ создания**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время в формате [ \_ даты и времени CIM](cim-datetime.md) при создании дескриптора безопасности.

</dd> </dl>

## <a name="remarks"></a>Remarks

Этот класс предоставляет свойства, наследуемые классом [**\_ доверенного лица Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , который является членом класса [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md) и [изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md). Дополнительные сведения об [элементах управления доступом](/windows/desktop/SecAuthZ/access-control-components)см. в разделе компоненты контроля доступа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> <dt>

[**\_Доверенное лицо Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[Поддержание безопасности WMI](maintaining-wmi-security.md)
</dt> </dl>

 

