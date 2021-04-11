---
description: '\_Класс источника CIM представляет возможности и управление логическим устройством источника питания.'
ms.assetid: a9b79564-01d9-42a4-8586-782f179c179f
ms.tgt_platform: multiple
title: Класс CIM_PowerSupply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PowerSupply
- CIM_PowerSupply.ActiveInputVoltage
- CIM_PowerSupply.Availability
- CIM_PowerSupply.Caption
- CIM_PowerSupply.ConfigManagerErrorCode
- CIM_PowerSupply.ConfigManagerUserConfig
- CIM_PowerSupply.CreationClassName
- CIM_PowerSupply.Description
- CIM_PowerSupply.DeviceID
- CIM_PowerSupply.ErrorCleared
- CIM_PowerSupply.ErrorDescription
- CIM_PowerSupply.InstallDate
- CIM_PowerSupply.IsSwitchingSupply
- CIM_PowerSupply.LastErrorCode
- CIM_PowerSupply.Name
- CIM_PowerSupply.PNPDeviceID
- CIM_PowerSupply.PowerManagementCapabilities
- CIM_PowerSupply.PowerManagementSupported
- CIM_PowerSupply.Range1InputFrequencyHigh
- CIM_PowerSupply.Range1InputFrequencyLow
- CIM_PowerSupply.Range1InputVoltageHigh
- CIM_PowerSupply.Range1InputVoltageLow
- CIM_PowerSupply.Range2InputFrequencyHigh
- CIM_PowerSupply.Range2InputFrequencyLow
- CIM_PowerSupply.Range2InputVoltageHigh
- CIM_PowerSupply.Range2InputVoltageLow
- CIM_PowerSupply.Status
- CIM_PowerSupply.StatusInfo
- CIM_PowerSupply.SystemCreationClassName
- CIM_PowerSupply.SystemName
- CIM_PowerSupply.TotalOutputPower
- CIM_PowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35a1eb73c258b800bb8b33ad7aa75ea86cd0ef4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262604"
---
# <a name="cim_powersupply-class"></a><span data-ttu-id="ac642-103">\_Класс источника питания CIM</span><span class="sxs-lookup"><span data-stu-id="ac642-103">CIM\_PowerSupply class</span></span>

<span data-ttu-id="ac642-104">Класс **\_ источника CIM** представляет возможности и управление логическим устройством источника питания.</span><span class="sxs-lookup"><span data-stu-id="ac642-104">The **CIM\_PowerSupply** class represents the capabilities and management of the power supply logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac642-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ac642-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ac642-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ac642-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ac642-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ac642-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ac642-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ac642-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac642-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac642-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C547-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PowerSupply : CIM_LogicalDevice
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
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="ac642-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ac642-110">Members</span></span>

<span data-ttu-id="ac642-111">Класс **\_ источника питания CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ac642-111">The **CIM\_PowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="ac642-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ac642-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ac642-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ac642-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ac642-114">Методы</span><span class="sxs-lookup"><span data-stu-id="ac642-114">Methods</span></span>

<span data-ttu-id="ac642-115">Класс **\_ источника питания CIM** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="ac642-115">The **CIM\_PowerSupply** class has these methods.</span></span>



| <span data-ttu-id="ac642-116">Метод</span><span class="sxs-lookup"><span data-stu-id="ac642-116">Method</span></span>                                                                 | <span data-ttu-id="ac642-117">Описание</span><span class="sxs-lookup"><span data-stu-id="ac642-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac642-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="ac642-118">**Reset**</span></span>](reset-method-in-class-cim-powersupply.md)                 | <span data-ttu-id="ac642-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ac642-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="ac642-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="ac642-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="ac642-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ac642-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-powersupply.md) | <span data-ttu-id="ac642-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="ac642-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="ac642-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="ac642-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ac642-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="ac642-124">Properties</span></span>

