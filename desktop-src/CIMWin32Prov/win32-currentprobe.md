---
description: '\_Класс WMI куррентпробе для Win32 представляет свойства текущего датчика мониторинга (амметер).'
ms.assetid: 2e1da856-b787-404b-ac4b-080c4950bad8
ms.tgt_platform: multiple
title: Класс Win32_CurrentProbe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CurrentProbe
- Win32_CurrentProbe.Reset
- Win32_CurrentProbe.SetPowerState
- Win32_CurrentProbe.Accuracy
- Win32_CurrentProbe.Availability
- Win32_CurrentProbe.Caption
- Win32_CurrentProbe.ConfigManagerErrorCode
- Win32_CurrentProbe.ConfigManagerUserConfig
- Win32_CurrentProbe.CreationClassName
- Win32_CurrentProbe.CurrentReading
- Win32_CurrentProbe.Description
- Win32_CurrentProbe.DeviceID
- Win32_CurrentProbe.ErrorCleared
- Win32_CurrentProbe.ErrorDescription
- Win32_CurrentProbe.InstallDate
- Win32_CurrentProbe.IsLinear
- Win32_CurrentProbe.LastErrorCode
- Win32_CurrentProbe.LowerThresholdCritical
- Win32_CurrentProbe.LowerThresholdFatal
- Win32_CurrentProbe.LowerThresholdNonCritical
- Win32_CurrentProbe.MaxReadable
- Win32_CurrentProbe.MinReadable
- Win32_CurrentProbe.Name
- Win32_CurrentProbe.NominalReading
- Win32_CurrentProbe.NormalMax
- Win32_CurrentProbe.NormalMin
- Win32_CurrentProbe.PNPDeviceID
- Win32_CurrentProbe.PowerManagementCapabilities
- Win32_CurrentProbe.PowerManagementSupported
- Win32_CurrentProbe.Resolution
- Win32_CurrentProbe.Status
- Win32_CurrentProbe.StatusInfo
- Win32_CurrentProbe.SystemCreationClassName
- Win32_CurrentProbe.SystemName
- Win32_CurrentProbe.Tolerance
- Win32_CurrentProbe.UpperThresholdCritical
- Win32_CurrentProbe.UpperThresholdFatal
- Win32_CurrentProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: be834e56eb3d958a8cd6ee653dc9a248c14ae3bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896489"
---
# <a name="win32_currentprobe-class"></a><span data-ttu-id="1577b-103">\_Класс Win32 куррентпробе</span><span class="sxs-lookup"><span data-stu-id="1577b-103">Win32\_CurrentProbe class</span></span>

<span data-ttu-id="1577b-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ куррентпробе для Win32** представляет свойства текущего датчика мониторинга (амметер).</span><span class="sxs-lookup"><span data-stu-id="1577b-104">The **Win32\_CurrentProbe** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a current monitoring sensor (ammeter).</span></span>

<span data-ttu-id="1577b-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1577b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1577b-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1577b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1577b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1577b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABA-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_CurrentProbe : CIM_CurrentSensor
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

## <a name="members"></a><span data-ttu-id="1577b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="1577b-108">Members</span></span>

<span data-ttu-id="1577b-109">Класс **Win32 \_ куррентпробе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1577b-109">The **Win32\_CurrentProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="1577b-110">Методы</span><span class="sxs-lookup"><span data-stu-id="1577b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1577b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="1577b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1577b-112">Методы</span><span class="sxs-lookup"><span data-stu-id="1577b-112">Methods</span></span>

<span data-ttu-id="1577b-113">Класс **Win32 \_ куррентпробе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1577b-113">The **Win32\_CurrentProbe** class has these methods.</span></span>



