---
description: Класс CIM \_ TapeDrive представляет ленточный накопитель в системе. Ленточные накопители в основном различаются тем, что доступ к ним можно получить только последовательно.
ms.assetid: 8b7f2277-e37d-4597-81bb-d3c8d4966a81
ms.tgt_platform: multiple
title: Класс CIM_TapeDrive (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.Availability
- CIM_TapeDrive.Capabilities
- CIM_TapeDrive.CapabilityDescriptions
- CIM_TapeDrive.Caption
- CIM_TapeDrive.CompressionMethod
- CIM_TapeDrive.ConfigManagerErrorCode
- CIM_TapeDrive.ConfigManagerUserConfig
- CIM_TapeDrive.CreationClassName
- CIM_TapeDrive.DefaultBlockSize
- CIM_TapeDrive.Description
- CIM_TapeDrive.DeviceID
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.ErrorCleared
- CIM_TapeDrive.ErrorDescription
- CIM_TapeDrive.ErrorMethodology
- CIM_TapeDrive.InstallDate
- CIM_TapeDrive.LastErrorCode
- CIM_TapeDrive.MaxBlockSize
- CIM_TapeDrive.MaxMediaSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.MinBlockSize
- CIM_TapeDrive.Name
- CIM_TapeDrive.NeedsCleaning
- CIM_TapeDrive.NumberOfMediaSupported
- CIM_TapeDrive.Padding
- CIM_TapeDrive.PNPDeviceID
- CIM_TapeDrive.PowerManagementCapabilities
- CIM_TapeDrive.PowerManagementSupported
- CIM_TapeDrive.Status
- CIM_TapeDrive.StatusInfo
- CIM_TapeDrive.SystemCreationClassName
- CIM_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 184b855d5989c77292e51e8b477c5392893deccb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896530"
---
# <a name="cim_tapedrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="11a59-104">Класс CIM_TapeDrive (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="11a59-104">CIM_TapeDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="11a59-105">Класс **CIM \_ TapeDrive** представляет ленточный накопитель в системе.</span><span class="sxs-lookup"><span data-stu-id="11a59-105">The **CIM\_TapeDrive** class represents a tape drive on the system.</span></span> <span data-ttu-id="11a59-106">Ленточные накопители в основном различаются тем, что доступ к ним можно получить только последовательно.</span><span class="sxs-lookup"><span data-stu-id="11a59-106">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="11a59-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="11a59-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="11a59-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="11a59-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="11a59-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="11a59-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="11a59-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="11a59-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a59-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11a59-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="11a59-112">Члены</span><span class="sxs-lookup"><span data-stu-id="11a59-112">Members</span></span>

<span data-ttu-id="11a59-113">Класс **CIM \_ TapeDrive** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="11a59-113">The **CIM\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="11a59-114">Методы</span><span class="sxs-lookup"><span data-stu-id="11a59-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="11a59-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="11a59-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="11a59-116">Методы</span><span class="sxs-lookup"><span data-stu-id="11a59-116">Methods</span></span>

<span data-ttu-id="11a59-117">Класс **CIM \_ TapeDrive** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="11a59-117">The **CIM\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="11a59-118">Метод</span><span class="sxs-lookup"><span data-stu-id="11a59-118">Method</span></span>                                                               | <span data-ttu-id="11a59-119">Описание</span><span class="sxs-lookup"><span data-stu-id="11a59-119">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11a59-120">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="11a59-120">**Reset**</span></span>](reset-method-in-class-cim-tapedrive.md)                 | <span data-ttu-id="11a59-121">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="11a59-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="11a59-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="11a59-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="11a59-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="11a59-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-tapedrive.md) | <span data-ttu-id="11a59-124">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="11a59-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="11a59-125">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="11a59-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="11a59-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="11a59-126">Properties</span></span>

<span data-ttu-id="11a59-127">Класс **CIM \_ TapeDrive** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="11a59-127">The **CIM\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11a59-128">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="11a59-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11a59-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-131">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="11a59-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-132">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="11a59-132">Availability and status of the device.</span></span>

