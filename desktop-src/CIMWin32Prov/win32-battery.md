---
description: Представляет батарею, подключенную к компьютерной системе.
ms.assetid: b07ccb1d-008e-4bf1-8299-33706cbcbaee
ms.tgt_platform: multiple
title: Класс Win32_Battery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Battery
- Win32_Battery.Reset
- Win32_Battery.SetPowerState
- Win32_Battery.Availability
- Win32_Battery.BatteryRechargeTime
- Win32_Battery.BatteryStatus
- Win32_Battery.Caption
- Win32_Battery.Chemistry
- Win32_Battery.ConfigManagerErrorCode
- Win32_Battery.ConfigManagerUserConfig
- Win32_Battery.CreationClassName
- Win32_Battery.Description
- Win32_Battery.DesignCapacity
- Win32_Battery.DesignVoltage
- Win32_Battery.DeviceID
- Win32_Battery.ErrorCleared
- Win32_Battery.ErrorDescription
- Win32_Battery.EstimatedChargeRemaining
- Win32_Battery.EstimatedRunTime
- Win32_Battery.ExpectedBatteryLife
- Win32_Battery.ExpectedLife
- Win32_Battery.FullChargeCapacity
- Win32_Battery.InstallDate
- Win32_Battery.LastErrorCode
- Win32_Battery.MaxRechargeTime
- Win32_Battery.Name
- Win32_Battery.PNPDeviceID
- Win32_Battery.PowerManagementCapabilities
- Win32_Battery.PowerManagementSupported
- Win32_Battery.SmartBatteryVersion
- Win32_Battery.Status
- Win32_Battery.StatusInfo
- Win32_Battery.SystemCreationClassName
- Win32_Battery.SystemName
- Win32_Battery.TimeOnBattery
- Win32_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75477bcf670bcc0cf16c63f130f95d4c38d7b783
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072530"
---
# <a name="win32_battery-class"></a><span data-ttu-id="1795a-103">\_Класс аккумулятора Win32</span><span class="sxs-lookup"><span data-stu-id="1795a-103">Win32\_Battery class</span></span>

<span data-ttu-id="1795a-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ батареи Win32** представляет батарею, подключенную к компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="1795a-104">The **Win32\_Battery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a battery connected to the computer system.</span></span>

<span data-ttu-id="1795a-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1795a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1795a-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1795a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1795a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1795a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Battery : CIM_Battery
{
  uint16   Availability;
  uint32   BatteryRechargeTime;
  uint16   BatteryStatus;
  string   Caption;
  uint16   Chemistry;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedBatteryLife;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxRechargeTime;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   SmartBatteryVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="1795a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="1795a-108">Members</span></span>

<span data-ttu-id="1795a-109">Класс **\_ аккумулятора Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1795a-109">The **Win32\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="1795a-110">Методы</span><span class="sxs-lookup"><span data-stu-id="1795a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1795a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="1795a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1795a-112">Методы</span><span class="sxs-lookup"><span data-stu-id="1795a-112">Methods</span></span>

<span data-ttu-id="1795a-113">Класс **\_ аккумулятора Win32** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1795a-113">The **Win32\_Battery** class has these methods.</span></span>



| <span data-ttu-id="1795a-114">Метод</span><span class="sxs-lookup"><span data-stu-id="1795a-114">Method</span></span>            | <span data-ttu-id="1795a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1795a-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1795a-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="1795a-116">**Reset**</span></span>         | <span data-ttu-id="1795a-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="1795a-117">Not implemented.</span></span> <span data-ttu-id="1795a-118">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**\_ батарее CIM**](cim-battery.md) .</span><span class="sxs-lookup"><span data-stu-id="1795a-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="1795a-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1795a-119">**SetPowerState**</span></span> | <span data-ttu-id="1795a-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="1795a-120">Not implemented.</span></span> <span data-ttu-id="1795a-121">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в разделе [**\_ аккумулятора CIM**](cim-battery.md) .</span><span class="sxs-lookup"><span data-stu-id="1795a-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1795a-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="1795a-122">Properties</span></span>

