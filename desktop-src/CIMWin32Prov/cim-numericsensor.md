---
description: Класс CIM \_ NumericSensor представляет числовой датчик, который возвращает числовые показания и при необходимости поддерживает параметры пороговых значений.
ms.assetid: 9be9ee28-24ee-49d1-871f-73b504c77518
ms.tgt_platform: multiple
title: Класс CIM_NumericSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NumericSensor
- CIM_NumericSensor.Accuracy
- CIM_NumericSensor.Availability
- CIM_NumericSensor.Caption
- CIM_NumericSensor.ConfigManagerErrorCode
- CIM_NumericSensor.ConfigManagerUserConfig
- CIM_NumericSensor.CreationClassName
- CIM_NumericSensor.CurrentReading
- CIM_NumericSensor.Description
- CIM_NumericSensor.DeviceID
- CIM_NumericSensor.ErrorCleared
- CIM_NumericSensor.ErrorDescription
- CIM_NumericSensor.InstallDate
- CIM_NumericSensor.IsLinear
- CIM_NumericSensor.LastErrorCode
- CIM_NumericSensor.LowerThresholdCritical
- CIM_NumericSensor.LowerThresholdFatal
- CIM_NumericSensor.LowerThresholdNonCritical
- CIM_NumericSensor.MaxReadable
- CIM_NumericSensor.MinReadable
- CIM_NumericSensor.Name
- CIM_NumericSensor.NominalReading
- CIM_NumericSensor.NormalMax
- CIM_NumericSensor.NormalMin
- CIM_NumericSensor.PNPDeviceID
- CIM_NumericSensor.PowerManagementCapabilities
- CIM_NumericSensor.PowerManagementSupported
- CIM_NumericSensor.Resolution
- CIM_NumericSensor.Status
- CIM_NumericSensor.StatusInfo
- CIM_NumericSensor.SystemCreationClassName
- CIM_NumericSensor.SystemName
- CIM_NumericSensor.Tolerance
- CIM_NumericSensor.UpperThresholdCritical
- CIM_NumericSensor.UpperThresholdFatal
- CIM_NumericSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2888b56e39184b05484cacd587be140b94dc732e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655733"
---
# <a name="cim_numericsensor-class"></a><span data-ttu-id="e5636-103">\_Класс CIM NumericSensor</span><span class="sxs-lookup"><span data-stu-id="e5636-103">CIM\_NumericSensor class</span></span>

<span data-ttu-id="e5636-104">Класс **CIM \_ NumericSensor** представляет числовой датчик, который возвращает числовые показания и при необходимости поддерживает параметры пороговых значений.</span><span class="sxs-lookup"><span data-stu-id="e5636-104">The **CIM\_NumericSensor** class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e5636-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="e5636-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e5636-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e5636-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e5636-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e5636-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e5636-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="e5636-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5636-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5636-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979C-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_NumericSensor : CIM_Sensor
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

## <a name="members"></a><span data-ttu-id="e5636-110">Члены</span><span class="sxs-lookup"><span data-stu-id="e5636-110">Members</span></span>

<span data-ttu-id="e5636-111">Класс **CIM \_ NumericSensor** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e5636-111">The **CIM\_NumericSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="e5636-112">Методы</span><span class="sxs-lookup"><span data-stu-id="e5636-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="e5636-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5636-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e5636-114">Методы</span><span class="sxs-lookup"><span data-stu-id="e5636-114">Methods</span></span>

<span data-ttu-id="e5636-115">Класс **CIM \_ NumericSensor** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e5636-115">The **CIM\_NumericSensor** class has these methods.</span></span>



| <span data-ttu-id="e5636-116">Метод</span><span class="sxs-lookup"><span data-stu-id="e5636-116">Method</span></span>                                                                   | <span data-ttu-id="e5636-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e5636-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5636-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="e5636-118">**Reset**</span></span>](reset-method-in-class-cim-numericsensor.md)                 | <span data-ttu-id="e5636-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e5636-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="e5636-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="e5636-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="e5636-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e5636-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-numericsensor.md) | <span data-ttu-id="e5636-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="e5636-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="e5636-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="e5636-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e5636-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5636-124">Properties</span></span>