<span data-ttu-id="11a59-133">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="11a59-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="11a59-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11a59-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="11a59-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="11a59-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="11a59-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="11a59-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="11a59-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="11a59-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="11a59-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="11a59-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="11a59-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="11a59-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="11a59-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="11a59-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="11a59-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="11a59-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="11a59-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="11a59-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="11a59-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="11a59-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="11a59-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="11a59-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="11a59-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="11a59-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="11a59-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-147">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="11a59-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="11a59-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="11a59-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-149">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="11a59-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="11a59-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="11a59-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-151">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="11a59-151">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="11a59-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="11a59-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="11a59-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="11a59-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-154">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="11a59-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="11a59-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="11a59-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-156">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="11a59-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="11a59-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="11a59-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-158">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="11a59-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="11a59-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="11a59-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-160">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="11a59-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="11a59-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="11a59-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-162">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="11a59-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="11a59-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="11a59-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-164">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="11a59-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="11a59-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-166">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Устройства хранения DMTF \| 001,9 "," MIF. \|Устройства хранения DMTF \| 001,11 "," MIF. \|Устройства хранения DMTF \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="11a59-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-167">Возможности устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="11a59-167">Capabilities of the media access device.</span></span> <span data-ttu-id="11a59-168">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-168">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11a59-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="11a59-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-170">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="11a59-170">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="11a59-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="11a59-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-172">Другое</span><span class="sxs-lookup"><span data-stu-id="11a59-172">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="11a59-173"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Последовательный доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="11a59-173"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-174">Последовательный доступ.</span><span class="sxs-lookup"><span data-stu-id="11a59-174">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="11a59-175"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Произвольный доступ** (3)</span><span class="sxs-lookup"><span data-stu-id="11a59-175"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-176">Произвольный доступ.</span><span class="sxs-lookup"><span data-stu-id="11a59-176">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="11a59-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Поддерживает запись** (4)</span><span class="sxs-lookup"><span data-stu-id="11a59-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-178">Запись.</span><span class="sxs-lookup"><span data-stu-id="11a59-178">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="11a59-179"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Шифрование** (5)</span><span class="sxs-lookup"><span data-stu-id="11a59-179"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-180">Шифрование.</span><span class="sxs-lookup"><span data-stu-id="11a59-180">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="11a59-181"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Сжатие** (6)</span><span class="sxs-lookup"><span data-stu-id="11a59-181"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-182">Сжатие.</span><span class="sxs-lookup"><span data-stu-id="11a59-182">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="11a59-183"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Поддерживает** съемные носители (7)</span><span class="sxs-lookup"><span data-stu-id="11a59-183"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-184">Съемный носитель.</span><span class="sxs-lookup"><span data-stu-id="11a59-184">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="11a59-185"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Очистка вручную** (8)</span><span class="sxs-lookup"><span data-stu-id="11a59-185"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-186">Очистка вручную.</span><span class="sxs-lookup"><span data-stu-id="11a59-186">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="11a59-187"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Автоматическая очистка** (9)</span><span class="sxs-lookup"><span data-stu-id="11a59-187"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-188">Автоматическая очистка.</span><span class="sxs-lookup"><span data-stu-id="11a59-188">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="11a59-189"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Интеллектуальное уведомление** (10)</span><span class="sxs-lookup"><span data-stu-id="11a59-189"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-190">ИНТЕЛЛЕКТУАЛЬНое уведомление.</span><span class="sxs-lookup"><span data-stu-id="11a59-190">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="11a59-191"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Поддержка двусторонних носителей** (11)</span><span class="sxs-lookup"><span data-stu-id="11a59-191"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-192">Различает устройство, которое может получить доступ к обеим сторонам двусторонних носителей с устройства, которое считывает только одну сторону и требует включения носителя.</span><span class="sxs-lookup"><span data-stu-id="11a59-192">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="11a59-193"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Извлечение с отключением не требуется** (12)</span><span class="sxs-lookup"><span data-stu-id="11a59-193"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-194">Указывает, что носитель не обязательно должен быть явно извлечен с устройства перед обращением к элементу выбора.</span><span class="sxs-lookup"><span data-stu-id="11a59-194">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="11a59-195">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="11a59-195">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-196">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="11a59-196">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="11a59-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-198">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="11a59-198">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-199">Строки произвольной формы, содержащие подробные пояснения к функциям доступа к устройствам, указанным в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="11a59-199">Free-form strings that provide detailed explanations for the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="11a59-200">Обратите внимание, что каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="11a59-200">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="11a59-201">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-202">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="11a59-202">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-205">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="11a59-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-206">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="11a59-206">Short textual description of the object.</span></span>

