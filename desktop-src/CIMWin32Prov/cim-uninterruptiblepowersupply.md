---
description: Класс CIM \_ унинтерруптиблеповерсуппли представляет возможности и управление источником бесперебойного питания (ИБП).
ms.assetid: 27ddc955-906b-40b9-981b-96872356477c
ms.tgt_platform: multiple
title: Класс CIM_UninterruptiblePowerSupply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UninterruptiblePowerSupply
- CIM_UninterruptiblePowerSupply.ActiveInputVoltage
- CIM_UninterruptiblePowerSupply.Availability
- CIM_UninterruptiblePowerSupply.Caption
- CIM_UninterruptiblePowerSupply.ConfigManagerErrorCode
- CIM_UninterruptiblePowerSupply.ConfigManagerUserConfig
- CIM_UninterruptiblePowerSupply.CreationClassName
- CIM_UninterruptiblePowerSupply.Description
- CIM_UninterruptiblePowerSupply.DeviceID
- CIM_UninterruptiblePowerSupply.ErrorCleared
- CIM_UninterruptiblePowerSupply.ErrorDescription
- CIM_UninterruptiblePowerSupply.EstimatedChargeRemaining
- CIM_UninterruptiblePowerSupply.EstimatedRunTime
- CIM_UninterruptiblePowerSupply.InstallDate
- CIM_UninterruptiblePowerSupply.IsSwitchingSupply
- CIM_UninterruptiblePowerSupply.LastErrorCode
- CIM_UninterruptiblePowerSupply.Name
- CIM_UninterruptiblePowerSupply.PNPDeviceID
- CIM_UninterruptiblePowerSupply.PowerManagementCapabilities
- CIM_UninterruptiblePowerSupply.PowerManagementSupported
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range1InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range1InputVoltageLow
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range2InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range2InputVoltageLow
- CIM_UninterruptiblePowerSupply.RemainingCapacityStatus
- CIM_UninterruptiblePowerSupply.Status
- CIM_UninterruptiblePowerSupply.StatusInfo
- CIM_UninterruptiblePowerSupply.SystemCreationClassName
- CIM_UninterruptiblePowerSupply.SystemName
- CIM_UninterruptiblePowerSupply.TimeOnBackup
- CIM_UninterruptiblePowerSupply.TotalOutputPower
- CIM_UninterruptiblePowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 214517fd6518cf2ca406523c61f522ae9c1adc46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655726"
---
# <a name="cim_uninterruptiblepowersupply-class"></a><span data-ttu-id="b8b0a-103">\_Класс CIM унинтерруптиблеповерсуппли</span><span class="sxs-lookup"><span data-stu-id="b8b0a-103">CIM\_UninterruptiblePowerSupply class</span></span>

<span data-ttu-id="b8b0a-104">Класс **CIM \_ унинтерруптиблеповерсуппли** представляет возможности и управление источником бесперебойного питания (ИБП).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-104">The **CIM\_UninterruptiblePowerSupply** class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span> <span data-ttu-id="b8b0a-105">Свойства ИБП указывают, когда обрезается или повышается Входящая мощность, а также сводные данные о батареях, генераторах и т. д., которые составляют устройство.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-105">The properties of the UPS device indicate when incoming power is trimmed or boosted, and the aggregated information of the batteries, generators, and so on, that make up the device.</span></span> <span data-ttu-id="b8b0a-106">Отдельные компоненты (например, несколько батарей) также могут быть независимо смоделированы и связаны с ИБП.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-106">The individual components (for example, multiple batteries) can also be independently modeled and associated with the UPS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8b0a-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b8b0a-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b8b0a-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b8b0a-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8b0a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8b0a-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UninterruptiblePowerSupply : CIM_PowerSupply
{
  uint16   ActiveInputVoltage;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  datetime InstallDate;
  boolean  IsSwitchingSupply;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Range1InputFrequencyHigh;
  uint32   Range1InputFrequencyLow;
  uint32   Range1InputVoltageHigh;
  uint32   Range1InputVoltageLow;
  uint32   Range2InputFrequencyHigh;
  uint32   Range2InputFrequencyLow;
  uint32   Range2InputVoltageHigh;
  uint32   Range2InputVoltageLow;
  uint16   RemainingCapacityStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBackup;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="b8b0a-112">Члены</span><span class="sxs-lookup"><span data-stu-id="b8b0a-112">Members</span></span>

<span data-ttu-id="b8b0a-113">Класс **CIM \_ унинтерруптиблеповерсуппли** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b8b0a-113">The **CIM\_UninterruptiblePowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="b8b0a-114">Методы</span><span class="sxs-lookup"><span data-stu-id="b8b0a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8b0a-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="b8b0a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8b0a-116">Методы</span><span class="sxs-lookup"><span data-stu-id="b8b0a-116">Methods</span></span>

<span data-ttu-id="b8b0a-117">Класс **CIM \_ унинтерруптиблеповерсуппли** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-117">The **CIM\_UninterruptiblePowerSupply** class has these methods.</span></span>



| <span data-ttu-id="b8b0a-118">Метод</span><span class="sxs-lookup"><span data-stu-id="b8b0a-118">Method</span></span>                                                                                | <span data-ttu-id="b8b0a-119">Описание</span><span class="sxs-lookup"><span data-stu-id="b8b0a-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8b0a-120">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-120">**Reset**</span></span>](reset-method-in-class-cim-uninterruptiblepowersupply.md)                 | <span data-ttu-id="b8b0a-121">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="b8b0a-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b8b0a-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-uninterruptiblepowersupply.md) | <span data-ttu-id="b8b0a-124">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b8b0a-125">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b8b0a-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="b8b0a-126">Properties</span></span>

