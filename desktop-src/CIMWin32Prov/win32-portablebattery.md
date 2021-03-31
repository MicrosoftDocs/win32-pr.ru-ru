---
description: '\_Класс WMI портаблебаттери для Win32 содержит свойства, связанные с переносным аккумулятором, например ноутбук ноутбука.'
ms.assetid: ca7d061f-8fc6-4a1e-aa75-2465ce5e2735
ms.tgt_platform: multiple
title: Класс Win32_PortableBattery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortableBattery
- Win32_PortableBattery.Reset
- Win32_PortableBattery.SetPowerState
- Win32_PortableBattery.Availability
- Win32_PortableBattery.BatteryStatus
- Win32_PortableBattery.CapacityMultiplier
- Win32_PortableBattery.Caption
- Win32_PortableBattery.Chemistry
- Win32_PortableBattery.ConfigManagerErrorCode
- Win32_PortableBattery.ConfigManagerUserConfig
- Win32_PortableBattery.CreationClassName
- Win32_PortableBattery.Description
- Win32_PortableBattery.DesignCapacity
- Win32_PortableBattery.DesignVoltage
- Win32_PortableBattery.DeviceID
- Win32_PortableBattery.ErrorCleared
- Win32_PortableBattery.ErrorDescription
- Win32_PortableBattery.EstimatedChargeRemaining
- Win32_PortableBattery.EstimatedRunTime
- Win32_PortableBattery.ExpectedBatteryLife
- Win32_PortableBattery.ExpectedLife
- Win32_PortableBattery.FullChargeCapacity
- Win32_PortableBattery.InstallDate
- Win32_PortableBattery.LastErrorCode
- Win32_PortableBattery.Location
- Win32_PortableBattery.ManufactureDate
- Win32_PortableBattery.Manufacturer
- Win32_PortableBattery.MaxBatteryError
- Win32_PortableBattery.MaxRechargeTime
- Win32_PortableBattery.Name
- Win32_PortableBattery.PNPDeviceID
- Win32_PortableBattery.PowerManagementCapabilities
- Win32_PortableBattery.PowerManagementSupported
- Win32_PortableBattery.SmartBatteryVersion
- Win32_PortableBattery.Status
- Win32_PortableBattery.StatusInfo
- Win32_PortableBattery.SystemCreationClassName
- Win32_PortableBattery.SystemName
- Win32_PortableBattery.TimeOnBattery
- Win32_PortableBattery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9db875e7e4d1736cf45945b53f2f20fec0490a47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807084"
---
# <a name="win32_portablebattery-class"></a><span data-ttu-id="dc87a-103">\_Класс Win32 портаблебаттери</span><span class="sxs-lookup"><span data-stu-id="dc87a-103">Win32\_PortableBattery class</span></span>

<span data-ttu-id="dc87a-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ портаблебаттери для Win32** содержит свойства, связанные с переносным аккумулятором, например ноутбук ноутбука.</span><span class="sxs-lookup"><span data-stu-id="dc87a-104">The **Win32\_PortableBattery** [WMI class](../wmisdk/retrieving-a-class.md) contains the properties related to a portable battery, such as a notebook computer battery.</span></span>