<span data-ttu-id="11a59-207">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-207">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-208">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="11a59-208">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-209">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11a59-211">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="11a59-211">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="11a59-212">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="11a59-212">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="11a59-213">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="11a59-213">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="11a59-214">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="11a59-214">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="11a59-215">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-215">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="11a59-216">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="11a59-216">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="11a59-217">Схема сжатия неизвестна или не описана.</span><span class="sxs-lookup"><span data-stu-id="11a59-217">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="11a59-218">("Сжатый")</span><span class="sxs-lookup"><span data-stu-id="11a59-218">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="11a59-219">Логический файл сжат, но схема сжатия неизвестна или не описана</span><span class="sxs-lookup"><span data-stu-id="11a59-219">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="11a59-220">("Не сжато")</span><span class="sxs-lookup"><span data-stu-id="11a59-220">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="11a59-221">Если логический файл не сжат</span><span class="sxs-lookup"><span data-stu-id="11a59-221">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="11a59-222">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="11a59-222">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-223">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11a59-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-225">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="11a59-225">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-226">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="11a59-226">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="11a59-227">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-227">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="11a59-228"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="11a59-228"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="11a59-229"> (0)</span><span class="sxs-lookup"><span data-stu-id="11a59-229">(0)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-230">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="11a59-230">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="11a59-231"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="11a59-231"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="11a59-232">(1)</span><span class="sxs-lookup"><span data-stu-id="11a59-232">(1)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-233">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="11a59-233">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="11a59-234"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="11a59-234"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="11a59-235">(2)</span><span class="sxs-lookup"><span data-stu-id="11a59-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="11a59-236"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="11a59-236"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="11a59-237">(3)</span><span class="sxs-lookup"><span data-stu-id="11a59-237">(3)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-238">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11a59-238">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="11a59-239"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="11a59-239"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="11a59-240">(4)</span><span class="sxs-lookup"><span data-stu-id="11a59-240">(4)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-241">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="11a59-241">Device is not working properly.</span></span> <span data-ttu-id="11a59-242">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="11a59-242">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="11a59-243"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="11a59-243"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="11a59-244">(5)</span><span class="sxs-lookup"><span data-stu-id="11a59-244">(5)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-245">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="11a59-245">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="11a59-246"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="11a59-246"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="11a59-247"> (6)</span><span class="sxs-lookup"><span data-stu-id="11a59-247">(6)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-248">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="11a59-248">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="11a59-249"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="11a59-249"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="11a59-250">(7)</span><span class="sxs-lookup"><span data-stu-id="11a59-250">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="11a59-251"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="11a59-251"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="11a59-252">(8)</span><span class="sxs-lookup"><span data-stu-id="11a59-252">(8)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-253">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="11a59-253">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="11a59-254"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="11a59-254"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="11a59-255">(9)</span><span class="sxs-lookup"><span data-stu-id="11a59-255">(9)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-256">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="11a59-256">Device is not working properly.</span></span> <span data-ttu-id="11a59-257">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="11a59-257">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="11a59-258"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="11a59-258"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="11a59-259">(10)</span><span class="sxs-lookup"><span data-stu-id="11a59-259">(10)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-260">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="11a59-260">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="11a59-261"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="11a59-261"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="11a59-262">(11)</span><span class="sxs-lookup"><span data-stu-id="11a59-262">(11)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-263">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="11a59-263">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="11a59-264"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="11a59-264"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="11a59-265">(12)</span><span class="sxs-lookup"><span data-stu-id="11a59-265">(12)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-266">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="11a59-266">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="11a59-267"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="11a59-267"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="11a59-268">(13)</span><span class="sxs-lookup"><span data-stu-id="11a59-268">(13)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-269">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="11a59-269">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="11a59-270"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="11a59-270"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="11a59-271">(14)</span><span class="sxs-lookup"><span data-stu-id="11a59-271">(14)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-272">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="11a59-272">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="11a59-273"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="11a59-273"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="11a59-274">(15)</span><span class="sxs-lookup"><span data-stu-id="11a59-274">(15)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-275">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="11a59-275">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="11a59-276"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="11a59-276"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="11a59-277">(16)</span><span class="sxs-lookup"><span data-stu-id="11a59-277">(16)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-278">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="11a59-278">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="11a59-279"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="11a59-279"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="11a59-280">(17)</span><span class="sxs-lookup"><span data-stu-id="11a59-280">(17)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-281">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="11a59-281">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="11a59-282"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="11a59-282"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="11a59-283">(18)</span><span class="sxs-lookup"><span data-stu-id="11a59-283">(18)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-284">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="11a59-284">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="11a59-285"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="11a59-285"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="11a59-286">(19)</span><span class="sxs-lookup"><span data-stu-id="11a59-286">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="11a59-287"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="11a59-287"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="11a59-288">(20)</span><span class="sxs-lookup"><span data-stu-id="11a59-288">(20)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-289">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="11a59-289">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="11a59-290"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="11a59-290"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="11a59-291">(21)</span><span class="sxs-lookup"><span data-stu-id="11a59-291">(21)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-292">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="11a59-292">System failure.</span></span> <span data-ttu-id="11a59-293">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="11a59-293">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="11a59-294">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="11a59-294">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="11a59-295"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="11a59-295"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="11a59-296">(22)</span><span class="sxs-lookup"><span data-stu-id="11a59-296">(22)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-297">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="11a59-297">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="11a59-298"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="11a59-298"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="11a59-299">(23)</span><span class="sxs-lookup"><span data-stu-id="11a59-299">(23)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-300">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="11a59-300">System failure.</span></span> <span data-ttu-id="11a59-301">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="11a59-301">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="11a59-302"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="11a59-302"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="11a59-303">(24)</span><span class="sxs-lookup"><span data-stu-id="11a59-303">(24)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-304">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="11a59-304">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="11a59-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="11a59-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="11a59-306">(25)</span><span class="sxs-lookup"><span data-stu-id="11a59-306">(25)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-307">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="11a59-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="11a59-308"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="11a59-308"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="11a59-309">(26)</span><span class="sxs-lookup"><span data-stu-id="11a59-309">(26)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-310">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="11a59-310">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="11a59-311"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="11a59-311"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="11a59-312">(27)</span><span class="sxs-lookup"><span data-stu-id="11a59-312">(27)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-313">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="11a59-313">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="11a59-314"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="11a59-314"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="11a59-315">(28)</span><span class="sxs-lookup"><span data-stu-id="11a59-315">(28)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-316">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="11a59-316">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="11a59-317"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="11a59-317"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="11a59-318">(29)</span><span class="sxs-lookup"><span data-stu-id="11a59-318">(29)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-319">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="11a59-319">Device is disabled.</span></span> <span data-ttu-id="11a59-320">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="11a59-320">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="11a59-321"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="11a59-321"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="11a59-322">(30)</span><span class="sxs-lookup"><span data-stu-id="11a59-322">(30)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-323">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="11a59-323">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="11a59-324"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="11a59-324"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="11a59-325">1-31</span><span class="sxs-lookup"><span data-stu-id="11a59-325">(31)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-326">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="11a59-326">Device is not working properly.</span></span> <span data-ttu-id="11a59-327">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="11a59-327">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="11a59-328">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="11a59-328">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-329">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="11a59-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-331">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="11a59-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-332">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="11a59-332">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="11a59-333">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-333">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-334">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="11a59-334">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-335">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-337">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11a59-337">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11a59-338">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="11a59-338">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="11a59-339">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="11a59-339">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="11a59-340">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-341">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="11a59-341">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-342">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="11a59-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-344">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="11a59-344">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-345">Размер блока по умолчанию для устройства (в байтах).</span><span class="sxs-lookup"><span data-stu-id="11a59-345">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="11a59-346">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-346">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="11a59-347">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="11a59-347">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-348">**Описание**</span><span class="sxs-lookup"><span data-stu-id="11a59-348">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-351">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="11a59-351">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-352">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="11a59-352">Textual description of the object.</span></span>