<span data-ttu-id="b8b0a-127">Класс **CIM \_ унинтерруптиблеповерсуппли** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-127">The **CIM\_UninterruptiblePowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8b0a-128">**активеинпутволтаже**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-128">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-131">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,15 ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-132">Диапазон входного напряжения в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-132">Input voltage range is currently in use.</span></span> <span data-ttu-id="b8b0a-133">Если в данный момент не выполняется прорисовка энергии, можно указать значение 6 ("ни одного").</span><span class="sxs-lookup"><span data-stu-id="b8b0a-133">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="b8b0a-134">Эти сведения необходимы в случае ИБП, подклассом [**\_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-134">This information is necessary in the case of a UPS, a subclass of [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="b8b0a-135">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-135">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b8b0a-136">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8b0a-137">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-137">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="b8b0a-138">**Диапазон 1** (3)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-138">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="b8b0a-139">**Диапазон 2** (4)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-139">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="b8b0a-140">**Оба** (5)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-140">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="b8b0a-141">Нет **ни одного** (6)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-141">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8b0a-142">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-143">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-145">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-146">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-146">Availability and status of the device.</span></span>

<span data-ttu-id="b8b0a-147">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b8b0a-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8b0a-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b8b0a-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-151">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="b8b0a-151">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b8b0a-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b8b0a-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b8b0a-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b8b0a-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b8b0a-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b8b0a-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b8b0a-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b8b0a-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b8b0a-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b8b0a-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-162">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b8b0a-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-164">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-164">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b8b0a-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-166">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b8b0a-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b8b0a-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-169">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-169">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b8b0a-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-171">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b8b0a-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-173">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b8b0a-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-175">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b8b0a-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-177">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8b0a-178">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-178">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-181">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-182">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-182">Short textual description of the object.</span></span>

<span data-ttu-id="b8b0a-183">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-184">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-184">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-185">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-185">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-187">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-188">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-188">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b8b0a-189">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-189">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b8b0a-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b8b0a-191"> (0)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-191">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-192">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-192">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b8b0a-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b8b0a-194">(1)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-194">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-195">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-195">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b8b0a-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b8b0a-197">(2)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-197">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b8b0a-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b8b0a-199">(3)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-199">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-200">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-200">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b8b0a-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b8b0a-202">(4)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-203">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-203">Device is not working properly.</span></span> <span data-ttu-id="b8b0a-204">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-204">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b8b0a-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b8b0a-206">(5)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-206">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-207">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-207">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b8b0a-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b8b0a-209"> (6)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-209">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-210">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-210">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b8b0a-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b8b0a-212">(7)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-212">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b8b0a-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b8b0a-214">(8)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-214">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-215">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-215">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b8b0a-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b8b0a-217">(9)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-217">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-218">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-218">Device is not working properly.</span></span> <span data-ttu-id="b8b0a-219">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-219">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b8b0a-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b8b0a-221">(10)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-221">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-222">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-222">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b8b0a-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b8b0a-224">(11)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-224">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-225">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-225">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b8b0a-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b8b0a-227">(12)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-227">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-228">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-228">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b8b0a-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b8b0a-230">(13)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-230">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-231">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-231">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b8b0a-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b8b0a-233">(14)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-233">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-234">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-234">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b8b0a-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b8b0a-236">(15)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-236">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-237">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-237">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b8b0a-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b8b0a-239">(16)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-239">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-240">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-240">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b8b0a-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b8b0a-242">(17)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-242">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-243">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-243">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b8b0a-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b8b0a-245">(18)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-245">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-246">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-246">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b8b0a-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b8b0a-248">(19)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-248">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b8b0a-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b8b0a-250">(20)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-250">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-251">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-251">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b8b0a-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b8b0a-253">(21)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-253">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-254">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-254">System failure.</span></span> <span data-ttu-id="b8b0a-255">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-255">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b8b0a-256">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-256">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b8b0a-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b8b0a-258">(22)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-258">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-259">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-259">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b8b0a-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b8b0a-261">(23)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-261">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-262">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-262">System failure.</span></span> <span data-ttu-id="b8b0a-263">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-263">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b8b0a-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b8b0a-265">(24)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-265">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-266">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-266">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b8b0a-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b8b0a-268">(25)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-268">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-269">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b8b0a-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b8b0a-271">(26)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-271">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-272">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b8b0a-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b8b0a-274">(27)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-274">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-275">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-275">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b8b0a-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b8b0a-277">(28)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-277">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-278">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-278">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b8b0a-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b8b0a-280">(29)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-280">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-281">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-281">Device is disabled.</span></span> <span data-ttu-id="b8b0a-282">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-282">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b8b0a-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b8b0a-284">(30)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-284">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-285">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-285">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b8b0a-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b8b0a-287">1-31</span><span class="sxs-lookup"><span data-stu-id="b8b0a-287">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-288">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-288">Device is not working properly.</span></span> <span data-ttu-id="b8b0a-289">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-289">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8b0a-290">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-290">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-291">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-293">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-293">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-294">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-294">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b8b0a-295">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-296">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-296">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-299">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-300">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-300">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b8b0a-301">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-301">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b8b0a-302">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-303">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-303">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-306">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-307">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-307">Textual description of the object.</span></span>

<span data-ttu-id="b8b0a-308">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-309">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-309">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-312">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-313">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-313">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b8b0a-314">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-315">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-315">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-316">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-318">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-318">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b8b0a-319">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-320">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-320">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-323">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-323">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b8b0a-324">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-325">**естиматедчаржеремаининг**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-325">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-326">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-328">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| UPS батарея \| 001,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" процент ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-329">Процентная Оценка оставшегося полной оплаты за ИБП, использующий технологию аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-329">Percentage estimate of the remaining full charge for a UPS that uses battery technology.</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-330">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-330">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-331">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-333">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| UPS аккумулятора \| 001,3 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" минуты ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-334">Предполагаемое время в минутах, пока батарея, генератор или другой источник питания не будут исчерпаны в условиях текущей нагрузки, если выключена программа или она потеряна и остается выключенной.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-334">Estimated time, in minutes, until the battery, generator, or other power source is depleted under the present load conditions if the utility power is off, or is lost and remains off.</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-336">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-338">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-339">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-339">Date and time the object was installed.</span></span> <span data-ttu-id="b8b0a-340">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b8b0a-341">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-342">**иссвитчингсуппли**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-342">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-343">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-345">Если **значение равно true**, источник питания является переключением (а не линейным).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-345">If **TRUE**, the power supply is a switching (rather than linear) supply.</span></span>

<span data-ttu-id="b8b0a-346">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-346">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-347">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-347">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-348">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-350">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-350">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b8b0a-351">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-352">**Name**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-355">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-356">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-356">Label by which the object is known.</span></span> <span data-ttu-id="b8b0a-357">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-357">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b8b0a-358">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-359">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-359">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-362">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-362">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-363">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-363">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b8b0a-364">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b8b0a-365">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b8b0a-365">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-366">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-366">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-367">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="b8b0a-367">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-369">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-369">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b8b0a-370">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-370">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8b0a-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b8b0a-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b8b0a-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b8b0a-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-375">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-375">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b8b0a-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-377">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-377">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b8b0a-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-379">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b8b0a-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b8b0a-380">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-380">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b8b0a-381">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-381">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b8b0a-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-383">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-383">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b8b0a-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-385">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-385">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8b0a-386">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-386">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-387">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-389">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-389">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b8b0a-390">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b8b0a-390">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b8b0a-391">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-391">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b8b0a-392">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b8b0a-392">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b8b0a-393">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-393">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-394">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-394">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-395">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-395">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-397">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("Герц")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-397">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-398">Частота (в герцах) в верхней части диапазона входной частоты источника питания 1.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-398">Frequency, in hertz, at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="b8b0a-399">Значение 0 (нуль) подразумевает использование контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-399">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="b8b0a-400">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-400">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-401">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-401">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-402">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-404">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,17 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-405">Частота в герцах в нижней части диапазона входной частоты источника питания 1.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-405">Frequency, in hertz, at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="b8b0a-406">Значение 0 (нуль) подразумевает использование контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-406">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="b8b0a-407">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-407">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-408">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-408">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-409">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-411">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("милливольтах")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-411">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-412">Если напряжение в милливольтах превышает значение, указанное свойством **Range1InputVoltageHigh** , ИБП будет компенсировать, обрезая напряжение.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-412">If the voltage, in millivolts, rises above the value specified by the **Range1InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="b8b0a-413">Значение 0 (ноль) указывает, что напряжение, при котором происходит усечение, неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-413">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="b8b0a-414">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-414">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-415">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-415">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-416">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-418">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("милливольтах")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-418">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-419">Если напряжение в милливольтах падает ниже значения, указанного свойством **Range1InputVoltageLow** , ИБП будет компенсировать, повышая напряжение с помощью источников питания.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-419">If the voltage, in millivolts, drops below the value specified by the **Range1InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="b8b0a-420">Значение 0 указывает, что напряжение, при котором происходит повышение, неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-420">A value of 0 indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="b8b0a-421">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-421">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-422">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-422">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-423">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-423">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-424">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-425">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,20 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-426">Частота в герцах в высоком уровне диапазона входной частоты источника питания 2.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-426">Frequency, in hertz, at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="b8b0a-427">Значение 0 (нуль) подразумевает использование контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-427">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="b8b0a-428">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-428">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-429">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-429">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-430">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-432">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,19 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-433">Частота в герцах в нижней части диапазона входной частоты источника питания 2.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-433">Frequency, in hertz, at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="b8b0a-434">Значение 0 означает, что DC.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-434">A value of 0 implies DC.</span></span>

<span data-ttu-id="b8b0a-435">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-435">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-436">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-436">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-437">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-437">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-438">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-439">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("милливольтах")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-439">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-440">Если напряжение в милливольтах превышает значение, указанное свойством **Range2InputVoltageHigh** , ИБП будет компенсировать, обрезая напряжение.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-440">If the voltage, in millivolts, rises above the value specified by the **Range2InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="b8b0a-441">Значение 0 (ноль) указывает, что напряжение, при котором происходит усечение, неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-441">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="b8b0a-442">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-442">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-443">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-443">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-444">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-444">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-445">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-446">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("милливольтах")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-446">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-447">Если напряжение в милливольтах падает ниже значения, указанного свойством **Range2InputVoltageLow** , ИБП будет компенсировать, повышая напряжение с помощью источников питания.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-447">If the voltage, in millivolts, drops below the value specified by the **Range2InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="b8b0a-448">Значение 0 (ноль) указывает, что напряжение, при котором происходит повышение, неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-448">A value of 0 (zero) indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="b8b0a-449">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-449">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-450">**ремаинингкапаЦитистатус**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-450">**RemainingCapacityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-451">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-452">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-453">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Заряд батареи ибп \| 001,1 (DMTF)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-453">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-454">Сведения о емкости, остающейся в батареях ИБП, генераторе или другом источнике.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-454">Indication of the capacity remaining in the UPS's batteries, generator, or other source.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8b0a-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (1)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="b8b0a-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** (2)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-457">Оставшиеся расчетные минуты времени выполнения больше, чем заданное состояние низкого энергопотребления (обычно две минуты).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-457">Remaining estimated minutes of run-time is greater than the UPS's defined low-power state (typically, two minutes).</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="b8b0a-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Низкая** (3)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-459">Оставшиеся расчетные минуты времени выполнения меньше или равны определению низкого энергопотребления.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-459">Remaining estimated minutes of run-time is less than or equal to the UPS's defined low-power state.</span></span>

</dd> <dt>

<span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>

<span data-ttu-id="b8b0a-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>**Исчерпано** (4)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>**Depleted** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b8b0a-461">ИБП не сможет поддерживать текущую нагрузку при потере питания служебной программы (в том числе о том, что в настоящее время она отсутствует).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-461">The UPS will be unable to sustain the present load when the utility power is lost (including the possibility that the utility power is currently absent).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8b0a-462">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-462">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-463">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-464">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-465">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-465">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-466">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-466">Current status of the object.</span></span> <span data-ttu-id="b8b0a-467">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-467">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b8b0a-468">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="b8b0a-468">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b8b0a-469">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-469">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b8b0a-470">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-470">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b8b0a-471">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-471">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8b0a-472">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-472">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b8b0a-473">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-473">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b8b0a-474">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-474">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b8b0a-475">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-475">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b8b0a-476">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-476">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b8b0a-477">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-477">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b8b0a-478">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-478">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b8b0a-479">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-479">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b8b0a-480">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-480">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8b0a-481">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-481">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-482">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-483">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-484">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-485">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-485">State of the logical device.</span></span> <span data-ttu-id="b8b0a-486">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-486">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b8b0a-487">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b8b0a-488">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-488">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8b0a-489">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-489">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b8b0a-490">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-490">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b8b0a-491">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-491">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b8b0a-492">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-492">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8b0a-493">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-493">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-494">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-495">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-496">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-496">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-497">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-497">Scoping system's creation class name.</span></span>

<span data-ttu-id="b8b0a-498">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-498">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-499">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-499">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-500">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-500">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-501">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-502">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-502">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-503">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-503">Scoping system's name.</span></span>

<span data-ttu-id="b8b0a-504">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-504">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-505">**тимеонбаккуп**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-505">**TimeOnBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-506">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-507">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-508">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| UPS батарея \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" секунды ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-508">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-509">Затраченное время в секундах с момента последнего переключения ИБП на питание от аккумулятора, генератор или другой источник питания.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-509">Elapsed time, in seconds, since the UPS last switched to battery power, generator, or other power source.</span></span> <span data-ttu-id="b8b0a-510">Или, время с момента последнего перезапуска ИБП, в зависимости от того, что меньше.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-510">Or, the time since the UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="b8b0a-511">Если ИБП находится в режиме «в сети», будет возвращено значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-511">If the UPS is online, 0 (zero) will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-512">**тоталаутпутповер**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-512">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-513">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-514">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-515">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,21 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" МВт ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-515">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-516">Общая выходная мощность источника питания в МВт.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-516">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="b8b0a-517">Значение 0 (ноль) обозначает Unknown.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-517">A value of 0 (zero) denotes unknown.</span></span>

<span data-ttu-id="b8b0a-518">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-518">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8b0a-519">**типеофранжесвитчинг**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-519">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8b0a-520">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-521">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b8b0a-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8b0a-522">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,16 ")</span><span class="sxs-lookup"><span data-stu-id="b8b0a-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="b8b0a-523">Тип переключения диапазона входного напряжения, реализованного в источнике питания.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-523">Type of input-voltage range switching implemented in the power supply.</span></span>

<span data-ttu-id="b8b0a-524">Это свойство наследуется [**от \_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-524">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b8b0a-525">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-525">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8b0a-526">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-526">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="b8b0a-527">**Вручную** (3)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-527">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="b8b0a-528">**Автопереключение** (4)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-528">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="b8b0a-529">**Широкий диапазон** (5)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-529">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b8b0a-530">**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="b8b0a-530">**Not Applicable** (6)</span></span>


<span data-ttu-id="b8b0a-531"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b8b0a-531"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b8b0a-532">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8b0a-532">Remarks</span></span>

<span data-ttu-id="b8b0a-533">Класс **CIM \_ унинтерруптиблеповерсуппли** является производным от [**\_ источника питания CIM**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-533">The **CIM\_UninterruptiblePowerSupply** class is derived from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="b8b0a-534">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-534">WMI does not implement this class.</span></span> <span data-ttu-id="b8b0a-535">Классы WMI, производные от **CIM \_ унинтерруптиблеповерсуппли**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b8b0a-535">For WMI classes derived from **CIM\_UninterruptiblePowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b8b0a-536">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-536">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b8b0a-537">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b8b0a-537">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b0a-538">Требования</span><span class="sxs-lookup"><span data-stu-id="b8b0a-538">Requirements</span></span>



| <span data-ttu-id="b8b0a-539">Требование</span><span class="sxs-lookup"><span data-stu-id="b8b0a-539">Requirement</span></span> | <span data-ttu-id="b8b0a-540">Значение</span><span class="sxs-lookup"><span data-stu-id="b8b0a-540">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b0a-541">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8b0a-541">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b0a-542">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8b0a-542">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8b0a-543">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8b0a-543">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b0a-544">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8b0a-544">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8b0a-545">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b8b0a-545">Namespace</span></span><br/>                | <span data-ttu-id="b8b0a-546">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b8b0a-546">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8b0a-547">MOF</span><span class="sxs-lookup"><span data-stu-id="b8b0a-547">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8b0a-548"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8b0a-548"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8b0a-549">DLL</span><span class="sxs-lookup"><span data-stu-id="b8b0a-549">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8b0a-550"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8b0a-550"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8b0a-551">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8b0a-551">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b0a-552">**Источник \_ питания CIM**</span><span class="sxs-lookup"><span data-stu-id="b8b0a-552">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> </dl>

 

