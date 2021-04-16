---
description: Определяет средства, с помощью которых клиент может обнаружить методы, предоставляемые службой миграции, и допустимый диапазон данных параметров миграции виртуальной системы.
ms.assetid: 704fa81d-54a4-4d12-9b85-8836581d2784
title: Класс Msvm_VirtualSystemMigrationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationCapabilities
- Msvm_VirtualSystemMigrationCapabilities.InstanceID
- Msvm_VirtualSystemMigrationCapabilities.Caption
- Msvm_VirtualSystemMigrationCapabilities.Description
- Msvm_VirtualSystemMigrationCapabilities.ElementName
- Msvm_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c89e898cbf861d2bc3643e43a8bd9089062a2d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540282"
---
# <a name="msvm_virtualsystemmigrationcapabilities-class"></a>\_Класс мсвм виртуалсистеммигратионкапабилитиес

Определяет средства, с помощью которых клиент может обнаружить методы, предоставляемые службой миграции, и допустимый диапазон данных параметров миграции виртуальной системы. Объект **\_ виртуалсистеммигратионкапабилитиес мсвм** связан с объектами [**мсвм \_ виртуалсистеммигратионсеттингдата**](msvm-virtualsystemmigrationsettingdata.md) . Эти ассоциации определяют допустимый диапазон доступных служб миграции.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationCapabilities : CIM_VirtualSystemMigrationCapabilities
{
  string InstanceID;
  string Caption = "Migration Capabilities";
  string Description = "Virtual System Migration Capabilities";
  string ElementName;
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистеммигратионкапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистеммигратионкапабилитиес** имеет следующие свойства.

<dl> <dt>

**асинчронаусмесодссуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("асинчронаусмесодссуппортед")
</dt> </dl>

Определяет методы, реализация которых может быть асинхронной; Это значит, что операция не будет выполнена немедленно и вернет задание. Это свойство наследуется от **CIM \_ виртуалсистеммигратионкапабилитиес**.

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

**Мигратевиртуалсистемтохостсуппортед** (2)


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

**Мигратевиртуалсистемтосистемсуппортед** (3)


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableSupported"></span><span id="checkvirtualsystemismigratablesupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLESUPPORTED"></span>

**Чекквиртуалсистемисмигратаблесуппортед** (32768)


</dt> <dd></dd> </dl>

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности миграции".

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности миграции виртуальной системы".

</dd> <dt>

**дестинатионхостформатссуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив форматов имен, поддерживаемых для параметра *дестинатионхост* методов [**мигратевиртуалсистемтохост**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) и [**чекквиртуалсистемисмигратабле**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) . Это свойство наследуется от **CIM \_ виртуалсистеммигратионкапабилитиес**.



| Значение                                                                                                                                                                                                                                                                                                                           | Значение                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span><dl> <dt>**Домаиннамеформатсуппортед**</dt> <dt>2</dt> </dl>                             | Поддержка формата доменных имен в соответствии с RFC 10353.<br/>         |
| <span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span><dl> <dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt> </dl> | Поддержка десятичного формата IPv4 в соответствии с RFC 12084.<br/> |
| <span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span><dl> <dt>**IPv6TextFormatSupported**</dt> <dt>4</dt> </dl>                                     | Поддержка формата текста IPv6 в соответствии с RFC 4291.<br/>            |



 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**синчронаусмесодссуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Определяет методы, реализация которых может быть синхронной; то есть операция будет завершена немедленно и не будет возвращать задание. Это свойство наследуется от **CIM \_ виртуалсистеммигратионкапабилитиес**.

<dl> <dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**Мигратевиртуалсистемтохостсуппортед** (2)
</dt> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**Мигратевиртуалсистемтосистемсуппортед** (3)
</dt> <dt>

<span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**Чекквиртуалсистемисмигратаблетохостсуппортед** (4)
</dt> <dt>

<span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**Чекквиртуалсистемисмигратаблетосистемсуппортед** (5)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (.. )
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

