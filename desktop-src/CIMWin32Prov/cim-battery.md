---
description: '\_Класс батареи CIM представляет возможности и управление логическим устройством с батареей. Этот класс применяется к батареям в ноутбуках и других внутренних и внешних батареях.'
ms.assetid: af127b7a-021b-4cd8-af1b-176aff760858
ms.tgt_platform: multiple
title: Класс CIM_Battery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Battery
- CIM_Battery.Caption
- CIM_Battery.Description
- CIM_Battery.InstallDate
- CIM_Battery.Name
- CIM_Battery.Status
- CIM_Battery.Availability
- CIM_Battery.ConfigManagerErrorCode
- CIM_Battery.ConfigManagerUserConfig
- CIM_Battery.CreationClassName
- CIM_Battery.DeviceID
- CIM_Battery.PowerManagementCapabilities
- CIM_Battery.ErrorCleared
- CIM_Battery.ErrorDescription
- CIM_Battery.LastErrorCode
- CIM_Battery.PNPDeviceID
- CIM_Battery.PowerManagementSupported
- CIM_Battery.StatusInfo
- CIM_Battery.SystemCreationClassName
- CIM_Battery.SystemName
- CIM_Battery.BatteryStatus
- CIM_Battery.Chemistry
- CIM_Battery.DesignCapacity
- CIM_Battery.DesignVoltage
- CIM_Battery.EstimatedChargeRemaining
- CIM_Battery.EstimatedRunTime
- CIM_Battery.ExpectedLife
- CIM_Battery.FullChargeCapacity
- CIM_Battery.MaxRechargeTime
- CIM_Battery.SmartBatteryVersion
- CIM_Battery.TimeOnBattery
- CIM_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3719b2700c69cfa58921bed1242aa8a6de158466
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655968"
---
# <a name="cim_battery-class"></a><span data-ttu-id="b36f5-104">\_Класс аккумулятора CIM</span><span class="sxs-lookup"><span data-stu-id="b36f5-104">CIM\_Battery class</span></span>

<span data-ttu-id="b36f5-105">Класс **\_ батареи CIM** представляет возможности и управление логическим устройством с батареей.</span><span class="sxs-lookup"><span data-stu-id="b36f5-105">The **CIM\_Battery** class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="b36f5-106">Этот класс применяется к батареям в ноутбуках и других внутренних и внешних батареях.</span><span class="sxs-lookup"><span data-stu-id="b36f5-106">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b36f5-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b36f5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b36f5-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b36f5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b36f5-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b36f5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b36f5-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b36f5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b36f5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b36f5-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C548-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Battery : CIM_LogicalDevice
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   BatteryStatus;
  uint16   Chemistry;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  uint32   MaxRechargeTime;
  string   SmartBatteryVersion;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="b36f5-112">Члены</span><span class="sxs-lookup"><span data-stu-id="b36f5-112">Members</span></span>

<span data-ttu-id="b36f5-113">Класс **\_ батареи CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b36f5-113">The **CIM\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="b36f5-114">Методы</span><span class="sxs-lookup"><span data-stu-id="b36f5-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b36f5-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="b36f5-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b36f5-116">Методы</span><span class="sxs-lookup"><span data-stu-id="b36f5-116">Methods</span></span>

<span data-ttu-id="b36f5-117">Класс **\_ батареи CIM** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b36f5-117">The **CIM\_Battery** class has these methods.</span></span>



| <span data-ttu-id="b36f5-118">Метод</span><span class="sxs-lookup"><span data-stu-id="b36f5-118">Method</span></span>                                                             | <span data-ttu-id="b36f5-119">Описание</span><span class="sxs-lookup"><span data-stu-id="b36f5-119">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b36f5-120">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="b36f5-120">**Reset**</span></span>](reset-method-in-class-cim-battery.md)                 | <span data-ttu-id="b36f5-121">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b36f5-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="b36f5-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b36f5-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="b36f5-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b36f5-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-battery.md) | <span data-ttu-id="b36f5-124">Определяет требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="b36f5-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="b36f5-125">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b36f5-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b36f5-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="b36f5-126">Properties</span></span>

