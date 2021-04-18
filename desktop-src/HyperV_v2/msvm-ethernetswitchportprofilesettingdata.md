---
description: Представляет параметры профиля порта.
ms.assetid: 43ddb0a3-8621-4993-b0a9-8ddcfb0eaad5
title: Класс Msvm_EthernetSwitchPortProfileSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortProfileSettingData
- Msvm_EthernetSwitchPortProfileSettingData.InstanceID
- Msvm_EthernetSwitchPortProfileSettingData.Caption
- Msvm_EthernetSwitchPortProfileSettingData.Description
- Msvm_EthernetSwitchPortProfileSettingData.ElementName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileName
- Msvm_EthernetSwitchPortProfileSettingData.ProfileId
- Msvm_EthernetSwitchPortProfileSettingData.VendorName
- Msvm_EthernetSwitchPortProfileSettingData.VendorId
- Msvm_EthernetSwitchPortProfileSettingData.ProfileData
- Msvm_EthernetSwitchPortProfileSettingData.NetCfgInstanceId
- Msvm_EthernetSwitchPortProfileSettingData.PciSegmentNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciBusNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciDeviceNumber
- Msvm_EthernetSwitchPortProfileSettingData.PciFunctionNumber
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelId
- Msvm_EthernetSwitchPortProfileSettingData.CdnLabelString
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 611fd40b14b961369a847d6bb7b7746ceec2bb85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684696"
---
# <a name="msvm_ethernetswitchportprofilesettingdata-class"></a>\_Класс мсвм есернетсвитчпортпрофилесеттингдата

Представляет параметры профиля порта.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, UUID("9940CD46-8B06-43BB-B9D5-93D50381FD56"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Profile Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortProfileSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Profile Settings";
  string Description = "Represents the port profile settings.";
  string ElementName = "Ethernet Switch Port Profile Settings";
  string ProfileName = "";
  string ProfileId = "";
  string VendorName = "";
  string VendorId = 00000000-0000-0000-0000-000000000000}";
  uint32 ProfileData = 0;
  string NetCfgInstanceId = 00000000-0000-0000-0000-000000000000}";
  uint32 PciSegmentNumber = 0;
  uint32 PciBusNumber = 0;
  uint32 PciDeviceNumber = 0;
  uint32 PciFunctionNumber = 0;
  uint32 CdnLabelId = 0;
  string CdnLabelString = 0;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчпортпрофилесеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ есернетсвитчпортпрофилесеттингдата** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры профиля порта коммутатора Ethernet".

</dd> <dt>

**кднлабелид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (11), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Идентификатор метки CDN.

</dd> <dt>

**кднлабелстринг**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (12), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Строка метки CDN.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет параметры профиля порта".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры профиля порта коммутатора Ethernet".

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

**NetCfgInstanceId**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **вмидатаид** (6), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Уникальный идентификатор устройства для подинтерфейса.

</dd> <dt>

**пЦибуснумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (8), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Номер шины PCI.

</dd> <dt>

**пЦидевиценумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Номер устройства PCI.

</dd> <dt>

**пЦифунктионнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (10), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Номер функции PCI.

</dd> <dt>

**пЦисегментнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Номер сегмента PCI.

</dd> <dt>

**профиледата**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Дополнительные данные для профиля порта.

</dd> <dt>

**ProfileId**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **вмидатаид** (2), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Идентификатор профиля порта.

</dd> <dt>

**ProfileName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (1), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Имя профиля порта.

</dd> <dt>

**Поставщика**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **вмидатаид** (4), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Идентификатор поставщика, определяющего профиль.

</dd> <dt>

**ИмяПоставщика**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (3), **Интерфацеверсион** (1), **интерфацеревисион** (0)
</dt> </dl>

Имя поставщика, определяющего профиль.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