<span data-ttu-id="ac642-125">Класс **\_ источника питания CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="ac642-125">The **CIM\_PowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ac642-126">**активеинпутволтаже**</span><span class="sxs-lookup"><span data-stu-id="ac642-126">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac642-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,15 ")</span><span class="sxs-lookup"><span data-stu-id="ac642-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-130">Диапазон напряжений, который используется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="ac642-130">Voltage range that is currently in use.</span></span> <span data-ttu-id="ac642-131">Если в данный момент не выполняется прорисовка энергии, можно указать значение 6 ("ни одного").</span><span class="sxs-lookup"><span data-stu-id="ac642-131">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="ac642-132">Эти сведения необходимы в случае источника бесперебойного питания (ИБП), подклассом **\_ источника данных CIM**.</span><span class="sxs-lookup"><span data-stu-id="ac642-132">This information is necessary in the case of an uninterruptible power supply (UPS), a subclass of **CIM\_PowerSupply**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ac642-133">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ac642-133">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac642-134">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="ac642-134">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="ac642-135">**Диапазон 1** (3)</span><span class="sxs-lookup"><span data-stu-id="ac642-135">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="ac642-136">**Диапазон 2** (4)</span><span class="sxs-lookup"><span data-stu-id="ac642-136">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="ac642-137">**Оба** (5)</span><span class="sxs-lookup"><span data-stu-id="ac642-137">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="ac642-138">Нет **ни одного** (6)</span><span class="sxs-lookup"><span data-stu-id="ac642-138">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac642-139">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="ac642-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-140">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac642-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-142">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="ac642-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-143">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="ac642-143">Availability and status of the device.</span></span>

<span data-ttu-id="ac642-144">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ac642-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ac642-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac642-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="ac642-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="ac642-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="ac642-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-148">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="ac642-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="ac642-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="ac642-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="ac642-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="ac642-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ac642-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="ac642-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="ac642-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="ac642-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="ac642-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="ac642-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="ac642-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="ac642-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ac642-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="ac642-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="ac642-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="ac642-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="ac642-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="ac642-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="ac642-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="ac642-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-159">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="ac642-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="ac642-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="ac642-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-161">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="ac642-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="ac642-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="ac642-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-163">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="ac642-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="ac642-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="ac642-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="ac642-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="ac642-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-166">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="ac642-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="ac642-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="ac642-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-168">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="ac642-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="ac642-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="ac642-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-170">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="ac642-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="ac642-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="ac642-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-172">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="ac642-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="ac642-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="ac642-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-174">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="ac642-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ac642-175">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ac642-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac642-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-178">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ac642-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-179">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ac642-179">Short textual description of the object.</span></span>