| <span data-ttu-id="1577b-114">Метод</span><span class="sxs-lookup"><span data-stu-id="1577b-114">Method</span></span>            | <span data-ttu-id="1577b-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1577b-115">Description</span></span>                                                                                                                                                                                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1577b-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="1577b-116">**Reset**</span></span>         | <span data-ttu-id="1577b-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="1577b-117">Not implemented.</span></span> <span data-ttu-id="1577b-118">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ куррентсенсор**](cim-currentsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="1577b-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="1577b-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1577b-119">**SetPowerState**</span></span> | <span data-ttu-id="1577b-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="1577b-120">Not implemented.</span></span> <span data-ttu-id="1577b-121">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ куррентсенсор**](cim-currentsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="1577b-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1577b-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="1577b-122">Properties</span></span>

<span data-ttu-id="1577b-123">Класс **Win32 \_ куррентпробе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1577b-123">The **Win32\_CurrentProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1577b-124">**Точность**</span><span class="sxs-lookup"><span data-stu-id="1577b-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-125">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-127">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая пробная зонда 001,19 (DMTF \| )</span><span class="sxs-lookup"><span data-stu-id="1577b-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-128">Точность датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="1577b-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="1577b-129">Значение записывается в виде плюса или минуса в сотых долях процента.</span><span class="sxs-lookup"><span data-stu-id="1577b-129">The value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="1577b-130">Точность, а также разрешение и допуск используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="1577b-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="1577b-131">Точность может быть различной и зависит от того, линейно ли устройство находится в динамическом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="1577b-131">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="1577b-132">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-133">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="1577b-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-134">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1577b-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-136">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="1577b-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-137">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="1577b-137">Availability and status of the device.</span></span>

<span data-ttu-id="1577b-138">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1577b-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1577b-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1577b-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="1577b-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1577b-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="1577b-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-142">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="1577b-142">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1577b-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="1577b-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1577b-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="1577b-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1577b-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="1577b-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1577b-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="1577b-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1577b-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="1577b-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1577b-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="1577b-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1577b-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="1577b-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1577b-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="1577b-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1577b-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="1577b-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1577b-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="1577b-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-153">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="1577b-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1577b-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="1577b-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-155">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="1577b-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1577b-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="1577b-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-157">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="1577b-157">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1577b-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="1577b-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1577b-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="1577b-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-160">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="1577b-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1577b-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="1577b-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-162">приостановлено</span><span class="sxs-lookup"><span data-stu-id="1577b-162">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1577b-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="1577b-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-164">Не готово.</span><span class="sxs-lookup"><span data-stu-id="1577b-164">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1577b-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="1577b-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-166">не настроено.</span><span class="sxs-lookup"><span data-stu-id="1577b-166">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1577b-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="1577b-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-168">Текущий датчик недоступен.</span><span class="sxs-lookup"><span data-stu-id="1577b-168">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1577b-169">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1577b-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1577b-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-172">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1577b-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-173">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="1577b-173">Short description of the object a one-line string.</span></span>