<span data-ttu-id="dc87a-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="dc87a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dc87a-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="dc87a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc87a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc87a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortableBattery : CIM_Battery
{
  uint16   Availability;
  uint16   BatteryStatus;
  uint16   CapacityMultiplier;
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
  string   Location;
  string   ManufactureDate;
  string   Manufacturer;
  uint16   MaxBatteryError;
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

## <a name="members"></a><span data-ttu-id="dc87a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="dc87a-108">Members</span></span>

<span data-ttu-id="dc87a-109">Класс **Win32 \_ портаблебаттери** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dc87a-109">The **Win32\_PortableBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="dc87a-110">Методы</span><span class="sxs-lookup"><span data-stu-id="dc87a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="dc87a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc87a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dc87a-112">Методы</span><span class="sxs-lookup"><span data-stu-id="dc87a-112">Methods</span></span>

<span data-ttu-id="dc87a-113">Класс **Win32 \_ портаблебаттери** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dc87a-113">The **Win32\_PortableBattery** class has these methods.</span></span>



| <span data-ttu-id="dc87a-114">Метод</span><span class="sxs-lookup"><span data-stu-id="dc87a-114">Method</span></span>            | <span data-ttu-id="dc87a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="dc87a-115">Description</span></span>                                                                                                                                                                        |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc87a-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="dc87a-116">**Reset**</span></span>         | <span data-ttu-id="dc87a-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="dc87a-117">Not implemented.</span></span> <span data-ttu-id="dc87a-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**\_ батарее CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/>                 |
| <span data-ttu-id="dc87a-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dc87a-119">**SetPowerState**</span></span> | <span data-ttu-id="dc87a-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="dc87a-120">Not implemented.</span></span> <span data-ttu-id="dc87a-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**разделе \_ аккумулятор CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dc87a-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc87a-122">Properties</span></span>

<span data-ttu-id="dc87a-123">Класс **Win32 \_ портаблебаттери** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dc87a-123">The **Win32\_PortableBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc87a-124">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="dc87a-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc87a-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-127">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="dc87a-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-128">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="dc87a-128">Availability and status of the device.</span></span>

<span data-ttu-id="dc87a-129">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc87a-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dc87a-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc87a-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dc87a-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="dc87a-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="dc87a-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-133">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="dc87a-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dc87a-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="dc87a-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="dc87a-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="dc87a-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dc87a-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="dc87a-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dc87a-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="dc87a-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="dc87a-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="dc87a-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="dc87a-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="dc87a-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dc87a-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="dc87a-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="dc87a-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="dc87a-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="dc87a-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="dc87a-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="dc87a-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="dc87a-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-144">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="dc87a-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dc87a-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="dc87a-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-146">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="dc87a-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dc87a-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="dc87a-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-148">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="dc87a-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dc87a-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="dc87a-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="dc87a-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="dc87a-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-151">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="dc87a-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dc87a-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="dc87a-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-153">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="dc87a-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="dc87a-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="dc87a-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-155">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="dc87a-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="dc87a-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="dc87a-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-157">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="dc87a-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="dc87a-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="dc87a-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-159">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="dc87a-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc87a-160">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="dc87a-160">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-161">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc87a-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-163">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Портативная батарея DMTF \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="dc87a-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-164">Описание состояния зарядки аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="dc87a-164">Description of the battery's charge status.</span></span> <span data-ttu-id="dc87a-165">Значение 10 (undefine) недопустимо в схеме модель CIM (CIM), так как в интерфейсе управления рабочим столом (DMI) это означает, что батарея не установлена.</span><span class="sxs-lookup"><span data-stu-id="dc87a-165">The value 10 (Undefined) is not valid in the Common Information Model (CIM) schema because in Desktop Management Interface (DMI) it indicates that no battery is installed.</span></span> <span data-ttu-id="dc87a-166">В этом случае не следует создавать экземпляры этого объекта.</span><span class="sxs-lookup"><span data-stu-id="dc87a-166">In this case, this object should not be instantiated.</span></span>

<span data-ttu-id="dc87a-167">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-167">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc87a-168">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dc87a-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc87a-169">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dc87a-169">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="dc87a-170">**Полностью заряжена** (3)</span><span class="sxs-lookup"><span data-stu-id="dc87a-170">**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="dc87a-171">**Низкий** (4)</span><span class="sxs-lookup"><span data-stu-id="dc87a-171">**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="dc87a-172">**Критическая** (5)</span><span class="sxs-lookup"><span data-stu-id="dc87a-172">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="dc87a-173">**Зарядка** (6)</span><span class="sxs-lookup"><span data-stu-id="dc87a-173">**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="dc87a-174">**Зарядка и высокая** (7)</span><span class="sxs-lookup"><span data-stu-id="dc87a-174">**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="dc87a-175">**Зарядка и низкая** (8)</span><span class="sxs-lookup"><span data-stu-id="dc87a-175">**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="dc87a-176">**Зарядка и критическая** ошибка (9)</span><span class="sxs-lookup"><span data-stu-id="dc87a-176">**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="dc87a-177">Не **определено** (10)</span><span class="sxs-lookup"><span data-stu-id="dc87a-177">**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="dc87a-178">**Частично заряжена** (11)</span><span class="sxs-lookup"><span data-stu-id="dc87a-178">**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc87a-179">**капаЦитимултиплиер**</span><span class="sxs-lookup"><span data-stu-id="dc87a-179">**CapacityMultiplier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-180">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc87a-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-182">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 22. \| Коэффициент мощности проектирования")</span><span class="sxs-lookup"><span data-stu-id="dc87a-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Design Capacity Multiplier")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-183">Коэффициент умножения значения **десигнкапаЦити** , чтобы убедиться, что значение диаграмме милливаттах Hour не является переполнением для реализаций спецификации данных Smart аккумулятора (сбдс).</span><span class="sxs-lookup"><span data-stu-id="dc87a-183">Multiplication factor of the **DesignCapacity** value to ensure that the milliwatt hour value does not overflow for Smart Battery Data Specification (SBDS) implementations.</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-184">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="dc87a-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-187">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dc87a-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-188">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="dc87a-188">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="dc87a-189">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-190">**Химия**</span><span class="sxs-lookup"><span data-stu-id="dc87a-190">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-191">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc87a-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-193">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Портативная батарея DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="dc87a-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-194">Химия батареи.</span><span class="sxs-lookup"><span data-stu-id="dc87a-194">Chemistry of the battery.</span></span>