<span data-ttu-id="1795a-123">Класс **\_ аккумулятора Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1795a-123">The **Win32\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1795a-124">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="1795a-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1795a-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-127">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="1795a-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-128">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="1795a-128">Availability and status of the device.</span></span>

<span data-ttu-id="1795a-129">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1795a-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1795a-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1795a-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="1795a-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1795a-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="1795a-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-133">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="1795a-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1795a-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="1795a-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1795a-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="1795a-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1795a-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="1795a-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1795a-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="1795a-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1795a-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="1795a-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1795a-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="1795a-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1795a-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="1795a-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1795a-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="1795a-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1795a-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="1795a-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1795a-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="1795a-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-144">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="1795a-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1795a-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="1795a-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-146">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="1795a-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1795a-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="1795a-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-148">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="1795a-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1795a-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="1795a-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1795a-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="1795a-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-151">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="1795a-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1795a-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="1795a-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-153">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="1795a-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1795a-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="1795a-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-155">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="1795a-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1795a-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="1795a-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-157">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="1795a-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1795a-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="1795a-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-159">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="1795a-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1795a-160">**баттериречаржетиме**</span><span class="sxs-lookup"><span data-stu-id="1795a-160">**BatteryRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-161">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1795a-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-163">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("hKey \_ Local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| речаржерате"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="1795a-163">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|RechargeRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-164">Время, необходимое для полной зарядки аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="1795a-164">Time required to fully charge the battery.</span></span> <span data-ttu-id="1795a-165">Данное свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1795a-165">This property is not supported.</span></span> <span data-ttu-id="1795a-166">**Баттериречаржетиме** не имеет свойства замены и теперь считается устаревшим.</span><span class="sxs-lookup"><span data-stu-id="1795a-166">**BatteryRechargeTime** does not have a replacement property, and is now considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="1795a-167">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="1795a-167">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-168">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1795a-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-170">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="1795a-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-171">Состояние аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="1795a-171">Status of the battery.</span></span> <span data-ttu-id="1795a-172">Значение 10 (undefine) недопустимо в схеме CIM, так как в DMI оно представляет, что батарея не установлена.</span><span class="sxs-lookup"><span data-stu-id="1795a-172">The value 10 (Undefined) is not valid in the CIM schema because in DMI it represents that no battery is installed.</span></span> <span data-ttu-id="1795a-173">В этом случае не следует создавать экземпляры объекта.</span><span class="sxs-lookup"><span data-stu-id="1795a-173">In this case, the object should not be instantiated.</span></span>

<span data-ttu-id="1795a-174">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-174">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1795a-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1795a-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-176">Батарея отряжается.</span><span class="sxs-lookup"><span data-stu-id="1795a-176">The battery is discharging.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1795a-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="1795a-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-178">Система имеет доступ к AC, поэтому батарея не взимается.</span><span class="sxs-lookup"><span data-stu-id="1795a-178">The system has access to AC so no battery is being discharged.</span></span> <span data-ttu-id="1795a-179">Однако батарея не обязательно заряжается.</span><span class="sxs-lookup"><span data-stu-id="1795a-179">However, the battery is not necessarily charging.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="1795a-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Полностью заряжена** (3)</span><span class="sxs-lookup"><span data-stu-id="1795a-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="1795a-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Низкий** (4)</span><span class="sxs-lookup"><span data-stu-id="1795a-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="1795a-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (5)</span><span class="sxs-lookup"><span data-stu-id="1795a-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="1795a-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Зарядка** (6)</span><span class="sxs-lookup"><span data-stu-id="1795a-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="1795a-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Зарядка и высокая** (7)</span><span class="sxs-lookup"><span data-stu-id="1795a-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="1795a-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Зарядка и низкая** (8)</span><span class="sxs-lookup"><span data-stu-id="1795a-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="1795a-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Зарядка и критическая** ошибка (9)</span><span class="sxs-lookup"><span data-stu-id="1795a-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="1795a-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Не **определено** (10)</span><span class="sxs-lookup"><span data-stu-id="1795a-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="1795a-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Частично заряжена** (11)</span><span class="sxs-lookup"><span data-stu-id="1795a-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1795a-189">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1795a-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1795a-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-192">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1795a-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-193">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="1795a-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="1795a-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-195">**Химия**</span><span class="sxs-lookup"><span data-stu-id="1795a-195">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-196">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1795a-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-198">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="1795a-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-199">Перечисление, описывающее химия батареи.</span><span class="sxs-lookup"><span data-stu-id="1795a-199">Enumeration that describes the battery's chemistry.</span></span>

