---
description: Класс CIM \_ сетевого адаптера является абстрактным классом, который определяет основные понятия сетевого оборудования (например, постоянный адрес или скорость работы). Сведения передаются с помощью Ассоциации CIM \_ девицесапимплементатион.
ms.assetid: dd44e05a-1124-42c2-aa69-340c06da35a2
ms.tgt_platform: multiple
title: Класс CIM_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkAdapter
- CIM_NetworkAdapter.AutoSense
- CIM_NetworkAdapter.Availability
- CIM_NetworkAdapter.Caption
- CIM_NetworkAdapter.ConfigManagerErrorCode
- CIM_NetworkAdapter.ConfigManagerUserConfig
- CIM_NetworkAdapter.CreationClassName
- CIM_NetworkAdapter.Description
- CIM_NetworkAdapter.DeviceID
- CIM_NetworkAdapter.ErrorCleared
- CIM_NetworkAdapter.ErrorDescription
- CIM_NetworkAdapter.InstallDate
- CIM_NetworkAdapter.LastErrorCode
- CIM_NetworkAdapter.MaxSpeed
- CIM_NetworkAdapter.Name
- CIM_NetworkAdapter.NetworkAddresses
- CIM_NetworkAdapter.PermanentAddress
- CIM_NetworkAdapter.PNPDeviceID
- CIM_NetworkAdapter.PowerManagementCapabilities
- CIM_NetworkAdapter.PowerManagementSupported
- CIM_NetworkAdapter.Speed
- CIM_NetworkAdapter.Status
- CIM_NetworkAdapter.StatusInfo
- CIM_NetworkAdapter.SystemCreationClassName
- CIM_NetworkAdapter.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 76ec70bb74d74514dfe037c9e67604b29aee541a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141887"
---
# <a name="cim_networkadapter-class"></a><span data-ttu-id="f158e-104">\_Класс CIM сетевого адаптера</span><span class="sxs-lookup"><span data-stu-id="f158e-104">CIM\_NetworkAdapter class</span></span>

<span data-ttu-id="f158e-105">Класс **CIM \_ сетевого адаптера** является абстрактным классом, который определяет основные понятия сетевого оборудования (например, постоянный адрес или скорость работы).</span><span class="sxs-lookup"><span data-stu-id="f158e-105">The **CIM\_NetworkAdapter** class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="f158e-106">Сведения передаются с помощью ассоциации [**CIM \_ девицесапимплементатион**](cim-devicesapimplementation.md) .</span><span class="sxs-lookup"><span data-stu-id="f158e-106">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