<span data-ttu-id="dc87a-195">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-195">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc87a-196">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dc87a-196">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc87a-197">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dc87a-197">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="dc87a-198">**Ведущий ACID** (3)</span><span class="sxs-lookup"><span data-stu-id="dc87a-198">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="dc87a-199">**Никель кадмиум** (4)</span><span class="sxs-lookup"><span data-stu-id="dc87a-199">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="dc87a-200">**Никель металла хидриде** (5)</span><span class="sxs-lookup"><span data-stu-id="dc87a-200">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="dc87a-201">**Литий-ионный** (6)</span><span class="sxs-lookup"><span data-stu-id="dc87a-201">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="dc87a-202">**Зинк воздуха** (7)</span><span class="sxs-lookup"><span data-stu-id="dc87a-202">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="dc87a-203">**Литий-Polymer** (8)</span><span class="sxs-lookup"><span data-stu-id="dc87a-203">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc87a-204">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="dc87a-204">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-205">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc87a-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-207">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dc87a-207">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-208">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="dc87a-208">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="dc87a-209">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-209">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="dc87a-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="dc87a-211"> (0)</span><span class="sxs-lookup"><span data-stu-id="dc87a-211">(0)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-212">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="dc87a-212">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="dc87a-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="dc87a-214">(1)</span><span class="sxs-lookup"><span data-stu-id="dc87a-214">(1)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-215">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="dc87a-215">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dc87a-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="dc87a-217">(2)</span><span class="sxs-lookup"><span data-stu-id="dc87a-217">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="dc87a-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="dc87a-219">(3)</span><span class="sxs-lookup"><span data-stu-id="dc87a-219">(3)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-220">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc87a-220">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dc87a-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="dc87a-222">(4)</span><span class="sxs-lookup"><span data-stu-id="dc87a-222">(4)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-223">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="dc87a-223">Device is not working properly.</span></span> <span data-ttu-id="dc87a-224">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="dc87a-224">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="dc87a-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="dc87a-226">(5)</span><span class="sxs-lookup"><span data-stu-id="dc87a-226">(5)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-227">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="dc87a-227">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="dc87a-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="dc87a-229"> (6)</span><span class="sxs-lookup"><span data-stu-id="dc87a-229">(6)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-230">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="dc87a-230">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="dc87a-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="dc87a-232">(7)</span><span class="sxs-lookup"><span data-stu-id="dc87a-232">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="dc87a-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="dc87a-234">(8)</span><span class="sxs-lookup"><span data-stu-id="dc87a-234">(8)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-235">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="dc87a-235">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="dc87a-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="dc87a-237">(9)</span><span class="sxs-lookup"><span data-stu-id="dc87a-237">(9)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-238">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="dc87a-238">Device is not working properly.</span></span> <span data-ttu-id="dc87a-239">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="dc87a-239">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="dc87a-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="dc87a-241">(10)</span><span class="sxs-lookup"><span data-stu-id="dc87a-241">(10)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-242">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="dc87a-242">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="dc87a-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="dc87a-244">(11)</span><span class="sxs-lookup"><span data-stu-id="dc87a-244">(11)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-245">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="dc87a-245">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="dc87a-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="dc87a-247">(12)</span><span class="sxs-lookup"><span data-stu-id="dc87a-247">(12)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-248">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="dc87a-248">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="dc87a-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="dc87a-250">(13)</span><span class="sxs-lookup"><span data-stu-id="dc87a-250">(13)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-251">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="dc87a-251">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="dc87a-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="dc87a-253">(14)</span><span class="sxs-lookup"><span data-stu-id="dc87a-253">(14)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-254">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="dc87a-254">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="dc87a-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="dc87a-256">(15)</span><span class="sxs-lookup"><span data-stu-id="dc87a-256">(15)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-257">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="dc87a-257">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="dc87a-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="dc87a-259">(16)</span><span class="sxs-lookup"><span data-stu-id="dc87a-259">(16)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-260">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="dc87a-260">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="dc87a-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="dc87a-262">(17)</span><span class="sxs-lookup"><span data-stu-id="dc87a-262">(17)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-263">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="dc87a-263">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dc87a-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="dc87a-265">(18)</span><span class="sxs-lookup"><span data-stu-id="dc87a-265">(18)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-266">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="dc87a-266">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="dc87a-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="dc87a-268">(19)</span><span class="sxs-lookup"><span data-stu-id="dc87a-268">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dc87a-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="dc87a-270">(20)</span><span class="sxs-lookup"><span data-stu-id="dc87a-270">(20)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-271">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="dc87a-271">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="dc87a-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="dc87a-273">(21)</span><span class="sxs-lookup"><span data-stu-id="dc87a-273">(21)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-274">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="dc87a-274">System failure.</span></span> <span data-ttu-id="dc87a-275">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="dc87a-275">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="dc87a-276">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="dc87a-276">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="dc87a-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="dc87a-278">(22)</span><span class="sxs-lookup"><span data-stu-id="dc87a-278">(22)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-279">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="dc87a-279">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="dc87a-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="dc87a-281">(23)</span><span class="sxs-lookup"><span data-stu-id="dc87a-281">(23)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-282">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="dc87a-282">System failure.</span></span> <span data-ttu-id="dc87a-283">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="dc87a-283">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="dc87a-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="dc87a-285">(24)</span><span class="sxs-lookup"><span data-stu-id="dc87a-285">(24)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-286">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="dc87a-286">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dc87a-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dc87a-288">(25)</span><span class="sxs-lookup"><span data-stu-id="dc87a-288">(25)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-289">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="dc87a-289">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dc87a-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dc87a-291">(26)</span><span class="sxs-lookup"><span data-stu-id="dc87a-291">(26)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-292">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="dc87a-292">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="dc87a-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="dc87a-294">(27)</span><span class="sxs-lookup"><span data-stu-id="dc87a-294">(27)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-295">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="dc87a-295">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="dc87a-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="dc87a-297">(28)</span><span class="sxs-lookup"><span data-stu-id="dc87a-297">(28)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-298">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="dc87a-298">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="dc87a-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="dc87a-300">(29)</span><span class="sxs-lookup"><span data-stu-id="dc87a-300">(29)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-301">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="dc87a-301">Device is disabled.</span></span> <span data-ttu-id="dc87a-302">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="dc87a-302">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="dc87a-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="dc87a-304">(30)</span><span class="sxs-lookup"><span data-stu-id="dc87a-304">(30)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-305">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="dc87a-305">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dc87a-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dc87a-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="dc87a-307">1-31</span><span class="sxs-lookup"><span data-stu-id="dc87a-307">(31)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-308">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="dc87a-308">Device is not working properly.</span></span> <span data-ttu-id="dc87a-309">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="dc87a-309">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc87a-310">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="dc87a-310">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-311">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dc87a-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-313">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dc87a-313">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-314">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="dc87a-314">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="dc87a-315">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-316">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dc87a-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-319">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dc87a-319">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-320">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dc87a-320">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="dc87a-321">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="dc87a-321">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dc87a-322">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-323">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dc87a-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-326">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="dc87a-326">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-327">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dc87a-327">Description of the object.</span></span>