<span data-ttu-id="1795a-200">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-200">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1795a-201">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1795a-201">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1795a-202">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="1795a-202">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="1795a-203">**Ведущий ACID** (3)</span><span class="sxs-lookup"><span data-stu-id="1795a-203">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="1795a-204">**Никель кадмиум** (4)</span><span class="sxs-lookup"><span data-stu-id="1795a-204">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="1795a-205">**Никель металла хидриде** (5)</span><span class="sxs-lookup"><span data-stu-id="1795a-205">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="1795a-206">**Литий-ионный** (6)</span><span class="sxs-lookup"><span data-stu-id="1795a-206">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="1795a-207">**Зинк воздуха** (7)</span><span class="sxs-lookup"><span data-stu-id="1795a-207">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="1795a-208">**Литий-Polymer** (8)</span><span class="sxs-lookup"><span data-stu-id="1795a-208">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1795a-209">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="1795a-209">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-210">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1795a-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-212">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1795a-212">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-213">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="1795a-213">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="1795a-214">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-214">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1795a-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="1795a-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="1795a-216"> (0)</span><span class="sxs-lookup"><span data-stu-id="1795a-216">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-217">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="1795a-217">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1795a-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="1795a-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="1795a-219">(1)</span><span class="sxs-lookup"><span data-stu-id="1795a-219">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-220">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="1795a-220">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1795a-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1795a-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1795a-222">(2)</span><span class="sxs-lookup"><span data-stu-id="1795a-222">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1795a-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="1795a-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1795a-224">(3)</span><span class="sxs-lookup"><span data-stu-id="1795a-224">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-225">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1795a-225">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1795a-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="1795a-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1795a-227">(4)</span><span class="sxs-lookup"><span data-stu-id="1795a-227">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-228">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="1795a-228">Device is not working properly.</span></span> <span data-ttu-id="1795a-229">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="1795a-229">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1795a-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="1795a-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1795a-231">(5)</span><span class="sxs-lookup"><span data-stu-id="1795a-231">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-232">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="1795a-232">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1795a-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="1795a-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1795a-234"> (6)</span><span class="sxs-lookup"><span data-stu-id="1795a-234">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-235">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="1795a-235">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1795a-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="1795a-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="1795a-237">(7)</span><span class="sxs-lookup"><span data-stu-id="1795a-237">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1795a-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="1795a-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1795a-239">(8)</span><span class="sxs-lookup"><span data-stu-id="1795a-239">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-240">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="1795a-240">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1795a-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="1795a-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1795a-242">(9)</span><span class="sxs-lookup"><span data-stu-id="1795a-242">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-243">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="1795a-243">Device is not working properly.</span></span> <span data-ttu-id="1795a-244">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="1795a-244">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1795a-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="1795a-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="1795a-246">(10)</span><span class="sxs-lookup"><span data-stu-id="1795a-246">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-247">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="1795a-247">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1795a-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="1795a-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="1795a-249">(11)</span><span class="sxs-lookup"><span data-stu-id="1795a-249">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-250">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="1795a-250">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1795a-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="1795a-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1795a-252">(12)</span><span class="sxs-lookup"><span data-stu-id="1795a-252">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-253">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="1795a-253">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1795a-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1795a-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1795a-255">(13)</span><span class="sxs-lookup"><span data-stu-id="1795a-255">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-256">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="1795a-256">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1795a-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="1795a-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1795a-258">(14)</span><span class="sxs-lookup"><span data-stu-id="1795a-258">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-259">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="1795a-259">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1795a-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="1795a-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1795a-261">(15)</span><span class="sxs-lookup"><span data-stu-id="1795a-261">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-262">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="1795a-262">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1795a-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="1795a-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1795a-264">(16)</span><span class="sxs-lookup"><span data-stu-id="1795a-264">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-265">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="1795a-265">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1795a-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="1795a-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1795a-267">(17)</span><span class="sxs-lookup"><span data-stu-id="1795a-267">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-268">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="1795a-268">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1795a-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1795a-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1795a-270">(18)</span><span class="sxs-lookup"><span data-stu-id="1795a-270">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-271">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="1795a-271">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1795a-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="1795a-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="1795a-273">(19)</span><span class="sxs-lookup"><span data-stu-id="1795a-273">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1795a-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="1795a-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="1795a-275">(20)</span><span class="sxs-lookup"><span data-stu-id="1795a-275">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-276">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="1795a-276">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1795a-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="1795a-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1795a-278">(21)</span><span class="sxs-lookup"><span data-stu-id="1795a-278">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-279">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="1795a-279">System failure.</span></span> <span data-ttu-id="1795a-280">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="1795a-280">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="1795a-281">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="1795a-281">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1795a-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="1795a-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="1795a-283">(22)</span><span class="sxs-lookup"><span data-stu-id="1795a-283">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-284">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="1795a-284">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1795a-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="1795a-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1795a-286">(23)</span><span class="sxs-lookup"><span data-stu-id="1795a-286">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-287">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="1795a-287">System failure.</span></span> <span data-ttu-id="1795a-288">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="1795a-288">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1795a-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="1795a-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1795a-290">(24)</span><span class="sxs-lookup"><span data-stu-id="1795a-290">(24)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-291">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="1795a-291">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1795a-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="1795a-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1795a-293">(25)</span><span class="sxs-lookup"><span data-stu-id="1795a-293">(25)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-294">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="1795a-294">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1795a-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="1795a-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1795a-296">(26)</span><span class="sxs-lookup"><span data-stu-id="1795a-296">(26)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-297">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="1795a-297">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1795a-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="1795a-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1795a-299">(27)</span><span class="sxs-lookup"><span data-stu-id="1795a-299">(27)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-300">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="1795a-300">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1795a-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="1795a-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1795a-302">(28)</span><span class="sxs-lookup"><span data-stu-id="1795a-302">(28)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-303">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="1795a-303">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1795a-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="1795a-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1795a-305">(29)</span><span class="sxs-lookup"><span data-stu-id="1795a-305">(29)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-306">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="1795a-306">Device is disabled.</span></span> <span data-ttu-id="1795a-307">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="1795a-307">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1795a-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="1795a-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1795a-309">(30)</span><span class="sxs-lookup"><span data-stu-id="1795a-309">(30)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-310">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="1795a-310">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1795a-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1795a-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1795a-312">1-31</span><span class="sxs-lookup"><span data-stu-id="1795a-312">(31)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-313">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="1795a-313">Device is not working properly.</span></span> <span data-ttu-id="1795a-314">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="1795a-314">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1795a-315">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="1795a-315">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-316">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1795a-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-318">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1795a-318">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-319">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="1795a-319">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1795a-320">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-321">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1795a-321">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1795a-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-324">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1795a-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1795a-325">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1795a-325">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1795a-326">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="1795a-326">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="1795a-327">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-328">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1795a-328">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-329">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1795a-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-331">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="1795a-331">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-332">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1795a-332">Description of the object.</span></span>

