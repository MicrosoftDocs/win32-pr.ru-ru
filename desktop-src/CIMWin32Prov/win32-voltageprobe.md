---
description: '\_Класс WMI волтажепробе для Win32 представляет свойства датчика напряжения (Electronic волтметер).'
ms.assetid: ca27c1df-fb38-412d-b77c-d9ccf7941c66
ms.tgt_platform: multiple
title: Класс Win32_VoltageProbe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VoltageProbe
- Win32_VoltageProbe.Reset
- Win32_VoltageProbe.SetPowerState
- Win32_VoltageProbe.Accuracy
- Win32_VoltageProbe.Availability
- Win32_VoltageProbe.Caption
- Win32_VoltageProbe.ConfigManagerErrorCode
- Win32_VoltageProbe.ConfigManagerUserConfig
- Win32_VoltageProbe.CreationClassName
- Win32_VoltageProbe.CurrentReading
- Win32_VoltageProbe.Description
- Win32_VoltageProbe.DeviceID
- Win32_VoltageProbe.ErrorCleared
- Win32_VoltageProbe.ErrorDescription
- Win32_VoltageProbe.InstallDate
- Win32_VoltageProbe.IsLinear
- Win32_VoltageProbe.LastErrorCode
- Win32_VoltageProbe.LowerThresholdCritical
- Win32_VoltageProbe.LowerThresholdFatal
- Win32_VoltageProbe.LowerThresholdNonCritical
- Win32_VoltageProbe.MaxReadable
- Win32_VoltageProbe.MinReadable
- Win32_VoltageProbe.Name
- Win32_VoltageProbe.NominalReading
- Win32_VoltageProbe.NormalMax
- Win32_VoltageProbe.NormalMin
- Win32_VoltageProbe.PNPDeviceID
- Win32_VoltageProbe.PowerManagementCapabilities
- Win32_VoltageProbe.PowerManagementSupported
- Win32_VoltageProbe.Resolution
- Win32_VoltageProbe.Status
- Win32_VoltageProbe.StatusInfo
- Win32_VoltageProbe.SystemCreationClassName
- Win32_VoltageProbe.SystemName
- Win32_VoltageProbe.Tolerance
- Win32_VoltageProbe.UpperThresholdCritical
- Win32_VoltageProbe.UpperThresholdFatal
- Win32_VoltageProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: acb5fe56706ed55098443ad9667eb980a1fe6d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262526"
---
# <a name="win32_voltageprobe-class"></a><span data-ttu-id="27e5d-103">\_Класс Win32 волтажепробе</span><span class="sxs-lookup"><span data-stu-id="27e5d-103">Win32\_VoltageProbe class</span></span>

<span data-ttu-id="27e5d-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ волтажепробе для Win32** представляет свойства датчика напряжения (Electronic волтметер).</span><span class="sxs-lookup"><span data-stu-id="27e5d-104">The **Win32\_VoltageProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a voltage sensor (electronic voltmeter).</span></span>

<span data-ttu-id="27e5d-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="27e5d-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="27e5d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="27e5d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27e5d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB8-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_VoltageProbe : CIM_VoltageSensor
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

## <a name="members"></a><span data-ttu-id="27e5d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="27e5d-108">Members</span></span>

<span data-ttu-id="27e5d-109">Класс **Win32 \_ волтажепробе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="27e5d-109">The **Win32\_VoltageProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="27e5d-110">Методы</span><span class="sxs-lookup"><span data-stu-id="27e5d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="27e5d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="27e5d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="27e5d-112">Методы</span><span class="sxs-lookup"><span data-stu-id="27e5d-112">Methods</span></span>

<span data-ttu-id="27e5d-113">Класс **Win32 \_ волтажепробе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="27e5d-113">The **Win32\_VoltageProbe** class has these methods.</span></span>