<span data-ttu-id="dc87a-328">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-329">**десигнкапаЦити**</span><span class="sxs-lookup"><span data-stu-id="dc87a-329">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-330">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc87a-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-332">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Портативная батарея DMTF \| 002,8 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" диаграмме милливаттах-hours ")</span><span class="sxs-lookup"><span data-stu-id="dc87a-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-333">Разработайте емкость аккумулятора в диаграмме милливаттах-hours.</span><span class="sxs-lookup"><span data-stu-id="dc87a-333">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="dc87a-334">Если это свойство не поддерживается, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="dc87a-334">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="dc87a-335">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-335">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-336">**десигнволтаже**</span><span class="sxs-lookup"><span data-stu-id="dc87a-336">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-337">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc87a-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-339">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Переносная батарея DMTF \| 002,9 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="dc87a-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-340">Проектирование напряжения батареи в милливольтах.</span><span class="sxs-lookup"><span data-stu-id="dc87a-340">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="dc87a-341">Если этот атрибут не поддерживается, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="dc87a-341">If this attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="dc87a-342">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-342">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="dc87a-343">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-343">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-344">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dc87a-344">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-345">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-347">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dc87a-347">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-348">Идентификатор аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="dc87a-348">Battery identifier.</span></span>

<span data-ttu-id="dc87a-349">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="dc87a-350">Пример: "Внутренняя батарея"</span><span class="sxs-lookup"><span data-stu-id="dc87a-350">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-351">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="dc87a-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-352">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dc87a-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-354">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="dc87a-354">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="dc87a-355">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dc87a-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-357">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-359">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="dc87a-359">More information about the error recorded in **LastErrorCode**, and any corrective actions that may be taken.</span></span>