<span data-ttu-id="1577b-174">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-175">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="1577b-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-176">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1577b-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-178">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1577b-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-179">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="1577b-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="1577b-180">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1577b-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="1577b-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="1577b-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="1577b-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-183">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="1577b-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1577b-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="1577b-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="1577b-185">(1)</span><span class="sxs-lookup"><span data-stu-id="1577b-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-186">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="1577b-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1577b-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1577b-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1577b-188">(2)</span><span class="sxs-lookup"><span data-stu-id="1577b-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1577b-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="1577b-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1577b-190">(3)</span><span class="sxs-lookup"><span data-stu-id="1577b-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-191">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1577b-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1577b-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="1577b-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1577b-193">(4)</span><span class="sxs-lookup"><span data-stu-id="1577b-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-194">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="1577b-194">Device is not working properly.</span></span> <span data-ttu-id="1577b-195">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="1577b-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1577b-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="1577b-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1577b-197">(5)</span><span class="sxs-lookup"><span data-stu-id="1577b-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-198">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="1577b-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1577b-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="1577b-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1577b-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="1577b-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-201">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="1577b-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1577b-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="1577b-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="1577b-203">(7)</span><span class="sxs-lookup"><span data-stu-id="1577b-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1577b-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="1577b-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1577b-205">(8)</span><span class="sxs-lookup"><span data-stu-id="1577b-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-206">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="1577b-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1577b-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="1577b-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1577b-208">(9)</span><span class="sxs-lookup"><span data-stu-id="1577b-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-209">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="1577b-209">Device is not working properly.</span></span> <span data-ttu-id="1577b-210">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="1577b-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1577b-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="1577b-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="1577b-212">(10)</span><span class="sxs-lookup"><span data-stu-id="1577b-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-213">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="1577b-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1577b-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="1577b-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="1577b-215">(11)</span><span class="sxs-lookup"><span data-stu-id="1577b-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-216">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="1577b-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1577b-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="1577b-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1577b-218">(12)</span><span class="sxs-lookup"><span data-stu-id="1577b-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-219">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="1577b-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1577b-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1577b-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1577b-221">(13)</span><span class="sxs-lookup"><span data-stu-id="1577b-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-222">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="1577b-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1577b-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="1577b-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1577b-224">(14)</span><span class="sxs-lookup"><span data-stu-id="1577b-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-225">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="1577b-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1577b-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="1577b-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1577b-227">(15)</span><span class="sxs-lookup"><span data-stu-id="1577b-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-228">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="1577b-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1577b-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="1577b-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1577b-230">(16)</span><span class="sxs-lookup"><span data-stu-id="1577b-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-231">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="1577b-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1577b-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="1577b-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1577b-233">(17)</span><span class="sxs-lookup"><span data-stu-id="1577b-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-234">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="1577b-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1577b-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1577b-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1577b-236">(18)</span><span class="sxs-lookup"><span data-stu-id="1577b-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-237">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="1577b-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1577b-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="1577b-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="1577b-239">(19)</span><span class="sxs-lookup"><span data-stu-id="1577b-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1577b-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="1577b-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="1577b-241">(20)</span><span class="sxs-lookup"><span data-stu-id="1577b-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-242">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="1577b-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1577b-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="1577b-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1577b-244">(21)</span><span class="sxs-lookup"><span data-stu-id="1577b-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-245">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="1577b-245">System failure.</span></span> <span data-ttu-id="1577b-246">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="1577b-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="1577b-247">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="1577b-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1577b-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="1577b-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="1577b-249">(22)</span><span class="sxs-lookup"><span data-stu-id="1577b-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-250">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="1577b-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1577b-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="1577b-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1577b-252">(23)</span><span class="sxs-lookup"><span data-stu-id="1577b-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-253">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="1577b-253">System failure.</span></span> <span data-ttu-id="1577b-254">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="1577b-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1577b-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="1577b-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1577b-256">(24)</span><span class="sxs-lookup"><span data-stu-id="1577b-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-257">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="1577b-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1577b-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="1577b-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1577b-259">(25)</span><span class="sxs-lookup"><span data-stu-id="1577b-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-260">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="1577b-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1577b-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="1577b-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1577b-262">(26)</span><span class="sxs-lookup"><span data-stu-id="1577b-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-263">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="1577b-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1577b-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="1577b-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1577b-265">(27)</span><span class="sxs-lookup"><span data-stu-id="1577b-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-266">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="1577b-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1577b-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="1577b-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1577b-268">(28)</span><span class="sxs-lookup"><span data-stu-id="1577b-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-269">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="1577b-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1577b-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="1577b-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1577b-271">(29)</span><span class="sxs-lookup"><span data-stu-id="1577b-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-272">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="1577b-272">Device is disabled.</span></span> <span data-ttu-id="1577b-273">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="1577b-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1577b-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="1577b-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1577b-275">(30)</span><span class="sxs-lookup"><span data-stu-id="1577b-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-276">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="1577b-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1577b-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1577b-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1577b-278">1-31</span><span class="sxs-lookup"><span data-stu-id="1577b-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-279">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="1577b-279">Device is not working properly.</span></span> <span data-ttu-id="1577b-280">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="1577b-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1577b-281">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="1577b-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-282">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1577b-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-284">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1577b-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-285">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="1577b-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1577b-286">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1577b-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1577b-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-290">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1577b-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1577b-291">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1577b-291">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1577b-292">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="1577b-292">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="1577b-293">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-294">**куррентреадинг**</span><span class="sxs-lookup"><span data-stu-id="1577b-294">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-295">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-295">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-297">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,5 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-297">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-298">Текущее значение, указываемое датчиком.</span><span class="sxs-lookup"><span data-stu-id="1577b-298">Current value indicated by the sensor.</span></span>