| <span data-ttu-id="27e5d-114">Метод</span><span class="sxs-lookup"><span data-stu-id="27e5d-114">Method</span></span>            | <span data-ttu-id="27e5d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="27e5d-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27e5d-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="27e5d-116">**Reset**</span></span>         | <span data-ttu-id="27e5d-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="27e5d-117">Not implemented.</span></span> <span data-ttu-id="27e5d-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ датчик напряжения**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/>                 |
| <span data-ttu-id="27e5d-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="27e5d-119">**SetPowerState**</span></span> | <span data-ttu-id="27e5d-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="27e5d-120">Not implemented.</span></span> <span data-ttu-id="27e5d-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ датчик напряжения**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="27e5d-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="27e5d-122">Properties</span></span>

<span data-ttu-id="27e5d-123">Класс **Win32 \_ волтажепробе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-123">The **Win32\_VoltageProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27e5d-124">**Точность**</span><span class="sxs-lookup"><span data-stu-id="27e5d-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-125">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-127">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-128">Точность датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="27e5d-129">Значение точности записывается как плюс или минус сотые доли процента.</span><span class="sxs-lookup"><span data-stu-id="27e5d-129">The accuracy value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="27e5d-130">Точность, а также разрешение и допуск используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="27e5d-131">Точность может быть различной и зависит от того, является ли устройство линейным в динамическом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="27e5d-131">The accuracy may vary and depends on whether or not the device is linear in its dynamic range.</span></span>

<span data-ttu-id="27e5d-132">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-133">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="27e5d-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-134">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27e5d-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-136">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-137">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-137">Availability and status of the device.</span></span>

