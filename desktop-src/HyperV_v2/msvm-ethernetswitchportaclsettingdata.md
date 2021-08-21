---
description: Представляет список управления доступом (ACL) для параметров порта коммутатора.
ms.assetid: c0d6dfa1-017c-4e66-9ee3-425182d84231
title: Класс Msvm_EthernetSwitchPortAclSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortAclSettingData
- Msvm_EthernetSwitchPortAclSettingData.InstanceID
- Msvm_EthernetSwitchPortAclSettingData.Caption
- Msvm_EthernetSwitchPortAclSettingData.Description
- Msvm_EthernetSwitchPortAclSettingData.ElementName
- Msvm_EthernetSwitchPortAclSettingData.Name
- Msvm_EthernetSwitchPortAclSettingData.Direction
- Msvm_EthernetSwitchPortAclSettingData.Applicability
- Msvm_EthernetSwitchPortAclSettingData.AclType
- Msvm_EthernetSwitchPortAclSettingData.Action
- Msvm_EthernetSwitchPortAclSettingData.LocalAddress
- Msvm_EthernetSwitchPortAclSettingData.LocalAddressPrefixLength
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddress
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddressPrefixLength
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a9cecb30265de4a86c3b6bd6b07d7047607349a74cef9da379fb384ca5a5dc9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524194"
---
# <a name="msvm_ethernetswitchportaclsettingdata-class"></a>\_Класс мсвм есернетсвитчпортаклсеттингдата

Представляет список управления доступом (ACL) для параметров порта коммутатора.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, UUID("998BEF4A-5D55-492A-9C43-8B2F5EAE9F2B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port ACL Settings";
  string Description = "Represents the base class for switch port settings.";
  string ElementName = "Ethernet Switch Port ACL Settings";
  string Name = "";
  uint8  Direction = 0;
  uint8  Applicability = 0;
  uint8  AclType = 0;
  uint8  Action = 0;
  string LocalAddress = "";
  uint8  LocalAddressPrefixLength = 0;
  string RemoteAddress = length = 0;
  uint8  RemoteAddressPrefixLength = 0;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчпортаклсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ есернетсвитчпортаклсеттингдата** имеет следующие свойства.

<dl> <dt>

**аклтипе**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает тип конечной точки ACL.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="MAC_Acl"></span><span id="mac_acl"></span><span id="MAC_ACL"></span>

**Список ACL Mac** (1)


</dt> <dd></dd> <dt>

<span id="IPv4_Acl"></span><span id="ipv4_acl"></span><span id="IPV4_ACL"></span>

**Список ACL IPv4** (2)


</dt> <dd></dd> <dt>

<span id="IPv6_Acl"></span><span id="ipv6_acl"></span><span id="IPV6_ACL"></span>

**Список ACL IPv6** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Действие**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Это указывает на действие списка управления доступом.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

**Разрешить** (1)


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

**Deny** (2)


</dt> <dd></dd> <dt>

<span id="Meter"></span><span id="meter"></span><span id="METER"></span>

**Счетчик** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Сущности, к которым применяется триггер**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает, применяется ли ACL к локальной или удаленной конечной точке.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>

**Локальный** (1)


</dt> <dd></dd> <dt>

<span id="Remote"></span><span id="remote"></span><span id="REMOTE"></span>

**Удаленный** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "ACL порта коммутатора Ethernet Параметры".

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет базовый класс для параметров порта коммутатора".

</dd> <dt>

**Направление**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает, применяется ли ACL к входящим или исходящим направлениям.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

**Входящий** трафик (1)


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

**Исходящие** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "ACL порта коммутатора Ethernet Параметры".

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

**LocalAddress**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **вмидатаид** (6), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Локальный адрес виртуальной машины. Это может быть IPv4, IPv6 или MAC-адрес.

</dd> <dt>

**локаладдресспрефиксленгс**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Длина префикса локального адреса.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **вмидатаид** (1), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Отображаемое имя списка управления доступом.

</dd> <dt>

**RemoteAddress**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **вмидатаид** (8), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Удаленный адрес виртуальной машины. Это может быть IPv4, IPv6 или MAC-адрес.

</dd> <dt>

**ремотеаддресспрефиксленгс**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Длина префикса удаленного адреса.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