<span data-ttu-id="dc87a-360">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-361">**естиматедчаржеремаининг**</span><span class="sxs-lookup"><span data-stu-id="dc87a-361">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-362">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc87a-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-364">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("процент")</span><span class="sxs-lookup"><span data-stu-id="dc87a-364">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-365">Оценка оставшегося процента от полной зарядки.</span><span class="sxs-lookup"><span data-stu-id="dc87a-365">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="dc87a-366">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-366">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-367">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="dc87a-367">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-368">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc87a-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-370">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Портативная батарея DMTF \| 002,15 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" минуты ")</span><span class="sxs-lookup"><span data-stu-id="dc87a-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-371">Оцените в минутах время, в течение которого заряд батареи заряжается при условиях текущей нагрузки, если работа программы отключена или потеряна и не работает, или ноутбук отключен от источника питания.</span><span class="sxs-lookup"><span data-stu-id="dc87a-371">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="dc87a-372">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-372">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-373">**експектедбаттерилифе**</span><span class="sxs-lookup"><span data-stu-id="dc87a-373">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-374">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc87a-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-376">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dc87a-376">Not supported.</span></span>

<span data-ttu-id="dc87a-377">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-378">**експектедлифе**</span><span class="sxs-lookup"><span data-stu-id="dc87a-378">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-379">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc87a-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-381">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="dc87a-381">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-382">Ожидаемое время существования аккумулятора в минутах, предполагая, что батарея полностью заряжена.</span><span class="sxs-lookup"><span data-stu-id="dc87a-382">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="dc87a-383">Это свойство представляет общий ожидаемый срок работы батареи, а не текущий оставшийся срок, который указывается свойством **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="dc87a-383">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="dc87a-384">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-384">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-385">**фуллчаржекапаЦити**</span><span class="sxs-lookup"><span data-stu-id="dc87a-385">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-386">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc87a-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-388">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Портативная батарея DMTF \| 002,11 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" диаграмме милливаттах-hours ")</span><span class="sxs-lookup"><span data-stu-id="dc87a-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-389">Полная плата за батарею в диаграмме милливаттах-часах.</span><span class="sxs-lookup"><span data-stu-id="dc87a-389">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="dc87a-390">Сравнение этого значения со свойством **десигнкапаЦити** определяет, когда батарея требует замены.</span><span class="sxs-lookup"><span data-stu-id="dc87a-390">Comparison of this value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="dc87a-391">Окончание работы батареи обычно происходит, когда свойство **фуллчаржекапаЦити** становится менее 80% от свойства **десигнкапаЦити** .</span><span class="sxs-lookup"><span data-stu-id="dc87a-391">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="dc87a-392">Если это свойство не поддерживается, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="dc87a-392">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="dc87a-393">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-393">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-394">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dc87a-394">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-395">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dc87a-395">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-397">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="dc87a-397">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-398">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="dc87a-398">Date and time the object was installed.</span></span> <span data-ttu-id="dc87a-399">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="dc87a-399">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dc87a-400">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-400">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-401">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="dc87a-401">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-402">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc87a-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-404">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="dc87a-404">Last error code reported by the logical device.</span></span>