<span data-ttu-id="b36f5-127">Класс **\_ батареи CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b36f5-127">The **CIM\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b36f5-128">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="b36f5-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b36f5-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-131">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="b36f5-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-132">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="b36f5-132">Availability and status of the device.</span></span>

<span data-ttu-id="b36f5-133">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b36f5-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b36f5-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b36f5-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b36f5-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b36f5-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="b36f5-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b36f5-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="b36f5-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b36f5-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="b36f5-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b36f5-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="b36f5-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b36f5-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="b36f5-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b36f5-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="b36f5-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b36f5-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="b36f5-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b36f5-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="b36f5-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b36f5-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="b36f5-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b36f5-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="b36f5-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b36f5-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="b36f5-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-147">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b36f5-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b36f5-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="b36f5-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-149">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="b36f5-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b36f5-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="b36f5-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-151">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="b36f5-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b36f5-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="b36f5-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b36f5-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="b36f5-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-154">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b36f5-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b36f5-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="b36f5-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-156">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="b36f5-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b36f5-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="b36f5-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-158">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="b36f5-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b36f5-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="b36f5-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-160">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="b36f5-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b36f5-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="b36f5-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-162">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="b36f5-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b36f5-163">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="b36f5-163">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-164">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b36f5-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-166">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="b36f5-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-167">Описание состояния зарядки аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="b36f5-167">Description of the battery's charge status.</span></span> <span data-ttu-id="b36f5-168">Значение 10 недопустимо в схеме CIM, которая представляет отсутствие батареи, установленной в интерфейсе управления рабочим столом (DMI).</span><span class="sxs-lookup"><span data-stu-id="b36f5-168">The value 10 is not valid in the CIM schema, which represents no battery being installed in Desktop Management Interface (DMI).</span></span> <span data-ttu-id="b36f5-169">В этом случае не следует создавать экземпляры объекта.</span><span class="sxs-lookup"><span data-stu-id="b36f5-169">In this case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b36f5-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b36f5-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-171">Другое</span><span class="sxs-lookup"><span data-stu-id="b36f5-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b36f5-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b36f5-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-173">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b36f5-173">Unknown.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="b36f5-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Полностью заряжена** (3)</span><span class="sxs-lookup"><span data-stu-id="b36f5-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-175">Полностью заряжена.</span><span class="sxs-lookup"><span data-stu-id="b36f5-175">Fully charged.</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="b36f5-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Низкий** (4)</span><span class="sxs-lookup"><span data-stu-id="b36f5-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-177">Низкий.</span><span class="sxs-lookup"><span data-stu-id="b36f5-177">Low.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="b36f5-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (5)</span><span class="sxs-lookup"><span data-stu-id="b36f5-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-179">Критическое —</span><span class="sxs-lookup"><span data-stu-id="b36f5-179">Critical.</span></span>

</dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="b36f5-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Зарядка** (6)</span><span class="sxs-lookup"><span data-stu-id="b36f5-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-181">Списание.</span><span class="sxs-lookup"><span data-stu-id="b36f5-181">Charging.</span></span>

</dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="b36f5-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Зарядка и высокая** (7)</span><span class="sxs-lookup"><span data-stu-id="b36f5-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-183">Зарядка и высокая.</span><span class="sxs-lookup"><span data-stu-id="b36f5-183">Charging and high.</span></span>

</dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="b36f5-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Зарядка и низкая** (8)</span><span class="sxs-lookup"><span data-stu-id="b36f5-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-185">Зарядка и низкая.</span><span class="sxs-lookup"><span data-stu-id="b36f5-185">Charging and low.</span></span>

</dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="b36f5-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Зарядка и критическая** ошибка (9)</span><span class="sxs-lookup"><span data-stu-id="b36f5-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-187">Зарядка и критическая ошибка.</span><span class="sxs-lookup"><span data-stu-id="b36f5-187">Charging and critical.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="b36f5-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Не **определено** (10)</span><span class="sxs-lookup"><span data-stu-id="b36f5-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-189">Не определено.</span><span class="sxs-lookup"><span data-stu-id="b36f5-189">Undefined.</span></span>

</dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="b36f5-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Частично заряжена** (11)</span><span class="sxs-lookup"><span data-stu-id="b36f5-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-191">Частичное выставление счетов.</span><span class="sxs-lookup"><span data-stu-id="b36f5-191">Partially charged.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b36f5-192">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b36f5-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b36f5-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-195">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b36f5-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-196">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b36f5-196">A short textual description of the object.</span></span>

<span data-ttu-id="b36f5-197">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b36f5-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-198">**Химия**</span><span class="sxs-lookup"><span data-stu-id="b36f5-198">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-199">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b36f5-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-201">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="b36f5-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-202">Перечисление, описывающее химия батареи.</span><span class="sxs-lookup"><span data-stu-id="b36f5-202">Enumeration that describes the battery's chemistry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b36f5-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b36f5-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-204">Другое</span><span class="sxs-lookup"><span data-stu-id="b36f5-204">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b36f5-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b36f5-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-206">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b36f5-206">Unknown.</span></span>

</dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="b36f5-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Ведущий ACID** (3)</span><span class="sxs-lookup"><span data-stu-id="b36f5-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Lead Acid** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-208">Ведущий ACID.</span><span class="sxs-lookup"><span data-stu-id="b36f5-208">Lead acid.</span></span>

</dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="b36f5-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Никель кадмиум** (4)</span><span class="sxs-lookup"><span data-stu-id="b36f5-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Nickel Cadmium** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-210">Никель кадмиум.</span><span class="sxs-lookup"><span data-stu-id="b36f5-210">Nickel cadmium.</span></span>

</dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="b36f5-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Никель металла хидриде** (5)</span><span class="sxs-lookup"><span data-stu-id="b36f5-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Nickel Metal Hydride** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-212">Никель металла хидриде.</span><span class="sxs-lookup"><span data-stu-id="b36f5-212">Nickel metal hydride.</span></span>

</dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="b36f5-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Литий-ионный** (6)</span><span class="sxs-lookup"><span data-stu-id="b36f5-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Lithium-ion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-214">Литий — ионный.</span><span class="sxs-lookup"><span data-stu-id="b36f5-214">Lithium ion.</span></span>

</dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="b36f5-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Зинк воздуха** (7)</span><span class="sxs-lookup"><span data-stu-id="b36f5-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Zinc air** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-216">Зинк воздух.</span><span class="sxs-lookup"><span data-stu-id="b36f5-216">Zinc air.</span></span>

</dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="b36f5-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Литий-Polymer** (8)</span><span class="sxs-lookup"><span data-stu-id="b36f5-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Lithium Polymer** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-218">Литий Polymer.</span><span class="sxs-lookup"><span data-stu-id="b36f5-218">Lithium polymer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b36f5-219">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b36f5-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-220">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b36f5-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-222">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b36f5-222">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-223">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b36f5-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b36f5-224">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b36f5-225">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-225">**This device is working properly.**</span></span> <span data-ttu-id="b36f5-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="b36f5-226">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b36f5-227">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-227">**This device is not configured correctly.**</span></span> <span data-ttu-id="b36f5-228">(1)</span><span class="sxs-lookup"><span data-stu-id="b36f5-228">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b36f5-229">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-229">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b36f5-230">(2)</span><span class="sxs-lookup"><span data-stu-id="b36f5-230">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b36f5-231">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-231">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b36f5-232">(3)</span><span class="sxs-lookup"><span data-stu-id="b36f5-232">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b36f5-233">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-233">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b36f5-234">(4)</span><span class="sxs-lookup"><span data-stu-id="b36f5-234">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b36f5-235">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-235">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b36f5-236">(5)</span><span class="sxs-lookup"><span data-stu-id="b36f5-236">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b36f5-237">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-237">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b36f5-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="b36f5-238">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b36f5-239">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-239">**Cannot filter.**</span></span> <span data-ttu-id="b36f5-240">(7)</span><span class="sxs-lookup"><span data-stu-id="b36f5-240">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b36f5-241">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-241">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b36f5-242">(8)</span><span class="sxs-lookup"><span data-stu-id="b36f5-242">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b36f5-243">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-243">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b36f5-244">(9)</span><span class="sxs-lookup"><span data-stu-id="b36f5-244">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b36f5-245">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-245">**This device cannot start.**</span></span> <span data-ttu-id="b36f5-246">(10)</span><span class="sxs-lookup"><span data-stu-id="b36f5-246">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b36f5-247">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-247">**This device failed.**</span></span> <span data-ttu-id="b36f5-248">(11)</span><span class="sxs-lookup"><span data-stu-id="b36f5-248">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b36f5-249">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-249">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b36f5-250">(12)</span><span class="sxs-lookup"><span data-stu-id="b36f5-250">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b36f5-251">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-251">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b36f5-252">(13)</span><span class="sxs-lookup"><span data-stu-id="b36f5-252">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b36f5-253">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-253">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b36f5-254">(14)</span><span class="sxs-lookup"><span data-stu-id="b36f5-254">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b36f5-255">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-255">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b36f5-256">(15)</span><span class="sxs-lookup"><span data-stu-id="b36f5-256">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b36f5-257">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-257">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b36f5-258">(16)</span><span class="sxs-lookup"><span data-stu-id="b36f5-258">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b36f5-259">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-259">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b36f5-260">(17)</span><span class="sxs-lookup"><span data-stu-id="b36f5-260">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b36f5-261">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-261">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b36f5-262">(18)</span><span class="sxs-lookup"><span data-stu-id="b36f5-262">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b36f5-263">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-263">**Failure using the VxD loader.**</span></span> <span data-ttu-id="b36f5-264">(19)</span><span class="sxs-lookup"><span data-stu-id="b36f5-264">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b36f5-265">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-265">**Your registry might be corrupted.**</span></span> <span data-ttu-id="b36f5-266">(20)</span><span class="sxs-lookup"><span data-stu-id="b36f5-266">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b36f5-267">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-267">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b36f5-268">(21)</span><span class="sxs-lookup"><span data-stu-id="b36f5-268">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b36f5-269">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-269">**This device is disabled.**</span></span> <span data-ttu-id="b36f5-270">(22)</span><span class="sxs-lookup"><span data-stu-id="b36f5-270">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b36f5-271">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-271">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b36f5-272">(23)</span><span class="sxs-lookup"><span data-stu-id="b36f5-272">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b36f5-273">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-273">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b36f5-274">(24)</span><span class="sxs-lookup"><span data-stu-id="b36f5-274">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b36f5-275">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-275">**Windows is still setting up this device.**</span></span> <span data-ttu-id="b36f5-276">(25)</span><span class="sxs-lookup"><span data-stu-id="b36f5-276">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b36f5-277">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="b36f5-278">(26)</span><span class="sxs-lookup"><span data-stu-id="b36f5-278">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b36f5-279">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-279">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b36f5-280">(27)</span><span class="sxs-lookup"><span data-stu-id="b36f5-280">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b36f5-281">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-281">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b36f5-282">(28)</span><span class="sxs-lookup"><span data-stu-id="b36f5-282">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b36f5-283">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-283">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b36f5-284">(29)</span><span class="sxs-lookup"><span data-stu-id="b36f5-284">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b36f5-285">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-285">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b36f5-286">(30)</span><span class="sxs-lookup"><span data-stu-id="b36f5-286">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b36f5-287">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b36f5-287">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b36f5-288">1-31</span><span class="sxs-lookup"><span data-stu-id="b36f5-288">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b36f5-289">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="b36f5-289">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-290">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b36f5-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-292">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b36f5-292">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-293">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b36f5-293">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b36f5-294">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-295">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b36f5-295">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-296">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b36f5-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-298">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b36f5-298">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-299">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b36f5-299">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b36f5-300">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="b36f5-300">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b36f5-301">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-302">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b36f5-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b36f5-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-305">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="b36f5-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-306">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b36f5-306">A textual description of the object.</span></span>

