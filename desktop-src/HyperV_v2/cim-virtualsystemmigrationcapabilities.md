---
description: Представляет возможности \_ объекта ВИРТУАЛСИСТЕММИГРАТИОНСЕРВИЦЕ CIM.
ms.assetid: 5fe3a10b-c075-4c45-838d-0b5c2e491584
title: Класс CIM_VirtualSystemMigrationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationCapabilities
- CIM_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1caa9809bda8d90c6bcb51439745c5fafb213383a298d0f37e064521ae184945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427654"
---
# <a name="cim_virtualsystemmigrationcapabilities-class"></a>\_Класс CIM виртуалсистеммигратионкапабилитиес

Представляет возможности объекта [**\_ виртуалсистеммигратионсервице CIM**](cim-virtualsystemmigrationservice.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationCapabilities : CIM_Capabilities
{
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a>Члены

Класс **CIM \_ виртуалсистеммигратионкапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ виртуалсистеммигратионкапабилитиес** имеет следующие свойства.

<dl> <dt>

**асинчронаусмесодссуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, указывающий методы [**\_ виртуалсистеммигратионсервице CIM**](cim-virtualsystemmigrationservice.md) , которые поддерживаются для асинхронных операций.

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

**Мигратевиртуалсистемтохостсуппортед** (2)


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

**Мигратевиртуалсистемтосистемсуппортед** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**дестинатионхостформатссуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ виртуалсистеммигратионсервице**](cim-virtualsystemmigrationservice.md).**Мигратевиртуалсистемтохост (Дестинатионхост)**","**CIM \_ виртуалсистеммигратионсервице**.**Чекквиртуалсистемисмигратаблетохост (Дестинатионхост)**")
</dt> </dl>

Массив, содержащий Поддерживаемые форматы для параметра *дестинатионхост* методов [**мигратевиртуалсистемтохост**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) и [**чекквиртуалсистемисмигратаблетохост**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) для объекта [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .

<dt>

<span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>

<span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**Домаиннамеформатсуппортед** (2)


</dt> <dd>

Поддержка текстового формата доменного имени в соответствии с RFC 1035.

</dd> <dt>

<span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>

<span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)


</dt> <dd>

Поддержка десятичного формата IPv4 в соответствии с RFC 1208.

</dd> <dt>

<span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>

<span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)


</dt> <dd>

Поддержка формата текста IPv6 в соответствии с RFC 4291

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**синчронаусмесодссуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, указывающий методы [**\_ виртуалсистеммигратионсервице CIM**](cim-virtualsystemmigrationservice.md) , которые поддерживаются для синхронных операций.

Перечисление идентификаторов методов, реализация которых может быть синхронной; то есть операция может завершиться немедленно, поэтому метод может не возвращать задание.

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

**Мигратевиртуалсистемтохостсуппортед** (2)


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

**Мигратевиртуалсистемтосистемсуппортед** (3)


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>

**Чекквиртуалсистемисмигратаблетохостсуппортед** (4)


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>

**Чекквиртуалсистемисмигратаблетосистемсуппортед** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Возможности CIM**](cim-capabilities.md)
</dt> </dl>

 