<span data-ttu-id="e5636-125">Класс **CIM \_ NumericSensor** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="e5636-125">The **CIM\_NumericSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5636-126">**Точность**</span><span class="sxs-lookup"><span data-stu-id="e5636-126">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-127">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-129">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("сотые доли процента")</span><span class="sxs-lookup"><span data-stu-id="e5636-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hundredths of percent")</span></span>
</dt> </dl>

<span data-ttu-id="e5636-130">Точность датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="e5636-130">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="e5636-131">Его значение записывается как плюс или минус сотые доли процента.</span><span class="sxs-lookup"><span data-stu-id="e5636-131">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="e5636-132">Это свойство, а также свойства **разрешения** и **допуска** используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="e5636-132">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="e5636-133">Точность может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="e5636-133">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-134">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="e5636-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5636-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-137">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="e5636-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="e5636-138">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="e5636-138">Availability and status of the device.</span></span>

<span data-ttu-id="e5636-139">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e5636-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e5636-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e5636-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="e5636-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="e5636-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="e5636-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="e5636-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="e5636-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="e5636-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="e5636-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e5636-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="e5636-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="e5636-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="e5636-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="e5636-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="e5636-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="e5636-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="e5636-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e5636-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="e5636-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="e5636-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="e5636-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="e5636-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="e5636-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="e5636-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="e5636-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-153">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="e5636-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="e5636-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="e5636-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-155">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="e5636-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="e5636-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="e5636-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-157">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="e5636-157">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="e5636-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="e5636-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="e5636-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="e5636-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-160">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="e5636-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e5636-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="e5636-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-162">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="e5636-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="e5636-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="e5636-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-164">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="e5636-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="e5636-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="e5636-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-166">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="e5636-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="e5636-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="e5636-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-168">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="e5636-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e5636-169">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e5636-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5636-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-172">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e5636-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e5636-173">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e5636-173">Short textual description of the object.</span></span>

