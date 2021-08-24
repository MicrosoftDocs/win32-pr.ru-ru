---
description: Представляет коллекцию, которая предоставляет вычислительные возможности и состоит из \_ объектов CIM манажедсистемелемент.
ms.assetid: 410be43f-3368-4109-8b29-7b7cc2a3ec1b
title: Класс CIM_ComputerSystem (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.NameFormat
- CIM_ComputerSystem.Dedicated
- CIM_ComputerSystem.OtherDedicatedDescriptions
- CIM_ComputerSystem.ResetCapability
- CIM_ComputerSystem.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dd8aac2c3846c65b633061d15e6b4311b18c0a84663eca28cf2a928df2b13f4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431604"
---
# <a name="cim_computersystem-class-hyper-v-management"></a>Класс CIM_ComputerSystem (Управление Hyper-V)

Представляет коллекцию, которая предоставляет вычислительные возможности и состоит из объектов [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string NameFormat;
  uint16 Dedicated[];
  string OtherDedicatedDescriptions[];
  uint16 ResetCapability;
  uint16 PowerManagementCapabilities[];
};
```

## <a name="members"></a>Члены

Класс **CIM \_ ComputerSystem** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **CIM \_ ComputerSystem** содержит следующие методы.



| Метод                                                    | Описание                                                                                                                                                                                                          |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetPowerState**](cim-computersystem-setpowerstate.md) | Этот метод является устаревшим. Вместо этого используйте метод **рекуестповерстатечанже** в классе **CIM \_ поверманажементсервице** .<br/> **Нерекомендуемое описание:** Задает состояние электропитания компьютера.<br/> |



 

### <a name="properties"></a>Свойства

Класс **CIM \_ ComputerSystem** имеет следующие свойства.

<dl> <dt>

**Выделенные**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \|MIB-II.sysServices "," FC-GS. ИНЦИТС-T11 \| Platform \| PlatformType "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ComputerSystem**.**Осердедикатеддескриптионс**")
</dt> </dl>

Назначение и функции компьютерной системы. Например, система, предназначенная для печати, может указать «11» (печать). Системе общего назначения с возможностями печати можно присвоить значение "0" (не выделенное) и "11" (печать).

<dt>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Не выделено** (0)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (1)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (2)


</dt> <dd></dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**служба хранилища** (3)


</dt> <dd></dd> <dt>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Маршрутизатор** (4)


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)


</dt> <dd></dd> <dt>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Переключатель уровня 3** (6)


</dt> <dd></dd> <dt>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**центральный коммутатор Office** (7)


</dt> <dd></dd> <dt>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Концентратор** (8)


</dt> <dd></dd> <dt>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Сервер доступа** (9)


</dt> <dd></dd> <dt>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Брандмауэр** (10)


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Печать** (11)


</dt> <dd></dd> <dt>

<span id="I_O"></span><span id="i_o"></span>

<span id="I_O"></span><span id="i_o"></span>**Ввод-вывод** (12)


</dt> <dd></dd> <dt>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Веб-кэширование** (13)


</dt> <dd></dd> <dt>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Управление** (14)


</dt> <dd>

Этот экземпляр предназначен для размещения программного обеспечения управления системой

</dd> <dt>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Блокировка сервера** (15)


</dt> <dd></dd> <dt>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**Файловый сервер** (16)


</dt> <dd></dd> <dt>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Мобильное устройство пользователя** (17)


</dt> <dd>

Примером выделенного устройства пользователя является мобильный телефон или сканер штрихкодов в магазине, который взаимодействует через радиочастоту. Эти системы весьма ограничены функциональными возможностями и программируемостью и не считаются вычислительными платформами общего назначения. В качестве альтернативы, пример мобильной системы, которая является "общей целью" (т. е. не является выделенной), — это компьютер, удерживаемый вручную. Хотя это и ограничено программируемостью, можно скачать новое программное обеспечение и его функциональность, развернутую пользователем.

</dd> <dt>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)


</dt> <dd></dd> <dt>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Мост/расширитель** (19)


</dt> <dd></dd> <dt>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Шлюз** (20)


</dt> <dd></dd> <dt>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**служба хранилища виртуализации** (21)


</dt> <dd></dd> <dt>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Библиотека мультимедиа** (22)


</dt> <dd></dd> <dt>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**Екстендерноде** (23)


</dt> <dd></dd> <dt>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**Головка NAS** (24)


</dt> <dd></dd> <dt>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Автономный NAS** (25)


</dt> <dd></dd> <dt>

<span id="UPS"></span><span id="ups"></span>

<span id="UPS"></span><span id="ups"></span>**UPS** (26)


</dt> <dd></dd> <dt>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP-Телефон** (27)


</dt> <dd></dd> <dt>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Контроллер управления** (28)


</dt> <dd>

Этот экземпляр представляет специализированное оборудование, выделенное для управления системами (например, контроллер управления основной платой (BMC) или процессор служб).

Областью управления "контроллер управления" обычно является единая управляемая система, в которой он содержится.

</dd> <dt>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Диспетчер корпусов** (29)


</dt> <dd>

Этот экземпляр представляет систему, предназначенную для управления блейд-корпусом и содержащимися в нем устройствами. Это значение будет использоваться для представления контроллера полки. "Диспетчер шасси" — это точка статистической обработки для управления, которая может полагаться на подчиненные контроллеры управления для управления составляющими частями.

</dd> <dt>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**RAID-контроллер на основе узла** (30)


</dt> <dd>

Этот экземпляр представляет контроллер хранилища RAID, содержащийся на главном компьютере.

</dd> <dt>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**корпус устройства служба хранилища** (31)


</dt> <dd>

Этот экземпляр представляет корпус, содержащий устройства хранения.

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Рабочий стол** (32)


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Портативный компьютер** (33)


</dt> <dd></dd> <dt>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Виртуальная ленточная библиотека** (34)


</dt> <dd>

Эмуляция ленточной библиотеки с помощью виртуальной системы библиотеки.

</dd> <dt>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Виртуальная система библиотеки** (35)


</dt> <dd>

Использует дисковый накопитель для эмуляции ленточных библиотек

</dd> <dt>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**Сетевой компьютер или тонкий клиент** (36)


</dt> <dd></dd> <dt>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**Коммутатор FC** (37)


</dt> <dd>

Выделен для переключения на кадры Fibre Channel уровня 2.

</dd> <dt>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Коммутатор Ethernet** (38)


</dt> <dd>

Выделен для переключения кадров Ethernet уровня 2

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32568.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**намеформат**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("намеформат")
</dt> </dl>

Формат имени системы компьютера.

<dt>



 ("Другое")


</dt> <dd></dd> <dt>



 ("IP")


</dt> <dd></dd> <dt>



 ("Набрать")


</dt> <dd></dd> <dt>



 ("HID")


</dt> <dd></dd> <dt>



 ("НВА")


</dt> <dd></dd> <dt>



 ("Хва")


</dt> <dd></dd> <dt>



 ("X25")


</dt> <dd></dd> <dt>



 ("ISDN")


</dt> <dd></dd> <dt>



 ("IPX")


</dt> <dd></dd> <dt>



 ("ДКК")


</dt> <dd></dd> <dt>



 ("ICD")


</dt> <dd></dd> <dt>



 ("E. 164")


</dt> <dd></dd> <dt>



 ("SNA")


</dt> <dd></dd> <dt>



 ("OID/OSI")


</dt> <dd></dd> <dt>



 ("WWN")


</dt> <dd></dd> <dt>



 ("УДАЛЯЕМ")


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ComputerSystem**.**Выделенный**")
</dt> </dl>

Описывает, как или почему система выделяется, когда **выделенный** массив включает значение 2 (другое).

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ поверманажементкапабилитиес. поверкапабилитиес"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Элементы управления питанием системы DMTF \| 001,2 ")
</dt> </dl>

Это свойство использовать не рекомендуется. Вместо этого используйте метод **поверчанжекапабилитиес** в классе **CIM \_ поверманажементкапабилитиесЦим \_ поверманажементсервице** .

**Нерекомендуемое описание:** Возможности системы по управлению питанием.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Не поддерживается** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (3)


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

**Режимы энергосбережения** записываются автоматически (4)


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

**Настраиваемое состояние питания** (5)


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

**Поддержка циклов электропитания** (6)


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

**Поддерживается время включения** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**ресеткапабилити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| System Security аппаратная безопасность \| 001,4 ")
</dt> </dl>

Указывает, поддерживает ли система аппаратную операцию сброса.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (3)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (4)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Не реализовано** (5)


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

[**\_Система CIM**](cim-system.md)
</dt> </dl>

 