<span data-ttu-id="ac642-180">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ac642-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-181">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="ac642-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-182">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac642-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-184">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ac642-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-185">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ac642-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="ac642-186">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="ac642-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="ac642-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="ac642-188"> (0)</span><span class="sxs-lookup"><span data-stu-id="ac642-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-189">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="ac642-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="ac642-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="ac642-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="ac642-191">(1)</span><span class="sxs-lookup"><span data-stu-id="ac642-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-192">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="ac642-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ac642-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="ac642-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="ac642-194">(2)</span><span class="sxs-lookup"><span data-stu-id="ac642-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="ac642-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="ac642-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="ac642-196">(3)</span><span class="sxs-lookup"><span data-stu-id="ac642-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-197">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac642-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ac642-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="ac642-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="ac642-199">(4)</span><span class="sxs-lookup"><span data-stu-id="ac642-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-200">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="ac642-200">Device is not working properly.</span></span> <span data-ttu-id="ac642-201">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="ac642-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="ac642-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="ac642-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="ac642-203">(5)</span><span class="sxs-lookup"><span data-stu-id="ac642-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-204">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="ac642-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="ac642-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="ac642-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="ac642-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="ac642-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-207">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="ac642-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="ac642-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="ac642-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="ac642-209">(7)</span><span class="sxs-lookup"><span data-stu-id="ac642-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="ac642-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="ac642-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="ac642-211">(8)</span><span class="sxs-lookup"><span data-stu-id="ac642-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-212">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="ac642-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="ac642-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="ac642-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="ac642-214">(9)</span><span class="sxs-lookup"><span data-stu-id="ac642-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-215">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="ac642-215">Device is not working properly.</span></span> <span data-ttu-id="ac642-216">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="ac642-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="ac642-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="ac642-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="ac642-218">(10)</span><span class="sxs-lookup"><span data-stu-id="ac642-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-219">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="ac642-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="ac642-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="ac642-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="ac642-221">(11)</span><span class="sxs-lookup"><span data-stu-id="ac642-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-222">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="ac642-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="ac642-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="ac642-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="ac642-224">(12)</span><span class="sxs-lookup"><span data-stu-id="ac642-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-225">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="ac642-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="ac642-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="ac642-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="ac642-227">(13)</span><span class="sxs-lookup"><span data-stu-id="ac642-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-228">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="ac642-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="ac642-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="ac642-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="ac642-230">(14)</span><span class="sxs-lookup"><span data-stu-id="ac642-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-231">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="ac642-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="ac642-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="ac642-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="ac642-233">(15)</span><span class="sxs-lookup"><span data-stu-id="ac642-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-234">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="ac642-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="ac642-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="ac642-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="ac642-236">(16)</span><span class="sxs-lookup"><span data-stu-id="ac642-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-237">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="ac642-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="ac642-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="ac642-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="ac642-239">(17)</span><span class="sxs-lookup"><span data-stu-id="ac642-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-240">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="ac642-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ac642-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="ac642-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="ac642-242">(18)</span><span class="sxs-lookup"><span data-stu-id="ac642-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-243">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="ac642-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="ac642-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="ac642-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="ac642-245">(19)</span><span class="sxs-lookup"><span data-stu-id="ac642-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="ac642-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="ac642-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="ac642-247">(20)</span><span class="sxs-lookup"><span data-stu-id="ac642-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-248">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="ac642-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="ac642-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="ac642-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="ac642-250">(21)</span><span class="sxs-lookup"><span data-stu-id="ac642-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-251">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="ac642-251">System failure.</span></span> <span data-ttu-id="ac642-252">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="ac642-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="ac642-253">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="ac642-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="ac642-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="ac642-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="ac642-255">(22)</span><span class="sxs-lookup"><span data-stu-id="ac642-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-256">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="ac642-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="ac642-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="ac642-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="ac642-258">(23)</span><span class="sxs-lookup"><span data-stu-id="ac642-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-259">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="ac642-259">System failure.</span></span> <span data-ttu-id="ac642-260">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="ac642-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="ac642-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="ac642-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="ac642-262">(24)</span><span class="sxs-lookup"><span data-stu-id="ac642-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-263">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="ac642-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ac642-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="ac642-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ac642-265">(25)</span><span class="sxs-lookup"><span data-stu-id="ac642-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-266">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="ac642-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="ac642-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="ac642-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="ac642-268">(26)</span><span class="sxs-lookup"><span data-stu-id="ac642-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-269">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="ac642-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="ac642-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="ac642-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="ac642-271">(27)</span><span class="sxs-lookup"><span data-stu-id="ac642-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-272">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="ac642-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="ac642-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="ac642-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="ac642-274">(28)</span><span class="sxs-lookup"><span data-stu-id="ac642-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-275">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="ac642-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="ac642-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="ac642-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="ac642-277">(29)</span><span class="sxs-lookup"><span data-stu-id="ac642-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-278">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ac642-278">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="ac642-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="ac642-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="ac642-280">(30)</span><span class="sxs-lookup"><span data-stu-id="ac642-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-281">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="ac642-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="ac642-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="ac642-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="ac642-283">1-31</span><span class="sxs-lookup"><span data-stu-id="ac642-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-284">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="ac642-284">Device is not working properly.</span></span> <span data-ttu-id="ac642-285">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="ac642-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ac642-286">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="ac642-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-287">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ac642-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-289">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ac642-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-290">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ac642-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="ac642-291">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ac642-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac642-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-295">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ac642-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ac642-296">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ac642-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ac642-297">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="ac642-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="ac642-298">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-299">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ac642-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac642-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-302">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="ac642-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-303">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ac642-303">Textual description of the object.</span></span>

<span data-ttu-id="ac642-304">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ac642-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ac642-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-306">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac642-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-308">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ac642-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ac642-309">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ac642-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="ac642-310">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-311">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="ac642-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-312">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ac642-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac642-314">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="ac642-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="ac642-315">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ac642-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac642-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac642-319">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="ac642-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="ac642-320">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ac642-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-322">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ac642-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-324">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="ac642-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-325">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="ac642-325">Date and time the object was installed.</span></span> <span data-ttu-id="ac642-326">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="ac642-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="ac642-327">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ac642-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-328">**иссвитчингсуппли**</span><span class="sxs-lookup"><span data-stu-id="ac642-328">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-329">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ac642-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac642-331">Если **значение равно true**, источник питания является переключением (а не линейным).</span><span class="sxs-lookup"><span data-stu-id="ac642-331">If **TRUE**, the power supply is a switching (versus linear) supply.</span></span>

</dd> <dt>

<span data-ttu-id="ac642-332">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="ac642-332">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-333">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac642-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac642-335">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="ac642-335">Last error code reported by the logical device.</span></span>