<span data-ttu-id="11a59-353">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-353">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-354">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="11a59-354">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-357">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11a59-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11a59-358">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="11a59-358">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="11a59-359">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-360">**еотварнингзонесизе**</span><span class="sxs-lookup"><span data-stu-id="11a59-360">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-361">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11a59-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-363">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="11a59-363">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-364">Размер (в байтах) области, обозначенной как конец ленты.</span><span class="sxs-lookup"><span data-stu-id="11a59-364">Size, in bytes, of the area designated as end-of-tape.</span></span> <span data-ttu-id="11a59-365">При доступе в этой области создается предупреждение на конец ленты.</span><span class="sxs-lookup"><span data-stu-id="11a59-365">Access in this area generates an end-of-tape warning.</span></span>

</dd> <dt>

<span data-ttu-id="11a59-366">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="11a59-366">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-367">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="11a59-367">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11a59-369">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="11a59-369">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="11a59-370">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-371">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="11a59-371">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-372">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11a59-374">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="11a59-374">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="11a59-375">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-376">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="11a59-376">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-377">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11a59-379">Произвольная строка, описывающая типы обнаружения ошибок и исправления, поддерживаемые устройством.</span><span class="sxs-lookup"><span data-stu-id="11a59-379">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="11a59-380">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-380">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-381">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="11a59-381">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-382">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="11a59-382">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-384">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="11a59-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-385">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="11a59-385">Date and time the object was installed.</span></span> <span data-ttu-id="11a59-386">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="11a59-386">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="11a59-387">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-388">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="11a59-388">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-389">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11a59-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11a59-391">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="11a59-391">Last error code reported by the logical device.</span></span>

