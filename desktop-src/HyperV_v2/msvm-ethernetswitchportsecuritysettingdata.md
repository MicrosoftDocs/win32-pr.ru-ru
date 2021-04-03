---
description: Представляет данные настройки функции безопасности.
ms.assetid: 98e0de24-ccdc-4fc7-86a5-b68d454fde9d
title: Класс Msvm_EthernetSwitchPortSecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortSecuritySettingData
- Msvm_EthernetSwitchPortSecuritySettingData.InstanceID
- Msvm_EthernetSwitchPortSecuritySettingData.Caption
- Msvm_EthernetSwitchPortSecuritySettingData.Description
- Msvm_EthernetSwitchPortSecuritySettingData.ElementName
- Msvm_EthernetSwitchPortSecuritySettingData.AllowMacSpoofing
- Msvm_EthernetSwitchPortSecuritySettingData.EnableDhcpGuard
- Msvm_EthernetSwitchPortSecuritySettingData.EnableRouterGuard
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorMode
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorSession
- Msvm_EthernetSwitchPortSecuritySettingData.AllowIeeePriorityTag
- Msvm_EthernetSwitchPortSecuritySettingData.VirtualSubnetId
- Msvm_EthernetSwitchPortSecuritySettingData.AllowTeaming
- Msvm_EthernetSwitchPortSecuritySettingData.TeamName
- Msvm_EthernetSwitchPortSecuritySettingData.TeamNumber
- Msvm_EthernetSwitchPortSecuritySettingData.EnableFixSpeed10G
- Msvm_EthernetSwitchPortSecuritySettingData.Reserved
- Msvm_EthernetSwitchPortSecuritySettingData.DynamicIPAddressLimit
- Msvm_EthernetSwitchPortSecuritySettingData.StormLimit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d37913f015a3ffbfaa751a7bbb10f79cea2fb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913887"
---
# <a name="msvm_ethernetswitchportsecuritysettingdata-class"></a>\_Класс мсвм есернетсвитчпортсекуритисеттингдата

Представляет данные настройки функции безопасности.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("776E0BA7-94A1-41C8-8F28-951F524251B5"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Security Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortSecuritySettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Security Settings";
  string  Description = "Represents the security feature setting data.";
  string  ElementName = "Ethernet Switch Port Security Settings";
  boolean AllowMacSpoofing = FALSE;
  boolean EnableDhcpGuard = FALSE;
  boolean EnableRouterGuard = FALSE;
  uint8   MonitorMode = 0;
  uint8   MonitorSession = 0;
  boolean AllowIeeePriorityTag = FALSE;
  uint32  VirtualSubnetId = 0;
  boolean AllowTeaming = FALSE;
  string  TeamName = ;
  uint32  TeamNumber = 0;
  boolean EnableFixSpeed10G = FALSE;
  boolean Reserved = FALSE;
  uint32  DynamicIPAddressLimit = 0;
  uint32  StormLimit = 0;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчпортсекуритисеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ есернетсвитчпортсекуритисеттингдата** имеет следующие свойства.

<dl> <dt>

**алловииеприорититаг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (6), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает, должен ли трафик, переданный через порт, содержать сведения о 802.1 P. Содержит **значение true** , если трафик к порту или в него 802.1 сведения о p или **значение false** в противном случае. Значение по умолчанию равно **False**.

</dd> <dt>

**алловмакспуфинг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает, будет ли порт разрешать подмену MAC-адресов. Если это свойство имеет **значение true**, порт разрешит подмену MAC-адресов. Разрешены все допустимые значения MAC-адреса одноадресной рассылки. Если это свойство имеет **значение false**, порт будет разрешать использование только MAC-адресов, настроенных в управлении Hyper/V. Значение по умолчанию равно **False**.

</dd> <dt>

**алловтеаминг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (8), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает, могут ли сетевые карты, подключенные к порту, быть частью команды. Это относится только к сетевым адаптерам, подключенным к виртуальным машинам. Содержит **значение true** , если объединение сетевых карт разрешено или **false** в противном случае. Значение по умолчанию равно **False**.

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры безопасности порта коммутатора Ethernet".

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет данные параметров функции безопасности".

</dd> <dt>

**динамиЦипаддресслимит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (12), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Определяет предельное число полученных динамических IP-адресов. Значение по умолчанию — none (Отсутствует).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры безопасности порта коммутатора Ethernet".

</dd> <dt>

**енабледхкпгуард**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает, блокируются ли DHCP-предложения от порта. Содержит **значение true** , если предложения DHCP заблокированы с помощью порта или **false** в противном случае. Значение по умолчанию равно **False**.

</dd> <dt>

**EnableFixSpeed10G**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (14), **интерфацеверсион** (3), **интерфацеревисион** (0)
</dt> </dl>

Задайте значение TRUE, если для параметра фиксированная скорость 10G включено значение FALSE. Значение по умолчанию — FALSE.

> [!Note]  
> Свойство добавлено в Windows 10.

 

</dd> <dt>

**енаблераутергуард**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает, блокируются ли в порте объявления маршрутизатора и перенаправления маршрутизатора. Содержит **значение true** , если объявления маршрутизатора и перенаправления маршрутизаторов заблокированы с помощью порта или **false** в противном случае. Значение по умолчанию равно **False**.

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

**монитормоде**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает режим монитора для порта.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (0)


</dt> <dd></dd> <dt>

<span id="Destination"></span><span id="destination"></span><span id="DESTINATION"></span>

**Назначение** (1)


</dt> <dd></dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>

**Источник** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**мониторсессион**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Указывает идентификатор сеанса монитора, к которому принадлежит этот порт.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения"), **вмидатаид** (13), **Интерфацеверсион** (3), **интерфацеревисион** (0)
</dt> </dl>

Зарезервировано

> [!Note]  
> Свойство добавлено в Windows 10.

 

</dd> <dt>

**стормлимит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (11), **интерфацеверсион** (2), **интерфацеревисион** (0)
</dt> </dl>

Определяет ограничение количества пакетов в секунду для широковещательного и многоадресного трафика. Значение по умолчанию — none (Отсутствует).

</dd> <dt>

**теамнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (9), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Зарезервировано для последующего использования.

</dd> <dt>

**теамнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (10), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Зарезервировано для последующего использования.

</dd> <dt>

**VirtualSubnetId**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (1), **Интерфацеревисион** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)
</dt> </dl>

Указывает идентификатор виртуальной подсети, членом которой является порт. Значение по умолчанию — none.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

