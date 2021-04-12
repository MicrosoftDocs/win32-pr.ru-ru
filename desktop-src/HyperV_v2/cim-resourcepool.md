---
description: Представляет пул ресурсов, который является логической сущностью, предоставляемой хост-системой для выделения и назначения ресурсов.
ms.assetid: c8e0b701-1814-4409-a073-017f8fea841a
title: Класс CIM_ResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePool
- CIM_ResourcePool.InstanceID
- CIM_ResourcePool.PoolID
- CIM_ResourcePool.Primordial
- CIM_ResourcePool.Capacity
- CIM_ResourcePool.Reserved
- CIM_ResourcePool.ResourceType
- CIM_ResourcePool.OtherResourceType
- CIM_ResourcePool.ResourceSubType
- CIM_ResourcePool.AllocationUnits
- CIM_ResourcePool.ConsumedResourceUnits
- CIM_ResourcePool.CurrentlyConsumedResource
- CIM_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11a073f817da27dbbd45be26a008486a776470cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154539"
---
# <a name="cim_resourcepool-class"></a>\_Класс CIM ResourcePool

Представляет пул ресурсов, который является логической сущностью, предоставляемой хост-системой для выделения и назначения ресурсов.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourcePool : CIM_LogicalElement
{
  string  InstanceID;
  string  PoolID;
  boolean Primordial = FALSE;
  uint64  Capacity;
  uint64  Reserved;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  AllocationUnits;
  string  ConsumedResourceUnits = "count";
  uint64  CurrentlyConsumedResource;
  uint64  MaxConsumableResource;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ ResourcePool** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ ResourcePool** имеет следующие свойства.

<dl> <dt>

**аллокатионунитс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **испунит**
</dt> </dl>

Единицы распределения, используемые свойствами **резервирования** и **ограничения** . Например, если для **ResourceType** задано значение "процессор", **аллокатионунитс** может иметь значение "Герц \* 10 ^ 6" или "Percent". Значение этого свойства должно быть допустимым значением квалификатора программных единиц из приложения C. 1 *DSP0004 v 2.4* или более поздней версии.

</dd> <dt>

**Производительность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Максимальное количество резервирований, которое может поддерживать пул ресурсов. Свойство **аллокатионунитс** указывает тип единицы.

</dd> <dt>

**консумедресаурцеунитс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**Максконсумаблересаурце**","**CIM \_ ResourcePool**.**Куррентликонсумедресаурце**"), **испунит**
</dt> </dl>

Единицы измерения для **максконсумабле** и **использованных** свойств.

</dd> <dt>

**куррентликонсумедресаурце**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**Консумедресаурцеунитс**")
</dt> </dl>

Объем ресурса, который в настоящее время представлен пулом ресурсов для потребителей ресурсов. Это свойство отличается от **зарезервированного** свойства, так как оно описывает представление объекта "потребители" ресурса, а **зарезервированное** свойство описывает представление "производители" ресурса.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Уникально идентифицирует экземпляр этого класса в области содержащего его пространства имен.

> [!IMPORTANT]
>
> Чтобы обеспечить уникальность в пространстве имен, значение свойства **InstanceId** должно быть создано в следующем шаблоне: *OrgID*:*LocalId*
>
> -   *OrgID* должен включать уникальное имя, присвоенное товару или иным способом, которое принадлежит бизнес-сущности, определяющей свойство **InstanceId** , или быть зарегистрированным идентификатором, назначенным распознанным глобальным центром сертификации.
> -   *OrgID* не должно содержать двоеточие. Первое двоеточие в **InstanceId** должно находиться между *OrgID* и *LocalId*.
> -   *LocalId* выбирается бизнес-сущностью и не должна использоваться повторно для обнаружения различных базовых реальных элементов.
> -   Если приведенный выше шаблон не используется, определяющая сущность должна гарантировать, что результирующее значение **InstanceId** не будет повторно использоваться во всех свойствах **InstanceId** , созданных этим поставщиком или другими поставщиками для этого пространства имен.
> -   Для экземпляров, определенных DMTF, шаблон должен использоваться с *OrgID* , для которого задано значение "CIM".

 

</dd> <dt>

**максконсумаблересаурце**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**Консумедресаурцеунитс**")
</dt> </dl>

Максимальное количество потребляемых ресурсов, которые пул ресурсов может предоставить потребителям ресурсов. Это свойство отличается от свойства **Capacity** , так как оно описывает представление объекта "потребители" для ресурса, а свойство **Capacity** описывает представление "производители" ресурса.

</dd> <dt>

**осерресаурцетипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")
</dt> </dl>

Тип ресурса, если свойство **ResourceType** имеет значение "0" (другое).

</dd> <dt>

**пулид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md).**Пулид**")
</dt> </dl>

Непрозрачный идентификатор пула. Это свойство используется для обеспечения корреляции при сохранении и восстановлении данных конфигурации в базовом постоянном хранилище.

</dd> <dt>

**Исходный пул**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**значение true** , если пул ресурсов является первичным. **значение false** , если пул ресурсов является конкретным пулом ресурсов. Исходный пул ресурсов — это пул ресурсов, который не создается и не удаляется потребителями ресурса. Конкретный пул ресурсов может быть обновлен службами выделения ресурсов.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее количество резервирований, распределенное по всем активным выделениям из этого пула. В иерархической конфигурации это представляет сумму всех текущих резервирований потомков. Свойство **аллокатионунитс** указывает тип единицы.

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")
</dt> </dl>

Конкретный подтип реализации для пула ресурсов. Например, это можно использовать для различения разных моделей одного типа ресурсов.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**Осерресаурцетипе**","**CIM \_ ResourcePool**.**Ресаурцесубтипе**")
</dt> </dl>

Тип ресурса, выделенного пулом ресурсов.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

**Компьютерная система** (2)


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

**Процессор** (3)


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

**Память** (4)


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

**IDE-контроллер** (5)


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

**Параллельный SCSI HBA** (6)


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

**Адаптер шины FC** (7)


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

**адаптер шины iSCSI** (8)


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

**Геохка** (9)


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

**Ethernet-адаптер** (10)


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

**Другой сетевой адаптер** (11)


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

**Разъем ввода-вывода** (12)


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

**Устройство ввода-вывода** (13)


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

Дисковод **гибких дисков** (14)


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

**Дисковод компакт-дисков** (15)


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

**DVD-дисковод** (16)


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Диск** (17)


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

**Ленточный накопитель** (18)


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

**Область хранения** (19)


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

**Другое запоминающее устройство** (20)


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

**Последовательный порт** (21)


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

**Параллельный порт** (22)


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

**Контроллер USB** (23)


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

**Графический контроллер** (24)


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

**Контроллер IEEE 1394** (25)


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

**Единица секционирования** (26)


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

**Базовая единица секционирования** (27)


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

**Мощность** (28)


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

**Емкость системы охлаждения** (29)


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

**Порт коммутатора Ethernet** (30)


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

**Логический диск** (31)


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

**Том хранилища** (32)


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

**Ethernet-подключение** (33)


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (0x8000.. 0XFFFF


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЛОГИКАЛЕЛЕМЕНТ CIM**](cim-logicalelement.md)
</dt> </dl>

 