<span data-ttu-id="11a59-392">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-393">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="11a59-393">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-394">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="11a59-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-396">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="11a59-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-397">Максимальный размер блока в байтах для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="11a59-397">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="11a59-398">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-398">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="11a59-399">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="11a59-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-400">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="11a59-400">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-401">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="11a59-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-403">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="11a59-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-404">Максимальный размер носителя, поддерживаемого устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="11a59-404">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="11a59-405">Килобайты интерпретируется как число байтов, умноженное на 1000 (а не на число байтов, умноженное на 1024).</span><span class="sxs-lookup"><span data-stu-id="11a59-405">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="11a59-406">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-406">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="11a59-407">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="11a59-407">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-408">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="11a59-408">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-409">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11a59-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11a59-411">Максимальное число разделов для ленточного накопителя.</span><span class="sxs-lookup"><span data-stu-id="11a59-411">Maximum partition count for the tape drive.</span></span>

</dd> <dt>

<span data-ttu-id="11a59-412">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="11a59-412">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-413">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="11a59-413">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-415">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="11a59-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-416">Минимальный размер блока (в байтах) для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="11a59-416">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="11a59-417">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="11a59-418">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="11a59-418">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-419">**Name**</span><span class="sxs-lookup"><span data-stu-id="11a59-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-420">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-422">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="11a59-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-423">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="11a59-423">Label by which the object is known.</span></span> <span data-ttu-id="11a59-424">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="11a59-424">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="11a59-425">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-426">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="11a59-426">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-427">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="11a59-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11a59-429">Если задано **значение true**, устройству доступа к носителю требуется очистка.</span><span class="sxs-lookup"><span data-stu-id="11a59-429">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="11a59-430">Возможность ручной или автоматической очистки указывается в свойстве массива **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="11a59-430">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="11a59-431">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-432">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="11a59-432">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-433">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11a59-433">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-434">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11a59-435">Если устройство доступа к носителю поддерживает несколько отдельных носителей, это свойство определяет максимальное число, которое может поддерживаться или вставляться.</span><span class="sxs-lookup"><span data-stu-id="11a59-435">When the media access device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

<span data-ttu-id="11a59-436">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-436">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-437">**Заполнение**</span><span class="sxs-lookup"><span data-stu-id="11a59-437">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-438">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="11a59-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-439">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-440">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="11a59-440">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-441">Число байтов, вставленных между блоками на ленточном носителе.</span><span class="sxs-lookup"><span data-stu-id="11a59-441">Number of bytes inserted between blocks on a tape media.</span></span>

</dd> <dt>

