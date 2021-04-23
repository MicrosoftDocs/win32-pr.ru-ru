---
description: Класс CIM \_ датчик напряжения существует для обеспечения обратной совместимости с более ранними определениями схемы CIM. Благодаря дополнениям к \_ классам датчиков CIM и модели CIM \_ NumericSensor в версии 2,2 больше не требуется.
ms.assetid: a578c7a2-27d5-4bd8-86d7-3962d5091f14
ms.tgt_platform: multiple
title: Класс CIM_VoltageSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VoltageSensor
- CIM_VoltageSensor.Accuracy
- CIM_VoltageSensor.Availability
- CIM_VoltageSensor.Caption
- CIM_VoltageSensor.ConfigManagerErrorCode
- CIM_VoltageSensor.ConfigManagerUserConfig
- CIM_VoltageSensor.CreationClassName
- CIM_VoltageSensor.CurrentReading
- CIM_VoltageSensor.Description
- CIM_VoltageSensor.DeviceID
- CIM_VoltageSensor.ErrorCleared
- CIM_VoltageSensor.ErrorDescription
- CIM_VoltageSensor.InstallDate
- CIM_VoltageSensor.IsLinear
- CIM_VoltageSensor.LastErrorCode
- CIM_VoltageSensor.LowerThresholdCritical
- CIM_VoltageSensor.LowerThresholdFatal
- CIM_VoltageSensor.LowerThresholdNonCritical
- CIM_VoltageSensor.MaxReadable
- CIM_VoltageSensor.MinReadable
- CIM_VoltageSensor.Name
- CIM_VoltageSensor.NominalReading
- CIM_VoltageSensor.NormalMax
- CIM_VoltageSensor.NormalMin
- CIM_VoltageSensor.PNPDeviceID
- CIM_VoltageSensor.PowerManagementCapabilities
- CIM_VoltageSensor.PowerManagementSupported
- CIM_VoltageSensor.Resolution
- CIM_VoltageSensor.Status
- CIM_VoltageSensor.StatusInfo
- CIM_VoltageSensor.SystemCreationClassName
- CIM_VoltageSensor.SystemName
- CIM_VoltageSensor.Tolerance
- CIM_VoltageSensor.UpperThresholdCritical
- CIM_VoltageSensor.UpperThresholdFatal
- CIM_VoltageSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bd0f3d79415254d0af50429c8f1776d2eb451cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655724"
---
# <a name="cim_voltagesensor-class"></a><span data-ttu-id="123d3-104">\_Класс CIM датчик напряжения</span><span class="sxs-lookup"><span data-stu-id="123d3-104">CIM\_VoltageSensor class</span></span>

<span data-ttu-id="123d3-105">Класс **CIM \_ датчик напряжения** существует для обеспечения обратной совместимости с более ранними определениями схемы CIM.</span><span class="sxs-lookup"><span data-stu-id="123d3-105">The **CIM\_VoltageSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="123d3-106">Благодаря дополнениям к классам [**\_ датчиков CIM**](cim-sensor.md) и [**модели cim \_ NumericSensor**](cim-numericsensor.md) в версии 2,2 больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="123d3-106">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="123d3-107">Датчик напряжения можно определить, установив свойство **сенсортипе** , наследуемое от [**\_ датчика CIM**](cim-sensor.md), на 3 ("напряжение").</span><span class="sxs-lookup"><span data-stu-id="123d3-107">A voltage sensor can be defined by setting the **SensorType** property, inherited from [**CIM\_Sensor**](cim-sensor.md), to 3 ("Voltage").</span></span> <span data-ttu-id="123d3-108">Другие свойства этого класса жестко запрограммированы на постоянные значения, соответствующие определениям в иерархии датчика.</span><span class="sxs-lookup"><span data-stu-id="123d3-108">Other properties of this class are hard-coded to constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="123d3-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="123d3-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="123d3-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="123d3-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="123d3-111">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="123d3-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="123d3-112">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="123d3-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="123d3-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="123d3-113">Syntax</span></span>