<span data-ttu-id="dc87a-405">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-406">**Расположение**</span><span class="sxs-lookup"><span data-stu-id="dc87a-406">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-407">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-409">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 22 \| Location")</span><span class="sxs-lookup"><span data-stu-id="dc87a-409">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-410">Физическое расположение аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="dc87a-410">Physical location of the battery.</span></span> <span data-ttu-id="dc87a-411">Это свойство заполняется изготовителем компьютера.</span><span class="sxs-lookup"><span data-stu-id="dc87a-411">This property is filled by the computer manufacturer.</span></span>

<span data-ttu-id="dc87a-412">Пример: "на задней панели слева"</span><span class="sxs-lookup"><span data-stu-id="dc87a-412">Example: "In the back, on the left"</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-413">**мануфактуредате**</span><span class="sxs-lookup"><span data-stu-id="dc87a-413">**ManufactureDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-414">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-416">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 22 \| Дата изготовления")</span><span class="sxs-lookup"><span data-stu-id="dc87a-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacture Date")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-417">Дата изготовления аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="dc87a-417">Date when the battery was manufactured.</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-418">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="dc87a-418">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-419">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-420">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-421">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 22 \| Manufacturer")</span><span class="sxs-lookup"><span data-stu-id="dc87a-421">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-422">Производитель батареи.</span><span class="sxs-lookup"><span data-stu-id="dc87a-422">Manufacturer of the battery.</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-423">**максбаттереррор**</span><span class="sxs-lookup"><span data-stu-id="dc87a-423">**MaxBatteryError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-424">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc87a-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-426">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 22 \| Максимальная ошибка в данных аккумулятора"), [**единиц**](../wmisdk/standard-qualifiers.md) ("процент")</span><span class="sxs-lookup"><span data-stu-id="dc87a-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Maximum Error in Battery Data"), [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-427">Разница между самым высоким приблизительным объемом энергии в батарее и текущим значением, полученным от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="dc87a-427">Difference between the highest estimated amount of energy left in the battery and the current amount reported by the battery.</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-428">**максречаржетиме**</span><span class="sxs-lookup"><span data-stu-id="dc87a-428">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-429">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc87a-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-431">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="dc87a-431">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-432">Максимальное время (в минутах) для полной зарядки аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="dc87a-432">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="dc87a-433">Это свойство представляет время, которое будет выплатить полностью исчерпанный аккумулятор, а не текущее оставшееся время, которое указывается в свойстве **тиметофуллчарже** .</span><span class="sxs-lookup"><span data-stu-id="dc87a-433">This property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="dc87a-434">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-434">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-435">**Name**</span><span class="sxs-lookup"><span data-stu-id="dc87a-435">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-436">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-438">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="dc87a-438">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-439">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="dc87a-439">Label by which the object is known.</span></span> <span data-ttu-id="dc87a-440">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="dc87a-440">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="dc87a-441">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="dc87a-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-443">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-445">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dc87a-445">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-446">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dc87a-446">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="dc87a-447">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="dc87a-448">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="dc87a-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-449">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="dc87a-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-450">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dc87a-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-452">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="dc87a-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="dc87a-453">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc87a-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dc87a-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="dc87a-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="dc87a-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dc87a-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="dc87a-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dc87a-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="dc87a-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-458">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="dc87a-458">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="dc87a-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="dc87a-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-460">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="dc87a-460">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="dc87a-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="dc87a-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-462">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="dc87a-462">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="dc87a-463">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="dc87a-463">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="dc87a-464">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-464">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="dc87a-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="dc87a-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-466">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="dc87a-466">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="dc87a-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="dc87a-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dc87a-468">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="dc87a-468">Timed Power-On Supported</span></span>

