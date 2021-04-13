---
description: Класс CIM \_ датчик температуры существует для обеспечения обратной совместимости с более ранними определениями схемы CIM.
ms.assetid: ddef21db-e33a-4e2b-ac31-df3f0acd6fc2
ms.tgt_platform: multiple
title: Класс CIM_TemperatureSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TemperatureSensor
- CIM_TemperatureSensor.Accuracy
- CIM_TemperatureSensor.Availability
- CIM_TemperatureSensor.Caption
- CIM_TemperatureSensor.ConfigManagerErrorCode
- CIM_TemperatureSensor.ConfigManagerUserConfig
- CIM_TemperatureSensor.CreationClassName
- CIM_TemperatureSensor.CurrentReading
- CIM_TemperatureSensor.Description
- CIM_TemperatureSensor.DeviceID
- CIM_TemperatureSensor.ErrorCleared
- CIM_TemperatureSensor.ErrorDescription
- CIM_TemperatureSensor.InstallDate
- CIM_TemperatureSensor.IsLinear
- CIM_TemperatureSensor.LastErrorCode
- CIM_TemperatureSensor.LowerThresholdCritical
- CIM_TemperatureSensor.LowerThresholdFatal
- CIM_TemperatureSensor.LowerThresholdNonCritical
- CIM_TemperatureSensor.MaxReadable
- CIM_TemperatureSensor.MinReadable
- CIM_TemperatureSensor.Name
- CIM_TemperatureSensor.NominalReading
- CIM_TemperatureSensor.NormalMax
- CIM_TemperatureSensor.NormalMin
- CIM_TemperatureSensor.PNPDeviceID
- CIM_TemperatureSensor.PowerManagementCapabilities
- CIM_TemperatureSensor.PowerManagementSupported
- CIM_TemperatureSensor.Resolution
- CIM_TemperatureSensor.Status
- CIM_TemperatureSensor.StatusInfo
- CIM_TemperatureSensor.SystemCreationClassName
- CIM_TemperatureSensor.SystemName
- CIM_TemperatureSensor.Tolerance
- CIM_TemperatureSensor.UpperThresholdCritical
- CIM_TemperatureSensor.UpperThresholdFatal
- CIM_TemperatureSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f48988db3cb213c06013b7ebac61095dbc365daa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342362"
---
# <a name="cim_temperaturesensor-class"></a><span data-ttu-id="c0aa3-103">\_Класс CIM датчик температуры</span><span class="sxs-lookup"><span data-stu-id="c0aa3-103">CIM\_TemperatureSensor class</span></span>

<span data-ttu-id="c0aa3-104">Класс **CIM \_ датчик температуры** существует для обеспечения обратной совместимости с более ранними определениями схемы CIM.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-104">The **CIM\_TemperatureSensor** class exists for backward compatibility with earlier CIM schema definitions.</span></span> <span data-ttu-id="c0aa3-105">Благодаря дополнениям к классам [**\_ датчиков CIM**](cim-sensor.md) и [**модели cim \_ NumericSensor**](cim-numericsensor.md) в версии 2,2 больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-105">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="c0aa3-106">Датчик температуры можно определить, установив свойство **сенсортипе** , наследуемое от **\_ датчика CIM**, на 2 ("температура").</span><span class="sxs-lookup"><span data-stu-id="c0aa3-106">A temperature sensor can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 2 ("Temperature").</span></span> <span data-ttu-id="c0aa3-107">Другие свойства этого класса задаются жестко как постоянные значения, соответствующие определениям в иерархии датчика.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-107">Other properties of this class are hardcoded as constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0aa3-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c0aa3-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c0aa3-110">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c0aa3-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0aa3-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0aa3-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979D-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_TemperatureSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="c0aa3-113">Члены</span><span class="sxs-lookup"><span data-stu-id="c0aa3-113">Members</span></span>

<span data-ttu-id="c0aa3-114">Класс **CIM \_ датчик температуры** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c0aa3-114">The **CIM\_TemperatureSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="c0aa3-115">Методы</span><span class="sxs-lookup"><span data-stu-id="c0aa3-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="c0aa3-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0aa3-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c0aa3-117">Методы</span><span class="sxs-lookup"><span data-stu-id="c0aa3-117">Methods</span></span>

<span data-ttu-id="c0aa3-118">Класс **CIM \_ датчик температуры** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-118">The **CIM\_TemperatureSensor** class has these methods.</span></span>