<span data-ttu-id="e5636-174">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e5636-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-175">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="e5636-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-176">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5636-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-178">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e5636-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e5636-179">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="e5636-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="e5636-180">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="e5636-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="e5636-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="e5636-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="e5636-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-183">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="e5636-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="e5636-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="e5636-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="e5636-185">(1)</span><span class="sxs-lookup"><span data-stu-id="e5636-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-186">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="e5636-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e5636-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="e5636-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="e5636-188">(2)</span><span class="sxs-lookup"><span data-stu-id="e5636-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="e5636-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="e5636-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="e5636-190">(3)</span><span class="sxs-lookup"><span data-stu-id="e5636-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-191">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5636-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e5636-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="e5636-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="e5636-193">(4)</span><span class="sxs-lookup"><span data-stu-id="e5636-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-194">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="e5636-194">Device is not working properly.</span></span> <span data-ttu-id="e5636-195">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="e5636-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="e5636-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="e5636-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="e5636-197">(5)</span><span class="sxs-lookup"><span data-stu-id="e5636-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-198">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="e5636-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="e5636-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="e5636-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="e5636-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="e5636-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-201">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="e5636-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="e5636-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="e5636-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="e5636-203">(7)</span><span class="sxs-lookup"><span data-stu-id="e5636-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="e5636-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="e5636-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="e5636-205">(8)</span><span class="sxs-lookup"><span data-stu-id="e5636-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-206">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="e5636-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="e5636-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="e5636-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="e5636-208">(9)</span><span class="sxs-lookup"><span data-stu-id="e5636-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-209">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="e5636-209">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="e5636-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="e5636-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="e5636-211">(10)</span><span class="sxs-lookup"><span data-stu-id="e5636-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-212">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="e5636-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="e5636-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="e5636-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="e5636-214">(11)</span><span class="sxs-lookup"><span data-stu-id="e5636-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-215">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="e5636-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="e5636-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="e5636-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="e5636-217">(12)</span><span class="sxs-lookup"><span data-stu-id="e5636-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-218">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="e5636-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="e5636-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="e5636-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="e5636-220">(13)</span><span class="sxs-lookup"><span data-stu-id="e5636-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-221">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="e5636-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="e5636-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="e5636-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="e5636-223">(14)</span><span class="sxs-lookup"><span data-stu-id="e5636-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-224">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="e5636-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="e5636-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="e5636-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="e5636-226">(15)</span><span class="sxs-lookup"><span data-stu-id="e5636-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-227">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="e5636-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="e5636-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="e5636-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="e5636-229">(16)</span><span class="sxs-lookup"><span data-stu-id="e5636-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-230">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="e5636-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="e5636-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="e5636-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="e5636-232">(17)</span><span class="sxs-lookup"><span data-stu-id="e5636-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-233">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="e5636-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e5636-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="e5636-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="e5636-235">(18)</span><span class="sxs-lookup"><span data-stu-id="e5636-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-236">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="e5636-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="e5636-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="e5636-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="e5636-238">(19)</span><span class="sxs-lookup"><span data-stu-id="e5636-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="e5636-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="e5636-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="e5636-240">(20)</span><span class="sxs-lookup"><span data-stu-id="e5636-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-241">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="e5636-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="e5636-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="e5636-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="e5636-243">(21)</span><span class="sxs-lookup"><span data-stu-id="e5636-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-244">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="e5636-244">System failure.</span></span> <span data-ttu-id="e5636-245">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="e5636-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="e5636-246">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="e5636-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="e5636-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="e5636-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="e5636-248">(22)</span><span class="sxs-lookup"><span data-stu-id="e5636-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-249">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="e5636-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="e5636-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="e5636-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="e5636-251">(23)</span><span class="sxs-lookup"><span data-stu-id="e5636-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-252">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="e5636-252">System failure.</span></span> <span data-ttu-id="e5636-253">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="e5636-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="e5636-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="e5636-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="e5636-255">(24)</span><span class="sxs-lookup"><span data-stu-id="e5636-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-256">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="e5636-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e5636-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="e5636-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e5636-258">(25)</span><span class="sxs-lookup"><span data-stu-id="e5636-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-259">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="e5636-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="e5636-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="e5636-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="e5636-261">(26)</span><span class="sxs-lookup"><span data-stu-id="e5636-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-262">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="e5636-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="e5636-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="e5636-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="e5636-264">(27)</span><span class="sxs-lookup"><span data-stu-id="e5636-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-265">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="e5636-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="e5636-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="e5636-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="e5636-267">(28)</span><span class="sxs-lookup"><span data-stu-id="e5636-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-268">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="e5636-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="e5636-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="e5636-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="e5636-270">(29)</span><span class="sxs-lookup"><span data-stu-id="e5636-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-271">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e5636-271">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="e5636-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="e5636-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="e5636-273">(30)</span><span class="sxs-lookup"><span data-stu-id="e5636-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-274">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="e5636-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="e5636-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="e5636-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="e5636-276">1-31</span><span class="sxs-lookup"><span data-stu-id="e5636-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-277">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="e5636-277">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e5636-278">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="e5636-278">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-279">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5636-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-281">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e5636-281">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e5636-282">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="e5636-282">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="e5636-283">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-284">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e5636-284">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-285">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5636-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-287">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e5636-287">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e5636-288">Класс или подкласс, используемый при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="e5636-288">Class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e5636-289">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="e5636-289">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="e5636-290">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-291">**куррентреадинг**</span><span class="sxs-lookup"><span data-stu-id="e5636-291">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-292">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-292">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-294">Текущее значение, указываемое датчиком.</span><span class="sxs-lookup"><span data-stu-id="e5636-294">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-295">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5636-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-296">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5636-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-298">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="e5636-298">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e5636-299">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e5636-299">Textual description of the object.</span></span>

