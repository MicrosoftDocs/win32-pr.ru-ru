---
description: '&Win32 \_ температурепробе \# 32; Класс WMI представляет свойства датчика температуры (электронный термометр).'
ms.assetid: 63ba1ae2-6abc-4d86-a7f6-f02536ebd8ac
ms.tgt_platform: multiple
title: Класс Win32_TemperatureProbe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TemperatureProbe
- Win32_TemperatureProbe.Reset
- Win32_TemperatureProbe.SetPowerState
- Win32_TemperatureProbe.Accuracy
- Win32_TemperatureProbe.Availability
- Win32_TemperatureProbe.Caption
- Win32_TemperatureProbe.ConfigManagerErrorCode
- Win32_TemperatureProbe.ConfigManagerUserConfig
- Win32_TemperatureProbe.CreationClassName
- Win32_TemperatureProbe.CurrentReading
- Win32_TemperatureProbe.Description
- Win32_TemperatureProbe.DeviceID
- Win32_TemperatureProbe.ErrorCleared
- Win32_TemperatureProbe.ErrorDescription
- Win32_TemperatureProbe.InstallDate
- Win32_TemperatureProbe.IsLinear
- Win32_TemperatureProbe.LastErrorCode
- Win32_TemperatureProbe.LowerThresholdCritical
- Win32_TemperatureProbe.LowerThresholdFatal
- Win32_TemperatureProbe.LowerThresholdNonCritical
- Win32_TemperatureProbe.MaxReadable
- Win32_TemperatureProbe.MinReadable
- Win32_TemperatureProbe.Name
- Win32_TemperatureProbe.NominalReading
- Win32_TemperatureProbe.NormalMax
- Win32_TemperatureProbe.NormalMin
- Win32_TemperatureProbe.PNPDeviceID
- Win32_TemperatureProbe.PowerManagementCapabilities
- Win32_TemperatureProbe.PowerManagementSupported
- Win32_TemperatureProbe.Resolution
- Win32_TemperatureProbe.Status
- Win32_TemperatureProbe.StatusInfo
- Win32_TemperatureProbe.SystemCreationClassName
- Win32_TemperatureProbe.SystemName
- Win32_TemperatureProbe.Tolerance
- Win32_TemperatureProbe.UpperThresholdCritical
- Win32_TemperatureProbe.UpperThresholdFatal
- Win32_TemperatureProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6de4ed6334747e8313098075bc916a1975f520c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895922"
---
# <a name="win32_temperatureprobe-class"></a><span data-ttu-id="55cfa-103">\_Класс Win32 температурепробе</span><span class="sxs-lookup"><span data-stu-id="55cfa-103">Win32\_TemperatureProbe class</span></span>

<span data-ttu-id="55cfa-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ температурепробе для Win32** представляет свойства датчика температуры (электронный термометр).</span><span class="sxs-lookup"><span data-stu-id="55cfa-104">The **Win32\_TemperatureProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a temperature sensor (electronic thermometer).</span></span>

<span data-ttu-id="55cfa-105">Большая часть информации, предоставляемой классом WMI **\_ Температурепробе для Win32** , получена из SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="55cfa-105">Most of the information that the **Win32\_TemperatureProbe** WMI class provides comes from SMBIOS.</span></span> <span data-ttu-id="55cfa-106">Чтение в реальном времени для свойства **куррентреадинг** не может быть извлечено из таблиц SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="55cfa-106">Real-time readings for the **CurrentReading** property cannot be extracted from SMBIOS tables.</span></span> <span data-ttu-id="55cfa-107">По этой причине текущие реализации WMI не заполняют свойство **куррентреадинг** .</span><span class="sxs-lookup"><span data-stu-id="55cfa-107">For this reason, current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="55cfa-108">Присутствие свойства **куррентреадинг** зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="55cfa-108">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="55cfa-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="55cfa-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="55cfa-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="55cfa-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55cfa-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABB-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_TemperatureProbe : CIM_TemperatureSensor
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