<span data-ttu-id="11a59-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="11a59-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-443">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-445">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="11a59-445">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-446">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="11a59-446">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="11a59-447">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="11a59-448">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="11a59-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="11a59-449">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="11a59-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-450">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="11a59-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="11a59-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11a59-452">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="11a59-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="11a59-453">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11a59-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="11a59-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="11a59-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="11a59-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-456">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="11a59-456">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="11a59-457"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="11a59-457"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="11a59-458"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="11a59-458"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-459">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="11a59-459">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="11a59-460"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="11a59-460"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-461">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="11a59-461">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="11a59-462"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="11a59-462"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-463">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="11a59-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="11a59-464">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="11a59-464">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="11a59-465">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="11a59-465">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="11a59-466"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="11a59-466"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-467">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="11a59-467">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="11a59-468"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="11a59-468"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="11a59-469">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="11a59-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="11a59-470">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="11a59-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-471">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="11a59-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11a59-473">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="11a59-473">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="11a59-474">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="11a59-474">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="11a59-475">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="11a59-475">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="11a59-476">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="11a59-476">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="11a59-477">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-478">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="11a59-478">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-479">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-480">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-481">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="11a59-481">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-482">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="11a59-482">Current status of the object.</span></span> <span data-ttu-id="11a59-483">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-483">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="11a59-484">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="11a59-484">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="11a59-485">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="11a59-485">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="11a59-486">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="11a59-486">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="11a59-487">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="11a59-487">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11a59-488">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="11a59-488">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="11a59-489">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="11a59-489">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="11a59-490">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="11a59-490">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="11a59-491">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="11a59-491">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="11a59-492">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="11a59-492">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="11a59-493">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="11a59-493">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="11a59-494">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="11a59-494">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="11a59-495">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="11a59-495">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="11a59-496">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="11a59-496">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="11a59-497">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="11a59-497">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-498">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="11a59-498">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-499">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-500">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="11a59-500">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="11a59-501">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="11a59-501">State of the logical device.</span></span> <span data-ttu-id="11a59-502">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="11a59-502">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="11a59-503">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="11a59-504">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="11a59-504">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="11a59-505">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="11a59-505">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="11a59-506">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="11a59-506">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="11a59-507">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="11a59-507">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="11a59-508">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="11a59-508">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="11a59-509">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="11a59-509">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-510">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-511">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-512">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11a59-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11a59-513">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="11a59-513">Scoping system's creation class name.</span></span>

<span data-ttu-id="11a59-514">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="11a59-515">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="11a59-515">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11a59-516">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11a59-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11a59-517">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11a59-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11a59-518">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="11a59-518">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="11a59-519">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="11a59-519">Scoping system's name.</span></span>

<span data-ttu-id="11a59-520">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="11a59-520">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11a59-521">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11a59-521">Remarks</span></span>

<span data-ttu-id="11a59-522">Класс **CIM \_ TapeDrive** является производным от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-522">The **CIM\_TapeDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="11a59-523">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="11a59-523">WMI does not implement this class.</span></span> <span data-ttu-id="11a59-524">Классы WMI, производные от **CIM \_ TapeDrive**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="11a59-524">For WMI classes derived from **CIM\_TapeDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="11a59-525">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="11a59-525">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="11a59-526">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="11a59-526">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="11a59-527">Требования</span><span class="sxs-lookup"><span data-stu-id="11a59-527">Requirements</span></span>



| <span data-ttu-id="11a59-528">Требование</span><span class="sxs-lookup"><span data-stu-id="11a59-528">Requirement</span></span> | <span data-ttu-id="11a59-529">Значение</span><span class="sxs-lookup"><span data-stu-id="11a59-529">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11a59-530">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11a59-530">Minimum supported client</span></span><br/> | <span data-ttu-id="11a59-531">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11a59-531">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="11a59-532">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11a59-532">Minimum supported server</span></span><br/> | <span data-ttu-id="11a59-533">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11a59-533">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="11a59-534">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="11a59-534">Namespace</span></span><br/>                | <span data-ttu-id="11a59-535">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="11a59-535">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="11a59-536">MOF</span><span class="sxs-lookup"><span data-stu-id="11a59-536">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11a59-537"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11a59-537"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="11a59-538">DLL</span><span class="sxs-lookup"><span data-stu-id="11a59-538">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11a59-539"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11a59-539"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11a59-540">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11a59-540">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a59-541">**\_МЕДИААКЦЕССДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="11a59-541">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

