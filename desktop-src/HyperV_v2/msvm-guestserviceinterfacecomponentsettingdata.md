---
description: Представляет настроенное состояние компонента интерфейса гостевой службы.
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Класс Msvm_GuestServiceInterfaceComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e1171e5f303d5b122f0d2202978415206a26e94c15e69f09af73b811c33dcb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147810"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a>\_Класс мсвм гуестсервицеинтерфацекомпонентсеттингдата

Представляет настроенное состояние компонента интерфейса гостевой службы. Этот класс является производным от класса [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) .

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ гуестсервицеинтерфацекомпонентсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ гуестсервицеинтерфацекомпонентсеттингдата** имеет следующие свойства.

<dl> <dt>

**Адрес**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Адрес ресурса. Например, MAC-адрес порта Ethernet.

</dd> <dt>

**аллокатионунитс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство задает единицы распределения, используемые свойствами резервирования и ограничения. Например, если ResourceType = Processor, Аллокатионунитс может иметь значение МГц. Если ResourceType = Memory, Аллокатионунитс может иметь значение МБ

</dd> <dt>

**аутоматикаллокатион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство указывает, будет ли ресурс автоматически выделяться. Например, если задано значение true, то при включении виртуальной вычислительной системы этот ресурс будет выделен. Значение false указывает, что ресурс должен быть явно выделен. Например, параметр может представлять съемные носители (т. е. устройство CDROM или дискеты), где во время электропитания отсутствует носитель. Для выделения ресурса требуется явная операция.

</dd> <dt>

**аутоматикдеаллокатион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство указывает, будет ли ресурс автоматически освобожден. Например, если задано значение true, то при отключении использования виртуальной системы компьютера этот ресурс будет освобожден. Если задано значение false, ресурс останется выделенным и должен быть освобожден явным образом.

</dd> <dt>

**Соединение**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Объект, к которому подключен этот ресурс. Например, именованная сеть или порт коммутатора.

</dd> <dt>

**консумервисибилити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описывает видимость пользователей для выделенного ресурса.



| Значение                                                                                                                                                                                                                                                                  | Значение                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Неизвестно**</dt> <dt>0</dt> </dl>                                            | Неизвестно.<br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <dt>**Передано**</dt> <dt>2</dt> </dl>                | Базовый ресурс или ресурсы узла используются и передаются потребителю, возможно, с помощью секционирования. В свойстве DeviceID должен присутствовать хотя бы один элемент.<br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <dt>**Виртуализированный**</dt> <dt>3</dt> </dl>                            | Ресурс является виртуализированным и может не сопоставляться напрямую с базовым ресурсом или узлом узла. Некоторые реализации могут поддерживать определенное назначение виртуализованных ресурсов. в этом случае ресурсы узла предоставляются с помощью свойства DeviceID.<br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <dt>**Не представлено**</dt> <dt>4</dt> </dl>            | Представление ресурса не существует в контексте потребителя ресурса.<br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**Зарезервировано DMTF**</dt> <dt>..</dt> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Зарезервировано поставщиком**</dt> <dt>32767.. 65535</dt> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

**дефаултенабледстатеполици**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Включенные и отключенные состояния служб гостевой связи по умолчанию.

Это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифиресаурцесеттингс**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) класса [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) .

> [!Note]  
> Добавлено в Windows 10.

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя для этого экземпляра SettingData. Кроме того, отображаемое имя можно использовать в качестве свойства индекса для поиска или запроса. (Примечание. имя не обязательно должно быть уникальным в пределах пространства имен.)

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Включенные и отключенные состояния элемента.

это свойство доступно только для чтения, но его можно изменить с помощью метода [**модифивиртуалсистемресаурцес**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) (или [**модифиресаурцесеттингс**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) в Windows 10 или более поздней версии) класса [**мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md) .

Допустимые значения:

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**хостресаурце**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство предоставляет определенное назначение для размещения или базовых ресурсов. Внедренные экземпляры должны содержать только ключевые свойства и рассматриваться как пути к объектам. Если виртуальный ресурс может быть запланирован на несколько базовых ресурсов, это свойство должно оставаться **равным NULL**. В этом случае можно использовать ассоциации Девицеаллокатедфромпул или Ресаурцеаллокатионфромпул, чтобы определить пул ресурсов узла, на котором может быть запланирован этот виртуальный ресурс. Если используется конкретное назначение, все базовые ресурсы, используемые этим виртуальным ресурсом, должны быть перечислены в этом массиве. Как правило, массив будет содержать один элемент, однако для агрегатных распределений, таких как несколько процессоров, можно указать несколько ресурсов узла.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