<span data-ttu-id="f158e-107">Сетевые адаптеры и связанные конечные точки представляют потенциальную возможность подключения между одноранговыми узлами.</span><span class="sxs-lookup"><span data-stu-id="f158e-107">Network adapters and related endpoints represent the potential for connectivity among peers.</span></span> <span data-ttu-id="f158e-108">Возможность подключения существенно отличается от главного или подчиненного контроллера, а также от контроллеров [**CIM \_**](cim-controller.md)или управляемых отношений.</span><span class="sxs-lookup"><span data-stu-id="f158e-108">The potential for connectivity is significantly different from the master or subordinate and controller or controlled-by relationships of [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="f158e-109">Однако иногда одно устройство действует как сетевой адаптер, так и контроллер, например, когда адаптер волоконного канала работает в качестве контроллера SCSI компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="f158e-109">Occasionally, however, a single device acts as both a network adapter and a controller, for example, when a fiber channel adapter operates as a computer system's SCSI controller.</span></span> <span data-ttu-id="f158e-110">В этом случае аспекты устройства ориентированы на сеть, а другие являются ориентированными на контроллер.</span><span class="sxs-lookup"><span data-stu-id="f158e-110">In which case, aspects of the device are network oriented and others are controller oriented.</span></span> <span data-ttu-id="f158e-111">Для связывания различных аспектов устройства необходимо создать экземпляр контроллера и классов адаптеров, а также связь удостоверения устройства.</span><span class="sxs-lookup"><span data-stu-id="f158e-111">The controller and adapter classes should be instantiated and a device identity relationship should also be created to link the different aspects of the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f158e-112">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="f158e-112">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f158e-113">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f158e-113">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f158e-114">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f158e-114">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f158e-115">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f158e-115">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f158e-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f158e-116">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C532-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_NetworkAdapter : CIM_LogicalDevice
{
  boolean  AutoSense;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxSpeed;
  string   Name;
  string   NetworkAddresses[];
  string   PermanentAddress;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="f158e-117">Члены</span><span class="sxs-lookup"><span data-stu-id="f158e-117">Members</span></span>

<span data-ttu-id="f158e-118">Класс **CIM \_ сетевого адаптера** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f158e-118">The **CIM\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="f158e-119">Методы</span><span class="sxs-lookup"><span data-stu-id="f158e-119">Methods</span></span>](#methods)
-   [<span data-ttu-id="f158e-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="f158e-120">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f158e-121">Методы</span><span class="sxs-lookup"><span data-stu-id="f158e-121">Methods</span></span>

<span data-ttu-id="f158e-122">Класс **CIM \_ сетевого адаптера** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f158e-122">The **CIM\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="f158e-123">Метод</span><span class="sxs-lookup"><span data-stu-id="f158e-123">Method</span></span>                                                                    | <span data-ttu-id="f158e-124">Описание</span><span class="sxs-lookup"><span data-stu-id="f158e-124">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f158e-125">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="f158e-125">**Reset**</span></span>](reset-method-in-class-cim-networkadapter.md)                 | <span data-ttu-id="f158e-126">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f158e-126">Requests a reset of the logical device.</span></span> <span data-ttu-id="f158e-127">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="f158e-127">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="f158e-128">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f158e-128">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-networkadapter.md) | <span data-ttu-id="f158e-129">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="f158e-129">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f158e-130">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="f158e-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f158e-131">Свойства</span><span class="sxs-lookup"><span data-stu-id="f158e-131">Properties</span></span>

<span data-ttu-id="f158e-132">Класс **CIM \_ сетевого адаптера** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f158e-132">The **CIM\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f158e-133">**Авточувствительность**</span><span class="sxs-lookup"><span data-stu-id="f158e-133">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-134">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f158e-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f158e-136">Если **значение — true**, сетевой адаптер может автоматически определить скорость или другие характеристики связи подключенного сетевого носителя.</span><span class="sxs-lookup"><span data-stu-id="f158e-136">If **TRUE**, the network adapter can automatically determine the speed or other communications characteristics of the attached network media.</span></span>

</dd> <dt>

<span data-ttu-id="f158e-137">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="f158e-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-138">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f158e-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-140">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="f158e-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-141">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="f158e-141">Availability and status of the device.</span></span>

<span data-ttu-id="f158e-142">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f158e-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f158e-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f158e-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f158e-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f158e-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="f158e-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f158e-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="f158e-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f158e-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="f158e-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f158e-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="f158e-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f158e-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="f158e-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f158e-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="f158e-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f158e-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="f158e-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f158e-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="f158e-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f158e-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="f158e-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f158e-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="f158e-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f158e-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="f158e-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-156">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="f158e-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f158e-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="f158e-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-158">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="f158e-158">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f158e-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="f158e-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-160">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="f158e-160">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f158e-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="f158e-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f158e-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="f158e-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-163">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="f158e-163">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f158e-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="f158e-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-165">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="f158e-165">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f158e-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="f158e-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-167">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="f158e-167">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f158e-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="f158e-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-169">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="f158e-169">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f158e-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="f158e-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-171">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="f158e-171">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f158e-172">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f158e-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f158e-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-175">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f158e-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-176">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f158e-176">Short textual description of the object.</span></span>

<span data-ttu-id="f158e-177">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f158e-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-178">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="f158e-178">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-179">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f158e-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-181">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f158e-181">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-182">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f158e-182">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="f158e-183">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-183">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f158e-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="f158e-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f158e-185"> (0)</span><span class="sxs-lookup"><span data-stu-id="f158e-185">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-186">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="f158e-186">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f158e-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="f158e-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f158e-188">(1)</span><span class="sxs-lookup"><span data-stu-id="f158e-188">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-189">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="f158e-189">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f158e-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f158e-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f158e-191">(2)</span><span class="sxs-lookup"><span data-stu-id="f158e-191">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f158e-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="f158e-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f158e-193">(3)</span><span class="sxs-lookup"><span data-stu-id="f158e-193">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-194">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f158e-194">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f158e-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="f158e-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f158e-196">(4)</span><span class="sxs-lookup"><span data-stu-id="f158e-196">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-197">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="f158e-197">Device is not working properly.</span></span> <span data-ttu-id="f158e-198">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="f158e-198">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f158e-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="f158e-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f158e-200">(5)</span><span class="sxs-lookup"><span data-stu-id="f158e-200">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-201">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="f158e-201">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f158e-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="f158e-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f158e-203"> (6)</span><span class="sxs-lookup"><span data-stu-id="f158e-203">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-204">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="f158e-204">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f158e-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="f158e-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f158e-206">(7)</span><span class="sxs-lookup"><span data-stu-id="f158e-206">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f158e-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="f158e-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f158e-208">(8)</span><span class="sxs-lookup"><span data-stu-id="f158e-208">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-209">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="f158e-209">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f158e-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="f158e-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f158e-211">(9)</span><span class="sxs-lookup"><span data-stu-id="f158e-211">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-212">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="f158e-212">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f158e-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="f158e-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f158e-214">(10)</span><span class="sxs-lookup"><span data-stu-id="f158e-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-215">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="f158e-215">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f158e-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="f158e-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f158e-217">(11)</span><span class="sxs-lookup"><span data-stu-id="f158e-217">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-218">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="f158e-218">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f158e-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="f158e-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f158e-220">(12)</span><span class="sxs-lookup"><span data-stu-id="f158e-220">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-221">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="f158e-221">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f158e-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f158e-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f158e-223">(13)</span><span class="sxs-lookup"><span data-stu-id="f158e-223">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-224">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="f158e-224">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f158e-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="f158e-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f158e-226">(14)</span><span class="sxs-lookup"><span data-stu-id="f158e-226">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-227">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="f158e-227">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f158e-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="f158e-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f158e-229">(15)</span><span class="sxs-lookup"><span data-stu-id="f158e-229">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-230">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="f158e-230">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f158e-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="f158e-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f158e-232">(16)</span><span class="sxs-lookup"><span data-stu-id="f158e-232">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-233">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="f158e-233">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f158e-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="f158e-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f158e-235">(17)</span><span class="sxs-lookup"><span data-stu-id="f158e-235">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-236">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="f158e-236">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f158e-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f158e-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f158e-238">(18)</span><span class="sxs-lookup"><span data-stu-id="f158e-238">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-239">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="f158e-239">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f158e-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="f158e-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f158e-241">(19)</span><span class="sxs-lookup"><span data-stu-id="f158e-241">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f158e-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="f158e-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f158e-243">(20)</span><span class="sxs-lookup"><span data-stu-id="f158e-243">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-244">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="f158e-244">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f158e-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="f158e-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f158e-246">(21)</span><span class="sxs-lookup"><span data-stu-id="f158e-246">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-247">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="f158e-247">System failure.</span></span> <span data-ttu-id="f158e-248">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="f158e-248">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f158e-249">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="f158e-249">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f158e-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="f158e-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f158e-251">(22)</span><span class="sxs-lookup"><span data-stu-id="f158e-251">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-252">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="f158e-252">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f158e-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="f158e-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f158e-254">(23)</span><span class="sxs-lookup"><span data-stu-id="f158e-254">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-255">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="f158e-255">System failure.</span></span> <span data-ttu-id="f158e-256">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="f158e-256">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f158e-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="f158e-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f158e-258">(24)</span><span class="sxs-lookup"><span data-stu-id="f158e-258">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-259">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="f158e-259">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f158e-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="f158e-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f158e-261">(25)</span><span class="sxs-lookup"><span data-stu-id="f158e-261">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-262">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="f158e-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f158e-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="f158e-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f158e-264">(26)</span><span class="sxs-lookup"><span data-stu-id="f158e-264">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-265">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="f158e-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f158e-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="f158e-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f158e-267">(27)</span><span class="sxs-lookup"><span data-stu-id="f158e-267">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-268">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="f158e-268">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f158e-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="f158e-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f158e-270">(28)</span><span class="sxs-lookup"><span data-stu-id="f158e-270">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-271">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="f158e-271">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f158e-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="f158e-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f158e-273">(29)</span><span class="sxs-lookup"><span data-stu-id="f158e-273">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-274">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f158e-274">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f158e-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="f158e-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f158e-276">(30)</span><span class="sxs-lookup"><span data-stu-id="f158e-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-277">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="f158e-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f158e-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f158e-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f158e-279">1-31</span><span class="sxs-lookup"><span data-stu-id="f158e-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-280">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="f158e-280">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f158e-281">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="f158e-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-282">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f158e-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-284">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f158e-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-285">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f158e-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f158e-286">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f158e-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f158e-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-290">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f158e-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f158e-291">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f158e-291">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f158e-292">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="f158e-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f158e-293">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-294">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f158e-294">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-295">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f158e-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-297">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="f158e-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-298">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f158e-298">Textual description of the object.</span></span>

<span data-ttu-id="f158e-299">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f158e-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-300">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f158e-300">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f158e-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-303">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f158e-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f158e-304">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f158e-304">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="f158e-305">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-306">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="f158e-306">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-307">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f158e-307">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f158e-309">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="f158e-309">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="f158e-310">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-311">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f158e-311">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-312">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f158e-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f158e-314">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="f158e-314">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="f158e-315">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-316">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f158e-316">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-317">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f158e-317">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-319">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="f158e-319">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-320">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="f158e-320">Date and time the object was installed.</span></span> <span data-ttu-id="f158e-321">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="f158e-321">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f158e-322">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f158e-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-323">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="f158e-323">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-324">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f158e-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f158e-326">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="f158e-326">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f158e-327">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-328">**максспид**</span><span class="sxs-lookup"><span data-stu-id="f158e-328">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-329">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f158e-329">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-331">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="f158e-331">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-332">Максимальная скорость в битах в секунду (бит/с) для сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="f158e-332">Maximum speed, in bits per second (BPS), for the network adapter.</span></span>

<span data-ttu-id="f158e-333">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f158e-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-334">**Name**</span><span class="sxs-lookup"><span data-stu-id="f158e-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-335">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f158e-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-337">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="f158e-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-338">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="f158e-338">Label by which the object is known.</span></span> <span data-ttu-id="f158e-339">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="f158e-339">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f158e-340">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f158e-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-341">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="f158e-341">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-342">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="f158e-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f158e-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-344">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -сетевой адаптер 802, порт \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="f158e-344">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-345">Список сетевых адресов для адаптера.</span><span class="sxs-lookup"><span data-stu-id="f158e-345">List of network addresses for an adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f158e-346">**перманентаддресс**</span><span class="sxs-lookup"><span data-stu-id="f158e-346">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-347">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f158e-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-349">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| -сетевой адаптер 802, порт \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="f158e-349">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-350">Сетевой адрес жестко закодирован в адаптере.</span><span class="sxs-lookup"><span data-stu-id="f158e-350">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="f158e-351">Жестко заданный адрес можно изменить с помощью обновления встроенного по или конфигурации программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="f158e-351">The hard-coded address can be changed with a firmware upgrade or software configuration.</span></span> <span data-ttu-id="f158e-352">В случае изменения поле должно быть обновлено после внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="f158e-352">If changed, the field should be updated when the change is made.</span></span> <span data-ttu-id="f158e-353">Если для сетевого адаптера не существует жестко заданный адрес, это свойство следует оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="f158e-353">This property should be left blank if no hard-coded address exists for the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f158e-354">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f158e-354">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f158e-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-357">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f158e-357">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-358">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f158e-358">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="f158e-359">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f158e-360">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f158e-360">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="f158e-361">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="f158e-361">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-362">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f158e-362">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f158e-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f158e-364">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="f158e-364">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="f158e-365">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-365">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f158e-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f158e-366"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f158e-367"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="f158e-367"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f158e-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="f158e-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f158e-369"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="f158e-369"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-370">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="f158e-370">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f158e-371"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="f158e-371"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-372">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="f158e-372">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f158e-373"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="f158e-373"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-374">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="f158e-374">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="f158e-375">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="f158e-375">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="f158e-376">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="f158e-376">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f158e-377"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="f158e-377"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-378">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="f158e-378">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f158e-379"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="f158e-379"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f158e-380">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="f158e-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f158e-381">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="f158e-381">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-382">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f158e-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f158e-384">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="f158e-384">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="f158e-385">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="f158e-385">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f158e-386">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="f158e-386">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="f158e-387">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="f158e-387">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="f158e-388">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-388">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-389">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="f158e-389">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-390">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f158e-390">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-392">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| RFC1213-MIB. ифспид "," MIF. DMTF \| , сетевой адаптер 802 \| , порт 001,5 "), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) (" бит в секунду ")</span><span class="sxs-lookup"><span data-stu-id="f158e-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-393">Оценка текущей пропускной способности в бит/с.</span><span class="sxs-lookup"><span data-stu-id="f158e-393">Estimate of the current bandwidth, in BPS.</span></span> <span data-ttu-id="f158e-394">Для конечных точек, которые зависят от пропускной способности или для тех, для которых не может быть выполнена точная оценка, это свойство должно содержать номинальную пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="f158e-394">For endpoints that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="f158e-395">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f158e-395">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-396">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f158e-396">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-397">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f158e-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-398">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-399">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="f158e-399">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-400">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f158e-400">Current status of the object.</span></span>