<span data-ttu-id="dc87a-469">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="dc87a-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc87a-470">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="dc87a-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-471">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dc87a-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-473">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="dc87a-473">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="dc87a-474">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="dc87a-474">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="dc87a-475">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-476">**смартбаттериверсион**</span><span class="sxs-lookup"><span data-stu-id="dc87a-476">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-477">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-478">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-479">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. \|Портативная батарея DMTF \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="dc87a-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-480">Номер версии спецификации данных со смарт-батареей, поддерживаемый этим аккумулятором.</span><span class="sxs-lookup"><span data-stu-id="dc87a-480">Smart Battery Data Specification version number supported by this battery.</span></span> <span data-ttu-id="dc87a-481">Если батарея не поддерживает эту функцию, значение должно остаться пустым.</span><span class="sxs-lookup"><span data-stu-id="dc87a-481">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="dc87a-482">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-482">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-483">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="dc87a-483">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-484">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-485">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-486">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="dc87a-486">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-487">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="dc87a-487">Current status of the object.</span></span> <span data-ttu-id="dc87a-488">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="dc87a-488">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="dc87a-489">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="dc87a-489">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="dc87a-490">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="dc87a-490">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dc87a-491">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="dc87a-491">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dc87a-492">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="dc87a-492">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dc87a-493">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-493">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dc87a-494">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="dc87a-494">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dc87a-495">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="dc87a-495">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dc87a-496">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="dc87a-496">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dc87a-497">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="dc87a-497">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc87a-498">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="dc87a-498">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dc87a-499">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="dc87a-499">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dc87a-500">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="dc87a-500">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dc87a-501">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="dc87a-501">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dc87a-502">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="dc87a-502">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dc87a-503">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="dc87a-503">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dc87a-504">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="dc87a-504">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dc87a-505">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="dc87a-505">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dc87a-506">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="dc87a-506">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc87a-507">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dc87a-507">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-508">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc87a-508">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-509">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-510">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="dc87a-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-511">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dc87a-511">State of the logical device.</span></span> <span data-ttu-id="dc87a-512">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="dc87a-512">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="dc87a-513">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-513">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc87a-514">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dc87a-514">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc87a-515">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dc87a-515">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dc87a-516">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="dc87a-516">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dc87a-517">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="dc87a-517">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dc87a-518">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="dc87a-518">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc87a-519">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="dc87a-519">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-520">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-521">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-522">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dc87a-522">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-523">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="dc87a-523">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="dc87a-524">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-525">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dc87a-525">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-526">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc87a-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-527">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-528">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dc87a-528">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-529">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="dc87a-529">Name of the scoping system.</span></span>

