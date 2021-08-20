---
description: Определяет средства, с помощью которых клиент может обнаружить допустимый диапазон параметров по умолчанию для виртуального ресурса.
ms.assetid: AC516723-7CD2-4F10-B8BF-EF9D458D3E5B
title: Класс Msvm_AllocationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AllocationCapabilities
- Msvm_AllocationCapabilities.InstanceID
- Msvm_AllocationCapabilities.Caption
- Msvm_AllocationCapabilities.Description
- Msvm_AllocationCapabilities.ElementName
- Msvm_AllocationCapabilities.ResourceType
- Msvm_AllocationCapabilities.OtherResourceType
- Msvm_AllocationCapabilities.ResourceSubType
- Msvm_AllocationCapabilities.RequestTypesSupported
- Msvm_AllocationCapabilities.SharingMode
- Msvm_AllocationCapabilities.SupportedAddStates
- Msvm_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dfdbb9dc884bd84e15e02e004af3cef296ae7723733f572a4525542747449e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149324"
---
# <a name="msvm_allocationcapabilities-class"></a>\_Класс мсвм аллокатионкапабилитиес

Определяет средства, с помощью которых клиент может обнаружить допустимый диапазон параметров по умолчанию для виртуального ресурса. Объект **\_ аллокатионкапабилитиес мсвм** связан с каждым пулом ресурсов. Четыре объекта [**мсвм \_ ресаурцеаллокатионсеттингдата**](msvm-resourceallocationsettingdata.md) связаны с объектом **мсвм \_ аллокатионкапабилитиес** для описания минимального, максимального, по умолчанию и добавочных значений для выделения данного ресурса. Вместе эти классы описывают общий диапазон поддерживаемых возможностей.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AllocationCapabilities : CIM_AllocationCapabilities
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ аллокатионкапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ аллокатионкапабилитиес** имеет следующие свойства.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство позволяет каждому экземпляру определить отображаемое имя в дополнение к его ключевым свойствам, идентификационным данным и сведениям о описании. Свойство [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) класса **CIM \_ манажедсистемелемент** также определяется как отображаемое имя. Но часто этот класс является ключом. Не целесообразно, что одно и то же свойство может передать как удостоверение, так и отображаемое имя без несогласованности. Если [**имя**](msvm-keyboard.md) существует и не является ключом (например, для экземпляров логического устройства), то одни и те же сведения могут присутствовать в свойствах **Name** и **ElementName** . Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уникальный идентификатор для этого пула ресурсов. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**осерресаурцетипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая тип ресурса, если четко определенное значение недоступно, а **ResourceType** имеет значение other. Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).

</dd> <dt>

**рекуесттипессуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, поддерживается ли запрос определенного ресурса. Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).



| Значение                                                                                                                                                                                                                           | Значение                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Неизвестно**</dt> <dt>0</dt> </dl>     | Неизвестно<br/>                                                         |
| <span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span><dl> <dt>**Конкретное**</dt> <dt>2</dt> </dl> | Запрос может включать запрос определенного ресурса.<br/>      |
| <span id="General"></span><span id="general"></span><span id="GENERAL"></span><dl> <dt>**Общее**</dt> <dt>3</dt> </dl>     | Запрос не включает запрос определенного ресурса.<br/> |
| <span id="Both"></span><span id="both"></span><span id="BOTH"></span><dl> <dt>**Оба**</dt> <dt>4</dt> </dl>                 | Поддерживаются как конкретные, так и общие запросы.<br/>               |



 

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая конкретный подтип реализации для этого ресурса. Например, это можно использовать для различения разных моделей одного типа ресурсов. Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип ресурса, который представляет этот параметр выделения. Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)
</dt> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Компьютерная система** (2)
</dt> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Процессор** (3)
</dt> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Память** (4)
</dt> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-контроллер** (5)
</dt> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Параллельный SCSI HBA** (6)
</dt> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>**Адаптер шины FC** (7)
</dt> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**адаптер шины iSCSI** (8)
</dt> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>**Геохка** (9)
</dt> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-адаптер** (10)
</dt> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Другой сетевой адаптер** (11)
</dt> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Разъем ввода-вывода** (12)
</dt> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Устройство ввода-вывода** (13)
</dt> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>Дисковод **гибких дисков** (14)
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Дисковод компакт-дисков** (15)
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-дисковод** (16)
</dt> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Диск** (17)
</dt> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Ленточный накопитель** (18)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**экстент служба хранилища** (19)
</dt> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**другое устройство служба хранилища** (20)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Последовательный порт** (21)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Параллельный порт** (22)
</dt> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Контроллер USB** (23)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Графический контроллер** (24)
</dt> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Контроллер IEEE 1394** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Единица секционирования** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Базовая единица секционирования** (27)
</dt> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>**Мощность** (28)
</dt> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Емкость системы охлаждения** (29)
</dt> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Порт коммутатора Ethernet** (30)
</dt> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Логический диск** (31)
</dt> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**служба хранилища том** (32)
</dt> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet-подключение** (33)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. 0XFFFF
</dt> </dl>

</dd> <dt>

**шарингмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, как предоставляется доступ к базовому ресурсу. Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).



| Значение                                                                                                                                                                                                                               | Значение                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Неизвестно**</dt> <dt>0</dt> </dl>         | Неизвестно<br/>                                     |
| <span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span><dl> <dt>**Выделенный**</dt> <dt>2</dt> </dl> | Монопольный доступ к базовому ресурсу.<br/> |
| <span id="Shared"></span><span id="shared"></span><span id="SHARED"></span><dl> <dt>**Общее**</dt> <dt>3</dt> </dl>             | Общее использование базового ресурса.<br/>       |



 

</dd> <dt>

**суппортедаддстатес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает состояния, в которых система, с которой будет связан ресурс, может входить в систему при создании нового ресурса. Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (4)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (5)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (7)
</dt> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Отложено** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (10)
</dt> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (11)
</dt> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Приостановлено** (12)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. 0XFFFF
</dt> </dl>

</dd> <dt>

**суппортедремовестатес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает состояния, в которых система, с которой связан ресурс, может находиться в случае удаления ресурса. Это свойство наследуется от [**CIM \_ аллокатионкапабилитиес**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (4)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (5)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Включено, но отключено** (6)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (7)
</dt> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Отложено** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (10)
</dt> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (11)
</dt> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Приостановлено** (12)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. 0XFFFF
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу **\_ аллокатионкапабилитиес мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_АЛЛОКАТИОНКАПАБИЛИТИЕС CIM**](cim-allocationcapabilities.md)
</dt> <dt>

[**\_АЛЛОКАТИОНКАПАБИЛИТИЕС CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)
</dt> <dt>

[**Мсвм \_ аллокатионкапабилитиес (v1)**](/previous-versions/windows/desktop/virtual/msvm-allocationcapabilities)
</dt> <dt>

[Классы управления ресурсами](resource-management-classes.md)
</dt> </dl>

 