<span data-ttu-id="ac642-336">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-337">**Name**</span><span class="sxs-lookup"><span data-stu-id="ac642-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-338">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac642-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-340">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="ac642-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-341">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="ac642-341">Label by which the object is known.</span></span> <span data-ttu-id="ac642-342">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="ac642-342">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="ac642-343">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ac642-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ac642-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-345">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac642-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-347">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="ac642-347">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-348">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ac642-348">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="ac642-349">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ac642-350">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="ac642-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="ac642-351">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="ac642-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-352">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ac642-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ac642-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac642-354">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="ac642-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="ac642-355">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac642-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ac642-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="ac642-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="ac642-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ac642-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="ac642-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ac642-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="ac642-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-360">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="ac642-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="ac642-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="ac642-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-362">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="ac642-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="ac642-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="ac642-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-364">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="ac642-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="ac642-365">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="ac642-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="ac642-366">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="ac642-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="ac642-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="ac642-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-368">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="ac642-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="ac642-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="ac642-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="ac642-370">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="ac642-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ac642-371">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="ac642-371">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-372">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="ac642-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ac642-374">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="ac642-374">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="ac642-375">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="ac642-375">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="ac642-376">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="ac642-376">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="ac642-377">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="ac642-377">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="ac642-378">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-379">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="ac642-379">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-380">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac642-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-382">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("Герц")</span><span class="sxs-lookup"><span data-stu-id="ac642-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-383">Частота (в герцах) в верхней части диапазона входной частоты источника питания 1.</span><span class="sxs-lookup"><span data-stu-id="ac642-383">Frequency (in hertz) at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="ac642-384">Значение 0 означает, что DC.</span><span class="sxs-lookup"><span data-stu-id="ac642-384">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="ac642-385">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="ac642-385">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-386">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac642-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-388">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,17 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="ac642-388">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-389">Частота (в герцах) в нижней части диапазона входной частоты источника питания 1.</span><span class="sxs-lookup"><span data-stu-id="ac642-389">Frequency (in hertz) at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="ac642-390">Значение 0 означает, что DC.</span><span class="sxs-lookup"><span data-stu-id="ac642-390">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="ac642-391">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="ac642-391">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-392">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac642-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-394">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,8 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="ac642-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-395">Высокое напряжение входного напряжения диапазона 1 для источника питания в милливольтах.</span><span class="sxs-lookup"><span data-stu-id="ac642-395">High voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="ac642-396">Значение 0 означает "неизвестно".</span><span class="sxs-lookup"><span data-stu-id="ac642-396">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="ac642-397">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="ac642-397">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-398">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac642-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-400">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,7 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="ac642-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-401">Низкое напряжение диапазона входного напряжения 1 для источника питания в милливольтах.</span><span class="sxs-lookup"><span data-stu-id="ac642-401">Low voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="ac642-402">Значение 0 означает "неизвестно".</span><span class="sxs-lookup"><span data-stu-id="ac642-402">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="ac642-403">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="ac642-403">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-404">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac642-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-406">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,20 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="ac642-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-407">Частота (в герцах) в верхней части диапазона входной частоты источника питания 2.</span><span class="sxs-lookup"><span data-stu-id="ac642-407">Frequency (in hertz) at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="ac642-408">Значение 0 означает, что DC.</span><span class="sxs-lookup"><span data-stu-id="ac642-408">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="ac642-409">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="ac642-409">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-410">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac642-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-412">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,19 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="ac642-412">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-413">Частота (в герцах) в нижней части диапазона входной частоты источника питания 2.</span><span class="sxs-lookup"><span data-stu-id="ac642-413">Frequency (in hertz) at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="ac642-414">Значение 0 означает, что DC.</span><span class="sxs-lookup"><span data-stu-id="ac642-414">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="ac642-415">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="ac642-415">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-416">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac642-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-418">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,12 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="ac642-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-419">Высокое напряжение диапазона входного напряжения 2 для источника питания в милливольтах.</span><span class="sxs-lookup"><span data-stu-id="ac642-419">High voltage of input voltage range 2 for the power supply, in millivolts.</span></span> <span data-ttu-id="ac642-420">Значение 0 означает "неизвестно".</span><span class="sxs-lookup"><span data-stu-id="ac642-420">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="ac642-421">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="ac642-421">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-422">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac642-422">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-423">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-424">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,11 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="ac642-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-425">Низкое напряжение диапазона входного напряжения 2 для этого источника питания, в милливольтах.</span><span class="sxs-lookup"><span data-stu-id="ac642-425">Low voltage of input voltage range 2 for this power supply, in Millivolts.</span></span> <span data-ttu-id="ac642-426">Значение 0 означает "неизвестно".</span><span class="sxs-lookup"><span data-stu-id="ac642-426">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="ac642-427">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ac642-427">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-428">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac642-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-430">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="ac642-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-431">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="ac642-431">Current status of the object.</span></span>