<span data-ttu-id="1795a-333">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-334">**десигнкапаЦити**</span><span class="sxs-lookup"><span data-stu-id="1795a-334">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-335">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1795a-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-337">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,8 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" диаграмме милливаттах-hours ")</span><span class="sxs-lookup"><span data-stu-id="1795a-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-338">Разработайте емкость аккумулятора в диаграмме милливаттах-hours.</span><span class="sxs-lookup"><span data-stu-id="1795a-338">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="1795a-339">Если свойство не поддерживается, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="1795a-339">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="1795a-340">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-340">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-341">**десигнволтаже**</span><span class="sxs-lookup"><span data-stu-id="1795a-341">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-342">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1795a-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-344">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Переносная батарея DMTF \| 002,9 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="1795a-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-345">Проектирование напряжения батареи в милливольтах.</span><span class="sxs-lookup"><span data-stu-id="1795a-345">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="1795a-346">Если атрибут не поддерживается, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="1795a-346">If the attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="1795a-347">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-347">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="1795a-348">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1795a-348">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-349">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1795a-349">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-350">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1795a-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-352">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1795a-352">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-353">Определяет батарею.</span><span class="sxs-lookup"><span data-stu-id="1795a-353">Identifies the battery.</span></span>

<span data-ttu-id="1795a-354">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1795a-355">Пример: "Внутренняя батарея"</span><span class="sxs-lookup"><span data-stu-id="1795a-355">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="1795a-356">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="1795a-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-357">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1795a-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1795a-359">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="1795a-359">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="1795a-360">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-361">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1795a-361">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-362">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1795a-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1795a-364">Произвольная строка, которая предоставляет дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="1795a-364">Free-form string that supplies more information about the error recorded in **LastErrorCode** property, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="1795a-365">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-366">**естиматедчаржеремаининг**</span><span class="sxs-lookup"><span data-stu-id="1795a-366">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-367">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1795a-367">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-369">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("процент")</span><span class="sxs-lookup"><span data-stu-id="1795a-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-370">Оценка оставшегося процента от полной зарядки.</span><span class="sxs-lookup"><span data-stu-id="1795a-370">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="1795a-371">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-371">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-372">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="1795a-372">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-373">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1795a-373">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-375">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,15 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" минуты ")</span><span class="sxs-lookup"><span data-stu-id="1795a-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-376">Оцените в минутах время, в течение которого заряд батареи заряжается при условиях текущей нагрузки, если работа программы отключена или потеряна и не работает, или ноутбук отключен от источника питания.</span><span class="sxs-lookup"><span data-stu-id="1795a-376">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="1795a-377">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-378">**експектедбаттерилифе**</span><span class="sxs-lookup"><span data-stu-id="1795a-378">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-379">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1795a-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-381">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("hKey \_ Local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| баттерилифе"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="1795a-381">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|BatteryLife"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-382">Время, необходимое для полной очистки аккумулятора после полной оплаты.</span><span class="sxs-lookup"><span data-stu-id="1795a-382">Amount of time it takes to completely drain the battery after it is fully charged.</span></span> <span data-ttu-id="1795a-383">Это свойство больше не используется и считается устаревшим.</span><span class="sxs-lookup"><span data-stu-id="1795a-383">This property is no longer used and is considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="1795a-384">**експектедлифе**</span><span class="sxs-lookup"><span data-stu-id="1795a-384">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-385">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1795a-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-386">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-387">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="1795a-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-388">Ожидаемое время существования аккумулятора в минутах, предполагая, что батарея полностью заряжена.</span><span class="sxs-lookup"><span data-stu-id="1795a-388">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="1795a-389">Свойство представляет общее ожидаемое время работы батареи, а не текущий оставшийся срок жизни, которое указывается свойством **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="1795a-389">The property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="1795a-390">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-390">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-391">**фуллчаржекапаЦити**</span><span class="sxs-lookup"><span data-stu-id="1795a-391">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-392">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1795a-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-394">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" диаграмме милливаттах-hours ")</span><span class="sxs-lookup"><span data-stu-id="1795a-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-395">Полная плата за батарею в диаграмме милливаттах-часах.</span><span class="sxs-lookup"><span data-stu-id="1795a-395">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="1795a-396">Сравнение значения со свойством **десигнкапаЦити** определяет, когда батарея требует замены.</span><span class="sxs-lookup"><span data-stu-id="1795a-396">Comparison of the value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="1795a-397">Окончание работы батареи обычно происходит, когда свойство **фуллчаржекапаЦити** становится менее 80% от свойства **десигнкапаЦити** .</span><span class="sxs-lookup"><span data-stu-id="1795a-397">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="1795a-398">Если свойство не поддерживается, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="1795a-398">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="1795a-399">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-399">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-400">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1795a-400">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-401">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1795a-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-403">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="1795a-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-404">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="1795a-404">Date and time the object was installed.</span></span> <span data-ttu-id="1795a-405">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="1795a-405">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1795a-406">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-407">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="1795a-407">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-408">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1795a-408">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1795a-410">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="1795a-410">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1795a-411">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-412">**максречаржетиме**</span><span class="sxs-lookup"><span data-stu-id="1795a-412">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-413">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1795a-413">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-415">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="1795a-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-416">Максимальное время (в минутах) для полной зарядки аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="1795a-416">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="1795a-417">Свойство представляет время, которое будет выплатить полностью исчерпанный аккумулятор, а не текущее оставшееся время, которое указывается в свойстве **тиметофуллчарже** .</span><span class="sxs-lookup"><span data-stu-id="1795a-417">The property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="1795a-418">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-418">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-419">**Name**</span><span class="sxs-lookup"><span data-stu-id="1795a-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-420">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1795a-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-422">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="1795a-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-423">Определяет метку, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="1795a-423">Defines the label by which the object is known.</span></span> <span data-ttu-id="1795a-424">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="1795a-424">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="1795a-425">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-426">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1795a-426">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-427">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1795a-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-429">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1795a-429">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-430">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="1795a-430">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="1795a-431">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1795a-432">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1795a-432">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="1795a-433">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="1795a-433">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-434">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="1795a-434">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1795a-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1795a-436">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="1795a-436">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="1795a-437">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-437">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1795a-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1795a-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1795a-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="1795a-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1795a-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="1795a-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1795a-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="1795a-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-442">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="1795a-442">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1795a-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="1795a-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-444">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="1795a-444">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1795a-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="1795a-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-446">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="1795a-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="1795a-447">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="1795a-447">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="1795a-448">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="1795a-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1795a-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="1795a-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-450">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="1795a-450">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1795a-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="1795a-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1795a-452">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="1795a-452">Timed Power-On Supported</span></span>

<span data-ttu-id="1795a-453">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="1795a-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1795a-454">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="1795a-454">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-455">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1795a-455">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-456">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1795a-457">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="1795a-457">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="1795a-458">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="1795a-458">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="1795a-459">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-460">**смартбаттериверсион**</span><span class="sxs-lookup"><span data-stu-id="1795a-460">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-461">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1795a-461">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-462">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-463">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Портативная батарея DMTF \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="1795a-463">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-464">Номер версии спецификации данных, поддерживаемый батареей.</span><span class="sxs-lookup"><span data-stu-id="1795a-464">Data Specification version number supported by the battery.</span></span> <span data-ttu-id="1795a-465">Если батарея не поддерживает эту функцию, значение должно остаться пустым.</span><span class="sxs-lookup"><span data-stu-id="1795a-465">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="1795a-466">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-466">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-467">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1795a-467">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-468">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1795a-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-469">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-470">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="1795a-470">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-471">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="1795a-471">Current status of the object.</span></span> <span data-ttu-id="1795a-472">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="1795a-472">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1795a-473">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="1795a-473">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1795a-474">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="1795a-474">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1795a-475">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="1795a-475">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1795a-476">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="1795a-476">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1795a-477">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-477">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1795a-478">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="1795a-478">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1795a-479">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="1795a-479">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1795a-480">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="1795a-480">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1795a-481">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="1795a-481">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1795a-482">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="1795a-482">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1795a-483">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="1795a-483">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1795a-484">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="1795a-484">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1795a-485">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="1795a-485">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1795a-486">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="1795a-486">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1795a-487">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="1795a-487">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1795a-488">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="1795a-488">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1795a-489">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="1795a-489">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1795a-490">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="1795a-490">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1795a-491">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1795a-491">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-492">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1795a-492">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-493">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-494">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="1795a-494">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-495">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="1795a-495">State of the logical device.</span></span> <span data-ttu-id="1795a-496">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="1795a-496">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="1795a-497">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1795a-498">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1795a-498">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1795a-499">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="1795a-499">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1795a-500">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="1795a-500">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1795a-501">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="1795a-501">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1795a-502">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="1795a-502">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1795a-503">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="1795a-503">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-504">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1795a-504">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-505">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-506">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1795a-506">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1795a-507">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="1795a-507">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="1795a-508">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-508">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-509">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1795a-509">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-510">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1795a-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-511">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-512">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1795a-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1795a-513">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="1795a-513">Name of the scoping system.</span></span>

<span data-ttu-id="1795a-514">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1795a-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-515">**тимеонбаттери**</span><span class="sxs-lookup"><span data-stu-id="1795a-515">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-516">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1795a-516">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-517">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-518">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("секунды")</span><span class="sxs-lookup"><span data-stu-id="1795a-518">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-519">Время в секундах, прошедшее с момента последнего переключения ИБП компьютера на питание от аккумулятора или с момента последнего перезапуска системы или ИБП, в зависимости от того, какое значение меньше.</span><span class="sxs-lookup"><span data-stu-id="1795a-519">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="1795a-520">Если батарея находится в строке, возвращается значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="1795a-520">If the battery is "on line", 0 (zero) is returned.</span></span>

<span data-ttu-id="1795a-521">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-521">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="1795a-522">**тиметофуллчарже**</span><span class="sxs-lookup"><span data-stu-id="1795a-522">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1795a-523">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1795a-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1795a-524">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1795a-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1795a-525">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,16 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" минуты ")</span><span class="sxs-lookup"><span data-stu-id="1795a-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="1795a-526">Оставшееся время для полной зарядки аккумулятора в минутах по текущей ставке и использованию.</span><span class="sxs-lookup"><span data-stu-id="1795a-526">Remaining time to charge the battery fully in minutes at the current charging rate and usage.</span></span>

