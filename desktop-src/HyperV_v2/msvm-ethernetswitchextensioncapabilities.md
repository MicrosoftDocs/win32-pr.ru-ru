---
description: Представляет ассоциацию между расширениями Ethernet и их возможностями.
ms.assetid: 6b32235a-175d-48f9-af3a-2d40f748a518
title: Класс Msvm_EthernetSwitchExtensionCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtensionCapabilities
- Msvm_EthernetSwitchExtensionCapabilities.ManagedElement
- Msvm_EthernetSwitchExtensionCapabilities.Capabilities
- Msvm_EthernetSwitchExtensionCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 950a8a0288487bf557e9dd201100b2a894417641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819497"
---
# <a name="msvm_ethernetswitchextensioncapabilities-class"></a>\_Класс мсвм есернетсвитчекстенсионкапабилитиес

Представляет ассоциацию между расширениями Ethernet и их возможностями.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtensionCapabilities : CIM_ElementCapabilities
{
  Msvm_InstalledEthernetSwitchExtension  REF ManagedElement;
  Msvm_EthernetSwitchFeatureCapabilities REF Capabilities;
  uint16                                     Characteristics[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ есернетсвитчекстенсионкапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ есернетсвитчекстенсионкапабилитиес** имеет следующие свойства.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ есернетсвитчфеатурекапабилитиес**](msvm-ethernetswitchfeaturecapabilities.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("возможности")
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ есернетсвитчфеатурекапабилитиес**](msvm-ethernetswitchfeaturecapabilities.md) , представляющий объект capabilities, связанный с параметром. Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> <dt>

**Характеристики**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Содержит описательные сведения о возможностях. Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).



| Значение                                                                                                                                                                                                                       | Значение                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**По умолчанию**</dt> <dt>2</dt> </dl> | Связанные возможности представляют возможности управляемого элемента по умолчанию.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Текущие**</dt> <dt>3</dt> </dl> | Связанные возможности представляют текущие возможности управляемого элемента.<br/> |



 

</dd> <dt>

**манажеделемент**
</dt> <dd> <dl> <dt>

Тип данных: **[ **мсвм \_ инсталледесернетсвитчекстенсион**](msvm-installedethernetswitchextension.md)**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("манажеделемент")
</dt> </dl>

Ссылка на экземпляр класса [**мсвм \_ инсталледесернетсвитчекстенсион**](msvm-installedethernetswitchextension.md) , представляющий установленное расширение. Это свойство наследуется от [**CIM \_ елементкапабилитиес**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

