---
description: '\_Класс WMI TapeDrive для Win32 представляет ленточный накопитель в компьютерной системе под Windows. Ленточные накопители в основном различаются тем фактом, что доступ к ним можно получить только последовательно.'
ms.assetid: ceefec7b-a904-4b2f-a6b6-b84917a33023
ms.tgt_platform: multiple
title: Класс Win32_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TapeDrive
- Win32_TapeDrive.Reset
- Win32_TapeDrive.SetPowerState
- Win32_TapeDrive.Availability
- Win32_TapeDrive.Capabilities
- Win32_TapeDrive.CapabilityDescriptions
- Win32_TapeDrive.Caption
- Win32_TapeDrive.Compression
- Win32_TapeDrive.CompressionMethod
- Win32_TapeDrive.ConfigManagerErrorCode
- Win32_TapeDrive.ConfigManagerUserConfig
- Win32_TapeDrive.CreationClassName
- Win32_TapeDrive.DefaultBlockSize
- Win32_TapeDrive.Description
- Win32_TapeDrive.DeviceID
- Win32_TapeDrive.ECC
- Win32_TapeDrive.EOTWarningZoneSize
- Win32_TapeDrive.ErrorCleared
- Win32_TapeDrive.ErrorDescription
- Win32_TapeDrive.ErrorMethodology
- Win32_TapeDrive.FeaturesHigh
- Win32_TapeDrive.FeaturesLow
- Win32_TapeDrive.Id
- Win32_TapeDrive.InstallDate
- Win32_TapeDrive.LastErrorCode
- Win32_TapeDrive.Manufacturer
- Win32_TapeDrive.MaxBlockSize
- Win32_TapeDrive.MaxMediaSize
- Win32_TapeDrive.MaxPartitionCount
- Win32_TapeDrive.MediaType
- Win32_TapeDrive.MinBlockSize
- Win32_TapeDrive.Name
- Win32_TapeDrive.NeedsCleaning
- Win32_TapeDrive.NumberOfMediaSupported
- Win32_TapeDrive.Padding
- Win32_TapeDrive.PNPDeviceID
- Win32_TapeDrive.PowerManagementCapabilities
- Win32_TapeDrive.PowerManagementSupported
- Win32_TapeDrive.ReportSetMarks
- Win32_TapeDrive.Status
- Win32_TapeDrive.StatusInfo
- Win32_TapeDrive.SystemCreationClassName
- Win32_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c7e7d3b754a0399acb152dba043da269f67a06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655873"
---
# <a name="win32_tapedrive-class"></a><span data-ttu-id="ae999-104">\_Класс Win32 TapeDrive</span><span class="sxs-lookup"><span data-stu-id="ae999-104">Win32\_TapeDrive class</span></span>

<span data-ttu-id="ae999-105">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ TapeDrive для Win32** представляет ленточный накопитель в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="ae999-105">The **Win32\_TapeDrive** [WMI class](../wmisdk/retrieving-a-class.md) represents a tape drive on a computer system running Windows.</span></span> <span data-ttu-id="ae999-106">Ленточные накопители в основном различаются тем фактом, что доступ к ним можно получить только последовательно.</span><span class="sxs-lookup"><span data-stu-id="ae999-106">Tape drives are primarily distinguished by the fact that they can only be accessed sequentially.</span></span>

<span data-ttu-id="ae999-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ae999-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ae999-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ae999-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae999-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae999-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TapeDrive : CIM_TapeDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   Compression;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  uint32   ECC;
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   FeaturesHigh;
  uint32   FeaturesLow;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  string   MediaType;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ReportSetMarks;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="ae999-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ae999-110">Members</span></span>

<span data-ttu-id="ae999-111">Класс **Win32 \_ TapeDrive** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ae999-111">The **Win32\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="ae999-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ae999-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ae999-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ae999-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ae999-114">Методы</span><span class="sxs-lookup"><span data-stu-id="ae999-114">Methods</span></span>