<span data-ttu-id="1577b-299">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-299">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-300">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1577b-300">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1577b-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-303">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="1577b-303">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-304">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1577b-304">Description of the object.</span></span>

<span data-ttu-id="1577b-305">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-306">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1577b-306">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1577b-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-309">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1577b-309">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-310">Уникальный идентификатор текущей проверки.</span><span class="sxs-lookup"><span data-stu-id="1577b-310">Unique identifier of the current probe.</span></span>

<span data-ttu-id="1577b-311">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-312">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="1577b-312">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-313">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1577b-313">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1577b-315">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="1577b-315">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="1577b-316">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-317">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1577b-317">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-318">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1577b-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1577b-320">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="1577b-320">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="1577b-321">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1577b-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-323">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1577b-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-325">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="1577b-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-326">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="1577b-326">Date and time the object was installed.</span></span> <span data-ttu-id="1577b-327">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="1577b-327">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1577b-328">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-329">**Линейно**</span><span class="sxs-lookup"><span data-stu-id="1577b-329">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-330">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1577b-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1577b-332">Если **значение равно true**, датчик линейно помещается в динамический диапазон.</span><span class="sxs-lookup"><span data-stu-id="1577b-332">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="1577b-333">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-333">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-334">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="1577b-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-335">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1577b-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1577b-337">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="1577b-337">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1577b-338">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-339">**ловерсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="1577b-339">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-340">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-340">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-342">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,13 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-342">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-343">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения), чтобы определить, работает ли датчик в нормальных, некритических, критических или неустранимых условиях.</span><span class="sxs-lookup"><span data-stu-id="1577b-343">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether or not the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="1577b-344">Если **куррентреадинг** находится между **ловерсрешолдкритикал** и **ловерсрешолдфатал**, то текущее состояние является критически важным.</span><span class="sxs-lookup"><span data-stu-id="1577b-344">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="1577b-345">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-345">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-346">**ловерсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="1577b-346">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-347">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-347">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-349">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,15 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-350">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="1577b-350">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="1577b-351">Если **куррентреадинг** находится ниже **ловерсрешолдфатал**, текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="1577b-351">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="1577b-352">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-352">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-353">**ловерсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="1577b-353">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-354">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-354">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-356">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,11 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-357">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="1577b-357">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="1577b-358">Если **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="1577b-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="1577b-359">Если **куррентреадинг** находится между **ловерсрешолднонкритикал** и **ловерсрешолдкритикал**, текущее состояние является некритическим.</span><span class="sxs-lookup"><span data-stu-id="1577b-359">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="1577b-360">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-360">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-361">**максреадабле**</span><span class="sxs-lookup"><span data-stu-id="1577b-361">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-362">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-362">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-364">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,9 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-365">Самое большое значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="1577b-365">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="1577b-366">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-367">**минреадабле**</span><span class="sxs-lookup"><span data-stu-id="1577b-367">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-368">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-370">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,10 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-371">Наименьшее значение измеряемого свойства, которое может быть считано цифровым датчиком.</span><span class="sxs-lookup"><span data-stu-id="1577b-371">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="1577b-372">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-373">**Name**</span><span class="sxs-lookup"><span data-stu-id="1577b-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-374">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1577b-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-376">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="1577b-376">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-377">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="1577b-377">Label by which the object is known.</span></span> <span data-ttu-id="1577b-378">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="1577b-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="1577b-379">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-380">**номиналреадинг**</span><span class="sxs-lookup"><span data-stu-id="1577b-380">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-381">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-381">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-383">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,6 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-384">Обычное или ожидаемое значение для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="1577b-384">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="1577b-385">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-385">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-386">**нормалмакс**</span><span class="sxs-lookup"><span data-stu-id="1577b-386">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-387">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-389">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,7 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-390">Обычное или ожидаемое значение для числового датчика.</span><span class="sxs-lookup"><span data-stu-id="1577b-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="1577b-391">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-392">**нормалмин**</span><span class="sxs-lookup"><span data-stu-id="1577b-392">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-393">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-395">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,8 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-396">Рекомендации для пользователя в качестве обычного минимального диапазона для цифрового датчика.</span><span class="sxs-lookup"><span data-stu-id="1577b-396">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="1577b-397">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-398">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1577b-398">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-399">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1577b-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-401">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1577b-401">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-402">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="1577b-402">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="1577b-403">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1577b-404">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1577b-404">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="1577b-405">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="1577b-405">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-406">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="1577b-406">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1577b-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1577b-408">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="1577b-408">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="1577b-409">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-409">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1577b-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1577b-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1577b-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="1577b-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1577b-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="1577b-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1577b-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="1577b-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-414">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="1577b-414">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1577b-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="1577b-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-416">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="1577b-416">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1577b-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="1577b-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-418">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="1577b-418">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="1577b-419">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="1577b-419">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="1577b-420">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="1577b-420">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1577b-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="1577b-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-422">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="1577b-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1577b-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="1577b-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1577b-424">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="1577b-424">Timed Power-On Supported</span></span>