``` syntax
[UUID("{A998F9B4-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VoltageSensor : CIM_NumericSensor
{
  sint32   Accuracy;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  sint32   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLinear;
  uint32   LastErrorCode;
  sint32   LowerThresholdCritical;
  sint32   LowerThresholdFatal;
  sint32   LowerThresholdNonCritical;
  sint32   MaxReadable;
  sint32   MinReadable;
  string   Name;
  sint32   NominalReading;
  sint32   NormalMax;
  sint32   NormalMin;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  sint32   Tolerance;
  sint32   UpperThresholdCritical;
  sint32   UpperThresholdFatal;
  sint32   UpperThresholdNonCritical;
};
```

## <a name="members"></a><span data-ttu-id="123d3-114">Члены</span><span class="sxs-lookup"><span data-stu-id="123d3-114">Members</span></span>

<span data-ttu-id="123d3-115">Класс **CIM \_ датчик напряжения** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="123d3-115">The **CIM\_VoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="123d3-116">Методы</span><span class="sxs-lookup"><span data-stu-id="123d3-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="123d3-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="123d3-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="123d3-118">Методы</span><span class="sxs-lookup"><span data-stu-id="123d3-118">Methods</span></span>

<span data-ttu-id="123d3-119">Класс **CIM \_ датчик напряжения** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="123d3-119">The **CIM\_VoltageSensor** class has these methods.</span></span>



| <span data-ttu-id="123d3-120">Метод</span><span class="sxs-lookup"><span data-stu-id="123d3-120">Method</span></span>                                                                   | <span data-ttu-id="123d3-121">Описание</span><span class="sxs-lookup"><span data-stu-id="123d3-121">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="123d3-122">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="123d3-122">**Reset**</span></span>](reset-method-in-class-cim-voltagesensor.md)                 | <span data-ttu-id="123d3-123">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="123d3-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="123d3-124">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="123d3-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="123d3-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="123d3-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-voltagesensor.md) | <span data-ttu-id="123d3-126">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="123d3-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="123d3-127">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="123d3-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="123d3-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="123d3-128">Properties</span></span>