<span data-ttu-id="f158e-401">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f158e-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f158e-402">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="f158e-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f158e-403">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="f158e-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f158e-404">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="f158e-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f158e-405">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="f158e-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f158e-406">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="f158e-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f158e-407">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="f158e-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f158e-408">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="f158e-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f158e-409">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="f158e-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f158e-410">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="f158e-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f158e-411">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="f158e-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f158e-412">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="f158e-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f158e-413">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="f158e-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f158e-414">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="f158e-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f158e-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f158e-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-416">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f158e-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-418">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f158e-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f158e-419">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f158e-419">State of the logical device.</span></span> <span data-ttu-id="f158e-420">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="f158e-420">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f158e-421">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f158e-422">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f158e-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f158e-423">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f158e-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f158e-424">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="f158e-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f158e-425">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="f158e-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f158e-426">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="f158e-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f158e-427">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="f158e-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-428">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f158e-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-430">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f158e-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f158e-431">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="f158e-431">Scoping system's creation class name.</span></span>

<span data-ttu-id="f158e-432">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f158e-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f158e-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f158e-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f158e-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f158e-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f158e-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f158e-436">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f158e-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f158e-437">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="f158e-437">Scoping system's name.</span></span>

<span data-ttu-id="f158e-438">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f158e-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f158e-439">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f158e-439">Remarks</span></span>