<span data-ttu-id="ae999-115">Класс **Win32 \_ TapeDrive** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ae999-115">The **Win32\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="ae999-116">Метод</span><span class="sxs-lookup"><span data-stu-id="ae999-116">Method</span></span>            | <span data-ttu-id="ae999-117">Описание</span><span class="sxs-lookup"><span data-stu-id="ae999-117">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae999-118">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="ae999-118">**Reset**</span></span>         | <span data-ttu-id="ae999-119">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ae999-119">Not implemented.</span></span> <span data-ttu-id="ae999-120">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/>                 |
| <span data-ttu-id="ae999-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ae999-121">**SetPowerState**</span></span> | <span data-ttu-id="ae999-122">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="ae999-122">Not implemented.</span></span> <span data-ttu-id="ae999-123">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ae999-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="ae999-124">Properties</span></span>

<span data-ttu-id="ae999-125">Класс **Win32 \_ TapeDrive** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ae999-125">The **Win32\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae999-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="ae999-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae999-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-129">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="ae999-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="ae999-130">Availability and status of the device.</span></span>

<span data-ttu-id="ae999-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae999-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ae999-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae999-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="ae999-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ae999-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="ae999-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-135">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="ae999-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ae999-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="ae999-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ae999-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="ae999-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ae999-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="ae999-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ae999-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="ae999-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ae999-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="ae999-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ae999-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="ae999-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ae999-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="ae999-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ae999-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="ae999-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ae999-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="ae999-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ae999-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="ae999-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-146">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="ae999-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ae999-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="ae999-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-148">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="ae999-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ae999-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="ae999-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-150">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="ae999-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ae999-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="ae999-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ae999-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="ae999-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-153">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="ae999-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ae999-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="ae999-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-155">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="ae999-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ae999-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="ae999-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-157">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="ae999-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ae999-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="ae999-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-159">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="ae999-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ae999-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="ae999-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-161">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="ae999-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ae999-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="ae999-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-163">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ae999-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ae999-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-165">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. \|Устройства хранения DMTF \| 001,9 "," MIF. \|Устройства хранения DMTF \| 001,11 "," MIF. \|Устройства хранения DMTF \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="ae999-165">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-166">Массив возможностей устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="ae999-166">Array of capabilities of the media access device.</span></span> <span data-ttu-id="ae999-167">Например, устройство может поддерживать произвольный доступ, съемные носители и автоматическую очистку.</span><span class="sxs-lookup"><span data-stu-id="ae999-167">For example, the device may support Random Access, removable media and Automatic Cleaning.</span></span> <span data-ttu-id="ae999-168">В этом случае значения 3, 7 и 9 будут записаны в массив.</span><span class="sxs-lookup"><span data-stu-id="ae999-168">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="ae999-169">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae999-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ae999-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae999-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ae999-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="ae999-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Последовательный доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="ae999-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="ae999-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Произвольный доступ** (3)</span><span class="sxs-lookup"><span data-stu-id="ae999-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="ae999-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Поддерживает запись** (4)</span><span class="sxs-lookup"><span data-stu-id="ae999-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="ae999-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Шифрование** (5)</span><span class="sxs-lookup"><span data-stu-id="ae999-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="ae999-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Сжатие** (6)</span><span class="sxs-lookup"><span data-stu-id="ae999-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="ae999-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Поддерживает** съемные носители (7)</span><span class="sxs-lookup"><span data-stu-id="ae999-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-178">Поддержка съемных носителей</span><span class="sxs-lookup"><span data-stu-id="ae999-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="ae999-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Очистка вручную** (8)</span><span class="sxs-lookup"><span data-stu-id="ae999-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="ae999-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Автоматическая очистка** (9)</span><span class="sxs-lookup"><span data-stu-id="ae999-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="ae999-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Интеллектуальное уведомление** (10)</span><span class="sxs-lookup"><span data-stu-id="ae999-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="ae999-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Поддержка двусторонних носителей** (11)</span><span class="sxs-lookup"><span data-stu-id="ae999-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-183">Поддержка носителя Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="ae999-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="ae999-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Извлечение с отключением не требуется** (12)</span><span class="sxs-lookup"><span data-stu-id="ae999-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae999-185">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="ae999-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-186">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ae999-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ae999-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-188">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="ae999-188">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-189">Массив строк произвольной формы, предоставляющий более подробные объяснения для любых функций доступа к устройствам, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="ae999-189">Array of free-form strings providing more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="ae999-190">Обратите внимание, что каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="ae999-190">Note that each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="ae999-191">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-191">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-192">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ae999-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-195">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ae999-195">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-196">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ae999-196">Short description of the object.</span></span>