<span data-ttu-id="dc87a-530">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dc87a-530">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-531">**тимеонбаттери**</span><span class="sxs-lookup"><span data-stu-id="dc87a-531">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-532">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc87a-532">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-533">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-533">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-534">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("секунды")</span><span class="sxs-lookup"><span data-stu-id="dc87a-534">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-535">Время в секундах, прошедшее с момента последнего переключения ИБП компьютера на питание от аккумулятора или с момента последнего перезапуска системы или ИБП, в зависимости от того, какое значение меньше.</span><span class="sxs-lookup"><span data-stu-id="dc87a-535">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="dc87a-536">Если батарея находится в оперативном режиме, возвращается значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="dc87a-536">If the battery is online, 0 (zero) is returned.</span></span>

<span data-ttu-id="dc87a-537">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-537">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc87a-538">**тиметофуллчарже**</span><span class="sxs-lookup"><span data-stu-id="dc87a-538">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc87a-539">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc87a-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-540">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc87a-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc87a-541">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Портативная батарея DMTF \| 002,16 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" минуты ")</span><span class="sxs-lookup"><span data-stu-id="dc87a-541">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="dc87a-542">Оставшееся время в минутах для полной оплаты батареи по текущей ставке и использованию.</span><span class="sxs-lookup"><span data-stu-id="dc87a-542">Remaining time in minutes to charge the battery fully at the current charge rate and usage.</span></span>

<span data-ttu-id="dc87a-543">Это свойство наследуется [**от \_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-543">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc87a-544">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc87a-544">Remarks</span></span>

<span data-ttu-id="dc87a-545">Класс **Win32 \_ портаблебаттери** является производным от [**\_ аккумулятора CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="dc87a-545">The **Win32\_PortableBattery** class is derived from [**CIM\_Battery**](cim-battery.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc87a-546">Требования</span><span class="sxs-lookup"><span data-stu-id="dc87a-546">Requirements</span></span>



| <span data-ttu-id="dc87a-547">Требование</span><span class="sxs-lookup"><span data-stu-id="dc87a-547">Requirement</span></span> | <span data-ttu-id="dc87a-548">Значение</span><span class="sxs-lookup"><span data-stu-id="dc87a-548">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc87a-549">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc87a-549">Minimum supported client</span></span><br/> | <span data-ttu-id="dc87a-550">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc87a-550">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc87a-551">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc87a-551">Minimum supported server</span></span><br/> | <span data-ttu-id="dc87a-552">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc87a-552">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc87a-553">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dc87a-553">Namespace</span></span><br/>                | <span data-ttu-id="dc87a-554">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dc87a-554">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc87a-555">MOF</span><span class="sxs-lookup"><span data-stu-id="dc87a-555">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc87a-556"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc87a-556"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc87a-557">DLL</span><span class="sxs-lookup"><span data-stu-id="dc87a-557">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc87a-558"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc87a-558"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc87a-559">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc87a-559">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc87a-560">**\_Аккумулятор CIM**</span><span class="sxs-lookup"><span data-stu-id="dc87a-560">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="dc87a-561">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="dc87a-561">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
