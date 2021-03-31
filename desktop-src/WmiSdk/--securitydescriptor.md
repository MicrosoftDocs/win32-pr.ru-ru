---
description: Представляет дескриптор безопасности.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: Класс __SecurityDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
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
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264801"
---
# <a name="__securitydescriptor-class"></a>\_\_Класс SecurityDescriptor

Абстрактный системный класс **\_ \_ SecurityDescriptor** представляет [*дескриптор безопасности*](/windows/desktop/SecGloss/s-gly).

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ SecurityDescriptor** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ \_ SecurityDescriptor** имеет следующие свойства.

<dl> <dt>

**контролфлагс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Битовые флаги, предоставляющие сведения о содержимом и формате дескриптора. Описание флагов см. в свойстве **контролфлагс** в классе [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .

</dd> <dt>

**КОНТРОЛЯ**
</dt> <dd> <dl> <dt>

Тип данных: массив **[**\_ \_ ACE**](--ace.md)**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Массив записей [**\_ \_ ACE**](--ace.md) , которые определяют доступ к объекту.

</dd> <dt>

**Группа**
</dt> <dd> <dl> <dt>

Тип данных: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

ACE, определяющий доверенное лицо, представляющее группу объекта.

</dd> <dt>

**Владелец**
</dt> <dd> <dl> <dt>

Тип данных: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

ACE, определяющий доверенное лицо, представляющее владельца объекта.

</dd> <dt>

**СИСТЕМНЫЙ**
</dt> <dd> <dl> <dt>

Тип данных: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив записей [**\_ \_ ACE**](--ace.md) , определяющих пользователей и группы, для которых собираются данные аудита.

</dd> <dt>

**ВРЕМЯ \_ создания**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время в формате [ \_ даты и времени CIM](cim-datetime.md) при создании дескриптора безопасности.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот класс предоставляет свойства, наследуемые с помощью [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md) и [изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md). Дополнительные сведения об [элементах управления доступом](/windows/desktop/SecAuthZ/access-control-components)см. в разделе компоненты контроля доступа.

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

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Поддержание безопасности WMI](maintaining-wmi-security.md)
</dt> </dl>

 