<span data-ttu-id="123d3-129">Класс **CIM \_ датчик напряжения** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="123d3-129">The **CIM\_VoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="123d3-130">**Точность**</span><span class="sxs-lookup"><span data-stu-id="123d3-130">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-131">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-133">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("точность"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="123d3-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-134">Точность датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="123d3-134">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="123d3-135">Его значение записывается как плюс или минус сотые доли процента.</span><span class="sxs-lookup"><span data-stu-id="123d3-135">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="123d3-136">Это свойство, а также свойства **разрешения** и **допуска** используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="123d3-136">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="123d3-137">Точность может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="123d3-137">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="123d3-138">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-138">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-139">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="123d3-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-140">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="123d3-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-142">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="123d3-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-143">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="123d3-143">Availability and status of the device.</span></span>

<span data-ttu-id="123d3-144">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="123d3-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="123d3-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="123d3-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="123d3-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="123d3-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="123d3-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-148">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="123d3-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="123d3-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="123d3-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="123d3-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="123d3-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="123d3-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="123d3-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="123d3-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="123d3-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="123d3-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="123d3-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="123d3-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="123d3-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="123d3-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="123d3-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="123d3-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="123d3-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="123d3-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="123d3-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="123d3-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="123d3-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-159">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="123d3-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="123d3-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="123d3-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-161">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="123d3-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="123d3-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="123d3-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-163">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="123d3-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="123d3-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="123d3-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="123d3-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="123d3-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-166">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="123d3-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="123d3-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="123d3-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-168">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="123d3-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="123d3-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="123d3-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-170">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="123d3-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="123d3-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="123d3-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-172">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="123d3-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="123d3-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="123d3-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-174">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="123d3-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="123d3-175">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="123d3-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="123d3-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-178">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="123d3-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-179">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="123d3-179">Short textual description of the object.</span></span>

<span data-ttu-id="123d3-180">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-181">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="123d3-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-182">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="123d3-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-184">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="123d3-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-185">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="123d3-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="123d3-186">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="123d3-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="123d3-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="123d3-188"> (0)</span><span class="sxs-lookup"><span data-stu-id="123d3-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-189">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="123d3-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="123d3-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="123d3-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="123d3-191">(1)</span><span class="sxs-lookup"><span data-stu-id="123d3-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-192">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="123d3-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="123d3-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="123d3-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="123d3-194">(2)</span><span class="sxs-lookup"><span data-stu-id="123d3-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="123d3-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="123d3-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="123d3-196">(3)</span><span class="sxs-lookup"><span data-stu-id="123d3-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-197">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="123d3-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="123d3-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="123d3-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="123d3-199">(4)</span><span class="sxs-lookup"><span data-stu-id="123d3-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-200">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="123d3-200">Device is not working properly.</span></span> <span data-ttu-id="123d3-201">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="123d3-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="123d3-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="123d3-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="123d3-203">(5)</span><span class="sxs-lookup"><span data-stu-id="123d3-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-204">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="123d3-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="123d3-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="123d3-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="123d3-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="123d3-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-207">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="123d3-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="123d3-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="123d3-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="123d3-209">(7)</span><span class="sxs-lookup"><span data-stu-id="123d3-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="123d3-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="123d3-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="123d3-211">(8)</span><span class="sxs-lookup"><span data-stu-id="123d3-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-212">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="123d3-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="123d3-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="123d3-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="123d3-214">(9)</span><span class="sxs-lookup"><span data-stu-id="123d3-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-215">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="123d3-215">Device is not working properly.</span></span> <span data-ttu-id="123d3-216">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="123d3-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="123d3-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="123d3-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="123d3-218">(10)</span><span class="sxs-lookup"><span data-stu-id="123d3-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-219">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="123d3-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="123d3-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="123d3-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="123d3-221">(11)</span><span class="sxs-lookup"><span data-stu-id="123d3-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-222">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="123d3-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="123d3-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="123d3-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="123d3-224">(12)</span><span class="sxs-lookup"><span data-stu-id="123d3-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-225">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="123d3-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="123d3-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="123d3-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="123d3-227">(13)</span><span class="sxs-lookup"><span data-stu-id="123d3-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-228">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="123d3-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="123d3-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="123d3-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="123d3-230">(14)</span><span class="sxs-lookup"><span data-stu-id="123d3-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-231">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="123d3-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="123d3-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="123d3-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="123d3-233">(15)</span><span class="sxs-lookup"><span data-stu-id="123d3-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-234">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="123d3-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="123d3-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="123d3-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="123d3-236">(16)</span><span class="sxs-lookup"><span data-stu-id="123d3-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-237">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="123d3-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="123d3-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="123d3-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="123d3-239">(17)</span><span class="sxs-lookup"><span data-stu-id="123d3-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-240">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="123d3-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="123d3-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="123d3-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="123d3-242">(18)</span><span class="sxs-lookup"><span data-stu-id="123d3-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-243">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="123d3-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="123d3-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="123d3-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="123d3-245">(19)</span><span class="sxs-lookup"><span data-stu-id="123d3-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="123d3-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="123d3-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="123d3-247">(20)</span><span class="sxs-lookup"><span data-stu-id="123d3-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-248">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="123d3-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="123d3-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="123d3-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="123d3-250">(21)</span><span class="sxs-lookup"><span data-stu-id="123d3-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-251">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="123d3-251">System failure.</span></span> <span data-ttu-id="123d3-252">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="123d3-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="123d3-253">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="123d3-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="123d3-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="123d3-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="123d3-255">(22)</span><span class="sxs-lookup"><span data-stu-id="123d3-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-256">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="123d3-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="123d3-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="123d3-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="123d3-258">(23)</span><span class="sxs-lookup"><span data-stu-id="123d3-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-259">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="123d3-259">System failure.</span></span> <span data-ttu-id="123d3-260">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="123d3-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="123d3-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="123d3-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="123d3-262">(24)</span><span class="sxs-lookup"><span data-stu-id="123d3-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-263">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="123d3-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="123d3-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="123d3-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="123d3-265">(25)</span><span class="sxs-lookup"><span data-stu-id="123d3-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-266">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="123d3-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="123d3-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="123d3-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="123d3-268">(26)</span><span class="sxs-lookup"><span data-stu-id="123d3-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-269">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="123d3-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="123d3-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="123d3-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="123d3-271">(27)</span><span class="sxs-lookup"><span data-stu-id="123d3-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-272">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="123d3-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="123d3-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="123d3-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="123d3-274">(28)</span><span class="sxs-lookup"><span data-stu-id="123d3-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-275">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="123d3-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="123d3-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="123d3-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="123d3-277">(29)</span><span class="sxs-lookup"><span data-stu-id="123d3-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-278">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="123d3-278">Device is disabled.</span></span> <span data-ttu-id="123d3-279">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="123d3-279">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="123d3-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="123d3-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="123d3-281">(30)</span><span class="sxs-lookup"><span data-stu-id="123d3-281">(30)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-282">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="123d3-282">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="123d3-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="123d3-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="123d3-284">1-31</span><span class="sxs-lookup"><span data-stu-id="123d3-284">(31)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-285">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="123d3-285">Device is not working properly.</span></span> <span data-ttu-id="123d3-286">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="123d3-286">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="123d3-287">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="123d3-287">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-288">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="123d3-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-290">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="123d3-290">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-291">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="123d3-291">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="123d3-292">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-293">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="123d3-293">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-294">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="123d3-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-296">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="123d3-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="123d3-297">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="123d3-297">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="123d3-298">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="123d3-298">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="123d3-299">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-300">**куррентреадинг**</span><span class="sxs-lookup"><span data-stu-id="123d3-300">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-301">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-301">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-303">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("куррентреадинг"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,5 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-303">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-304">Текущее значение, указываемое датчиком.</span><span class="sxs-lookup"><span data-stu-id="123d3-304">Current value indicated by the sensor.</span></span>

<span data-ttu-id="123d3-305">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-306">**Описание**</span><span class="sxs-lookup"><span data-stu-id="123d3-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="123d3-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-309">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="123d3-309">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-310">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="123d3-310">Textual description of the object.</span></span>

<span data-ttu-id="123d3-311">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="123d3-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="123d3-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-315">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="123d3-315">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="123d3-316">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="123d3-316">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="123d3-317">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-318">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="123d3-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-319">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="123d3-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="123d3-321">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="123d3-321">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="123d3-322">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="123d3-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="123d3-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="123d3-326">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="123d3-326">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="123d3-327">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="123d3-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-329">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="123d3-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-331">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="123d3-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-332">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="123d3-332">Date and time the object was installed.</span></span> <span data-ttu-id="123d3-333">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="123d3-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="123d3-334">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-335">**Линейно**</span><span class="sxs-lookup"><span data-stu-id="123d3-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-336">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="123d3-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="123d3-338">Если **значение равно true**, датчик линейно помещается в динамический диапазон.</span><span class="sxs-lookup"><span data-stu-id="123d3-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="123d3-339">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-340">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="123d3-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-341">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="123d3-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="123d3-343">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="123d3-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="123d3-344">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-345">**ловерсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="123d3-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-346">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-348">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ловерсрешолдкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,13 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-348">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-349">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="123d3-349">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="123d3-350">Если свойство **куррентреадинг** находится между **ловерсрешолдкритикал** и **ловерсрешолдфатал**, то текущее состояние является критическим.</span><span class="sxs-lookup"><span data-stu-id="123d3-350">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="123d3-351">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-352">**ловерсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="123d3-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-353">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-355">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ловерсрешолдфатал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,15 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-355">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-356">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="123d3-356">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="123d3-357">Если свойство **куррентреадинг** находится ниже **ловерсрешолдфатал**, то текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="123d3-357">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="123d3-358">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-359">**ловерсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="123d3-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-360">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-362">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ловерсрешолднонкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-362">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-363">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="123d3-363">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="123d3-364">Если свойство **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, то датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="123d3-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="123d3-365">Если свойство **куррентреадинг** находится между **ловерсрешолднонкритикал** и **ловерсрешолдкритикал**, то текущее состояние является некритическим.</span><span class="sxs-lookup"><span data-stu-id="123d3-365">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="123d3-366">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-367">**максреадабле**</span><span class="sxs-lookup"><span data-stu-id="123d3-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-368">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-370">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("максреадабле"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,9 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-371">Самое большое значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="123d3-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="123d3-372">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-373">**минреадабле**</span><span class="sxs-lookup"><span data-stu-id="123d3-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-374">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-376">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("минреадабле"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,10 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-376">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-377">Наименьшее значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="123d3-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="123d3-378">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-379">**Name**</span><span class="sxs-lookup"><span data-stu-id="123d3-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-380">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="123d3-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-382">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="123d3-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-383">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="123d3-383">Label by which the object is known.</span></span> <span data-ttu-id="123d3-384">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="123d3-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="123d3-385">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-386">**номиналреадинг**</span><span class="sxs-lookup"><span data-stu-id="123d3-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-387">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-389">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("номиналреадинг"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,6 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-390">Для числового датчика требуется или нормальное значение.</span><span class="sxs-lookup"><span data-stu-id="123d3-390">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="123d3-391">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-392">**нормалмакс**</span><span class="sxs-lookup"><span data-stu-id="123d3-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-393">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-395">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("нормалмакс"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,7 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-395">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-396">Нормальный максимальный диапазон для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="123d3-396">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="123d3-397">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-398">**нормалмин**</span><span class="sxs-lookup"><span data-stu-id="123d3-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-399">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-401">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("нормалмин"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,8 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-401">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-402">Нормальный минимальный диапазон для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="123d3-402">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="123d3-403">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="123d3-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-405">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="123d3-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-407">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="123d3-407">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-408">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="123d3-408">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="123d3-409">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-409">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="123d3-410">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="123d3-410">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="123d3-411">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="123d3-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-412">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="123d3-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="123d3-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="123d3-414">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="123d3-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="123d3-415">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-415">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="123d3-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="123d3-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="123d3-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="123d3-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="123d3-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="123d3-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="123d3-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="123d3-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-420">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="123d3-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="123d3-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="123d3-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-422">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="123d3-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="123d3-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="123d3-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-424">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="123d3-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="123d3-425">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="123d3-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="123d3-426">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="123d3-426">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="123d3-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="123d3-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-428">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="123d3-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="123d3-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="123d3-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="123d3-430">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="123d3-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="123d3-431">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="123d3-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-432">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="123d3-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-433">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="123d3-434">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="123d3-434">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="123d3-435">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="123d3-435">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="123d3-436">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="123d3-436">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="123d3-437">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="123d3-437">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="123d3-438">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-439">**Решение**</span><span class="sxs-lookup"><span data-stu-id="123d3-439">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-440">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="123d3-440">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-442">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("разрешение"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,17 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-443">Способность датчика разрешать различия в измеряемом свойстве.</span><span class="sxs-lookup"><span data-stu-id="123d3-443">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="123d3-444">Это свойство, а также свойства **точности** и **допуска** используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="123d3-444">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="123d3-445">Это значение может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="123d3-445">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="123d3-446">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-446">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-447">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="123d3-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-448">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="123d3-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-449">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-450">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="123d3-450">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-451">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="123d3-451">Current status of the object.</span></span>

<span data-ttu-id="123d3-452">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="123d3-453">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="123d3-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="123d3-454">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="123d3-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="123d3-455">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="123d3-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="123d3-456">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="123d3-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="123d3-457">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="123d3-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="123d3-458">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="123d3-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="123d3-459">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="123d3-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="123d3-460">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="123d3-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="123d3-461">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="123d3-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="123d3-462">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="123d3-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="123d3-463">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="123d3-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="123d3-464">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="123d3-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="123d3-465">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="123d3-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="123d3-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="123d3-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-467">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="123d3-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-468">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-469">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="123d3-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-470">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="123d3-470">State of the logical device.</span></span> <span data-ttu-id="123d3-471">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="123d3-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="123d3-472">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="123d3-473">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="123d3-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="123d3-474">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="123d3-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="123d3-475">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="123d3-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="123d3-476">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="123d3-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="123d3-477">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="123d3-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="123d3-478">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="123d3-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-479">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="123d3-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-480">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-481">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="123d3-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="123d3-482">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="123d3-482">Scoping system's creation class name.</span></span>

<span data-ttu-id="123d3-483">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-484">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="123d3-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-485">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="123d3-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-486">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-487">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="123d3-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="123d3-488">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="123d3-488">Scoping system's name.</span></span>

<span data-ttu-id="123d3-489">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="123d3-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-490">**Отклонение**</span><span class="sxs-lookup"><span data-stu-id="123d3-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-491">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-492">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-493">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Допуск"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,18 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-494">Допуск датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="123d3-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="123d3-495">Это свойство, а также свойства **разрешения** и **точности** используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="123d3-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="123d3-496">Допуск может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="123d3-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="123d3-497">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-497">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-498">**упперсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="123d3-498">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-499">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-499">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-500">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-501">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("упперсрешолдкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,14 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-501">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-502">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="123d3-502">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="123d3-503">Если свойство **куррентреадинг** находится между **упперсрешолдкритикал** и **упперсрешолдфатал**, то текущее состояние является критическим.</span><span class="sxs-lookup"><span data-stu-id="123d3-503">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="123d3-504">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-504">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-505">**упперсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="123d3-505">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-506">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-506">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-507">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-508">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("упперсрешолдфатал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,16 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-508">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-509">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="123d3-509">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="123d3-510">Если свойство **куррентреадинг** выше **упперсрешолдфатал**, то текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="123d3-510">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="123d3-511">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-511">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="123d3-512">**упперсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="123d3-512">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123d3-513">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="123d3-513">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="123d3-514">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="123d3-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123d3-515">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("упперсрешолднонкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд напряжения DMTF \| 001,12 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="123d3-515">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="123d3-516">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="123d3-516">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="123d3-517">Если свойство **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, то датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="123d3-517">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="123d3-518">Если свойство **куррентреадинг** находится между **упперсрешолднонкритикал** и **упперсрешолдкритикал**, то текущее состояние является некритическим.</span><span class="sxs-lookup"><span data-stu-id="123d3-518">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="123d3-519">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-519">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="123d3-520">Комментарии</span><span class="sxs-lookup"><span data-stu-id="123d3-520">Remarks</span></span>

<span data-ttu-id="123d3-521">Класс **CIM \_ датчик напряжения** является производным от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-521">The **CIM\_VoltageSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="123d3-522">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="123d3-522">WMI does not implement this class.</span></span> <span data-ttu-id="123d3-523">Классы WMI, производные от **CIM \_ датчик напряжения**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="123d3-523">For WMI classes derived from **CIM\_VoltageSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="123d3-524">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="123d3-524">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="123d3-525">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="123d3-525">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="123d3-526">Требования</span><span class="sxs-lookup"><span data-stu-id="123d3-526">Requirements</span></span>



| <span data-ttu-id="123d3-527">Требование</span><span class="sxs-lookup"><span data-stu-id="123d3-527">Requirement</span></span> | <span data-ttu-id="123d3-528">Значение</span><span class="sxs-lookup"><span data-stu-id="123d3-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="123d3-529">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="123d3-529">Minimum supported client</span></span><br/> | <span data-ttu-id="123d3-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="123d3-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="123d3-531">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="123d3-531">Minimum supported server</span></span><br/> | <span data-ttu-id="123d3-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="123d3-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="123d3-533">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="123d3-533">Namespace</span></span><br/>                | <span data-ttu-id="123d3-534">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="123d3-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="123d3-535">MOF</span><span class="sxs-lookup"><span data-stu-id="123d3-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="123d3-536"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="123d3-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="123d3-537">DLL</span><span class="sxs-lookup"><span data-stu-id="123d3-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="123d3-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="123d3-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="123d3-539">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="123d3-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123d3-540">**CIM \_ NumericSensor**</span><span class="sxs-lookup"><span data-stu-id="123d3-540">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