<span data-ttu-id="1795a-527">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="1795a-527">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1795a-528">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1795a-528">Remarks</span></span>

<span data-ttu-id="1795a-529">Класс **\_ батареи Win32** является производным от [**\_ аккумулятора CIM**](cim-battery.md) , который является производным от CIM-класса. [**\_**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="1795a-529">The **Win32\_Battery** class is derived from [**CIM\_Battery**](cim-battery.md) which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1795a-530">Windows Server 2008 содержит драйверы ИБП (APC) в ОС, что позволяет рассматривать ИБП как питание от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="1795a-530">Windows Server 2008 contains the (APC) UPS drivers in the OS, which allows you to treat the UPS as a battery supply.</span></span> <span data-ttu-id="1795a-531">Это позволяет отслеживать состояние ИБП с помощью сценария и предпринимать необходимые действия.</span><span class="sxs-lookup"><span data-stu-id="1795a-531">This allows you to monitor the UPS status using a script and take actions when necessary.</span></span>

## <a name="examples"></a><span data-ttu-id="1795a-532">Примеры</span><span class="sxs-lookup"><span data-stu-id="1795a-532">Examples</span></span>

<span data-ttu-id="1795a-533">[Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) пример кода PowerShell запрашивает **\_ батарею Win32** , чтобы определить, следует ли переключать беспроводную сеть для экономии энергии.</span><span class="sxs-lookup"><span data-stu-id="1795a-533">The [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell code sample queries **Win32\_Battery** to determine whether or not to toggle the wireless in order to save power.</span></span>

<span data-ttu-id="1795a-534">В списке примеров Perl для [получения сведений](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) о источниках питания, подключенных к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="1795a-534">The [List UPS Information](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) Perl sample Lists information about the uninterruptible power sources attached to a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1795a-535">Требования</span><span class="sxs-lookup"><span data-stu-id="1795a-535">Requirements</span></span>



| <span data-ttu-id="1795a-536">Требование</span><span class="sxs-lookup"><span data-stu-id="1795a-536">Requirement</span></span> | <span data-ttu-id="1795a-537">Значение</span><span class="sxs-lookup"><span data-stu-id="1795a-537">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1795a-538">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1795a-538">Minimum supported client</span></span><br/> | <span data-ttu-id="1795a-539">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1795a-539">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1795a-540">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1795a-540">Minimum supported server</span></span><br/> | <span data-ttu-id="1795a-541">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1795a-541">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1795a-542">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1795a-542">Namespace</span></span><br/>                | <span data-ttu-id="1795a-543">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1795a-543">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1795a-544">MOF</span><span class="sxs-lookup"><span data-stu-id="1795a-544">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1795a-545"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1795a-545"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1795a-546">DLL</span><span class="sxs-lookup"><span data-stu-id="1795a-546">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1795a-547"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1795a-547"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1795a-548">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1795a-548">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1795a-549">**\_Аккумулятор CIM**</span><span class="sxs-lookup"><span data-stu-id="1795a-549">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="1795a-550">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="1795a-550">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