<span data-ttu-id="ae999-197">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-198">**Сжатие**</span><span class="sxs-lookup"><span data-stu-id="ae999-198">**Compression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-199">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae999-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-201">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| ленточные структуры резервного копирования \| [**Лента \_ Получение \_ \_ параметров диска**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| Сжатие")</span><span class="sxs-lookup"><span data-stu-id="ae999-201">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|Compression")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-202">Если задано **значение true**, аппаратное сжатие данных включено.</span><span class="sxs-lookup"><span data-stu-id="ae999-202">If **TRUE**, hardware data compression is enabled.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="ae999-203"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="ae999-203"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="ae999-204">FALSE</span><span class="sxs-lookup"><span data-stu-id="ae999-204">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="ae999-205"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="ae999-205"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="ae999-206">true</span><span class="sxs-lookup"><span data-stu-id="ae999-206">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ae999-207">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="ae999-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae999-210">Строка произвольной формы, указывающая алгоритм или средство, используемые устройством для поддержки сжатия.</span><span class="sxs-lookup"><span data-stu-id="ae999-210">Free-form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="ae999-211">Если нет возможности описать схему сжатия (возможно, потому, что она неизвестна), используйте следующие слова: "Unknown", чтобы указать, что устройство поддерживает сжатие или нет. "Сжатый" для представления того, что устройство поддерживает возможности сжатия, но либо схема сжатия неизвестна, либо не раскрывается. и "не сжато" для представления того, что устройство не поддерживает возможности сжатия.</span><span class="sxs-lookup"><span data-stu-id="ae999-211">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="ae999-212">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-212">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="ae999-213">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="ae999-213">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="ae999-214">Схема сжатия неизвестна или не описана.</span><span class="sxs-lookup"><span data-stu-id="ae999-214">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="ae999-215">("Сжатый")</span><span class="sxs-lookup"><span data-stu-id="ae999-215">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="ae999-216">Логический файл сжат, но схема сжатия неизвестна или не описана</span><span class="sxs-lookup"><span data-stu-id="ae999-216">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="ae999-217">("Не сжато")</span><span class="sxs-lookup"><span data-stu-id="ae999-217">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="ae999-218">Если логический файл не сжат</span><span class="sxs-lookup"><span data-stu-id="ae999-218">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ae999-219">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="ae999-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-220">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae999-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-222">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ae999-222">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-223">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ae999-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="ae999-224">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="ae999-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="ae999-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="ae999-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="ae999-226">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-227">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="ae999-227">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="ae999-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="ae999-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="ae999-229">(1)</span><span class="sxs-lookup"><span data-stu-id="ae999-229">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-230">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="ae999-230">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ae999-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="ae999-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="ae999-232">(2)</span><span class="sxs-lookup"><span data-stu-id="ae999-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="ae999-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="ae999-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="ae999-234">(3)</span><span class="sxs-lookup"><span data-stu-id="ae999-234">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-235">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae999-235">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ae999-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="ae999-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="ae999-237">(4)</span><span class="sxs-lookup"><span data-stu-id="ae999-237">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-238">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="ae999-238">Device is not working properly.</span></span> <span data-ttu-id="ae999-239">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="ae999-239">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="ae999-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="ae999-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="ae999-241">(5)</span><span class="sxs-lookup"><span data-stu-id="ae999-241">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-242">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="ae999-242">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="ae999-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="ae999-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="ae999-244"> (6)</span><span class="sxs-lookup"><span data-stu-id="ae999-244">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-245">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="ae999-245">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="ae999-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="ae999-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="ae999-247">(7)</span><span class="sxs-lookup"><span data-stu-id="ae999-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="ae999-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="ae999-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="ae999-249">(8)</span><span class="sxs-lookup"><span data-stu-id="ae999-249">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-250">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="ae999-250">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="ae999-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="ae999-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="ae999-252">(9)</span><span class="sxs-lookup"><span data-stu-id="ae999-252">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-253">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="ae999-253">Device is not working properly.</span></span> <span data-ttu-id="ae999-254">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="ae999-254">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="ae999-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="ae999-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="ae999-256">(10)</span><span class="sxs-lookup"><span data-stu-id="ae999-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-257">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="ae999-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="ae999-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="ae999-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="ae999-259">(11)</span><span class="sxs-lookup"><span data-stu-id="ae999-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-260">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="ae999-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="ae999-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="ae999-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="ae999-262">(12)</span><span class="sxs-lookup"><span data-stu-id="ae999-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-263">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="ae999-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="ae999-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="ae999-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="ae999-265">(13)</span><span class="sxs-lookup"><span data-stu-id="ae999-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-266">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="ae999-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="ae999-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="ae999-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="ae999-268">(14)</span><span class="sxs-lookup"><span data-stu-id="ae999-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-269">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="ae999-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="ae999-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="ae999-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="ae999-271">(15)</span><span class="sxs-lookup"><span data-stu-id="ae999-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-272">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="ae999-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="ae999-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="ae999-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="ae999-274">(16)</span><span class="sxs-lookup"><span data-stu-id="ae999-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-275">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="ae999-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="ae999-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="ae999-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="ae999-277">(17)</span><span class="sxs-lookup"><span data-stu-id="ae999-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-278">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae999-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ae999-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="ae999-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="ae999-280">(18)</span><span class="sxs-lookup"><span data-stu-id="ae999-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-281">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="ae999-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="ae999-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="ae999-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="ae999-283">(19)</span><span class="sxs-lookup"><span data-stu-id="ae999-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ae999-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="ae999-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="ae999-285">(20)</span><span class="sxs-lookup"><span data-stu-id="ae999-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-286">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="ae999-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="ae999-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="ae999-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="ae999-288">(21)</span><span class="sxs-lookup"><span data-stu-id="ae999-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-289">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="ae999-289">System failure.</span></span> <span data-ttu-id="ae999-290">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="ae999-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="ae999-291">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="ae999-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="ae999-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="ae999-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="ae999-293">(22)</span><span class="sxs-lookup"><span data-stu-id="ae999-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-294">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="ae999-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="ae999-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="ae999-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="ae999-296">(23)</span><span class="sxs-lookup"><span data-stu-id="ae999-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-297">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="ae999-297">System failure.</span></span> <span data-ttu-id="ae999-298">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="ae999-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="ae999-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="ae999-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="ae999-300">(24)</span><span class="sxs-lookup"><span data-stu-id="ae999-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-301">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="ae999-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ae999-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="ae999-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ae999-303">(25)</span><span class="sxs-lookup"><span data-stu-id="ae999-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-304">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="ae999-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ae999-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="ae999-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ae999-306">(26)</span><span class="sxs-lookup"><span data-stu-id="ae999-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-307">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="ae999-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="ae999-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="ae999-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="ae999-309">(27)</span><span class="sxs-lookup"><span data-stu-id="ae999-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-310">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="ae999-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="ae999-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="ae999-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="ae999-312">(28)</span><span class="sxs-lookup"><span data-stu-id="ae999-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-313">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="ae999-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="ae999-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="ae999-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="ae999-315">(29)</span><span class="sxs-lookup"><span data-stu-id="ae999-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-316">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="ae999-316">Device is disabled.</span></span> <span data-ttu-id="ae999-317">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ae999-317">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="ae999-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="ae999-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="ae999-319">(30)</span><span class="sxs-lookup"><span data-stu-id="ae999-319">(30)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-320">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="ae999-320">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ae999-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="ae999-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="ae999-322">1-31</span><span class="sxs-lookup"><span data-stu-id="ae999-322">(31)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-323">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="ae999-323">Device is not working properly.</span></span> <span data-ttu-id="ae999-324">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="ae999-324">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ae999-325">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="ae999-325">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-326">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ae999-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-328">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ae999-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-329">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ae999-329">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="ae999-330">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-331">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ae999-331">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-332">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-334">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ae999-334">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ae999-335">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ae999-335">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="ae999-336">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="ae999-336">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ae999-337">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-338">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="ae999-338">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-339">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae999-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-341">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="ae999-341">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-342">Размер блока по умолчанию (в байтах) для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="ae999-342">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="ae999-343">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-343">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="ae999-344">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-345">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ae999-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-348">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="ae999-348">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-349">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ae999-349">Description of the object.</span></span>

