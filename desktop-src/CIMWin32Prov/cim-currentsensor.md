---
description: Класс CIM \_ куррентсенсор существует для обеспечения обратной совместимости с более ранними определениями схемы CIM.
ms.assetid: d1835b09-4286-4586-92ec-f5f77791aea6
ms.tgt_platform: multiple
title: Класс CIM_CurrentSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CurrentSensor
- CIM_CurrentSensor.Accuracy
- CIM_CurrentSensor.Availability
- CIM_CurrentSensor.Caption
- CIM_CurrentSensor.ConfigManagerErrorCode
- CIM_CurrentSensor.ConfigManagerUserConfig
- CIM_CurrentSensor.CreationClassName
- CIM_CurrentSensor.CurrentReading
- CIM_CurrentSensor.Description
- CIM_CurrentSensor.DeviceID
- CIM_CurrentSensor.ErrorCleared
- CIM_CurrentSensor.ErrorDescription
- CIM_CurrentSensor.InstallDate
- CIM_CurrentSensor.IsLinear
- CIM_CurrentSensor.LastErrorCode
- CIM_CurrentSensor.LowerThresholdCritical
- CIM_CurrentSensor.LowerThresholdFatal
- CIM_CurrentSensor.LowerThresholdNonCritical
- CIM_CurrentSensor.MaxReadable
- CIM_CurrentSensor.MinReadable
- CIM_CurrentSensor.Name
- CIM_CurrentSensor.NominalReading
- CIM_CurrentSensor.NormalMax
- CIM_CurrentSensor.NormalMin
- CIM_CurrentSensor.PNPDeviceID
- CIM_CurrentSensor.PowerManagementCapabilities
- CIM_CurrentSensor.PowerManagementSupported
- CIM_CurrentSensor.Resolution
- CIM_CurrentSensor.Status
- CIM_CurrentSensor.StatusInfo
- CIM_CurrentSensor.SystemCreationClassName
- CIM_CurrentSensor.SystemName
- CIM_CurrentSensor.Tolerance
- CIM_CurrentSensor.UpperThresholdCritical
- CIM_CurrentSensor.UpperThresholdFatal
- CIM_CurrentSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1fe2a34e2e598d5c9655abbf84324dbf9982e416
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141773"
---
# <a name="cim_currentsensor-class"></a><span data-ttu-id="e10b9-103">\_Класс CIM куррентсенсор</span><span class="sxs-lookup"><span data-stu-id="e10b9-103">CIM\_CurrentSensor class</span></span>

<span data-ttu-id="e10b9-104">Класс **CIM \_ куррентсенсор** существует для обеспечения обратной совместимости с более ранними определениями схемы CIM.</span><span class="sxs-lookup"><span data-stu-id="e10b9-104">The **CIM\_CurrentSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span>

<span data-ttu-id="e10b9-105">Добавление к [**\_ датчику CIM**](cim-sensor.md) и [**cim \_ NumericSensor**](cim-numericsensor.md) в версии 2,2 больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="e10b9-105">Additions to [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) in version 2.2 make it no longer necessary.</span></span> <span data-ttu-id="e10b9-106">Класс **CIM \_ куррентсенсор** можно определить, установив свойство **сенсортипе** , наследуемое от **\_ датчика CIM**, на 4 ("Current").</span><span class="sxs-lookup"><span data-stu-id="e10b9-106">A **CIM\_CurrentSensor** class can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 4 ("Current").</span></span> <span data-ttu-id="e10b9-107">Другие свойства этого класса жестко запрограммированы на постоянные значения, которые соответствуют определениям в иерархии датчика.</span><span class="sxs-lookup"><span data-stu-id="e10b9-107">Other properties of this class are hard-coded to constant values, which correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e10b9-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="e10b9-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e10b9-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e10b9-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e10b9-110">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e10b9-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="e10b9-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e10b9-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e10b9-112">Syntax</span></span>