<span data-ttu-id="b36f5-307">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b36f5-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-308">**десигнкапаЦити**</span><span class="sxs-lookup"><span data-stu-id="b36f5-308">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-309">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b36f5-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-311">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,8 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" диаграмме милливаттах-hours ")</span><span class="sxs-lookup"><span data-stu-id="b36f5-311">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-312">Емкость аккумулятора в диаграмме милливаттах-часах.</span><span class="sxs-lookup"><span data-stu-id="b36f5-312">Designed capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="b36f5-313">Если это свойство не поддерживается, введите 0.</span><span class="sxs-lookup"><span data-stu-id="b36f5-313">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-314">**десигнволтаже**</span><span class="sxs-lookup"><span data-stu-id="b36f5-314">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-315">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b36f5-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-317">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Переносная батарея DMTF \| 002,9 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" милливольтах ")</span><span class="sxs-lookup"><span data-stu-id="b36f5-317">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-318">Спроектированное напряжение батареи в милливольтах.</span><span class="sxs-lookup"><span data-stu-id="b36f5-318">Designed voltage of the battery in millivolts.</span></span> <span data-ttu-id="b36f5-319">Если этот атрибут не поддерживается, введите 0.</span><span class="sxs-lookup"><span data-stu-id="b36f5-319">If this attribute is not supported, enter 0.</span></span>

<span data-ttu-id="b36f5-320">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b36f5-320">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-321">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b36f5-321">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b36f5-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-324">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b36f5-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-325">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b36f5-325">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b36f5-326">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-327">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="b36f5-327">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-328">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b36f5-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-330">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="b36f5-330">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b36f5-331">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-332">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b36f5-332">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b36f5-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-335">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="b36f5-335">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b36f5-336">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-337">**естиматедчаржеремаининг**</span><span class="sxs-lookup"><span data-stu-id="b36f5-337">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-338">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b36f5-338">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-340">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("процент")</span><span class="sxs-lookup"><span data-stu-id="b36f5-340">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-341">Предполагаемый процент оставшегося полного платежа.</span><span class="sxs-lookup"><span data-stu-id="b36f5-341">Estimated percentage of the remaining full charge.</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-342">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="b36f5-342">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-343">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b36f5-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-345">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,15 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" минуты ")</span><span class="sxs-lookup"><span data-stu-id="b36f5-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-346">Предполагаемое время в минутах, пока заряд батареи не будет исчерпан в условиях текущей нагрузки, если выключена программа, будет утрачена и останется отключенной, или если ноутбук отключен от источника питания.</span><span class="sxs-lookup"><span data-stu-id="b36f5-346">Estimated time, in minutes, until the battery charge is depleted under the present load conditions if the utility power is off, is lost and remains off, or if a laptop is disconnected from a power source.</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-347">**експектедлифе**</span><span class="sxs-lookup"><span data-stu-id="b36f5-347">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-348">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b36f5-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-350">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="b36f5-350">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-351">Ожидаемое время работы батареи (в минутах), предполагая, что батарея полностью заряжена.</span><span class="sxs-lookup"><span data-stu-id="b36f5-351">Battery's expected lifetime, in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="b36f5-352">Это свойство представляет общий ожидаемый срок работы батареи, а не текущий оставшийся срок, который указывается свойством **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="b36f5-352">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-353">**фуллчаржекапаЦити**</span><span class="sxs-lookup"><span data-stu-id="b36f5-353">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-354">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b36f5-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-356">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" диаграмме милливаттах-hours ")</span><span class="sxs-lookup"><span data-stu-id="b36f5-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-357">Полная емкость батареи в диаграмме милливаттах-часах.</span><span class="sxs-lookup"><span data-stu-id="b36f5-357">The full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="b36f5-358">Сравните это значение со свойством **десигнкапаЦити** , чтобы определить, когда батарея требует замены.</span><span class="sxs-lookup"><span data-stu-id="b36f5-358">Compare this value to the **DesignCapacity** property to determine when the battery requires replacement.</span></span> <span data-ttu-id="b36f5-359">Окончание работы батареи обычно происходит, когда свойство **фуллчаржекапаЦити** становится менее 80% от свойства **десигнкапаЦити** .</span><span class="sxs-lookup"><span data-stu-id="b36f5-359">A battery's end-life is typically when the **FullChargeCapacity** property falls below 80 percent of the **DesignCapacity** property.</span></span> <span data-ttu-id="b36f5-360">Если это свойство не поддерживается, введите 0.</span><span class="sxs-lookup"><span data-stu-id="b36f5-360">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-361">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b36f5-361">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-362">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b36f5-362">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-364">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="b36f5-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-365">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="b36f5-365">Indicates when the object was installed.</span></span> <span data-ttu-id="b36f5-366">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="b36f5-366">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b36f5-367">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b36f5-367">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-368">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b36f5-368">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-369">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b36f5-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-371">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="b36f5-371">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b36f5-372">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-373">**максречаржетиме**</span><span class="sxs-lookup"><span data-stu-id="b36f5-373">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-374">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b36f5-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-376">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="b36f5-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-377">Максимальное время (в минутах) для полной зарядки аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="b36f5-377">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="b36f5-378">Это свойство представляет время, которое будет выставлять полностью исчерпанную батарею, а не текущее оставшееся время зарядки, которое указывается в свойстве **тиметофуллчарже** .</span><span class="sxs-lookup"><span data-stu-id="b36f5-378">This property represents the time to recharge a fully depleted battery, not the current remaining charging time, which is indicated in the **TimeToFullCharge** property.</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-379">**Name**</span><span class="sxs-lookup"><span data-stu-id="b36f5-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-380">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b36f5-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-382">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="b36f5-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-383">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="b36f5-383">Label by which the object is known.</span></span> <span data-ttu-id="b36f5-384">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="b36f5-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b36f5-385">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b36f5-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b36f5-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-387">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b36f5-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-389">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b36f5-389">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-390">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b36f5-390">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b36f5-391">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b36f5-391">Example: "\*PNP030b"</span></span>