<span data-ttu-id="e5636-300">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e5636-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-301">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e5636-301">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-302">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5636-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-304">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e5636-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e5636-305">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e5636-305">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="e5636-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-307">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="e5636-307">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-308">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5636-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-310">Если **значение — true**, то ошибка, сообщаемая в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="e5636-310">If **TRUE**, the error reported in **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="e5636-311">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-312">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e5636-312">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5636-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-315">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="e5636-315">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="e5636-316">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e5636-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-318">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e5636-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-320">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="e5636-320">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e5636-321">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="e5636-321">Date and time the object was installed.</span></span> <span data-ttu-id="e5636-322">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="e5636-322">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="e5636-323">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e5636-323">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-324">**Линейно**</span><span class="sxs-lookup"><span data-stu-id="e5636-324">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-325">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5636-325">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-327">Если **значение равно true**, датчик линейно помещается в динамический диапазон.</span><span class="sxs-lookup"><span data-stu-id="e5636-327">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-328">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="e5636-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-329">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5636-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-331">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="e5636-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="e5636-332">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-333">**ловерсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="e5636-333">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-334">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-334">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-336">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="e5636-336">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="e5636-337">Если свойство **куррентреадинг** находится между **ловерсрешолдкритикал** и **ловерсрешолдфатал**, то текущее состояние является критическим.</span><span class="sxs-lookup"><span data-stu-id="e5636-337">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="e5636-338">Это свойство наследуется от **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="e5636-338">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-339">**ловерсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="e5636-339">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-340">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-340">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-342">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="e5636-342">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="e5636-343">Если свойство **куррентреадинг** находится ниже **ловерсрешолдфатал**, то текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="e5636-343">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="e5636-344">Это свойство наследуется от **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="e5636-344">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-345">**ловерсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="e5636-345">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-346">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-348">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="e5636-348">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="e5636-349">Если свойство **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, то датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="e5636-349">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="e5636-350">Если свойство **куррентреадинг** находится между **ловерсрешолднонкритикал** и **ловерсрешолдкритикал**, то текущее состояние не является критическим.</span><span class="sxs-lookup"><span data-stu-id="e5636-350">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="e5636-351">Это свойство наследуется от **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="e5636-351">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-352">**максреадабле**</span><span class="sxs-lookup"><span data-stu-id="e5636-352">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-353">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-355">Самое большое значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="e5636-355">Largest value of the measured property that can be read by the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-356">**минреадабле**</span><span class="sxs-lookup"><span data-stu-id="e5636-356">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-357">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-359">Наименьшее значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="e5636-359">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-360">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5636-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5636-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-363">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="e5636-363">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e5636-364">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="e5636-364">Label by which the object is known.</span></span> <span data-ttu-id="e5636-365">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="e5636-365">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e5636-366">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e5636-366">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-367">**номиналреадинг**</span><span class="sxs-lookup"><span data-stu-id="e5636-367">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-368">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-370">Для числового датчика требуется или "нормальное" значение.</span><span class="sxs-lookup"><span data-stu-id="e5636-370">Expected or "normal" value for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-371">**нормалмакс**</span><span class="sxs-lookup"><span data-stu-id="e5636-371">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-372">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-372">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-374">Нормальный максимальный диапазон для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="e5636-374">Normal maximum range for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-375">**нормалмин**</span><span class="sxs-lookup"><span data-stu-id="e5636-375">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-376">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-376">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-378">Нормальный минимальный диапазон для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="e5636-378">Normal minimum range for the numeric sensor.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-379">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="e5636-379">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-380">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5636-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-382">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e5636-382">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e5636-383">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e5636-383">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="e5636-384">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="e5636-385">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="e5636-385">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="e5636-386">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="e5636-386">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-387">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="e5636-387">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e5636-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-389">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="e5636-389">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="e5636-390">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-390">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e5636-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e5636-391"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="e5636-392"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="e5636-392"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e5636-393"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="e5636-393"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e5636-394"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="e5636-394"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-395">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="e5636-395">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="e5636-396"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="e5636-396"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-397">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="e5636-397">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="e5636-398"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="e5636-398"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-399">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="e5636-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="e5636-400">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="e5636-400">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="e5636-401">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="e5636-401">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="e5636-402"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="e5636-402"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-403">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="e5636-403">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="e5636-404"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="e5636-404"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e5636-405">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="e5636-405">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e5636-406">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="e5636-406">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-407">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="e5636-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-409">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="e5636-409">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="e5636-410">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="e5636-410">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="e5636-411">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e5636-411">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="e5636-412">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="e5636-412">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="e5636-413">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-414">**Решение**</span><span class="sxs-lookup"><span data-stu-id="e5636-414">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-415">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e5636-415">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-417">Способность датчика разрешать различия в измеряемом свойстве.</span><span class="sxs-lookup"><span data-stu-id="e5636-417">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="e5636-418">Это значение может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="e5636-418">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-419">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="e5636-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-420">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5636-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-422">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="e5636-422">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e5636-423">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="e5636-423">Current status of the object.</span></span>