<span data-ttu-id="1577b-425">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="1577b-425">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1577b-426">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="1577b-426">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-427">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1577b-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1577b-429">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="1577b-429">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="1577b-430">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="1577b-430">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="1577b-431">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-432">**Решение**</span><span class="sxs-lookup"><span data-stu-id="1577b-432">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-433">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1577b-433">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-434">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-435">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,17 (DMTF), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("десятые доли миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-436">Способность датчика разрешать различия в измеряемом свойстве.</span><span class="sxs-lookup"><span data-stu-id="1577b-436">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="1577b-437">Это значение может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="1577b-437">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="1577b-438">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-438">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-439">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1577b-439">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-440">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1577b-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-442">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="1577b-442">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-443">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="1577b-443">Current status of the object.</span></span> <span data-ttu-id="1577b-444">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="1577b-444">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1577b-445">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="1577b-445">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1577b-446">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="1577b-446">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1577b-447">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="1577b-447">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1577b-448">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="1577b-448">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1577b-449">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-449">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1577b-450">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="1577b-450">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1577b-451">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="1577b-451">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1577b-452">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="1577b-452">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1577b-453">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="1577b-453">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1577b-454">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="1577b-454">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1577b-455">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="1577b-455">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1577b-456">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="1577b-456">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1577b-457">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="1577b-457">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1577b-458">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="1577b-458">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1577b-459">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="1577b-459">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1577b-460">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="1577b-460">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1577b-461">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="1577b-461">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1577b-462">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="1577b-462">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1577b-463">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1577b-463">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-464">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1577b-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-465">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-466">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="1577b-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-467">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="1577b-467">State of the logical device.</span></span> <span data-ttu-id="1577b-468">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="1577b-468">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="1577b-469">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1577b-470">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1577b-470">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1577b-471">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="1577b-471">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1577b-472">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="1577b-472">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1577b-473">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="1577b-473">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1577b-474">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="1577b-474">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1577b-475">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="1577b-475">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-476">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1577b-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-477">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-478">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1577b-478">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1577b-479">Значение для свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="1577b-479">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="1577b-480">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-481">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1577b-481">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-482">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1577b-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-483">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-484">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1577b-484">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1577b-485">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="1577b-485">Name of the scoping system.</span></span>

<span data-ttu-id="1577b-486">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1577b-486">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-487">**Отклонение**</span><span class="sxs-lookup"><span data-stu-id="1577b-487">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-488">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-488">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-489">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-490">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,18 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-490">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-491">Допуск датчика для измеряемого свойства.</span><span class="sxs-lookup"><span data-stu-id="1577b-491">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="1577b-492">Допуск, а также разрешение и точность используются для вычисления фактического значения измеряемого физического свойства.</span><span class="sxs-lookup"><span data-stu-id="1577b-492">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="1577b-493">Допуск может различаться в зависимости от того, является ли устройство линейным по отношению к динамическому диапазону.</span><span class="sxs-lookup"><span data-stu-id="1577b-493">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="1577b-494">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-494">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-495">**упперсрешолдкритикал**</span><span class="sxs-lookup"><span data-stu-id="1577b-495">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-496">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-496">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-497">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-498">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,14 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-499">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="1577b-499">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="1577b-500">Если **куррентреадинг** находится между **упперсрешолдкритикал** и **упперсрешолдфатал**, то текущее состояние является критически важным.</span><span class="sxs-lookup"><span data-stu-id="1577b-500">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="1577b-501">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-501">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-502">**упперсрешолдфатал**</span><span class="sxs-lookup"><span data-stu-id="1577b-502">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-503">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-503">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-504">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-505">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,16 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-506">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="1577b-506">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="1577b-507">Если **куррентреадинг** выше **упперсрешолдфатал**, текущее состояние является неустранимым.</span><span class="sxs-lookup"><span data-stu-id="1577b-507">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="1577b-508">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-508">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="1577b-509">**упперсрешолднонкритикал**</span><span class="sxs-lookup"><span data-stu-id="1577b-509">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1577b-510">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1577b-510">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1577b-511">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1577b-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1577b-512">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Текущая зонда \| 001,12 (DMTF), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллиампс")</span><span class="sxs-lookup"><span data-stu-id="1577b-512">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="1577b-513">Пороговые значения датчика задают диапазоны (минимальное и максимальное значения) для определения того, работает ли датчик как обычные, некритические, критические или неустранимые.</span><span class="sxs-lookup"><span data-stu-id="1577b-513">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="1577b-514">Если **куррентреадинг** находится между **ловерсрешолднонкритикал** и **упперсрешолднонкритикал**, датчик сообщает о нормальном значении.</span><span class="sxs-lookup"><span data-stu-id="1577b-514">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="1577b-515">Если **куррентреадинг** находится между **упперсрешолднонкритикал** и **упперсрешолдкритикал**, текущее состояние является некритическим.</span><span class="sxs-lookup"><span data-stu-id="1577b-515">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="1577b-516">Это свойство наследуется от [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-516">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1577b-517">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1577b-517">Remarks</span></span>

<span data-ttu-id="1577b-518">Класс **Win32 \_ куррентпробе** является производным от [**CIM \_ куррентсенсор**](cim-currentsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1577b-518">The **Win32\_CurrentProbe** class is derived from [**CIM\_CurrentSensor**](cim-currentsensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1577b-519">Требования</span><span class="sxs-lookup"><span data-stu-id="1577b-519">Requirements</span></span>



| <span data-ttu-id="1577b-520">Требование</span><span class="sxs-lookup"><span data-stu-id="1577b-520">Requirement</span></span> | <span data-ttu-id="1577b-521">Значение</span><span class="sxs-lookup"><span data-stu-id="1577b-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1577b-522">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1577b-522">Minimum supported client</span></span><br/> | <span data-ttu-id="1577b-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1577b-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1577b-524">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1577b-524">Minimum supported server</span></span><br/> | <span data-ttu-id="1577b-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1577b-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1577b-526">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1577b-526">Namespace</span></span><br/>                | <span data-ttu-id="1577b-527">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1577b-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1577b-528">MOF</span><span class="sxs-lookup"><span data-stu-id="1577b-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1577b-529"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1577b-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1577b-530">DLL</span><span class="sxs-lookup"><span data-stu-id="1577b-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1577b-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1577b-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1577b-532">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1577b-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1577b-533">**\_КУРРЕНТСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="1577b-533">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dt>

[<span data-ttu-id="1577b-534">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="1577b-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