<span data-ttu-id="ae999-350">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-351">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ae999-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-354">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| File functions \| CreateFile")</span><span class="sxs-lookup"><span data-stu-id="ae999-354">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-355">Уникальный идентификатор ленточного накопителя с другими устройствами в системе.</span><span class="sxs-lookup"><span data-stu-id="ae999-355">Unique identifier of the tape drive with other devices on the system.</span></span>

<span data-ttu-id="ae999-356">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-357">**ECC**</span><span class="sxs-lookup"><span data-stu-id="ae999-357">**ECC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-358">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae999-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-360">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| ленточные структуры резервного копирования \| [**Лента \_ получить \_ \_ Параметры диска**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ECC")</span><span class="sxs-lookup"><span data-stu-id="ae999-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ECC")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-361">Если **значение — true**, устройство поддерживает исправление ошибок оборудования.</span><span class="sxs-lookup"><span data-stu-id="ae999-361">If **TRUE**, the device supports hardware error correction.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="ae999-362">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ae999-362">**False** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="ae999-363">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ae999-363">**True** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae999-364">**еотварнингзонесизе**</span><span class="sxs-lookup"><span data-stu-id="ae999-364">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-365">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae999-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-367">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="ae999-367">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-368">Размер зоны для предупреждения об окончании ленты (EOT).</span><span class="sxs-lookup"><span data-stu-id="ae999-368">Zone size for the end of tape (EOT) warning.</span></span>