<span data-ttu-id="b36f5-392">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-393">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="b36f5-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-394">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="b36f5-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-396">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="b36f5-396">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="b36f5-397">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b36f5-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b36f5-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-399">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="b36f5-399">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b36f5-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="b36f5-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-401">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="b36f5-401">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b36f5-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="b36f5-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-403">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="b36f5-403">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b36f5-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b36f5-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-405">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="b36f5-405">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b36f5-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="b36f5-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-407">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="b36f5-407">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b36f5-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="b36f5-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-409">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="b36f5-409">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="b36f5-410">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="b36f5-410">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="b36f5-411">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b36f5-411">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b36f5-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="b36f5-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-413">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="b36f5-413">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b36f5-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="b36f5-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b36f5-415">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="b36f5-415">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b36f5-416">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="b36f5-416">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-417">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b36f5-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-419">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b36f5-419">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b36f5-420">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b36f5-420">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b36f5-421">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b36f5-421">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b36f5-422">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b36f5-422">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b36f5-423">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-423">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-424">**смартбаттериверсион**</span><span class="sxs-lookup"><span data-stu-id="b36f5-424">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-425">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b36f5-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-426">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-426">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-427">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Портативная батарея DMTF \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="b36f5-427">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-428">Номер версии спецификации данных Smart аккумулятора, поддерживаемый этим аккумулятором.</span><span class="sxs-lookup"><span data-stu-id="b36f5-428">Smart battery data-specification version number that is supported by this battery.</span></span> <span data-ttu-id="b36f5-429">Если батарея не поддерживает эту функцию, значение должно остаться пустым.</span><span class="sxs-lookup"><span data-stu-id="b36f5-429">If the battery does not support this function, the value should be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-430">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b36f5-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-431">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b36f5-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-433">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="b36f5-433">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-434">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b36f5-434">String that indicates the current status of the object.</span></span> <span data-ttu-id="b36f5-435">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="b36f5-435">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b36f5-436">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="b36f5-436">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b36f5-437">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="b36f5-437">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b36f5-438">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="b36f5-438">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b36f5-439">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="b36f5-439">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b36f5-440">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="b36f5-440">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b36f5-441">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b36f5-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b36f5-442">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="b36f5-442">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b36f5-443">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="b36f5-443">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b36f5-444">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="b36f5-444">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b36f5-445">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="b36f5-445">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b36f5-446">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b36f5-446">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b36f5-447">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b36f5-447">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b36f5-448">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b36f5-448">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b36f5-449">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="b36f5-449">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b36f5-450">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="b36f5-450">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b36f5-451">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="b36f5-451">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b36f5-452">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="b36f5-452">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b36f5-453">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="b36f5-453">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b36f5-454">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="b36f5-454">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b36f5-455">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b36f5-455">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-456">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b36f5-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-457">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-458">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b36f5-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-459">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b36f5-459">State of the logical device.</span></span> <span data-ttu-id="b36f5-460">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="b36f5-460">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="b36f5-461">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b36f5-462">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b36f5-462">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b36f5-463">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b36f5-463">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b36f5-464">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b36f5-464">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b36f5-465">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="b36f5-465">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b36f5-466">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="b36f5-466">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b36f5-467">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="b36f5-467">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-468">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b36f5-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-469">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-470">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b36f5-470">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-471">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="b36f5-471">The scoping system's creation class name.</span></span>