В пределах области создания экземпляра пространства имен InstanceID непрозрачно и уникально идентифицирует экземпляр этого класса. Чтобы обеспечить уникальность в пространстве имен, значение InstanceID должно быть создано с использованием следующего "предпочтительного" алгоритма: *OrgID*:*LocalId* , где *OrgID* и *LocalID* разделяются двоеточием (:), и там, где *OrgID* необходимо включать уникальное имя, которое принадлежит бизнес-сущности, которая создает или определяет InstanceId или является зарегистрированным идентификатором, назначенным бизнес-сущности в известном Глобальном центре сертификации. (Это требование похоже на объект *SchemaName* \_ . Структура *className* имен классов схемы.) Кроме того, чтобы обеспечить уникальность, *OrgID* не должен содержать двоеточия (:). При использовании этого алгоритма первое двоеточие должно появиться в идентификаторе InstanceID между *OrgID* и *LocalId*. *LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых (реальных) элементов. Если приведенный выше "предпочтительный" алгоритм не используется, определяющая сущность должна гарантировать, что полученный идентификатор InstanceID не будет повторно использоваться в любых InstanceId, созданных этим или другими поставщиками для пространства имен данного экземпляра. Для экземпляров, определяемых DMTF, необходимо использовать "предпочтительный" алгоритм с *OrgID* , для которого задано значение CIM.

</dd> <dt>

**Ограничение**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство задает верхнюю границу или максимальный объем ресурса, который будет предоставлен для этого выделения. Например, система, поддерживающая подкачку памяти, может поддерживать установку ограничения выделения памяти ниже, чем Виртуалкуантити, таким образом принудительное разбиение на страницы для этого выделения.

</dd> <dt>

**маппингбехавиор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, как этот ресурс сопоставляется с базовыми ресурсами. Если массив Хостресаурце содержит какие бы то ни было записи, это свойство отражает, как ресурс сопоставляется с этими конкретными ресурсами.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)
</dt> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (2)
</dt> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Мягкое сходство** (3)
</dt> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Жесткое сходство** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Зарезервировано поставщиком** (32767.. 65535)
</dt> </dl>

</dd> <dt>

**осерресаурцетипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая тип ресурса, когда хорошо определенное значение недоступно, а ResourceType имеет значение other.

</dd> <dt>

**Родительский объект**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Родительский объект ресурса. Например, контроллер для текущего выделения.

</dd> <dt>

**пулид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство указывает, какой ResourcePool ресурс в данный момент выделяется из, или что ResourcePool ресурс будет выделен при выделении.

</dd> <dt>

**Резервирование**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство определяет объем ресурса, который должен быть доступен для этого выделения. В системе, которая поддерживает чрезмерное использование ресурсов, это значение обычно используется для управления допуском, чтобы предотвратить принятие выделения, что препятствует исчерпанию ресурсов.

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая конкретный подтип реализации для этого ресурса. Например, это можно использовать для различения разных моделей одного типа ресурсов.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип ресурса, который представляет этот параметр выделения.

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

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Последовательный порт** (17)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Параллельный порт** (18)
</dt> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-контроллер** (19)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Графический контроллер** (20)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**экстент служба хранилища** (21)
</dt> <dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Диск** (22)
</dt> <dt>

<span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Лента** (23)
</dt> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Другое запоминающее устройство** (24)
</dt> <dt>

<span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Контроллер FireWire** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Единица секционирования** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Базовая единица секционирования** (27)
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Источник питания** (28)
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Охлаждающее устройство** (29)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Зарезервировано поставщиком** (32767.. 65535)
</dt> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство указывает количество ресурсов, представленных потребителю. Например, если ResourceType = Processor, это свойство будет отражать количество дискретных процессоров, представленных в системе виртуального компьютера. Если ResourceType = Memory, это свойство может отражать число МБ, переданных в систему виртуального компьютера.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство задает относительный приоритет для этого выделения относительно других выделений из того же ResourcePool. Это свойство не имеет единицы измерения и имеет смысл только в сравнении с другими выделениями, конкурирующими за те же ресурсы узла.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