<span data-ttu-id="27e5d-138">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="27e5d-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="27e5d-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27e5d-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="27e5d-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="27e5d-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="27e5d-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="27e5d-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="27e5d-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="27e5d-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="27e5d-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="27e5d-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="27e5d-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="27e5d-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="27e5d-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="27e5d-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="27e5d-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="27e5d-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="27e5d-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="27e5d-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="27e5d-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="27e5d-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="27e5d-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="27e5d-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="27e5d-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="27e5d-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="27e5d-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-152">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="27e5d-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="27e5d-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="27e5d-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-154">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="27e5d-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="27e5d-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="27e5d-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-156">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="27e5d-156">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="27e5d-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="27e5d-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="27e5d-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="27e5d-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-159">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="27e5d-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="27e5d-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="27e5d-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-161">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="27e5d-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="27e5d-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="27e5d-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-163">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="27e5d-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="27e5d-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="27e5d-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-165">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="27e5d-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="27e5d-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="27e5d-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-167">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="27e5d-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="27e5d-168">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="27e5d-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e5d-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-171">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="27e5d-171">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-172">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="27e5d-172">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="27e5d-173">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-174">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="27e5d-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-175">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-177">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="27e5d-177">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-178">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="27e5d-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="27e5d-179">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="27e5d-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="27e5d-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="27e5d-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-182">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="27e5d-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="27e5d-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="27e5d-184">(1)</span><span class="sxs-lookup"><span data-stu-id="27e5d-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-185">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="27e5d-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="27e5d-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="27e5d-187">(2)</span><span class="sxs-lookup"><span data-stu-id="27e5d-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="27e5d-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="27e5d-189">(3)</span><span class="sxs-lookup"><span data-stu-id="27e5d-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-190">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27e5d-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="27e5d-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="27e5d-192">(4)</span><span class="sxs-lookup"><span data-stu-id="27e5d-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-193">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="27e5d-193">Device is not working properly.</span></span> <span data-ttu-id="27e5d-194">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="27e5d-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="27e5d-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="27e5d-196">(5)</span><span class="sxs-lookup"><span data-stu-id="27e5d-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-197">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="27e5d-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="27e5d-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="27e5d-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="27e5d-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-200">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="27e5d-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="27e5d-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="27e5d-202">(7)</span><span class="sxs-lookup"><span data-stu-id="27e5d-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="27e5d-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="27e5d-204">(8)</span><span class="sxs-lookup"><span data-stu-id="27e5d-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-205">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="27e5d-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="27e5d-207">(9)</span><span class="sxs-lookup"><span data-stu-id="27e5d-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-208">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="27e5d-208">Device is not working properly.</span></span> <span data-ttu-id="27e5d-209">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="27e5d-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="27e5d-211">(10)</span><span class="sxs-lookup"><span data-stu-id="27e5d-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-212">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="27e5d-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="27e5d-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="27e5d-214">(11)</span><span class="sxs-lookup"><span data-stu-id="27e5d-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-215">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="27e5d-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="27e5d-217">(12)</span><span class="sxs-lookup"><span data-stu-id="27e5d-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-218">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="27e5d-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="27e5d-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="27e5d-220">(13)</span><span class="sxs-lookup"><span data-stu-id="27e5d-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-221">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="27e5d-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="27e5d-223">(14)</span><span class="sxs-lookup"><span data-stu-id="27e5d-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-224">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="27e5d-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="27e5d-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="27e5d-226">(15)</span><span class="sxs-lookup"><span data-stu-id="27e5d-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-227">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="27e5d-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="27e5d-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="27e5d-229">(16)</span><span class="sxs-lookup"><span data-stu-id="27e5d-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-230">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="27e5d-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="27e5d-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="27e5d-232">(17)</span><span class="sxs-lookup"><span data-stu-id="27e5d-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-233">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="27e5d-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="27e5d-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="27e5d-235">(18)</span><span class="sxs-lookup"><span data-stu-id="27e5d-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-236">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="27e5d-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="27e5d-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="27e5d-238">(19)</span><span class="sxs-lookup"><span data-stu-id="27e5d-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="27e5d-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="27e5d-240">(20)</span><span class="sxs-lookup"><span data-stu-id="27e5d-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-241">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="27e5d-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="27e5d-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="27e5d-243">(21)</span><span class="sxs-lookup"><span data-stu-id="27e5d-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-244">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="27e5d-244">System failure.</span></span> <span data-ttu-id="27e5d-245">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="27e5d-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="27e5d-246">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="27e5d-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="27e5d-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="27e5d-248">(22)</span><span class="sxs-lookup"><span data-stu-id="27e5d-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-249">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="27e5d-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="27e5d-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="27e5d-251">(23)</span><span class="sxs-lookup"><span data-stu-id="27e5d-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-252">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="27e5d-252">System failure.</span></span> <span data-ttu-id="27e5d-253">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="27e5d-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="27e5d-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="27e5d-255">(24)</span><span class="sxs-lookup"><span data-stu-id="27e5d-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-256">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="27e5d-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="27e5d-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="27e5d-258">(25)</span><span class="sxs-lookup"><span data-stu-id="27e5d-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-259">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="27e5d-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="27e5d-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="27e5d-261">(26)</span><span class="sxs-lookup"><span data-stu-id="27e5d-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-262">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="27e5d-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="27e5d-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="27e5d-264">(27)</span><span class="sxs-lookup"><span data-stu-id="27e5d-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-265">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="27e5d-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="27e5d-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="27e5d-267">(28)</span><span class="sxs-lookup"><span data-stu-id="27e5d-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-268">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="27e5d-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="27e5d-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="27e5d-270">(29)</span><span class="sxs-lookup"><span data-stu-id="27e5d-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-271">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="27e5d-271">Device is disabled.</span></span> <span data-ttu-id="27e5d-272">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="27e5d-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="27e5d-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="27e5d-274">(30)</span><span class="sxs-lookup"><span data-stu-id="27e5d-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-275">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="27e5d-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="27e5d-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="27e5d-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="27e5d-277">1-31</span><span class="sxs-lookup"><span data-stu-id="27e5d-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-278">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="27e5d-278">Device is not working properly.</span></span> <span data-ttu-id="27e5d-279">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="27e5d-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="27e5d-280">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="27e5d-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-281">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="27e5d-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-283">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="27e5d-283">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-284">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="27e5d-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="27e5d-285">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="27e5d-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-287">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e5d-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-289">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="27e5d-289">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-290">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="27e5d-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="27e5d-291">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="27e5d-291">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="27e5d-292">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-293">**куррентреадинг**</span><span class="sxs-lookup"><span data-stu-id="27e5d-293">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-294">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-294">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-296">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,5 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-297">Текущее значение, указываемое датчиком.</span><span class="sxs-lookup"><span data-stu-id="27e5d-297">Current value indicated by the sensor.</span></span>