``` syntax
[UUID("{DCA1D084-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_CurrentSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="e10b9-113">Члены</span><span class="sxs-lookup"><span data-stu-id="e10b9-113">Members</span></span>

<span data-ttu-id="e10b9-114">Класс **CIM \_ куррентсенсор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e10b9-114">The **CIM\_CurrentSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="e10b9-115">Методы</span><span class="sxs-lookup"><span data-stu-id="e10b9-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="e10b9-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="e10b9-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e10b9-117">Методы</span><span class="sxs-lookup"><span data-stu-id="e10b9-117">Methods</span></span>

<span data-ttu-id="e10b9-118">Класс **CIM \_ куррентсенсор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e10b9-118">The **CIM\_CurrentSensor** class has these methods.</span></span>



| <span data-ttu-id="e10b9-119">Метод</span><span class="sxs-lookup"><span data-stu-id="e10b9-119">Method</span></span>                                                                   | <span data-ttu-id="e10b9-120">Описание</span><span class="sxs-lookup"><span data-stu-id="e10b9-120">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e10b9-121">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="e10b9-121">**Reset**</span></span>](reset-method-in-class-cim-currentsensor.md)                 | <span data-ttu-id="e10b9-122">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="e10b9-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="e10b9-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="e10b9-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e10b9-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-currentsensor.md) | <span data-ttu-id="e10b9-125">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="e10b9-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="e10b9-126">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="e10b9-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e10b9-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="e10b9-127">Properties</span></span>

<span data-ttu-id="e10b9-128">Класс **CIM \_ куррентсенсор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-128">The **CIM\_CurrentSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e10b9-129">**Точность**</span><span class="sxs-lookup"><span data-stu-id="e10b9-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-130">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-132">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("точность"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая пробная зонда 001,19 (DMTF \| )</span><span class="sxs-lookup"><span data-stu-id="e10b9-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-133">Точность датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="e10b9-134">Его значение записывается как плюс или минус сотые доли процента.</span><span class="sxs-lookup"><span data-stu-id="e10b9-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="e10b9-135">Это свойство, а также свойства **разрешения** и **допуска** используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="e10b9-136">Точность может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="e10b9-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="e10b9-137">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-138">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="e10b9-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e10b9-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-141">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="e10b9-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-142">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-142">Availability and status of the device.</span></span>

<span data-ttu-id="e10b9-143">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e10b9-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e10b9-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e10b9-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="e10b9-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e10b9-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="e10b9-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e10b9-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="e10b9-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e10b9-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="e10b9-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e10b9-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="e10b9-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e10b9-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="e10b9-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e10b9-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="e10b9-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e10b9-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="e10b9-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e10b9-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="e10b9-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e10b9-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="e10b9-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e10b9-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="e10b9-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e10b9-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="e10b9-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-157">Энергосбережение неизвестно.</span><span class="sxs-lookup"><span data-stu-id="e10b9-157">Power save   unknown.</span></span>

<span data-ttu-id="e10b9-158">Устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="e10b9-158">Device is in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e10b9-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="e10b9-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-160">Режим энергосбережения с низким энергопотреблением.</span><span class="sxs-lookup"><span data-stu-id="e10b9-160">Power save   low-power mode.</span></span>

<span data-ttu-id="e10b9-161">Устройство находится в режиме энергосбережения и по-прежнему работает, но может демонстрировать снижение производительности.</span><span class="sxs-lookup"><span data-stu-id="e10b9-161">Device is in a power-save mode and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e10b9-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="e10b9-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-163">Энергосбережение в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="e10b9-163">Power save   standby.</span></span>

<span data-ttu-id="e10b9-164">Устройство не работает, но его можно полностью быстро включить.</span><span class="sxs-lookup"><span data-stu-id="e10b9-164">Device is not functioning, but it could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e10b9-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="e10b9-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e10b9-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="e10b9-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-167">Предупреждение Power Save.</span><span class="sxs-lookup"><span data-stu-id="e10b9-167">Power save   warning.</span></span>

<span data-ttu-id="e10b9-168">Устройство находится в состоянии предупреждения и режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="e10b9-168">Device is in a warning state and a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e10b9-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="e10b9-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e10b9-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="e10b9-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e10b9-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="e10b9-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e10b9-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="e10b9-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-173">Текущий датчик недоступен.</span><span class="sxs-lookup"><span data-stu-id="e10b9-173">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e10b9-174">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e10b9-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e10b9-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-177">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e10b9-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-178">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e10b9-178">Short textual description of the object.</span></span>

<span data-ttu-id="e10b9-179">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-180">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="e10b9-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-181">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-183">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e10b9-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-184">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e10b9-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="e10b9-185">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e10b9-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e10b9-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="e10b9-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-188">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="e10b9-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e10b9-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e10b9-190">(1)</span><span class="sxs-lookup"><span data-stu-id="e10b9-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-191">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="e10b9-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e10b9-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e10b9-193">(2)</span><span class="sxs-lookup"><span data-stu-id="e10b9-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e10b9-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e10b9-195">(3)</span><span class="sxs-lookup"><span data-stu-id="e10b9-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-196">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e10b9-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e10b9-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e10b9-198">(4)</span><span class="sxs-lookup"><span data-stu-id="e10b9-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-199">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="e10b9-199">Device is not working properly.</span></span> <span data-ttu-id="e10b9-200">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="e10b9-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e10b9-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e10b9-202">(5)</span><span class="sxs-lookup"><span data-stu-id="e10b9-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-203">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="e10b9-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e10b9-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e10b9-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="e10b9-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-206">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="e10b9-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e10b9-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e10b9-208">(7)</span><span class="sxs-lookup"><span data-stu-id="e10b9-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e10b9-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e10b9-210">(8)</span><span class="sxs-lookup"><span data-stu-id="e10b9-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-211">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e10b9-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e10b9-213">(9)</span><span class="sxs-lookup"><span data-stu-id="e10b9-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-214">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-214">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e10b9-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e10b9-216">(10)</span><span class="sxs-lookup"><span data-stu-id="e10b9-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-217">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="e10b9-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e10b9-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e10b9-219">(11)</span><span class="sxs-lookup"><span data-stu-id="e10b9-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-220">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e10b9-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e10b9-222">(12)</span><span class="sxs-lookup"><span data-stu-id="e10b9-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-223">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="e10b9-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e10b9-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e10b9-225">(13)</span><span class="sxs-lookup"><span data-stu-id="e10b9-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-226">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e10b9-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e10b9-228">(14)</span><span class="sxs-lookup"><span data-stu-id="e10b9-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-229">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="e10b9-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e10b9-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e10b9-231">(15)</span><span class="sxs-lookup"><span data-stu-id="e10b9-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-232">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="e10b9-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e10b9-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e10b9-234">(16)</span><span class="sxs-lookup"><span data-stu-id="e10b9-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-235">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="e10b9-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e10b9-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e10b9-237">(17)</span><span class="sxs-lookup"><span data-stu-id="e10b9-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-238">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="e10b9-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e10b9-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e10b9-240">(18)</span><span class="sxs-lookup"><span data-stu-id="e10b9-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-241">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="e10b9-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e10b9-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e10b9-243">(19)</span><span class="sxs-lookup"><span data-stu-id="e10b9-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e10b9-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e10b9-245">(20)</span><span class="sxs-lookup"><span data-stu-id="e10b9-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-246">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="e10b9-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e10b9-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e10b9-248">(21)</span><span class="sxs-lookup"><span data-stu-id="e10b9-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-249">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="e10b9-249">System failure.</span></span> <span data-ttu-id="e10b9-250">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="e10b9-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e10b9-251">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="e10b9-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e10b9-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e10b9-253">(22)</span><span class="sxs-lookup"><span data-stu-id="e10b9-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-254">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="e10b9-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e10b9-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e10b9-256">(23)</span><span class="sxs-lookup"><span data-stu-id="e10b9-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-257">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="e10b9-257">System failure.</span></span> <span data-ttu-id="e10b9-258">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="e10b9-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e10b9-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e10b9-260">(24)</span><span class="sxs-lookup"><span data-stu-id="e10b9-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-261">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="e10b9-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e10b9-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e10b9-263">(25)</span><span class="sxs-lookup"><span data-stu-id="e10b9-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-264">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="e10b9-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e10b9-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e10b9-266">(26)</span><span class="sxs-lookup"><span data-stu-id="e10b9-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-267">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="e10b9-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e10b9-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e10b9-269">(27)</span><span class="sxs-lookup"><span data-stu-id="e10b9-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-270">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="e10b9-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e10b9-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e10b9-272">(28)</span><span class="sxs-lookup"><span data-stu-id="e10b9-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-273">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="e10b9-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e10b9-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e10b9-275">(29)</span><span class="sxs-lookup"><span data-stu-id="e10b9-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-276">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e10b9-276">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e10b9-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e10b9-278">(30)</span><span class="sxs-lookup"><span data-stu-id="e10b9-278">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-279">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="e10b9-279">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e10b9-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="e10b9-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e10b9-281">1-31</span><span class="sxs-lookup"><span data-stu-id="e10b9-281">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-282">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="e10b9-282">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e10b9-283">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="e10b9-283">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-284">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e10b9-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-286">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e10b9-286">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-287">Указывает, использует ли устройство определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="e10b9-287">Indicates whether the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e10b9-288">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-288">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-289">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e10b9-289">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-290">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e10b9-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-292">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e10b9-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-293">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e10b9-293">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e10b9-294">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="e10b9-294">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e10b9-295">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-296">**куррентреадинг**</span><span class="sxs-lookup"><span data-stu-id="e10b9-296">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-297">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-297">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-299">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("куррентреадинг"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,5 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-299">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-300">Текущее значение, указываемое датчиком.</span><span class="sxs-lookup"><span data-stu-id="e10b9-300">Current value indicated by the sensor.</span></span>

<span data-ttu-id="e10b9-301">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-301">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-302">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e10b9-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e10b9-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-305">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="e10b9-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-306">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e10b9-306">Textual description of the object.</span></span>

<span data-ttu-id="e10b9-307">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e10b9-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e10b9-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-311">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e10b9-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-312">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="e10b9-313">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-314">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="e10b9-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-315">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e10b9-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-317">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="e10b9-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="e10b9-318">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e10b9-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-320">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e10b9-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-322">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="e10b9-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="e10b9-323">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-324">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e10b9-324">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-325">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e10b9-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-327">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="e10b9-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-328">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="e10b9-328">Date and time when the object was installed.</span></span> <span data-ttu-id="e10b9-329">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="e10b9-329">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e10b9-330">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-331">**Линейно**</span><span class="sxs-lookup"><span data-stu-id="e10b9-331">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-332">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e10b9-332">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-334">Если **значение равно true**, датчик линейно помещается в динамический диапазон.</span><span class="sxs-lookup"><span data-stu-id="e10b9-334">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="e10b9-335">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-335">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-336">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="e10b9-336">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-337">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-339">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="e10b9-339">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e10b9-340">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-341">**ловерсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="e10b9-341">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-342">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-342">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-344">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ловерсрешолдкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,13 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-344">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-345">Пороговое значение, указывающее, работает ли датчик под критическими условиями.</span><span class="sxs-lookup"><span data-stu-id="e10b9-345">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="e10b9-346">Если свойство **куррентреадинг** находится между **ловерсрешолдкритикал** и **ловерсрешолдфатал**, то текущее состояние является критическим.</span><span class="sxs-lookup"><span data-stu-id="e10b9-346">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="e10b9-347">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-347">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-348">**ловерсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="e10b9-348">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-349">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-349">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-351">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ловерсрешолдфатал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,15 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-351">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-352">Пороговое значение, указывающее, работает ли датчик при неустранимых условиях.</span><span class="sxs-lookup"><span data-stu-id="e10b9-352">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="e10b9-353">Если свойство **куррентреадинг** находится ниже **ловерсрешолдфатал**, то текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="e10b9-353">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="e10b9-354">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-354">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-355">**ловерсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="e10b9-355">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-356">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-356">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-358">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ловерсрешолднонкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,11 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-358">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-359">Пороговое значение, указывающее, работает ли датчик как обычные или некритические условия.</span><span class="sxs-lookup"><span data-stu-id="e10b9-359">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="e10b9-360">Если свойство **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, то датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="e10b9-360">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="e10b9-361">Если свойство **куррентреадинг** , однако, находится между **ловерсрешолднонкритикал** и **ловерсрешолдкритикал**, то текущее состояние не является критическим.</span><span class="sxs-lookup"><span data-stu-id="e10b9-361">If the **CurrentReading** property, however, is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="e10b9-362">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-362">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-363">**максреадабле**</span><span class="sxs-lookup"><span data-stu-id="e10b9-363">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-364">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-364">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-366">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("максреадабле"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,9 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-366">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-367">Самое большое значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="e10b9-367">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="e10b9-368">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-368">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-369">**минреадабле**</span><span class="sxs-lookup"><span data-stu-id="e10b9-369">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-370">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-370">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-372">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("минреадабле"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,10 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-372">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-373">Наименьшее значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="e10b9-373">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="e10b9-374">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-374">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-375">**Name**</span><span class="sxs-lookup"><span data-stu-id="e10b9-375">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-376">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e10b9-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-378">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="e10b9-378">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-379">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="e10b9-379">Label by which the object is known.</span></span> <span data-ttu-id="e10b9-380">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="e10b9-380">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e10b9-381">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-381">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-382">**номиналреадинг**</span><span class="sxs-lookup"><span data-stu-id="e10b9-382">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-383">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-383">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-385">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("номиналреадинг"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,6 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-385">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-386">Ожидаемое значение для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="e10b9-386">Expected value for the numeric sensor.</span></span>

<span data-ttu-id="e10b9-387">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-387">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-388">**нормалмакс**</span><span class="sxs-lookup"><span data-stu-id="e10b9-388">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-389">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-389">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-391">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("нормалмакс"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,7 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-391">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-392">Нормальный максимальный диапазон для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="e10b9-392">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="e10b9-393">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-393">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-394">**нормалмин**</span><span class="sxs-lookup"><span data-stu-id="e10b9-394">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-395">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-395">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-397">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("нормалмин"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,8 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-397">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-398">Нормальный минимальный диапазон для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="e10b9-398">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="e10b9-399">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-399">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-400">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e10b9-400">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-401">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e10b9-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-403">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e10b9-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-404">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-404">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="e10b9-405">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e10b9-405">Example: "\*PNP030b"</span></span>

<span data-ttu-id="e10b9-406">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-407">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="e10b9-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-408">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e10b9-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-410">Конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="e10b9-410">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="e10b9-411">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e10b9-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e10b9-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e10b9-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="e10b9-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e10b9-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="e10b9-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e10b9-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="e10b9-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-416">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="e10b9-416">Power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e10b9-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="e10b9-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-418">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="e10b9-418">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e10b9-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="e10b9-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-420">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="e10b9-420">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e10b9-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="e10b9-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-422">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="e10b9-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e10b9-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="e10b9-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e10b9-424">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="e10b9-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e10b9-425">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="e10b9-425">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-426">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e10b9-426">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-427">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-428">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="e10b9-428">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="e10b9-429">Это свойство не указывает на то, что функции управления питанием в настоящее время включены или включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e10b9-429">This property does not indicate that power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="e10b9-430">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="e10b9-430">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="e10b9-431">Если **false**, то целочисленное значение 1 для строки "не поддерживается" должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="e10b9-431">If **FALSE**, the integer value 1, for the string "Not Supported", should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="e10b9-432">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-433">**Решение**</span><span class="sxs-lookup"><span data-stu-id="e10b9-433">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-434">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-436">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("разрешение"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,17 (DMTF), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("десятые доли миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-436">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-437">Способность датчика разрешать различия в измеряемом свойстве.</span><span class="sxs-lookup"><span data-stu-id="e10b9-437">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="e10b9-438">Это свойство, а также свойства **точности** и **допуска** используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-438">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="e10b9-439">Это значение может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="e10b9-439">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="e10b9-440">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-440">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-441">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e10b9-441">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-442">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e10b9-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-443">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-444">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="e10b9-444">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-445">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e10b9-445">String that indicates the current status of the object.</span></span> <span data-ttu-id="e10b9-446">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="e10b9-446">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="e10b9-447">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="e10b9-447">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e10b9-448">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="e10b9-448">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e10b9-449">Невыполняемое состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="e10b9-449">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e10b9-450">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="e10b9-450">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e10b9-451">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="e10b9-451">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e10b9-452">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e10b9-453">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="e10b9-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e10b9-454">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="e10b9-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e10b9-455">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="e10b9-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e10b9-456">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="e10b9-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e10b9-457">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="e10b9-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e10b9-458">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="e10b9-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e10b9-459">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="e10b9-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e10b9-460">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="e10b9-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e10b9-461">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="e10b9-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e10b9-462">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="e10b9-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e10b9-463">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="e10b9-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e10b9-464">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="e10b9-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e10b9-465">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="e10b9-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e10b9-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e10b9-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-467">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e10b9-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-468">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-469">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="e10b9-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-470">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-470">State of the logical device.</span></span> <span data-ttu-id="e10b9-471">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="e10b9-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e10b9-472">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e10b9-473">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e10b9-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e10b9-474">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="e10b9-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e10b9-475">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="e10b9-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e10b9-476">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="e10b9-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e10b9-477">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="e10b9-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e10b9-478">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="e10b9-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-479">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e10b9-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-480">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-481">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e10b9-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-482">Свойство свойства **CreationClassName** системы.</span><span class="sxs-lookup"><span data-stu-id="e10b9-482">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="e10b9-483">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-484">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e10b9-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-485">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e10b9-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-486">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-487">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e10b9-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-488">Свойство **имени** системы области.</span><span class="sxs-lookup"><span data-stu-id="e10b9-488">Scoping system's **Name** property.</span></span>

<span data-ttu-id="e10b9-489">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e10b9-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-490">**Отклонение**</span><span class="sxs-lookup"><span data-stu-id="e10b9-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-491">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-492">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-493">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Допуск"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,18 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-494">Допуск датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="e10b9-495">Это свойство, а также свойства **разрешения** и **точности** используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="e10b9-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="e10b9-496">Допуск может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="e10b9-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-497">**упперсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="e10b9-497">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-498">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-498">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-499">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-500">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("упперсрешолдкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,14 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-500">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-501">Пороговое значение, указывающее, работает ли датчик под критическими условиями.</span><span class="sxs-lookup"><span data-stu-id="e10b9-501">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="e10b9-502">Если свойство **куррентреадинг** находится между **упперсрешолдкритикал** и **упперсрешолдфатал**, то текущее состояние является критическим.</span><span class="sxs-lookup"><span data-stu-id="e10b9-502">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="e10b9-503">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-503">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-504">**упперсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="e10b9-504">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-505">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-505">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-506">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-507">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("упперсрешолдфатал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,16 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-507">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-508">Пороговое значение, указывающее, работает ли датчик при неустранимых условиях.</span><span class="sxs-lookup"><span data-stu-id="e10b9-508">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="e10b9-509">Если свойство **куррентреадинг** выше **упперсрешолдфатал**, то текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="e10b9-509">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="e10b9-510">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-510">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="e10b9-511">**упперсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="e10b9-511">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e10b9-512">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e10b9-512">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-513">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e10b9-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e10b9-514">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("упперсрешолднонкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Текущая зонда \| 001,12 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="e10b9-514">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="e10b9-515">Пороговое значение, указывающее, работает ли датчик как обычные или некритические условия.</span><span class="sxs-lookup"><span data-stu-id="e10b9-515">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="e10b9-516">Если свойство **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, то датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="e10b9-516">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="e10b9-517">Если свойство **куррентреадинг** , однако, находится между **упперсрешолднонкритикал** и **упперсрешолдкритикал**, то текущее состояние не является критическим.</span><span class="sxs-lookup"><span data-stu-id="e10b9-517">If the **CurrentReading** property, however, is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="e10b9-518">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-518">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e10b9-519">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e10b9-519">Remarks</span></span>

<span data-ttu-id="e10b9-520">Класс **CIM \_ куррентсенсор** является производным от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-520">The **CIM\_CurrentSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="e10b9-521">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="e10b9-521">WMI does not implement this class.</span></span> <span data-ttu-id="e10b9-522">Дополнительные сведения о классах WMI, производных от **CIM \_ куррентсенсор**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e10b9-522">For more information about WMI classes derived from **CIM\_CurrentSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e10b9-523">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="e10b9-523">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e10b9-524">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e10b9-524">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e10b9-525">Требования</span><span class="sxs-lookup"><span data-stu-id="e10b9-525">Requirements</span></span>



| <span data-ttu-id="e10b9-526">Требование</span><span class="sxs-lookup"><span data-stu-id="e10b9-526">Requirement</span></span> | <span data-ttu-id="e10b9-527">Значение</span><span class="sxs-lookup"><span data-stu-id="e10b9-527">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e10b9-528">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e10b9-528">Minimum supported client</span></span><br/> | <span data-ttu-id="e10b9-529">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e10b9-529">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e10b9-530">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e10b9-530">Minimum supported server</span></span><br/> | <span data-ttu-id="e10b9-531">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e10b9-531">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e10b9-532">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e10b9-532">Namespace</span></span><br/>                | <span data-ttu-id="e10b9-533">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e10b9-533">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e10b9-534">MOF</span><span class="sxs-lookup"><span data-stu-id="e10b9-534">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e10b9-535"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e10b9-535"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e10b9-536">DLL</span><span class="sxs-lookup"><span data-stu-id="e10b9-536">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e10b9-537"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e10b9-537"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e10b9-538">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e10b9-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10b9-539">**CIM \_ NumericSensor**</span><span class="sxs-lookup"><span data-stu-id="e10b9-539">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

