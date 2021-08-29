---
description: Представляет элемент управления доступом.
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: Класс __ACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
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
ms.openlocfilehash: ad6713cea39f02e59b49b69e2fa2a8a060cb7a6f78d3b6143bc2c2dbc0de1965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051112"
---
# <a name="__ace-class"></a>\_\_Класс ACE

Абстрактный системный класс **\_ \_ ACE** представляет запись управления доступом ([*ACE*](/windows/desktop/SecGloss/a-gly)).

Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ ACE** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ ACE** имеет следующие свойства.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Тип данных: 
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Битовые флаги, представляющие права, которые предоставляются или запрещают доверенному лицу. Дополнительные сведения и описание флагов см. в разделе свойство **AccessMask** в классе [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

</dd> <dt>

**AceFlags**
</dt> <dd> <dl> <dt>

Тип данных: 
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Битовые флаги, определяющие наследование ACE. Дополнительные сведения и описание флагов см. в разделе свойство **AceFlags** в классе [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

</dd> <dt>

**AceType**
</dt> <dd> <dl> <dt>

Тип данных: 
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Тип записи ACE, представляемой этим экземпляром.

</dd> <dt>

**гуидинхеритедобжекттипе**
</dt> <dd> <dl> <dt>

Тип данных: 
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Идентификатор GUID родителя объекта, к которому применяются права доступа в свойстве **AccessMask** .

</dd> <dt>

**гуидобжекттипе**
</dt> <dd> <dl> <dt>

Тип данных: 
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Идентификатор GUID, указывающий тип объекта, к которому применяются права в свойстве **AccessMask** .

</dd> <dt>

**ВРЕМЯ \_ создания**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Время создания дескриптора безопасности в формате [ \_ даты и времени CIM](cim-datetime.md) .

</dd> <dt>

**Доверенное лицо**
</dt> <dd> <dl> <dt>

Тип данных: **[ **\_ \_ доверенное лицо**](--trustee.md)**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Доверенное лицо записи ACE, представленной этим экземпляром класса **\_ \_ ACE** .

</dd> </dl>

## <a name="remarks"></a>Remarks

Этот класс предоставляет свойства, наследуемые классом [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , который является членом класса [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Дополнительные сведения см. в разделе [объекты дескрипторов безопасности WMI](wmi-security-descriptor-objects.md) и [изменение параметров безопасности доступа для защищаемых объектов](changing-access-security-on-securable-objects.md). Дополнительные сведения об [элементах управления доступом](/windows/desktop/SecAuthZ/access-control-components)см. в разделе компоненты контроля доступа.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_\_секуритирелатедкласс**](--securityrelatedclass.md)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> <dt>

[**\_ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[Поддержание безопасности WMI](maintaining-wmi-security.md)
</dt> </dl>

 