<span data-ttu-id="27e5d-298">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-298">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-299">**Описание**</span><span class="sxs-lookup"><span data-stu-id="27e5d-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e5d-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-302">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="27e5d-302">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-303">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="27e5d-303">Description of the object.</span></span>

<span data-ttu-id="27e5d-304">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="27e5d-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-306">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e5d-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-308">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="27e5d-308">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-309">Уникальный идентификатор проверки напряжения.</span><span class="sxs-lookup"><span data-stu-id="27e5d-309">Unique identifier of the voltage probe.</span></span>

<span data-ttu-id="27e5d-310">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-311">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="27e5d-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-312">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="27e5d-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-314">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="27e5d-314">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="27e5d-315">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="27e5d-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e5d-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-319">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="27e5d-319">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="27e5d-320">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="27e5d-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-322">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="27e5d-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-324">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-324">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-325">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="27e5d-325">Date and time the object is installed.</span></span> <span data-ttu-id="27e5d-326">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="27e5d-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="27e5d-327">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-328">**Линейно**</span><span class="sxs-lookup"><span data-stu-id="27e5d-328">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-329">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="27e5d-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-331">Если **значение равно true**, датчик линейно помещается в динамический диапазон.</span><span class="sxs-lookup"><span data-stu-id="27e5d-331">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="27e5d-332">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-332">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-333">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="27e5d-333">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-334">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-334">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-336">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="27e5d-336">Last error code reported by the logical device.</span></span>