<span data-ttu-id="ae999-369">Это свойство наследуется от [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-369">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-370">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="ae999-370">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-371">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ae999-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae999-373">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="ae999-373">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="ae999-374">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-375">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ae999-375">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-376">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae999-378">Строка свободной формы, предоставляя дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="ae999-378">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="ae999-379">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-380">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="ae999-380">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-381">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae999-383">Произвольная строка, описывающая тип обнаружения и исправления ошибок, поддерживаемых этим устройством.</span><span class="sxs-lookup"><span data-stu-id="ae999-383">Free-form string describing the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="ae999-384">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-385">**феатурешигх**</span><span class="sxs-lookup"><span data-stu-id="ae999-385">**FeaturesHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-386">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae999-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-388">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| ленточные структуры резервного копирования \| [**Лента \_ получить \_ \_ Параметры диска**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| феатурешигх")</span><span class="sxs-lookup"><span data-stu-id="ae999-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesHigh")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-389">Высокий порядок 32 бит флагов возможностей устройства.</span><span class="sxs-lookup"><span data-stu-id="ae999-389">High-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="ae999-390">**феатуреслов**</span><span class="sxs-lookup"><span data-stu-id="ae999-390">**FeaturesLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-391">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae999-391">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-393">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| ленточные структуры резервного копирования \| [**Лента \_ получить \_ \_ Параметры диска**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| феатуреслов")</span><span class="sxs-lookup"><span data-stu-id="ae999-393">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesLow")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-394">Младшие биты 32 флага возможностей устройства.</span><span class="sxs-lookup"><span data-stu-id="ae999-394">Low-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="ae999-395">**Id**</span><span class="sxs-lookup"><span data-stu-id="ae999-395">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-396">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-398">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| функции файла Win32API")</span><span class="sxs-lookup"><span data-stu-id="ae999-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-399">Имя устройства чтения компакт-дисков Windows, установленное производителем.</span><span class="sxs-lookup"><span data-stu-id="ae999-399">Manufacturer's identifying name of the Windows CD ROM drive.</span></span>

<span data-ttu-id="ae999-400">Пример: "ПЛЕКСТОР CD-ROM PX-12CS 1,01"</span><span class="sxs-lookup"><span data-stu-id="ae999-400">Example: "PLEXTOR CD-ROM PX-12CS 1.01"</span></span>

</dd> <dt>

<span data-ttu-id="ae999-401">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ae999-401">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-402">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae999-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-404">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="ae999-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-405">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="ae999-405">Date and time the object was installed.</span></span> <span data-ttu-id="ae999-406">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="ae999-406">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ae999-407">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-408">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="ae999-408">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-409">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae999-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae999-411">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="ae999-411">Last error code reported by the logical device.</span></span>

<span data-ttu-id="ae999-412">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-412">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-413">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="ae999-413">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-414">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-416">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="ae999-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-417">Изготовитель устройства чтения компакт-дисков Windows.</span><span class="sxs-lookup"><span data-stu-id="ae999-417">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="ae999-418">Пример: "ПЛЕКСТОР"</span><span class="sxs-lookup"><span data-stu-id="ae999-418">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="ae999-419">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="ae999-419">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-420">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae999-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-422">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="ae999-422">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-423">Максимальный размер блока в байтах для носителя, доступного этому устройству.</span><span class="sxs-lookup"><span data-stu-id="ae999-423">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="ae999-424">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-424">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="ae999-425">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-426">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="ae999-426">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-427">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae999-427">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-429">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="ae999-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-430">Максимальный размер носителя, поддерживаемого этим устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="ae999-430">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="ae999-431">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="ae999-432">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-432">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-433">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="ae999-433">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-434">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae999-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae999-436">Максимальное число разделов для ленточного накопителя.</span><span class="sxs-lookup"><span data-stu-id="ae999-436">Maximum partition count for the tape drive.</span></span>

<span data-ttu-id="ae999-437">Это свойство наследуется от [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-437">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-438">**Мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="ae999-438">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-439">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-441">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32 \_ TapeDrive \| mediaType \| Tape Drive")</span><span class="sxs-lookup"><span data-stu-id="ae999-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_TapeDrive\|MediaType\|Tape Drive")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-442">Тип носителя, используемый этим устройством (или доступ к нему).</span><span class="sxs-lookup"><span data-stu-id="ae999-442">Media type used by (or accessed by) this device.</span></span> <span data-ttu-id="ae999-443">В этом случае для него задается значение "ленточный накопитель".</span><span class="sxs-lookup"><span data-stu-id="ae999-443">In this case, it is set to "Tape Drive".</span></span>

</dd> <dt>

<span data-ttu-id="ae999-444">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="ae999-444">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-445">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae999-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-447">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="ae999-447">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-448">Минимальный размер блока в байтах для носителя, доступного этому устройству.</span><span class="sxs-lookup"><span data-stu-id="ae999-448">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="ae999-449">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-449">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="ae999-450">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-451">**Name**</span><span class="sxs-lookup"><span data-stu-id="ae999-451">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-452">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-454">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="ae999-454">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-455">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="ae999-455">Label by which the object is known.</span></span> <span data-ttu-id="ae999-456">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="ae999-456">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="ae999-457">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-458">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="ae999-458">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-459">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ae999-459">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae999-461">Если задано **значение true**, устройству доступа к носителю требуется очистка.</span><span class="sxs-lookup"><span data-stu-id="ae999-461">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="ae999-462">Возможность ручной или автоматической очистки указывается в свойстве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="ae999-462">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="ae999-463">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-464">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="ae999-464">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-465">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae999-465">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-466">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae999-467">Максимальное число отдельных носителей, которые могут поддерживаться или вставляться на устройстве доступа к носителю (если поддерживается).</span><span class="sxs-lookup"><span data-stu-id="ae999-467">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="ae999-468">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-468">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-469">**Заполнение**</span><span class="sxs-lookup"><span data-stu-id="ae999-469">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-470">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae999-470">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-471">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-472">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="ae999-472">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-473">Число байтов, вставленных между блоками на ленточном носителе.</span><span class="sxs-lookup"><span data-stu-id="ae999-473">Number of bytes inserted between blocks on a tape media.</span></span>

<span data-ttu-id="ae999-474">Это свойство наследуется от [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-474">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-475">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ae999-475">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-476">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-477">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-478">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ae999-478">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-479">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ae999-479">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="ae999-480">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ae999-481">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="ae999-481">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="ae999-482">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="ae999-482">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-483">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ae999-483">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ae999-484">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-484">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae999-485">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="ae999-485">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="ae999-486">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-486">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae999-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ae999-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ae999-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="ae999-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-489">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="ae999-489">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ae999-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="ae999-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ae999-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="ae999-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-492">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="ae999-492">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ae999-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="ae999-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-494">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="ae999-494">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ae999-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="ae999-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-496">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="ae999-496">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="ae999-497">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="ae999-497">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="ae999-498">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-498">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ae999-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="ae999-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-500">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="ae999-500">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ae999-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="ae999-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ae999-502">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="ae999-502">Timed Power-On Supported</span></span>

<span data-ttu-id="ae999-503">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="ae999-503">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ae999-504">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="ae999-504">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-505">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ae999-505">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-506">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae999-507">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="ae999-507">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="ae999-508">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="ae999-508">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="ae999-509">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-510">**репортсетмаркс**</span><span class="sxs-lookup"><span data-stu-id="ae999-510">**ReportSetMarks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-511">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ae999-511">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-512">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-513">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| ленточные структуры резервного копирования \| [**Лента \_ получить \_ \_ Параметры диска**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| репортсетмаркс")</span><span class="sxs-lookup"><span data-stu-id="ae999-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ReportSetmarks")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-514">Если **значение — true**, отчеты сетмарк включены.</span><span class="sxs-lookup"><span data-stu-id="ae999-514">If **TRUE**, setmark reporting is enabled.</span></span> <span data-ttu-id="ae999-515">Сетмарк Reporting использует специализированный записанный элемент, который не содержит пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="ae999-515">Setmark reporting makes use of a specialized recorded element that does not contain user data.</span></span> <span data-ttu-id="ae999-516">Этот записанный элемент используется для создания схемы сегментации, которая является иерархически филемаркс.</span><span class="sxs-lookup"><span data-stu-id="ae999-516">This recorded element is used to provide a segmentation scheme that is hierarchically superior to filemarks.</span></span> <span data-ttu-id="ae999-517">Сетмаркс обеспечивают более быстрое размещение на лентах с высокой емкостью.</span><span class="sxs-lookup"><span data-stu-id="ae999-517">Setmarks provide faster positioning on high-capacity tapes.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="ae999-518"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="ae999-518"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="ae999-519">FALSE</span><span class="sxs-lookup"><span data-stu-id="ae999-519">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="ae999-520"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="ae999-520"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="ae999-521">true</span><span class="sxs-lookup"><span data-stu-id="ae999-521">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ae999-522">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ae999-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-523">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-524">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-525">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="ae999-525">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-526">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="ae999-526">Current status of the object.</span></span> <span data-ttu-id="ae999-527">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="ae999-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ae999-528">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="ae999-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ae999-529">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="ae999-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ae999-530">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="ae999-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ae999-531">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="ae999-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ae999-532">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ae999-533">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="ae999-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ae999-534">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="ae999-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ae999-535">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="ae999-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ae999-536">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="ae999-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae999-537">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="ae999-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ae999-538">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="ae999-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ae999-539">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="ae999-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ae999-540">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="ae999-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ae999-541">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="ae999-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ae999-542">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="ae999-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ae999-543">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="ae999-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ae999-544">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="ae999-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ae999-545">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="ae999-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae999-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ae999-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-547">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae999-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-548">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-549">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="ae999-549">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ae999-550">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ae999-550">State of the logical device.</span></span> <span data-ttu-id="ae999-551">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="ae999-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="ae999-552">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae999-553">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ae999-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae999-554">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="ae999-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ae999-555">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="ae999-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ae999-556">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="ae999-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ae999-557">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="ae999-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae999-558">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="ae999-558">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-559">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-560">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-560">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-561">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ae999-561">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ae999-562">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="ae999-562">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="ae999-563">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-563">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ae999-564">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ae999-564">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae999-565">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae999-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae999-566">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae999-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae999-567">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ae999-567">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ae999-568">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="ae999-568">Name of the scoping system.</span></span>

<span data-ttu-id="ae999-569">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ae999-569">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae999-570">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae999-570">Remarks</span></span>

<span data-ttu-id="ae999-571">Класс **Win32 \_ TapeDrive** является производным от [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="ae999-571">The **Win32\_TapeDrive** class is derived from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae999-572">Требования</span><span class="sxs-lookup"><span data-stu-id="ae999-572">Requirements</span></span>



| <span data-ttu-id="ae999-573">Требование</span><span class="sxs-lookup"><span data-stu-id="ae999-573">Requirement</span></span> | <span data-ttu-id="ae999-574">Значение</span><span class="sxs-lookup"><span data-stu-id="ae999-574">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae999-575">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae999-575">Minimum supported client</span></span><br/> | <span data-ttu-id="ae999-576">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae999-576">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ae999-577">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae999-577">Minimum supported server</span></span><br/> | <span data-ttu-id="ae999-578">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae999-578">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ae999-579">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ae999-579">Namespace</span></span><br/>                | <span data-ttu-id="ae999-580">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ae999-580">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ae999-581">MOF</span><span class="sxs-lookup"><span data-stu-id="ae999-581">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae999-582"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae999-582"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae999-583">DLL</span><span class="sxs-lookup"><span data-stu-id="ae999-583">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae999-584"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae999-584"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae999-585">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae999-585">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae999-586">**\_TAPEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="ae999-586">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="ae999-587">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="ae999-587">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