## <a name="members"></a><span data-ttu-id="55cfa-112">Члены</span><span class="sxs-lookup"><span data-stu-id="55cfa-112">Members</span></span>

<span data-ttu-id="55cfa-113">Класс **Win32 \_ температурепробе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="55cfa-113">The **Win32\_TemperatureProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="55cfa-114">Методы</span><span class="sxs-lookup"><span data-stu-id="55cfa-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="55cfa-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="55cfa-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="55cfa-116">Методы</span><span class="sxs-lookup"><span data-stu-id="55cfa-116">Methods</span></span>

<span data-ttu-id="55cfa-117">Класс **Win32 \_ температурепробе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="55cfa-117">The **Win32\_TemperatureProbe** class has these methods.</span></span>



| <span data-ttu-id="55cfa-118">Метод</span><span class="sxs-lookup"><span data-stu-id="55cfa-118">Method</span></span>            | <span data-ttu-id="55cfa-119">Описание</span><span class="sxs-lookup"><span data-stu-id="55cfa-119">Description</span></span>                                                                                                                                                                                                                     |
|:------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55cfa-120">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="55cfa-120">**Reset**</span></span>         | <span data-ttu-id="55cfa-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="55cfa-121">Not implemented.</span></span> <span data-ttu-id="55cfa-122">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-temperaturesensor.md) в [**CIM \_ датчик температуры**](cim-temperaturesensor.md) .</span><span class="sxs-lookup"><span data-stu-id="55cfa-122">To implement this method, see the [**Reset**](reset-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="55cfa-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="55cfa-123">**SetPowerState**</span></span> | <span data-ttu-id="55cfa-124">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="55cfa-124">Not implemented.</span></span> <span data-ttu-id="55cfa-125">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) в [**CIM \_ датчик температуры**](cim-temperaturesensor.md) .</span><span class="sxs-lookup"><span data-stu-id="55cfa-125">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="55cfa-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="55cfa-126">Properties</span></span>

<span data-ttu-id="55cfa-127">Класс **Win32 \_ температурепробе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-127">The **Win32\_TemperatureProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55cfa-128">**Точность**</span><span class="sxs-lookup"><span data-stu-id="55cfa-128">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-131">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Пробная температура DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-132">Точность датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-132">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="55cfa-133">Его значение записывается как плюс или минус сотые доли процента.</span><span class="sxs-lookup"><span data-stu-id="55cfa-133">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="55cfa-134">Точность, разрешение и допуск используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-134">Accuracy, resolution, and tolerance are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="55cfa-135">Точность может быть различной и зависит от того, линейно ли устройство находится в динамическом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="55cfa-135">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="55cfa-136">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-136">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-137">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="55cfa-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-138">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cfa-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-140">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-141">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-141">Availability and status of the device.</span></span>

<span data-ttu-id="55cfa-142">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="55cfa-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="55cfa-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55cfa-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="55cfa-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="55cfa-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="55cfa-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="55cfa-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="55cfa-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="55cfa-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="55cfa-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="55cfa-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="55cfa-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="55cfa-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="55cfa-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="55cfa-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="55cfa-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-151">Автономная миграция</span><span class="sxs-lookup"><span data-stu-id="55cfa-151">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="55cfa-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="55cfa-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="55cfa-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="55cfa-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="55cfa-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="55cfa-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="55cfa-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="55cfa-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="55cfa-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="55cfa-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-157">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="55cfa-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="55cfa-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="55cfa-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-159">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="55cfa-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="55cfa-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="55cfa-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-161">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="55cfa-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="55cfa-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="55cfa-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="55cfa-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="55cfa-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-164">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="55cfa-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="55cfa-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="55cfa-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-166">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="55cfa-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="55cfa-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="55cfa-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-168">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="55cfa-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="55cfa-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="55cfa-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-170">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="55cfa-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="55cfa-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="55cfa-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-172">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="55cfa-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="55cfa-173">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="55cfa-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55cfa-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-176">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="55cfa-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-177">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="55cfa-177">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="55cfa-178">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-179">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="55cfa-179">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-180">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-182">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="55cfa-182">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-183">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="55cfa-183">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="55cfa-184">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-184">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="55cfa-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="55cfa-186"> (0)</span><span class="sxs-lookup"><span data-stu-id="55cfa-186">(0)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-187">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="55cfa-187">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="55cfa-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="55cfa-189">(1)</span><span class="sxs-lookup"><span data-stu-id="55cfa-189">(1)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-190">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="55cfa-190">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="55cfa-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="55cfa-192">(2)</span><span class="sxs-lookup"><span data-stu-id="55cfa-192">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="55cfa-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="55cfa-194">(3)</span><span class="sxs-lookup"><span data-stu-id="55cfa-194">(3)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-195">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55cfa-195">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="55cfa-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="55cfa-197">(4)</span><span class="sxs-lookup"><span data-stu-id="55cfa-197">(4)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-198">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="55cfa-198">Device is not working properly.</span></span> <span data-ttu-id="55cfa-199">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="55cfa-199">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="55cfa-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="55cfa-201">(5)</span><span class="sxs-lookup"><span data-stu-id="55cfa-201">(5)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-202">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="55cfa-202">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="55cfa-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="55cfa-204"> (6)</span><span class="sxs-lookup"><span data-stu-id="55cfa-204">(6)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-205">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="55cfa-205">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="55cfa-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="55cfa-207">(7)</span><span class="sxs-lookup"><span data-stu-id="55cfa-207">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="55cfa-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="55cfa-209">(8)</span><span class="sxs-lookup"><span data-stu-id="55cfa-209">(8)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-210">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-210">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="55cfa-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="55cfa-212">(9)</span><span class="sxs-lookup"><span data-stu-id="55cfa-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-213">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="55cfa-213">Device is not working properly.</span></span> <span data-ttu-id="55cfa-214">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-214">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="55cfa-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="55cfa-216">(10)</span><span class="sxs-lookup"><span data-stu-id="55cfa-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-217">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="55cfa-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="55cfa-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="55cfa-219">(11)</span><span class="sxs-lookup"><span data-stu-id="55cfa-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-220">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="55cfa-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="55cfa-222">(12)</span><span class="sxs-lookup"><span data-stu-id="55cfa-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-223">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="55cfa-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="55cfa-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="55cfa-225">(13)</span><span class="sxs-lookup"><span data-stu-id="55cfa-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-226">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="55cfa-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="55cfa-228">(14)</span><span class="sxs-lookup"><span data-stu-id="55cfa-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-229">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="55cfa-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="55cfa-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="55cfa-231">(15)</span><span class="sxs-lookup"><span data-stu-id="55cfa-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-232">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="55cfa-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="55cfa-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="55cfa-234">(16)</span><span class="sxs-lookup"><span data-stu-id="55cfa-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-235">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="55cfa-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="55cfa-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="55cfa-237">(17)</span><span class="sxs-lookup"><span data-stu-id="55cfa-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-238">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="55cfa-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="55cfa-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="55cfa-240">(18)</span><span class="sxs-lookup"><span data-stu-id="55cfa-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-241">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="55cfa-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="55cfa-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="55cfa-243">(19)</span><span class="sxs-lookup"><span data-stu-id="55cfa-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="55cfa-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="55cfa-245">(20)</span><span class="sxs-lookup"><span data-stu-id="55cfa-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-246">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="55cfa-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="55cfa-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="55cfa-248">(21)</span><span class="sxs-lookup"><span data-stu-id="55cfa-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-249">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="55cfa-249">System failure.</span></span> <span data-ttu-id="55cfa-250">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="55cfa-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="55cfa-251">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="55cfa-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="55cfa-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="55cfa-253">(22)</span><span class="sxs-lookup"><span data-stu-id="55cfa-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-254">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="55cfa-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="55cfa-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="55cfa-256">(23)</span><span class="sxs-lookup"><span data-stu-id="55cfa-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-257">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="55cfa-257">System failure.</span></span> <span data-ttu-id="55cfa-258">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="55cfa-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="55cfa-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="55cfa-260">(24)</span><span class="sxs-lookup"><span data-stu-id="55cfa-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-261">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="55cfa-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="55cfa-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="55cfa-263">(25)</span><span class="sxs-lookup"><span data-stu-id="55cfa-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-264">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="55cfa-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="55cfa-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="55cfa-266">(26)</span><span class="sxs-lookup"><span data-stu-id="55cfa-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-267">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="55cfa-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="55cfa-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="55cfa-269">(27)</span><span class="sxs-lookup"><span data-stu-id="55cfa-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-270">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="55cfa-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="55cfa-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="55cfa-272">(28)</span><span class="sxs-lookup"><span data-stu-id="55cfa-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-273">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="55cfa-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="55cfa-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="55cfa-275">(29)</span><span class="sxs-lookup"><span data-stu-id="55cfa-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-276">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="55cfa-276">Device is disabled.</span></span> <span data-ttu-id="55cfa-277">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="55cfa-277">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="55cfa-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="55cfa-279">(30)</span><span class="sxs-lookup"><span data-stu-id="55cfa-279">(30)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-280">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="55cfa-280">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="55cfa-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="55cfa-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="55cfa-282">1-31</span><span class="sxs-lookup"><span data-stu-id="55cfa-282">(31)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-283">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="55cfa-283">Device is not working properly.</span></span> <span data-ttu-id="55cfa-284">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="55cfa-284">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="55cfa-285">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="55cfa-285">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-286">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="55cfa-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-288">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="55cfa-288">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-289">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="55cfa-289">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="55cfa-290">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-291">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="55cfa-291">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55cfa-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-294">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="55cfa-294">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-295">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="55cfa-295">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="55cfa-296">При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="55cfa-296">When used with the other key properties of a class, this property allows all instances of the class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="55cfa-297">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-298">**куррентреадинг**</span><span class="sxs-lookup"><span data-stu-id="55cfa-298">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-299">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-299">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-301">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,5 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-302">Текущее значение, указываемое датчиком.</span><span class="sxs-lookup"><span data-stu-id="55cfa-302">Current value indicated by the sensor.</span></span>

<span data-ttu-id="55cfa-303">Текущие реализации WMI не заполняют свойство **куррентреадинг** .</span><span class="sxs-lookup"><span data-stu-id="55cfa-303">Current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="55cfa-304">Присутствие свойства **куррентреадинг** зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="55cfa-304">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="55cfa-305">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-306">**Описание**</span><span class="sxs-lookup"><span data-stu-id="55cfa-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55cfa-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-309">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="55cfa-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-310">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="55cfa-310">Description of the object.</span></span>

<span data-ttu-id="55cfa-311">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="55cfa-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55cfa-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-315">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="55cfa-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-316">Уникальный идентификатор текущей проверки.</span><span class="sxs-lookup"><span data-stu-id="55cfa-316">Unique identifier of the current probe.</span></span>

<span data-ttu-id="55cfa-317">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-318">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="55cfa-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-319">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="55cfa-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-321">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="55cfa-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="55cfa-322">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="55cfa-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55cfa-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-326">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые можно предпринять.</span><span class="sxs-lookup"><span data-stu-id="55cfa-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that you can take.</span></span>

<span data-ttu-id="55cfa-327">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="55cfa-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-329">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="55cfa-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-331">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-332">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="55cfa-332">Date and time the object is installed.</span></span> <span data-ttu-id="55cfa-333">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="55cfa-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="55cfa-334">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-335">**Линейно**</span><span class="sxs-lookup"><span data-stu-id="55cfa-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-336">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="55cfa-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-338">Если **значение равно true**, датчик линейно помещается в динамический диапазон.</span><span class="sxs-lookup"><span data-stu-id="55cfa-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="55cfa-339">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-340">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="55cfa-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-341">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-343">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="55cfa-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="55cfa-344">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-345">**ловерсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="55cfa-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-346">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-348">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,13 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-349">Пороговое значение датчика для указания диапазонов (минимальное и максимальное значения), определяющих операционные условия датчика, которые могут быть нормальными, некритическими, критически важными или неустранимыми.</span><span class="sxs-lookup"><span data-stu-id="55cfa-349">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="55cfa-350">Если **куррентреадинг** находится между **ловерсрешолдкритикал** и **ловерсрешолдфатал**, то текущее состояние является критически важным.</span><span class="sxs-lookup"><span data-stu-id="55cfa-350">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="55cfa-351">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-352">**ловерсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="55cfa-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-353">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-355">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,15 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-356">Пороговое значение датчика для указания диапазонов (минимальное и максимальное значения), определяющих операционные условия датчика, которые могут быть нормальными, некритическими, критически важными или неустранимыми.</span><span class="sxs-lookup"><span data-stu-id="55cfa-356">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="55cfa-357">Если **куррентреадинг** находится ниже **ловерсрешолдфатал**, текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="55cfa-357">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="55cfa-358">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-359">**ловерсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="55cfa-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-360">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-362">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,11 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-363">Пороговое значение датчика для указания диапазонов (минимальное и максимальное значения), определяющих операционные условия датчика, которые могут быть нормальными, некритическими, критически важными или неустранимыми.</span><span class="sxs-lookup"><span data-stu-id="55cfa-363">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="55cfa-364">Если **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="55cfa-364">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="55cfa-365">Если **куррентреадинг** находится между **ловерсрешолднонкритикал** и **ловерсрешолдкритикал**, текущее состояние является некритическим.</span><span class="sxs-lookup"><span data-stu-id="55cfa-365">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="55cfa-366">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-367">**максреадабле**</span><span class="sxs-lookup"><span data-stu-id="55cfa-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-368">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-370">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,9 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-371">Самое большое значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="55cfa-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="55cfa-372">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-373">**минреадабле**</span><span class="sxs-lookup"><span data-stu-id="55cfa-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-374">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-376">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,10 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-377">Наименьшее значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="55cfa-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="55cfa-378">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-379">**Name**</span><span class="sxs-lookup"><span data-stu-id="55cfa-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-380">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55cfa-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-382">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="55cfa-382">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-383">Метка для объекта.</span><span class="sxs-lookup"><span data-stu-id="55cfa-383">Label for the object.</span></span> <span data-ttu-id="55cfa-384">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="55cfa-384">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="55cfa-385">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-386">**номиналреадинг**</span><span class="sxs-lookup"><span data-stu-id="55cfa-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-387">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-389">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,6 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-390">Обычное или ожидаемое значение для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="55cfa-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="55cfa-391">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-392">**нормалмакс**</span><span class="sxs-lookup"><span data-stu-id="55cfa-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-393">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-395">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,7 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-396">Обычное или ожидаемое значение для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="55cfa-396">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="55cfa-397">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-398">**нормалмин**</span><span class="sxs-lookup"><span data-stu-id="55cfa-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-399">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-401">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,8 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-402">Рекомендации для пользователя в качестве обычного минимального диапазона для цифрового датчика.</span><span class="sxs-lookup"><span data-stu-id="55cfa-402">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="55cfa-403">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="55cfa-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-405">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55cfa-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-407">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="55cfa-407">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-408">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-408">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="55cfa-409">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="55cfa-409">Example: "\*PNP030b"</span></span>

<span data-ttu-id="55cfa-410">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-411">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="55cfa-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-412">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="55cfa-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-414">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="55cfa-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="55cfa-415">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55cfa-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="55cfa-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="55cfa-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="55cfa-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="55cfa-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="55cfa-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="55cfa-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="55cfa-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-420">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="55cfa-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="55cfa-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="55cfa-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-422">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="55cfa-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="55cfa-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="55cfa-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-424">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="55cfa-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="55cfa-425">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="55cfa-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="55cfa-426">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-426">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="55cfa-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="55cfa-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-428">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="55cfa-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="55cfa-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="55cfa-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="55cfa-430">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="55cfa-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="55cfa-431">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="55cfa-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-432">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="55cfa-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-433">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-434">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="55cfa-434">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="55cfa-435">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="55cfa-435">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="55cfa-436">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-437">**Решение**</span><span class="sxs-lookup"><span data-stu-id="55cfa-437">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-438">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-439">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-440">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,17 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" сотые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("hundredths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-441">Способность датчика разрешать различия в измеряемом свойстве.</span><span class="sxs-lookup"><span data-stu-id="55cfa-441">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="55cfa-442">Это значение может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="55cfa-442">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="55cfa-443">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-443">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-444">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="55cfa-444">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-445">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55cfa-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-447">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="55cfa-447">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-448">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="55cfa-448">Current status of the object.</span></span> <span data-ttu-id="55cfa-449">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="55cfa-449">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="55cfa-450">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="55cfa-450">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="55cfa-451">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="55cfa-451">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="55cfa-452">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="55cfa-452">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="55cfa-453">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="55cfa-453">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="55cfa-454">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-454">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="55cfa-455">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="55cfa-455">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="55cfa-456">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="55cfa-456">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="55cfa-457">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="55cfa-457">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="55cfa-458">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="55cfa-458">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55cfa-459">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="55cfa-459">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="55cfa-460">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="55cfa-460">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="55cfa-461">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="55cfa-461">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="55cfa-462">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="55cfa-462">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="55cfa-463">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="55cfa-463">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="55cfa-464">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="55cfa-464">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="55cfa-465">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="55cfa-465">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="55cfa-466">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="55cfa-466">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="55cfa-467">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="55cfa-467">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55cfa-468">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="55cfa-468">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-469">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55cfa-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-471">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-471">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-472">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-472">State of the logical device.</span></span> <span data-ttu-id="55cfa-473">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="55cfa-473">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="55cfa-474">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="55cfa-475">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="55cfa-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55cfa-476">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="55cfa-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="55cfa-477">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="55cfa-477">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="55cfa-478">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="55cfa-478">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="55cfa-479">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="55cfa-479">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55cfa-480">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="55cfa-480">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-481">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55cfa-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-483">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="55cfa-483">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-484">Значение для свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="55cfa-484">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="55cfa-485">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="55cfa-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-487">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="55cfa-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-488">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-489">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="55cfa-489">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-490">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="55cfa-490">Name of the scoping system.</span></span>

<span data-ttu-id="55cfa-491">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="55cfa-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-492">**Отклонение**</span><span class="sxs-lookup"><span data-stu-id="55cfa-492">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-493">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-493">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-494">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-495">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,18 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-495">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-496">Допуск датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-496">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="55cfa-497">Допуск, а также разрешение и точность используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="55cfa-497">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="55cfa-498">Допуск может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="55cfa-498">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="55cfa-499">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-500">**упперсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="55cfa-500">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-501">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-502">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-503">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,14 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-504">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения), которые определяют операционные условия датчика, которые могут быть нормальными, некритическими, критическими или неустранимыми.</span><span class="sxs-lookup"><span data-stu-id="55cfa-504">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="55cfa-505">Если **куррентреадинг** находится между **упперсрешолдкритикал** и **упперсрешолдфатал**, то текущее состояние является критически важным.</span><span class="sxs-lookup"><span data-stu-id="55cfa-505">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="55cfa-506">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-507">**упперсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="55cfa-507">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-508">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-509">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-510">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,16 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-511">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения), которые определяют операционные условия датчика, которые могут быть нормальными, некритическими, критическими или неустранимыми.</span><span class="sxs-lookup"><span data-stu-id="55cfa-511">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="55cfa-512">Если **куррентреадинг** выше **упперсрешолдфатал**, текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="55cfa-512">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="55cfa-513">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-513">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="55cfa-514">**упперсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="55cfa-514">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55cfa-515">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="55cfa-515">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-516">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55cfa-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55cfa-517">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Зонд температуры DMTF \| 001,12 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" десятые доли градусов centigrade ")</span><span class="sxs-lookup"><span data-stu-id="55cfa-517">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="55cfa-518">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения), которые определяют операционные условия датчика, которые могут быть нормальными, некритическими, критическими или неустранимыми.</span><span class="sxs-lookup"><span data-stu-id="55cfa-518">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="55cfa-519">Если **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="55cfa-519">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="55cfa-520">Если **куррентреадинг** находится между **упперсрешолднонкритикал** и **упперсрешолдкритикал**, текущее состояние является некритическим.</span><span class="sxs-lookup"><span data-stu-id="55cfa-520">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="55cfa-521">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-521">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55cfa-522">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55cfa-522">Remarks</span></span>

<span data-ttu-id="55cfa-523">Класс **Win32 \_ температурепробе** является производным от [**CIM \_ датчик температуры**](cim-temperaturesensor.md).</span><span class="sxs-lookup"><span data-stu-id="55cfa-523">The **Win32\_TemperatureProbe** class is derived from [**CIM\_TemperatureSensor**](cim-temperaturesensor.md).</span></span>

## <a name="examples"></a><span data-ttu-id="55cfa-524">Примеры</span><span class="sxs-lookup"><span data-stu-id="55cfa-524">Examples</span></span>

<span data-ttu-id="55cfa-525">В следующем примере возвращаются данные проверки температуры для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="55cfa-525">The following example returns temperature probe data for the local computer.</span></span>


```VB
strComputer = "."
Set colTempProbe = GetObject("Winmgmts:"_
    & "{impersonationLevel=impersonate}!\\"_ 
    & strComputer & "\root\cimv2")._
    InstancesOf("Win32_TemperatureProbe")
Num = 0
For Each obj In colTempProbe      
    WScript.Echo   obj.Name & VBNewLine _
        & obj.DeviceID & VBNewLine _
        & obj.Status & VBNewLine _
        & obj.Resolution & VBNewLine _
        & obj.Tolerance & VBNewLine _
        & obj.Accuracy 
    Num = Num +1
Next
If Num = 0 Then
    WScript.Echo "No temperature probe data"
End If
```



## <a name="requirements"></a><span data-ttu-id="55cfa-526">Требования</span><span class="sxs-lookup"><span data-stu-id="55cfa-526">Requirements</span></span>



| <span data-ttu-id="55cfa-527">Требование</span><span class="sxs-lookup"><span data-stu-id="55cfa-527">Requirement</span></span> | <span data-ttu-id="55cfa-528">Значение</span><span class="sxs-lookup"><span data-stu-id="55cfa-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55cfa-529">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55cfa-529">Minimum supported client</span></span><br/> | <span data-ttu-id="55cfa-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55cfa-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55cfa-531">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55cfa-531">Minimum supported server</span></span><br/> | <span data-ttu-id="55cfa-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55cfa-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55cfa-533">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="55cfa-533">Namespace</span></span><br/>                | <span data-ttu-id="55cfa-534">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="55cfa-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55cfa-535">MOF</span><span class="sxs-lookup"><span data-stu-id="55cfa-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55cfa-536"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55cfa-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55cfa-537">DLL</span><span class="sxs-lookup"><span data-stu-id="55cfa-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55cfa-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55cfa-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55cfa-539">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55cfa-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55cfa-540">**\_Датчик температуры CIM**</span><span class="sxs-lookup"><span data-stu-id="55cfa-540">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dt>

[<span data-ttu-id="55cfa-541">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="55cfa-541">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