<span data-ttu-id="27e5d-337">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-338">**ловерсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="27e5d-338">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-339">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-341">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,13 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-342">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения), чтобы определить, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="27e5d-342">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="27e5d-343">Если **куррентреадинг** находится между **ловерсрешолдкритикал** и **ловерсрешолдфатал**, то текущее состояние является критически важным.</span><span class="sxs-lookup"><span data-stu-id="27e5d-343">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="27e5d-344">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-344">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-345">**ловерсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="27e5d-345">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-346">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-348">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,15 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-349">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения), чтобы определить, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="27e5d-349">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="27e5d-350">Если **куррентреадинг** находится ниже **ловерсрешолдфатал**, текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="27e5d-350">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="27e5d-351">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-352">**ловерсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="27e5d-352">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-353">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-355">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,11 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-356">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения), чтобы определить, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="27e5d-356">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="27e5d-357">Если **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="27e5d-357">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="27e5d-358">Если **куррентреадинг** находится между **ловерсрешолднонкритикал** и **ловерсрешолдкритикал**, текущее состояние является некритическим.</span><span class="sxs-lookup"><span data-stu-id="27e5d-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="27e5d-359">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-359">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-360">**максреадабле**</span><span class="sxs-lookup"><span data-stu-id="27e5d-360">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-361">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-361">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-363">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,9 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-364">Самое большое значение измеряемого свойства, которое может читать цифровой датчик.</span><span class="sxs-lookup"><span data-stu-id="27e5d-364">Largest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="27e5d-365">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-366">**минреадабле**</span><span class="sxs-lookup"><span data-stu-id="27e5d-366">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-367">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-369">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,10 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-370">Наименьшее значение измеряемого свойства, которое может читать цифровой датчик.</span><span class="sxs-lookup"><span data-stu-id="27e5d-370">Smallest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="27e5d-371">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-372">**Name**</span><span class="sxs-lookup"><span data-stu-id="27e5d-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-373">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e5d-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-375">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="27e5d-375">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-376">Метка для объекта.</span><span class="sxs-lookup"><span data-stu-id="27e5d-376">Label for an object.</span></span> <span data-ttu-id="27e5d-377">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="27e5d-377">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="27e5d-378">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-379">**номиналреадинг**</span><span class="sxs-lookup"><span data-stu-id="27e5d-379">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-380">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-380">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-382">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,6 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-383">Обычное или ожидаемое значение для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="27e5d-383">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="27e5d-384">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-384">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-385">**нормалмакс**</span><span class="sxs-lookup"><span data-stu-id="27e5d-385">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-386">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-388">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,7 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-389">Обычное или ожидаемое значение для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="27e5d-389">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="27e5d-390">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-391">**нормалмин**</span><span class="sxs-lookup"><span data-stu-id="27e5d-391">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-392">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-394">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,8 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-395">Руководство для пользователя, чтобы указать нормальный минимальный диапазон для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="27e5d-395">Guidance for the user to indicate the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="27e5d-396">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-397">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="27e5d-397">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-398">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e5d-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-400">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="27e5d-400">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-401">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-401">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="27e5d-402">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="27e5d-403">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="27e5d-403">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-404">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="27e5d-404">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-405">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="27e5d-405">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-407">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="27e5d-407">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="27e5d-408">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-408">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27e5d-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="27e5d-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="27e5d-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="27e5d-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="27e5d-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="27e5d-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="27e5d-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="27e5d-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-413">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="27e5d-413">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="27e5d-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="27e5d-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-415">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="27e5d-415">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="27e5d-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="27e5d-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-417">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="27e5d-417">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="27e5d-418">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="27e5d-418">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="27e5d-419">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-419">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="27e5d-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="27e5d-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-421">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="27e5d-421">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="27e5d-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="27e5d-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="27e5d-423">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="27e5d-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="27e5d-424">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="27e5d-424">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-425">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="27e5d-425">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-426">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-427">Если **значение — true**, устройство может управляться с помощью управления питанием. Это означает, что его можно перевести в режим приостановки и т. д.</span><span class="sxs-lookup"><span data-stu-id="27e5d-427">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="27e5d-428">Свойство не указывает на то, что функции управления питанием в настоящее время включены, но это означает, что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="27e5d-428">The property does not indicate that power management features are currently enabled, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="27e5d-429">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-429">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-430">**Решение**</span><span class="sxs-lookup"><span data-stu-id="27e5d-430">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-431">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-433">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,17 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-433">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-434">Способность датчика разрешать различия в измеряемом свойстве.</span><span class="sxs-lookup"><span data-stu-id="27e5d-434">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="27e5d-435">Это значение может различаться и зависит от того, является ли устройство линейным в динамическом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="27e5d-435">This value may vary and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="27e5d-436">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-436">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-437">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="27e5d-437">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-438">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e5d-438">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-439">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-440">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="27e5d-440">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-441">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="27e5d-441">Current status of the object.</span></span> <span data-ttu-id="27e5d-442">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="27e5d-442">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="27e5d-443">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="27e5d-443">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="27e5d-444">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="27e5d-444">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="27e5d-445">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="27e5d-445">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="27e5d-446">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="27e5d-446">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="27e5d-447">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="27e5d-448">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="27e5d-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="27e5d-449">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="27e5d-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="27e5d-450">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="27e5d-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="27e5d-451">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="27e5d-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27e5d-452">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="27e5d-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="27e5d-453">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="27e5d-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="27e5d-454">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="27e5d-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="27e5d-455">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="27e5d-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="27e5d-456">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="27e5d-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="27e5d-457">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="27e5d-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="27e5d-458">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="27e5d-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="27e5d-459">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="27e5d-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="27e5d-460">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="27e5d-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27e5d-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="27e5d-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-462">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="27e5d-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-463">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-464">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-464">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-465">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-465">State of the logical device.</span></span> <span data-ttu-id="27e5d-466">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="27e5d-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="27e5d-467">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="27e5d-468">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="27e5d-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="27e5d-469">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="27e5d-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="27e5d-470">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="27e5d-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="27e5d-471">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="27e5d-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="27e5d-472">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="27e5d-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="27e5d-473">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="27e5d-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-474">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e5d-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-476">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="27e5d-476">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-477">Значение свойства **CreationClassName** компьютера с областями.</span><span class="sxs-lookup"><span data-stu-id="27e5d-477">Value for the **CreationClassName** property of the scoping computer.</span></span>