| <span data-ttu-id="c0aa3-119">Метод</span><span class="sxs-lookup"><span data-stu-id="c0aa3-119">Method</span></span>                                                                       | <span data-ttu-id="c0aa3-120">Описание</span><span class="sxs-lookup"><span data-stu-id="c0aa3-120">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0aa3-121">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-121">**Reset**</span></span>](reset-method-in-class-cim-temperaturesensor.md)                 | <span data-ttu-id="c0aa3-122">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="c0aa3-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="c0aa3-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-temperaturesensor.md) | <span data-ttu-id="c0aa3-125">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c0aa3-126">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c0aa3-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0aa3-127">Properties</span></span>

<span data-ttu-id="c0aa3-128">Класс **CIM \_ датчик температуры** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-128">The **CIM\_TemperatureSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0aa3-129">**Точность**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-130">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-132">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("точность"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Пробная температура DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-133">Точность датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="c0aa3-134">Его значение записывается как плюс или минус сотые доли процента.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="c0aa3-135">Это свойство, а также свойства **разрешения** и **допуска** используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="c0aa3-136">Точность может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="c0aa3-137">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-138">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-141">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-142">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-142">Availability and status of the device.</span></span>

<span data-ttu-id="c0aa3-143">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c0aa3-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0aa3-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c0aa3-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-147">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="c0aa3-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c0aa3-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c0aa3-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c0aa3-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c0aa3-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c0aa3-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c0aa3-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c0aa3-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c0aa3-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c0aa3-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c0aa3-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-158">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c0aa3-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-160">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c0aa3-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-162">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c0aa3-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c0aa3-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-165">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c0aa3-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-167">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c0aa3-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-169">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c0aa3-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-171">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c0aa3-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-173">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0aa3-174">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-177">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-178">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-178">Short textual description of the object.</span></span>

<span data-ttu-id="c0aa3-179">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-180">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-181">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-183">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-184">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c0aa3-185">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c0aa3-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c0aa3-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-188">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c0aa3-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c0aa3-190">(1)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-191">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c0aa3-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c0aa3-193">(2)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c0aa3-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c0aa3-195">(3)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-196">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c0aa3-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c0aa3-198">(4)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-199">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-199">Device is not working properly.</span></span> <span data-ttu-id="c0aa3-200">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c0aa3-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c0aa3-202">(5)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-203">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c0aa3-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c0aa3-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-206">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c0aa3-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c0aa3-208">(7)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c0aa3-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c0aa3-210">(8)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-211">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c0aa3-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c0aa3-213">(9)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-214">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-214">Device is not working properly.</span></span> <span data-ttu-id="c0aa3-215">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c0aa3-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c0aa3-217">(10)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-218">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c0aa3-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c0aa3-220">(11)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-221">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c0aa3-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c0aa3-223">(12)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-224">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c0aa3-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c0aa3-226">(13)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-227">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c0aa3-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c0aa3-229">(14)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-230">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c0aa3-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c0aa3-232">(15)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-233">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c0aa3-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c0aa3-235">(16)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-236">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c0aa3-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c0aa3-238">(17)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-239">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c0aa3-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c0aa3-241">(18)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-242">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c0aa3-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c0aa3-244">(19)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c0aa3-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c0aa3-246">(20)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-247">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c0aa3-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c0aa3-249">(21)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-250">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-250">System failure.</span></span> <span data-ttu-id="c0aa3-251">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c0aa3-252">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c0aa3-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c0aa3-254">(22)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-255">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c0aa3-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c0aa3-257">(23)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-258">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-258">System failure.</span></span> <span data-ttu-id="c0aa3-259">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c0aa3-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c0aa3-261">(24)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-262">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c0aa3-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c0aa3-264">(25)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-265">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c0aa3-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c0aa3-267">(26)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-268">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c0aa3-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c0aa3-270">(27)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-271">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c0aa3-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c0aa3-273">(28)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-274">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c0aa3-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c0aa3-276">(29)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-277">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-277">Device is disabled.</span></span> <span data-ttu-id="c0aa3-278">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c0aa3-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c0aa3-280">(30)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-281">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c0aa3-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c0aa3-283">1-31</span><span class="sxs-lookup"><span data-stu-id="c0aa3-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-284">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-284">Device is not working properly.</span></span> <span data-ttu-id="c0aa3-285">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0aa3-286">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-287">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-289">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-290">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c0aa3-291">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-295">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-296">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c0aa3-297">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c0aa3-298">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-299">**куррентреадинг**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-299">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-300">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-300">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-302">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("куррентреадинг"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,5 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-302">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-303">Текущее значение, указываемое датчиком.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-303">Current value indicated by the sensor.</span></span>

<span data-ttu-id="c0aa3-304">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-304">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-305">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-305">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-306">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-308">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-308">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-309">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-309">Textual description of the object.</span></span>

<span data-ttu-id="c0aa3-310">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-311">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-311">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-312">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-314">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-314">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-315">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-315">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c0aa3-316">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-317">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-317">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-318">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-320">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-320">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c0aa3-321">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-322">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-322">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-323">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-325">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-325">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c0aa3-326">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-327">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-327">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-328">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-328">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-330">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-331">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-331">Date and time the object was installed.</span></span> <span data-ttu-id="c0aa3-332">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-332">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c0aa3-333">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-334">**Линейно**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-334">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-335">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-337">Если **значение равно true**, датчик линейно помещается в динамический диапазон.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-337">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="c0aa3-338">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-338">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-339">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-340">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-342">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-342">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c0aa3-343">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-343">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-344">**ловерсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-344">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-345">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-345">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-347">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ловерсрешолдкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,13 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-347">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-348">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="c0aa3-349">Если свойство **куррентреадинг** находится между **ловерсрешолдкритикал** и **ловерсрешолдфатал**, то текущее состояние является критическим.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-349">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="c0aa3-350">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-350">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-351">**ловерсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-351">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-352">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-352">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-354">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ловерсрешолдфатал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,15 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-354">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-355">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-355">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="c0aa3-356">Если свойство **куррентреадинг** находится ниже **ловерсрешолдфатал**, то текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-356">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="c0aa3-357">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-357">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-358">**ловерсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-358">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-359">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-359">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-360">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-361">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ловерсрешолднонкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-361">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-362">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-362">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="c0aa3-363">Если свойство **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, то датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-363">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="c0aa3-364">Если свойство **куррентреадинг** находится между **ловерсрешолднонкритикал** и **ловерсрешолдкритикал**, то текущее состояние не является критическим.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="c0aa3-365">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-366">**максреадабле**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-366">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-367">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-369">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("максреадабле"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,9 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-369">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-370">Самое большое значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-370">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="c0aa3-371">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-372">**минреадабле**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-372">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-373">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-373">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-375">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("минреадабле"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,10 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-375">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-376">Наименьшее значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-376">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="c0aa3-377">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-377">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-378">**Name**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-378">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-381">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-381">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-382">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-382">Label by which the object is known.</span></span> <span data-ttu-id="c0aa3-383">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-383">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c0aa3-384">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-384">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-385">**номиналреадинг**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-385">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-386">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-388">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("номиналреадинг"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,6 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-388">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-389">Для числового датчика требуется или нормальное значение.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-389">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="c0aa3-390">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-391">**нормалмакс**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-391">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-392">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-394">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("нормалмакс"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,7 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-394">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-395">Нормальный максимальный диапазон для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-395">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="c0aa3-396">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-397">**нормалмин**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-397">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-398">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-398">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-400">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("нормалмин"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,8 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-400">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-401">Нормальный минимальный диапазон для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-401">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="c0aa3-402">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-402">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-403">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-403">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-404">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-406">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-406">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-407">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-407">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="c0aa3-408">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c0aa3-409">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c0aa3-409">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-410">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-410">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-411">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c0aa3-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-412">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-413">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-413">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c0aa3-414">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-414">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0aa3-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-415"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c0aa3-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-416"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c0aa3-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-417"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c0aa3-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-418"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-419">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-419">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c0aa3-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-420"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-421">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-421">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c0aa3-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-422"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-423">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="c0aa3-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c0aa3-424">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-424">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c0aa3-425">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-425">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c0aa3-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-426"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-427">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-427">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c0aa3-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-428"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c0aa3-429">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-429">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c0aa3-430">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-430">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-431">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-431">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-433">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-433">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c0aa3-434">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="c0aa3-434">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c0aa3-435">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-435">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c0aa3-436">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="c0aa3-436">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="c0aa3-437">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-438">**Решение**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-438">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-439">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-441">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("разрешение"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,17 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" сотые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-441">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-442">Способность датчика разрешать различия в измеряемом свойстве.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-442">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="c0aa3-443">Это значение может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-443">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="c0aa3-444">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-444">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-445">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-446">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-447">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-448">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-449">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-449">Current status of the object.</span></span> <span data-ttu-id="c0aa3-450">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c0aa3-451">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="c0aa3-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c0aa3-452">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c0aa3-453">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c0aa3-454">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0aa3-455">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c0aa3-456">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c0aa3-457">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c0aa3-458">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c0aa3-459">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c0aa3-460">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c0aa3-461">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c0aa3-462">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c0aa3-463">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0aa3-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-465">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-466">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-467">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-468">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-468">State of the logical device.</span></span> <span data-ttu-id="c0aa3-469">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c0aa3-470">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c0aa3-471">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c0aa3-472">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c0aa3-473">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c0aa3-474">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c0aa3-475">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0aa3-476">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-477">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-478">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-479">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-480">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="c0aa3-481">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-482">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-483">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-484">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-485">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0aa3-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-486">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-486">Scoping system's name.</span></span>

<span data-ttu-id="c0aa3-487">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-488">**Отклонение**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-488">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-489">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-489">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-490">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-491">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Допуск"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,18 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-491">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-492">Допуск датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-492">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="c0aa3-493">Это свойство, а также свойства **разрешения** и **точности** используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-493">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="c0aa3-494">Допуск может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-494">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="c0aa3-495">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-495">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-496">**упперсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-496">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-497">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-497">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-498">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-498">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-499">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("упперсрешолдкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,14 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-499">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-500">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-500">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="c0aa3-501">Если свойство **куррентреадинг** находится между **упперсрешолдкритикал** и **упперсрешолдфатал**, то текущее состояние является критическим.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-501">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="c0aa3-502">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-502">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-503">**упперсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-503">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-504">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-504">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-505">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-506">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("упперсрешолдфатал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,16 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-506">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-507">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-507">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="c0aa3-508">Если свойство **куррентреадинг** выше **упперсрешолдфатал**, то текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-508">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="c0aa3-509">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-509">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0aa3-510">**упперсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-510">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0aa3-511">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-511">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-512">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0aa3-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0aa3-513">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("упперсрешолднонкритикал"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Зонд температуры DMTF \| 001,12 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="c0aa3-513">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Temperature Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="c0aa3-514">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-514">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="c0aa3-515">Если свойство **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, то датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-515">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="c0aa3-516">Если свойство **куррентреадинг** находится между **упперсрешолднонкритикал** и **упперсрешолдкритикал**, то текущее состояние не является критическим.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-516">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="c0aa3-517">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-517">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0aa3-518">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0aa3-518">Remarks</span></span>

<span data-ttu-id="c0aa3-519">Класс **CIM \_ датчик температуры** является производным от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-519">The **CIM\_TemperatureSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="c0aa3-520">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-520">WMI does not implement this class.</span></span> <span data-ttu-id="c0aa3-521">Классы WMI, производные от **CIM \_ датчик температуры**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c0aa3-521">For WMI classes derived from **CIM\_TemperatureSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c0aa3-522">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-522">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c0aa3-523">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c0aa3-523">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0aa3-524">Требования</span><span class="sxs-lookup"><span data-stu-id="c0aa3-524">Requirements</span></span>



| <span data-ttu-id="c0aa3-525">Требование</span><span class="sxs-lookup"><span data-stu-id="c0aa3-525">Requirement</span></span> | <span data-ttu-id="c0aa3-526">Значение</span><span class="sxs-lookup"><span data-stu-id="c0aa3-526">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0aa3-527">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0aa3-527">Minimum supported client</span></span><br/> | <span data-ttu-id="c0aa3-528">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0aa3-528">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0aa3-529">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0aa3-529">Minimum supported server</span></span><br/> | <span data-ttu-id="c0aa3-530">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0aa3-530">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0aa3-531">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c0aa3-531">Namespace</span></span><br/>                | <span data-ttu-id="c0aa3-532">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c0aa3-532">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c0aa3-533">MOF</span><span class="sxs-lookup"><span data-stu-id="c0aa3-533">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0aa3-534"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0aa3-534"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0aa3-535">DLL</span><span class="sxs-lookup"><span data-stu-id="c0aa3-535">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0aa3-536"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0aa3-536"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0aa3-537">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0aa3-537">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0aa3-538">**CIM \_ NumericSensor**</span><span class="sxs-lookup"><span data-stu-id="c0aa3-538">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