<span data-ttu-id="ac642-432">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ac642-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ac642-433">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="ac642-433">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ac642-434">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="ac642-434">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ac642-435">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="ac642-435">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ac642-436">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="ac642-436">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac642-437">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="ac642-437">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ac642-438">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="ac642-438">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ac642-439">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="ac642-439">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ac642-440">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="ac642-440">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ac642-441">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="ac642-441">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ac642-442">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="ac642-442">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ac642-443">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="ac642-443">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ac642-444">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="ac642-444">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ac642-445">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="ac642-445">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac642-446">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ac642-446">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-447">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac642-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-448">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-449">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="ac642-449">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-450">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ac642-450">State of the logical device.</span></span> <span data-ttu-id="ac642-451">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="ac642-451">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="ac642-452">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ac642-453">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ac642-453">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac642-454">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="ac642-454">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ac642-455">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="ac642-455">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ac642-456">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="ac642-456">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ac642-457">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="ac642-457">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ac642-458">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="ac642-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-459">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac642-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-461">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ac642-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ac642-462">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="ac642-462">Scoping system's creation class name.</span></span>

<span data-ttu-id="ac642-463">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ac642-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-465">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac642-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-466">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-467">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ac642-467">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ac642-468">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="ac642-468">Scoping system's name.</span></span>

<span data-ttu-id="ac642-469">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="ac642-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac642-470">**тоталаутпутповер**</span><span class="sxs-lookup"><span data-stu-id="ac642-470">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-471">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ac642-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-473">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,21 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" МВт ")</span><span class="sxs-lookup"><span data-stu-id="ac642-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-474">Общая выходная мощность источника питания в МВт.</span><span class="sxs-lookup"><span data-stu-id="ac642-474">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="ac642-475">Значение 0 означает "неизвестно".</span><span class="sxs-lookup"><span data-stu-id="ac642-475">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="ac642-476">**типеофранжесвитчинг**</span><span class="sxs-lookup"><span data-stu-id="ac642-476">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac642-477">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ac642-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ac642-478">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ac642-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac642-479">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Источник питания DMTF \| 002,16 ")</span><span class="sxs-lookup"><span data-stu-id="ac642-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="ac642-480">Тип переключения диапазона входного напряжения, реализованного в источнике питания.</span><span class="sxs-lookup"><span data-stu-id="ac642-480">Type of input voltage range switching implemented in the power supply.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ac642-481">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="ac642-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ac642-482">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="ac642-482">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="ac642-483">**Вручную** (3)</span><span class="sxs-lookup"><span data-stu-id="ac642-483">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="ac642-484">**Автопереключение** (4)</span><span class="sxs-lookup"><span data-stu-id="ac642-484">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="ac642-485">**Широкий диапазон** (5)</span><span class="sxs-lookup"><span data-stu-id="ac642-485">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="ac642-486">**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="ac642-486">**Not Applicable** (6)</span></span>


<span data-ttu-id="ac642-487"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ac642-487"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ac642-488">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac642-488">Remarks</span></span>

<span data-ttu-id="ac642-489">Класс **\_ источника питания CIM** является производным от CIM-класса. [**\_**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="ac642-489">The **CIM\_PowerSupply** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ac642-490">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="ac642-490">WMI does not implement this class.</span></span> <span data-ttu-id="ac642-491">Сведения о классах WMI, производных от **CIM источник \_ питания**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ac642-491">For WMI classed derived from **CIM\_PowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ac642-492">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ac642-492">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ac642-493">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ac642-493">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac642-494">Требования</span><span class="sxs-lookup"><span data-stu-id="ac642-494">Requirements</span></span>



| <span data-ttu-id="ac642-495">Требование</span><span class="sxs-lookup"><span data-stu-id="ac642-495">Requirement</span></span> | <span data-ttu-id="ac642-496">Значение</span><span class="sxs-lookup"><span data-stu-id="ac642-496">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac642-497">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac642-497">Minimum supported client</span></span><br/> | <span data-ttu-id="ac642-498">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac642-498">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ac642-499">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac642-499">Minimum supported server</span></span><br/> | <span data-ttu-id="ac642-500">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac642-500">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ac642-501">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac642-501">Namespace</span></span><br/>                | <span data-ttu-id="ac642-502">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ac642-502">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ac642-503">MOF</span><span class="sxs-lookup"><span data-stu-id="ac642-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac642-504"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac642-504"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac642-505">DLL</span><span class="sxs-lookup"><span data-stu-id="ac642-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac642-506"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac642-506"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac642-507">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac642-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac642-508">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="ac642-508">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