<span data-ttu-id="b36f5-472">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b36f5-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-474">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b36f5-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-476">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b36f5-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-477">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="b36f5-477">The scoping system's name.</span></span>

<span data-ttu-id="b36f5-478">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b36f5-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-479">**тимеонбаттери**</span><span class="sxs-lookup"><span data-stu-id="b36f5-479">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-480">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b36f5-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-482">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("секунды")</span><span class="sxs-lookup"><span data-stu-id="b36f5-482">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-483">Время в секундах, прошедшее с момента последнего переключения ИБП компьютера на питание от аккумулятора или от времени последнего перезапуска системы или ИБП, в зависимости от того, какое значение меньше.</span><span class="sxs-lookup"><span data-stu-id="b36f5-483">Elapsed time, in seconds, since the computer system's UPS last switched to battery power, or the amount of time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="b36f5-484">Если батарея находится в оперативном режиме, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="b36f5-484">A value of 0 is returned if the battery is "online."</span></span>

</dd> <dt>

<span data-ttu-id="b36f5-485">**тиметофуллчарже**</span><span class="sxs-lookup"><span data-stu-id="b36f5-485">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b36f5-486">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b36f5-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b36f5-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b36f5-488">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Портативная батарея DMTF \| 002,16 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" минуты ")</span><span class="sxs-lookup"><span data-stu-id="b36f5-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="b36f5-489">Оставшееся время (в минутах), в течение которого батарея полностью заряжена на текущий коэффициент зарядки и используется.</span><span class="sxs-lookup"><span data-stu-id="b36f5-489">Remaining time, in minutes, to charge the battery fully at the current charging rate and use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b36f5-490">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b36f5-490">Remarks</span></span>

<span data-ttu-id="b36f5-491">Класс **\_ батареи CIM** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="b36f5-491">The **CIM\_Battery** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b36f5-492">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="b36f5-492">WMI does not implement this class.</span></span> <span data-ttu-id="b36f5-493">Дополнительные сведения о классах, производных от **\_ аккумулятора CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b36f5-493">For more information about classes derived from **CIM\_Battery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b36f5-494">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b36f5-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b36f5-495">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b36f5-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b36f5-496">Требования</span><span class="sxs-lookup"><span data-stu-id="b36f5-496">Requirements</span></span>



| <span data-ttu-id="b36f5-497">Требование</span><span class="sxs-lookup"><span data-stu-id="b36f5-497">Requirement</span></span> | <span data-ttu-id="b36f5-498">Значение</span><span class="sxs-lookup"><span data-stu-id="b36f5-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b36f5-499">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b36f5-499">Minimum supported client</span></span><br/> | <span data-ttu-id="b36f5-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b36f5-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b36f5-501">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b36f5-501">Minimum supported server</span></span><br/> | <span data-ttu-id="b36f5-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b36f5-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b36f5-503">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b36f5-503">Namespace</span></span><br/>                | <span data-ttu-id="b36f5-504">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b36f5-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b36f5-505">MOF</span><span class="sxs-lookup"><span data-stu-id="b36f5-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b36f5-506"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b36f5-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b36f5-507">DLL</span><span class="sxs-lookup"><span data-stu-id="b36f5-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b36f5-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b36f5-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b36f5-509">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b36f5-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b36f5-510">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="b36f5-510">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