<span data-ttu-id="e5636-424">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e5636-424">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e5636-425">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="e5636-425">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e5636-426">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="e5636-426">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e5636-427">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="e5636-427">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e5636-428">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="e5636-428">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e5636-429">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="e5636-429">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e5636-430">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="e5636-430">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e5636-431">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="e5636-431">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e5636-432">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="e5636-432">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e5636-433">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="e5636-433">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e5636-434">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="e5636-434">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e5636-435">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="e5636-435">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e5636-436">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="e5636-436">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e5636-437">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="e5636-437">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e5636-438">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e5636-438">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-439">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e5636-439">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-441">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="e5636-441">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="e5636-442">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="e5636-442">State of the logical device.</span></span> <span data-ttu-id="e5636-443">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="e5636-443">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="e5636-444">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="e5636-445">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="e5636-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e5636-446">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="e5636-446">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e5636-447">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="e5636-447">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e5636-448">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="e5636-448">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="e5636-449">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="e5636-449">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e5636-450">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="e5636-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-451">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5636-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-452">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-453">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e5636-453">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e5636-454">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="e5636-454">Scoping system's creation class name.</span></span>

<span data-ttu-id="e5636-455">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-455">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-456">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e5636-456">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-457">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e5636-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-458">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5636-459">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e5636-459">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e5636-460">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="e5636-460">Scoping system's name.</span></span>

<span data-ttu-id="e5636-461">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="e5636-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="e5636-462">**Отклонение**</span><span class="sxs-lookup"><span data-stu-id="e5636-462">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-463">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-463">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-464">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-465">Допуск датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="e5636-465">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="e5636-466">Это свойство, а также свойства **разрешения** и **точности** используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="e5636-466">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="e5636-467">Допуск может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="e5636-467">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-468">**упперсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="e5636-468">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-469">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-469">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-471">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="e5636-471">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="e5636-472">Если свойство **куррентреадинг** находится между **упперсрешолдкритикал** и **упперсрешолдфатал**, то текущее состояние является критическим.</span><span class="sxs-lookup"><span data-stu-id="e5636-472">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="e5636-473">Это свойство наследуется от **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="e5636-473">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-474">**упперсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="e5636-474">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-475">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-475">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-476">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-477">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="e5636-477">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="e5636-478">Если свойство **куррентреадинг** выше **упперсрешолдфатал**, то текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="e5636-478">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="e5636-479">Это свойство наследуется от **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="e5636-479">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> <dt>

<span data-ttu-id="e5636-480">**упперсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="e5636-480">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5636-481">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e5636-481">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e5636-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e5636-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e5636-483">Пороговое значение, указывающее диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="e5636-483">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="e5636-484">Если свойство **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, то датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="e5636-484">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="e5636-485">Если свойство **куррентреадинг** находится между **упперсрешолднонкритикал** и **упперсрешолдкритикал**, то текущее состояние не является критическим.</span><span class="sxs-lookup"><span data-stu-id="e5636-485">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="e5636-486">Это свойство наследуется от **CIM \_ NumericSensor**.</span><span class="sxs-lookup"><span data-stu-id="e5636-486">This property is inherited from **CIM\_NumericSensor**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5636-487">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5636-487">Remarks</span></span>

<span data-ttu-id="e5636-488">Класс **CIM \_ NumericSensor** является производным от [**\_ датчика CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="e5636-488">The **CIM\_NumericSensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="e5636-489">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="e5636-489">WMI does not implement this class.</span></span> <span data-ttu-id="e5636-490">Классы, производные от **CIM \_ NumericSensor**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e5636-490">For classes derived from **CIM\_NumericSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e5636-491">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="e5636-491">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e5636-492">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e5636-492">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5636-493">Требования</span><span class="sxs-lookup"><span data-stu-id="e5636-493">Requirements</span></span>



| <span data-ttu-id="e5636-494">Требование</span><span class="sxs-lookup"><span data-stu-id="e5636-494">Requirement</span></span> | <span data-ttu-id="e5636-495">Значение</span><span class="sxs-lookup"><span data-stu-id="e5636-495">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5636-496">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e5636-496">Minimum supported client</span></span><br/> | <span data-ttu-id="e5636-497">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e5636-497">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e5636-498">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e5636-498">Minimum supported server</span></span><br/> | <span data-ttu-id="e5636-499">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5636-499">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5636-500">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e5636-500">Namespace</span></span><br/>                | <span data-ttu-id="e5636-501">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e5636-501">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e5636-502">MOF</span><span class="sxs-lookup"><span data-stu-id="e5636-502">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5636-503"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5636-503"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5636-504">DLL</span><span class="sxs-lookup"><span data-stu-id="e5636-504">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5636-505"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5636-505"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5636-506">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5636-506">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5636-507">**\_Датчик CIM**</span><span class="sxs-lookup"><span data-stu-id="e5636-507">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