<span data-ttu-id="27e5d-478">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-479">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="27e5d-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-480">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="27e5d-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-482">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="27e5d-482">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-483">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="27e5d-483">Name of the scoping system.</span></span>

<span data-ttu-id="27e5d-484">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="27e5d-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-485">**Отклонение**</span><span class="sxs-lookup"><span data-stu-id="27e5d-485">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-486">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-486">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-488">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,18 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-489">Допуск датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-489">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="27e5d-490">Допуск, а также разрешение и точность используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="27e5d-490">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="27e5d-491">Допуск может различаться и зависит от того, является ли устройство линейным в динамическом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="27e5d-491">Tolerance may vary, and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="27e5d-492">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-492">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-493">**упперсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="27e5d-493">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-494">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-494">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-495">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-496">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,14 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-497">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения), чтобы определить, работает ли датчик в нормальных, некритических, критических или неустранимых условиях.</span><span class="sxs-lookup"><span data-stu-id="27e5d-497">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="27e5d-498">Если **куррентреадинг** находится между **упперсрешолдкритикал** и **упперсрешолдфатал**, то текущее состояние является критически важным.</span><span class="sxs-lookup"><span data-stu-id="27e5d-498">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="27e5d-499">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-500">**упперсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="27e5d-500">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-501">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-502">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-503">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,16 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-504">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения), чтобы определить, работает ли датчик в нормальных, некритических, критических или неустранимых условиях.</span><span class="sxs-lookup"><span data-stu-id="27e5d-504">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="27e5d-505">Если **куррентреадинг** выше **упперсрешолдфатал**, текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="27e5d-505">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="27e5d-506">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="27e5d-507">**упперсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="27e5d-507">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27e5d-508">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="27e5d-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-509">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="27e5d-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27e5d-510">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд напряжения DMTF \| 001,12 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="27e5d-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="27e5d-511">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения), чтобы определить, работает ли датчик в нормальных, некритических, критических или неустранимых условиях.</span><span class="sxs-lookup"><span data-stu-id="27e5d-511">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="27e5d-512">Если **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="27e5d-512">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="27e5d-513">Если **куррентреадинг** находится между **упперсрешолднонкритикал** и **упперсрешолдкритикал**, текущее состояние является некритическим.</span><span class="sxs-lookup"><span data-stu-id="27e5d-513">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="27e5d-514">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-514">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27e5d-515">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27e5d-515">Remarks</span></span>

<span data-ttu-id="27e5d-516">Класс **Win32 \_ волтажепробе** является производным от [**CIM \_ датчик напряжения**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="27e5d-516">The **Win32\_VoltageProbe** class is derived from [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="27e5d-517">Требования</span><span class="sxs-lookup"><span data-stu-id="27e5d-517">Requirements</span></span>



| <span data-ttu-id="27e5d-518">Требование</span><span class="sxs-lookup"><span data-stu-id="27e5d-518">Requirement</span></span> | <span data-ttu-id="27e5d-519">Значение</span><span class="sxs-lookup"><span data-stu-id="27e5d-519">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27e5d-520">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27e5d-520">Minimum supported client</span></span><br/> | <span data-ttu-id="27e5d-521">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27e5d-521">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27e5d-522">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27e5d-522">Minimum supported server</span></span><br/> | <span data-ttu-id="27e5d-523">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27e5d-523">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27e5d-524">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="27e5d-524">Namespace</span></span><br/>                | <span data-ttu-id="27e5d-525">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="27e5d-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="27e5d-526">MOF</span><span class="sxs-lookup"><span data-stu-id="27e5d-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27e5d-527"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27e5d-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="27e5d-528">DLL</span><span class="sxs-lookup"><span data-stu-id="27e5d-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27e5d-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27e5d-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27e5d-530">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27e5d-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27e5d-531">**\_Датчик напряжения CIM**</span><span class="sxs-lookup"><span data-stu-id="27e5d-531">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dt>

[<span data-ttu-id="27e5d-532">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="27e5d-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