<span data-ttu-id="f158e-440">Класс **CIM \_ сетевого адаптера** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="f158e-440">The **CIM\_NetworkAdapter** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f158e-441">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="f158e-441">WMI does not implement this class.</span></span> <span data-ttu-id="f158e-442">Классы, производные от **CIM \_ сетевого адаптера**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f158e-442">For classes that are derived from **CIM\_NetworkAdapter**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f158e-443">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="f158e-443">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f158e-444">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f158e-444">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f158e-445">Требования</span><span class="sxs-lookup"><span data-stu-id="f158e-445">Requirements</span></span>



| <span data-ttu-id="f158e-446">Требование</span><span class="sxs-lookup"><span data-stu-id="f158e-446">Requirement</span></span> | <span data-ttu-id="f158e-447">Значение</span><span class="sxs-lookup"><span data-stu-id="f158e-447">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f158e-448">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f158e-448">Minimum supported client</span></span><br/> | <span data-ttu-id="f158e-449">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f158e-449">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f158e-450">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f158e-450">Minimum supported server</span></span><br/> | <span data-ttu-id="f158e-451">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f158e-451">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f158e-452">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f158e-452">Namespace</span></span><br/>                | <span data-ttu-id="f158e-453">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f158e-453">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f158e-454">MOF</span><span class="sxs-lookup"><span data-stu-id="f158e-454">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f158e-455"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f158e-455"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f158e-456">DLL</span><span class="sxs-lookup"><span data-stu-id="f158e-456">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f158e-457"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f158e-457"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f158e-458">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f158e-458">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f158e-459">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="f158e-459">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

