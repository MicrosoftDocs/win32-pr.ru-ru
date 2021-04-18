---
description: '\_Класс процессора CIM представляет возможности и управление логическим устройством процессора.'
ms.assetid: 7af3208f-f1d5-4911-b6ab-46b54eec0b69
ms.tgt_platform: multiple
title: Класс CIM_Processor (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Processor
- CIM_Processor.AddressWidth
- CIM_Processor.Availability
- CIM_Processor.Caption
- CIM_Processor.ConfigManagerErrorCode
- CIM_Processor.ConfigManagerUserConfig
- CIM_Processor.CreationClassName
- CIM_Processor.CurrentClockSpeed
- CIM_Processor.DataWidth
- CIM_Processor.Description
- CIM_Processor.DeviceID
- CIM_Processor.ErrorCleared
- CIM_Processor.ErrorDescription
- CIM_Processor.Family
- CIM_Processor.InstallDate
- CIM_Processor.LastErrorCode
- CIM_Processor.LoadPercentage
- CIM_Processor.MaxClockSpeed
- CIM_Processor.Name
- CIM_Processor.OtherFamilyDescription
- CIM_Processor.PNPDeviceID
- CIM_Processor.PowerManagementCapabilities
- CIM_Processor.PowerManagementSupported
- CIM_Processor.Role
- CIM_Processor.Status
- CIM_Processor.StatusInfo
- CIM_Processor.Stepping
- CIM_Processor.SystemCreationClassName
- CIM_Processor.SystemName
- CIM_Processor.UniqueId
- CIM_Processor.UpgradeMethod
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0120ce0327c21098b8c2950bd5dfa9a9fe2a709c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496002"
---
# <a name="cim_processor-class-cimwin32-wmi-providers"></a><span data-ttu-id="41deb-103">Класс CIM_Processor (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="41deb-103">CIM_Processor class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="41deb-104">Класс **\_ процессора CIM** представляет возможности и управление логическим устройством процессора.</span><span class="sxs-lookup"><span data-stu-id="41deb-104">The **CIM\_Processor** class represents the capabilities and management of the processor logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41deb-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="41deb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="41deb-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="41deb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="41deb-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="41deb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="41deb-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="41deb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="41deb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41deb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Processor : CIM_LogicalDevice
{
  uint16   AddressWidth;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Family;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint16   LoadPercentage;
  uint32   MaxClockSpeed;
  string   Name;
  string   OtherFamilyDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Role;
  string   Status;
  uint16   StatusInfo;
  string   Stepping;
  string   SystemCreationClassName;
  string   SystemName;
  string   UniqueId;
  uint16   UpgradeMethod;
};
```

## <a name="members"></a><span data-ttu-id="41deb-110">Члены</span><span class="sxs-lookup"><span data-stu-id="41deb-110">Members</span></span>

<span data-ttu-id="41deb-111">Класс **\_ процессора CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="41deb-111">The **CIM\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="41deb-112">Методы</span><span class="sxs-lookup"><span data-stu-id="41deb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="41deb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="41deb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="41deb-114">Методы</span><span class="sxs-lookup"><span data-stu-id="41deb-114">Methods</span></span>

<span data-ttu-id="41deb-115">Класс **\_ процессора CIM** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="41deb-115">The **CIM\_Processor** class has these methods.</span></span>



| <span data-ttu-id="41deb-116">Метод</span><span class="sxs-lookup"><span data-stu-id="41deb-116">Method</span></span>                                                               | <span data-ttu-id="41deb-117">Описание</span><span class="sxs-lookup"><span data-stu-id="41deb-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41deb-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="41deb-118">**Reset**</span></span>](reset-method-in-class-cim-processor.md)                 | <span data-ttu-id="41deb-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="41deb-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="41deb-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="41deb-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="41deb-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="41deb-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-processor.md) | <span data-ttu-id="41deb-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="41deb-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="41deb-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="41deb-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="41deb-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="41deb-124">Properties</span></span>

<span data-ttu-id="41deb-125">Класс **\_ процессора CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="41deb-125">The **CIM\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41deb-126">**аддрессвидс**</span><span class="sxs-lookup"><span data-stu-id="41deb-126">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41deb-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-129">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")</span><span class="sxs-lookup"><span data-stu-id="41deb-129">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-130">Ширина адреса процессора в битах.</span><span class="sxs-lookup"><span data-stu-id="41deb-130">Processor address width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="41deb-131">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="41deb-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-132">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41deb-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-134">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="41deb-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-135">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="41deb-135">Availability and status of the device.</span></span>

<span data-ttu-id="41deb-136">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="41deb-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="41deb-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41deb-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="41deb-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="41deb-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="41deb-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-140">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="41deb-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="41deb-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="41deb-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="41deb-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="41deb-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="41deb-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="41deb-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="41deb-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="41deb-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="41deb-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="41deb-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="41deb-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="41deb-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="41deb-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="41deb-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="41deb-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="41deb-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="41deb-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="41deb-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="41deb-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="41deb-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-151">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="41deb-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="41deb-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="41deb-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-153">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="41deb-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="41deb-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="41deb-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-155">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="41deb-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="41deb-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="41deb-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="41deb-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="41deb-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-158">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="41deb-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="41deb-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="41deb-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-160">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="41deb-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="41deb-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="41deb-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-162">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="41deb-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="41deb-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="41deb-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-164">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="41deb-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="41deb-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="41deb-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-166">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="41deb-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="41deb-167">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="41deb-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-170">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="41deb-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-171">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="41deb-171">Short textual description of the object.</span></span>

<span data-ttu-id="41deb-172">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41deb-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-173">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="41deb-173">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-174">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41deb-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-176">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="41deb-176">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-177">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="41deb-177">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="41deb-178">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-178">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="41deb-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="41deb-179"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="41deb-180"> (0)</span><span class="sxs-lookup"><span data-stu-id="41deb-180">(0)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-181">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="41deb-181">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="41deb-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="41deb-182"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="41deb-183">(1)</span><span class="sxs-lookup"><span data-stu-id="41deb-183">(1)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-184">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="41deb-184">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="41deb-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="41deb-185"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="41deb-186">(2)</span><span class="sxs-lookup"><span data-stu-id="41deb-186">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="41deb-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="41deb-187"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="41deb-188">(3)</span><span class="sxs-lookup"><span data-stu-id="41deb-188">(3)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-189">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41deb-189">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="41deb-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="41deb-190"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="41deb-191">(4)</span><span class="sxs-lookup"><span data-stu-id="41deb-191">(4)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-192">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="41deb-192">Device is not working properly.</span></span> <span data-ttu-id="41deb-193">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="41deb-193">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="41deb-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="41deb-194"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="41deb-195">(5)</span><span class="sxs-lookup"><span data-stu-id="41deb-195">(5)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-196">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="41deb-196">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="41deb-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="41deb-197"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="41deb-198"> (6)</span><span class="sxs-lookup"><span data-stu-id="41deb-198">(6)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-199">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="41deb-199">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="41deb-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="41deb-200"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="41deb-201">(7)</span><span class="sxs-lookup"><span data-stu-id="41deb-201">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="41deb-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="41deb-202"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="41deb-203">(8)</span><span class="sxs-lookup"><span data-stu-id="41deb-203">(8)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-204">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="41deb-204">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="41deb-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="41deb-205"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="41deb-206">(9)</span><span class="sxs-lookup"><span data-stu-id="41deb-206">(9)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-207">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="41deb-207">Device is not working properly.</span></span> <span data-ttu-id="41deb-208">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="41deb-208">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="41deb-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="41deb-209"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="41deb-210">(10)</span><span class="sxs-lookup"><span data-stu-id="41deb-210">(10)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-211">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="41deb-211">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="41deb-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="41deb-212"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="41deb-213">(11)</span><span class="sxs-lookup"><span data-stu-id="41deb-213">(11)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-214">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="41deb-214">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="41deb-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="41deb-215"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="41deb-216">(12)</span><span class="sxs-lookup"><span data-stu-id="41deb-216">(12)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-217">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="41deb-217">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="41deb-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="41deb-218"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="41deb-219">(13)</span><span class="sxs-lookup"><span data-stu-id="41deb-219">(13)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-220">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="41deb-220">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="41deb-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="41deb-221"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="41deb-222">(14)</span><span class="sxs-lookup"><span data-stu-id="41deb-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-223">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="41deb-223">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="41deb-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="41deb-224"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="41deb-225">(15)</span><span class="sxs-lookup"><span data-stu-id="41deb-225">(15)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-226">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="41deb-226">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="41deb-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="41deb-227"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="41deb-228">(16)</span><span class="sxs-lookup"><span data-stu-id="41deb-228">(16)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-229">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="41deb-229">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="41deb-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="41deb-230"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="41deb-231">(17)</span><span class="sxs-lookup"><span data-stu-id="41deb-231">(17)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-232">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="41deb-232">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="41deb-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="41deb-233"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="41deb-234">(18)</span><span class="sxs-lookup"><span data-stu-id="41deb-234">(18)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-235">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="41deb-235">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="41deb-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="41deb-236"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="41deb-237">(19)</span><span class="sxs-lookup"><span data-stu-id="41deb-237">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="41deb-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="41deb-238"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="41deb-239">(20)</span><span class="sxs-lookup"><span data-stu-id="41deb-239">(20)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-240">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="41deb-240">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="41deb-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="41deb-241"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="41deb-242">(21)</span><span class="sxs-lookup"><span data-stu-id="41deb-242">(21)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-243">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="41deb-243">System failure.</span></span> <span data-ttu-id="41deb-244">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="41deb-244">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="41deb-245">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="41deb-245">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="41deb-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="41deb-246"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="41deb-247">(22)</span><span class="sxs-lookup"><span data-stu-id="41deb-247">(22)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-248">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="41deb-248">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="41deb-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="41deb-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="41deb-250">(23)</span><span class="sxs-lookup"><span data-stu-id="41deb-250">(23)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-251">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="41deb-251">System failure.</span></span> <span data-ttu-id="41deb-252">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="41deb-252">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="41deb-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="41deb-253"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="41deb-254">(24)</span><span class="sxs-lookup"><span data-stu-id="41deb-254">(24)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-255">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="41deb-255">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="41deb-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="41deb-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="41deb-257">(25)</span><span class="sxs-lookup"><span data-stu-id="41deb-257">(25)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-258">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="41deb-258">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="41deb-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="41deb-259"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="41deb-260">(26)</span><span class="sxs-lookup"><span data-stu-id="41deb-260">(26)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-261">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="41deb-261">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="41deb-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="41deb-262"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="41deb-263">(27)</span><span class="sxs-lookup"><span data-stu-id="41deb-263">(27)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-264">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="41deb-264">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="41deb-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="41deb-265"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="41deb-266">(28)</span><span class="sxs-lookup"><span data-stu-id="41deb-266">(28)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-267">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="41deb-267">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="41deb-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="41deb-268"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="41deb-269">(29)</span><span class="sxs-lookup"><span data-stu-id="41deb-269">(29)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-270">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="41deb-270">Device is disabled.</span></span> <span data-ttu-id="41deb-271">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="41deb-271">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="41deb-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="41deb-272"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="41deb-273">(30)</span><span class="sxs-lookup"><span data-stu-id="41deb-273">(30)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-274">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="41deb-274">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="41deb-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="41deb-275"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="41deb-276">1-31</span><span class="sxs-lookup"><span data-stu-id="41deb-276">(31)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-277">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="41deb-277">Device is not working properly.</span></span> <span data-ttu-id="41deb-278">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="41deb-278">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="41deb-279">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="41deb-279">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-280">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="41deb-280">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-282">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="41deb-282">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-283">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="41deb-283">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="41deb-284">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-285">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="41deb-285">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-288">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="41deb-288">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="41deb-289">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="41deb-289">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="41deb-290">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="41deb-290">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="41deb-291">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-292">**куррентклоккспид**</span><span class="sxs-lookup"><span data-stu-id="41deb-292">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-293">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41deb-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-295">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF- \| процессор \| 006,6 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" мегагерц ")</span><span class="sxs-lookup"><span data-stu-id="41deb-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-296">Текущая скорость процессора (в мегагерцах).</span><span class="sxs-lookup"><span data-stu-id="41deb-296">Current speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="41deb-297">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="41deb-297">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-298">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41deb-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-300">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")</span><span class="sxs-lookup"><span data-stu-id="41deb-300">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-301">Ширина данных процессора в битах.</span><span class="sxs-lookup"><span data-stu-id="41deb-301">Processor data width, in bits.</span></span>

</dd> <dt>

<span data-ttu-id="41deb-302">**Описание**</span><span class="sxs-lookup"><span data-stu-id="41deb-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-305">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="41deb-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-306">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="41deb-306">Textual description of the object.</span></span>

<span data-ttu-id="41deb-307">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41deb-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="41deb-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-311">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="41deb-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="41deb-312">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="41deb-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="41deb-313">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-314">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="41deb-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-315">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="41deb-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41deb-317">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="41deb-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="41deb-318">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="41deb-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-320">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41deb-322">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="41deb-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="41deb-323">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-324">**Семейство**</span><span class="sxs-lookup"><span data-stu-id="41deb-324">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-325">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41deb-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-327">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -процессор 014,3 "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ процессор CIM**.**Осерфамилидескриптион**")</span><span class="sxs-lookup"><span data-stu-id="41deb-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|014.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**OtherFamilyDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-328">Тип семейства процессоров.</span><span class="sxs-lookup"><span data-stu-id="41deb-328">Processor family type.</span></span>

<span data-ttu-id="41deb-329">Это свойство наследуется **от \_ процессора CIM**.</span><span class="sxs-lookup"><span data-stu-id="41deb-329">This property is inherited from **CIM\_Processor**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="41deb-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="41deb-330"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41deb-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="41deb-331"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="8086"></span>

<span data-ttu-id="41deb-332"><span id="8086"></span>**8086** (3)</span><span class="sxs-lookup"><span data-stu-id="41deb-332"><span id="8086"></span>**8086** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="80286"></span>

<span data-ttu-id="41deb-333"><span id="80286"></span>**80286** (4)</span><span class="sxs-lookup"><span data-stu-id="41deb-333"><span id="80286"></span>**80286** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="80386"></span>

<span data-ttu-id="41deb-334"><span id="80386"></span>**80386** (5)</span><span class="sxs-lookup"><span data-stu-id="41deb-334"><span id="80386"></span>**80386** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="80486"></span>

<span data-ttu-id="41deb-335"><span id="80486"></span>**80486** (6)</span><span class="sxs-lookup"><span data-stu-id="41deb-335"><span id="80486"></span>**80486** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8087"></span>

<span data-ttu-id="41deb-336"><span id="8087"></span>**8087** (7)</span><span class="sxs-lookup"><span data-stu-id="41deb-336"><span id="8087"></span>**8087** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="80287"></span>

<span data-ttu-id="41deb-337"><span id="80287"></span>**80287** (8)</span><span class="sxs-lookup"><span data-stu-id="41deb-337"><span id="80287"></span>**80287** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="80387"></span>

<span data-ttu-id="41deb-338"><span id="80387"></span>**80387** (9)</span><span class="sxs-lookup"><span data-stu-id="41deb-338"><span id="80387"></span>**80387** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="80487"></span>

<span data-ttu-id="41deb-339"><span id="80487"></span>**80487** (10)</span><span class="sxs-lookup"><span data-stu-id="41deb-339"><span id="80487"></span>**80487** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>

<span data-ttu-id="41deb-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Торговая марка Pentium (R)** (11)</span><span class="sxs-lookup"><span data-stu-id="41deb-340"><span id="Pentium_R__brand"></span><span id="pentium_r__brand"></span><span id="PENTIUM_R__BRAND"></span>**Pentium(R) brand** (11)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-341">Торговая марка Pentium</span><span class="sxs-lookup"><span data-stu-id="41deb-341">Pentium brand</span></span>

</dd> <dt>

<span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>

<span data-ttu-id="41deb-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium (R) Pro** (12)</span><span class="sxs-lookup"><span data-stu-id="41deb-342"><span id="Pentium_R__Pro"></span><span id="pentium_r__pro"></span><span id="PENTIUM_R__PRO"></span>**Pentium(R) Pro** (12)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-343">Pentium Pro</span><span class="sxs-lookup"><span data-stu-id="41deb-343">Pentium Pro</span></span>

</dd> <dt>

<span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>

<span data-ttu-id="41deb-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium (R) II** (13)</span><span class="sxs-lookup"><span data-stu-id="41deb-344"><span id="Pentium_R__II"></span><span id="pentium_r__ii"></span><span id="PENTIUM_R__II"></span>**Pentium(R) II** (13)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-345">Pentium II</span><span class="sxs-lookup"><span data-stu-id="41deb-345">Pentium II</span></span>

</dd> <dt>

<span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>

<span data-ttu-id="41deb-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Процессор Pentium (R) с технологией MMX (TM** ) (14)</span><span class="sxs-lookup"><span data-stu-id="41deb-346"><span id="Pentium_R__processor_with_MMX_TM__technology"></span><span id="pentium_r__processor_with_mmx_tm__technology"></span><span id="PENTIUM_R__PROCESSOR_WITH_MMX_TM__TECHNOLOGY"></span>**Pentium(R) processor with MMX(TM) technology** (14)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-347">Процессор Pentium с технологией MMX</span><span class="sxs-lookup"><span data-stu-id="41deb-347">Pentium processor with MMX technology</span></span>

</dd> <dt>

<span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>

<span data-ttu-id="41deb-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron (TM)** (15)</span><span class="sxs-lookup"><span data-stu-id="41deb-348"><span id="Celeron_TM_"></span><span id="celeron_tm_"></span><span id="CELERON_TM_"></span>**Celeron(TM)** (15)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-349">Celeron</span><span class="sxs-lookup"><span data-stu-id="41deb-349">Celeron</span></span>

</dd> <dt>

<span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>

<span data-ttu-id="41deb-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r_:xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium (R) II Xeon (TM)** (16)</span><span class="sxs-lookup"><span data-stu-id="41deb-350"><span id="Pentium_R__II_Xeon_TM_"></span><span id="pentium_r__ii_xeon_tm_"></span><span id="PENTIUM_R__II_XEON_TM_"></span>**Pentium(R) II Xeon(TM)** (16)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-351">Pentium II Xeon</span><span class="sxs-lookup"><span data-stu-id="41deb-351">Pentium II Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>

<span data-ttu-id="41deb-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium (R) III** (17)</span><span class="sxs-lookup"><span data-stu-id="41deb-352"><span id="Pentium_R__III"></span><span id="pentium_r__iii"></span><span id="PENTIUM_R__III"></span>**Pentium(R) III** (17)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-353">Pentium III</span><span class="sxs-lookup"><span data-stu-id="41deb-353">Pentium III</span></span>

</dd> <dt>

<span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>

<span data-ttu-id="41deb-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**Семейство M1** (18)</span><span class="sxs-lookup"><span data-stu-id="41deb-354"><span id="M1_Family"></span><span id="m1_family"></span><span id="M1_FAMILY"></span>**M1 Family** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>

<span data-ttu-id="41deb-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**Семейство m2** (19)</span><span class="sxs-lookup"><span data-stu-id="41deb-355"><span id="M2_Family"></span><span id="m2_family"></span><span id="M2_FAMILY"></span>**M2 Family** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>

<span data-ttu-id="41deb-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**Семейство K5** (24)</span><span class="sxs-lookup"><span data-stu-id="41deb-356"><span id="K5_Family"></span><span id="k5_family"></span><span id="K5_FAMILY"></span>**K5 Family** (24)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-357">Семейство процессоров AMD Duron</span><span class="sxs-lookup"><span data-stu-id="41deb-357">AMD Duron  Processor Family</span></span>

</dd> <dt>

<span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>

<span data-ttu-id="41deb-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**Семейство K6** (25)</span><span class="sxs-lookup"><span data-stu-id="41deb-358"><span id="K6_Family"></span><span id="k6_family"></span><span id="K6_FAMILY"></span>**K6 Family** (25)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-359">Семейство K5</span><span class="sxs-lookup"><span data-stu-id="41deb-359">K5 Family</span></span>

</dd> <dt>

<span id="K6-2"></span><span id="k6-2"></span>

<span data-ttu-id="41deb-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)</span><span class="sxs-lookup"><span data-stu-id="41deb-360"><span id="K6-2"></span><span id="k6-2"></span>**K6-2** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="K6-3"></span><span id="k6-3"></span>

<span data-ttu-id="41deb-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)</span><span class="sxs-lookup"><span data-stu-id="41deb-361"><span id="K6-3"></span><span id="k6-3"></span>**K6-3** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>

<span data-ttu-id="41deb-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**Семейство процессоров AMD Athlon (TM)** (28)</span><span class="sxs-lookup"><span data-stu-id="41deb-362"><span id="AMD_Athlon_TM__Processor_Family"></span><span id="amd_athlon_tm__processor_family"></span><span id="AMD_ATHLON_TM__PROCESSOR_FAMILY"></span>**AMD Athlon(TM) Processor Family** (28)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-363">Семейство процессоров AMD Athlon</span><span class="sxs-lookup"><span data-stu-id="41deb-363">AMD Athlon Processor Family</span></span>

</dd> <dt>

<span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>

<span data-ttu-id="41deb-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**Процессор AMD (R) Duron (TM)** (29)</span><span class="sxs-lookup"><span data-stu-id="41deb-364"><span id="AMD_R__Duron_TM__Processor"></span><span id="amd_r__duron_tm__processor"></span><span id="AMD_R__DURON_TM__PROCESSOR"></span>**AMD(R) Duron(TM) Processor** (29)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-365">Процессор AMD Duron</span><span class="sxs-lookup"><span data-stu-id="41deb-365">AMD  Duron Processor</span></span>

</dd> <dt>

<span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>

<span data-ttu-id="41deb-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**Семейство AMD29000** (30)</span><span class="sxs-lookup"><span data-stu-id="41deb-366"><span id="AMD29000_Family"></span><span id="amd29000_family"></span><span id="AMD29000_FAMILY"></span>**AMD29000 Family** (30)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-367">Семейство AMD2900</span><span class="sxs-lookup"><span data-stu-id="41deb-367">AMD2900 Family</span></span>

</dd> <dt>

<span id="K6-2_"></span><span id="k6-2_"></span>

<span data-ttu-id="41deb-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2 +** (31)</span><span class="sxs-lookup"><span data-stu-id="41deb-368"><span id="K6-2_"></span><span id="k6-2_"></span>**K6-2+** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>

<span data-ttu-id="41deb-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Семейство Power PC** (32)</span><span class="sxs-lookup"><span data-stu-id="41deb-369"><span id="Power_PC_Family"></span><span id="power_pc_family"></span><span id="POWER_PC_FAMILY"></span>**Power PC Family** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>

<span data-ttu-id="41deb-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)</span><span class="sxs-lookup"><span data-stu-id="41deb-370"><span id="Power_PC_601"></span><span id="power_pc_601"></span><span id="POWER_PC_601"></span>**Power PC 601** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>

<span data-ttu-id="41deb-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)</span><span class="sxs-lookup"><span data-stu-id="41deb-371"><span id="Power_PC_603"></span><span id="power_pc_603"></span><span id="POWER_PC_603"></span>**Power PC 603** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>

<span data-ttu-id="41deb-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603 +** (35)</span><span class="sxs-lookup"><span data-stu-id="41deb-372"><span id="Power_PC_603_"></span><span id="power_pc_603_"></span><span id="POWER_PC_603_"></span>**Power PC 603+** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>

<span data-ttu-id="41deb-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)</span><span class="sxs-lookup"><span data-stu-id="41deb-373"><span id="Power_PC_604"></span><span id="power_pc_604"></span><span id="POWER_PC_604"></span>**Power PC 604** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>

<span data-ttu-id="41deb-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)</span><span class="sxs-lookup"><span data-stu-id="41deb-374"><span id="Power_PC_620"></span><span id="power_pc_620"></span><span id="POWER_PC_620"></span>**Power PC 620** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>

<span data-ttu-id="41deb-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**Power PC X704** (38)</span><span class="sxs-lookup"><span data-stu-id="41deb-375"><span id="Power_PC_X704"></span><span id="power_pc_x704"></span><span id="POWER_PC_X704"></span>**Power PC X704** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>

<span data-ttu-id="41deb-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)</span><span class="sxs-lookup"><span data-stu-id="41deb-376"><span id="Power_PC_750"></span><span id="power_pc_750"></span><span id="POWER_PC_750"></span>**Power PC 750** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>

<span data-ttu-id="41deb-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Семейство Alpha** (48)</span><span class="sxs-lookup"><span data-stu-id="41deb-377"><span id="Alpha_Family"></span><span id="alpha_family"></span><span id="ALPHA_FAMILY"></span>**Alpha Family** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>

<span data-ttu-id="41deb-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Альфа-21064** (49)</span><span class="sxs-lookup"><span data-stu-id="41deb-378"><span id="Alpha_21064"></span><span id="alpha_21064"></span><span id="ALPHA_21064"></span>**Alpha 21064** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>

<span data-ttu-id="41deb-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Альфа-21066** (50)</span><span class="sxs-lookup"><span data-stu-id="41deb-379"><span id="Alpha_21066"></span><span id="alpha_21066"></span><span id="ALPHA_21066"></span>**Alpha 21066** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>

<span data-ttu-id="41deb-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Альфа-21164** (51)</span><span class="sxs-lookup"><span data-stu-id="41deb-380"><span id="Alpha_21164"></span><span id="alpha_21164"></span><span id="ALPHA_21164"></span>**Alpha 21164** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>

<span data-ttu-id="41deb-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**Альфа-21164PC** (52)</span><span class="sxs-lookup"><span data-stu-id="41deb-381"><span id="Alpha_21164PC"></span><span id="alpha_21164pc"></span><span id="ALPHA_21164PC"></span>**Alpha 21164PC** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>

<span data-ttu-id="41deb-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**Альфа-21164a** (53)</span><span class="sxs-lookup"><span data-stu-id="41deb-382"><span id="Alpha_21164a"></span><span id="alpha_21164a"></span><span id="ALPHA_21164A"></span>**Alpha 21164a** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>

<span data-ttu-id="41deb-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Альфа-21264** (54)</span><span class="sxs-lookup"><span data-stu-id="41deb-383"><span id="Alpha_21264"></span><span id="alpha_21264"></span><span id="ALPHA_21264"></span>**Alpha 21264** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>

<span data-ttu-id="41deb-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Альфа-21364** (55)</span><span class="sxs-lookup"><span data-stu-id="41deb-384"><span id="Alpha_21364"></span><span id="alpha_21364"></span><span id="ALPHA_21364"></span>**Alpha 21364** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>

<span data-ttu-id="41deb-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**Семейство MIPS** (64)</span><span class="sxs-lookup"><span data-stu-id="41deb-385"><span id="MIPS_Family"></span><span id="mips_family"></span><span id="MIPS_FAMILY"></span>**MIPS Family** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4000"></span><span id="mips_r4000"></span>

<span data-ttu-id="41deb-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**MIPS R4000** (65)</span><span class="sxs-lookup"><span data-stu-id="41deb-386"><span id="MIPS_R4000"></span><span id="mips_r4000"></span>**MIPS R4000** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4200"></span><span id="mips_r4200"></span>

<span data-ttu-id="41deb-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**MIPS R4200** (66)</span><span class="sxs-lookup"><span data-stu-id="41deb-387"><span id="MIPS_R4200"></span><span id="mips_r4200"></span>**MIPS R4200** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4400"></span><span id="mips_r4400"></span>

<span data-ttu-id="41deb-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**MIPS R4400** (67)</span><span class="sxs-lookup"><span data-stu-id="41deb-388"><span id="MIPS_R4400"></span><span id="mips_r4400"></span>**MIPS R4400** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R4600"></span><span id="mips_r4600"></span>

<span data-ttu-id="41deb-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**MIPS R4600** (68)</span><span class="sxs-lookup"><span data-stu-id="41deb-389"><span id="MIPS_R4600"></span><span id="mips_r4600"></span>**MIPS R4600** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS_R10000"></span><span id="mips_r10000"></span>

<span data-ttu-id="41deb-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**MIPS R10000** (69)</span><span class="sxs-lookup"><span data-stu-id="41deb-390"><span id="MIPS_R10000"></span><span id="mips_r10000"></span>**MIPS R10000** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>

<span data-ttu-id="41deb-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**Семейство SPARC** (80)</span><span class="sxs-lookup"><span data-stu-id="41deb-391"><span id="SPARC_Family"></span><span id="sparc_family"></span><span id="SPARC_FAMILY"></span>**SPARC Family** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>

<span data-ttu-id="41deb-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>Очень **SPARC** (81)</span><span class="sxs-lookup"><span data-stu-id="41deb-392"><span id="SuperSPARC"></span><span id="supersparc"></span><span id="SUPERSPARC"></span>**SuperSPARC** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>

<span data-ttu-id="41deb-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**МИКРОSPARC II** (82)</span><span class="sxs-lookup"><span data-stu-id="41deb-393"><span id="microSPARC_II"></span><span id="microsparc_ii"></span><span id="MICROSPARC_II"></span>**microSPARC II** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>

<span data-ttu-id="41deb-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**Микроsparc ииеп** (83)</span><span class="sxs-lookup"><span data-stu-id="41deb-394"><span id="microSPARC_IIep"></span><span id="microsparc_iiep"></span><span id="MICROSPARC_IIEP"></span>**microSPARC IIep** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>

<span data-ttu-id="41deb-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**Ултраспарк** (84)</span><span class="sxs-lookup"><span data-stu-id="41deb-395"><span id="UltraSPARC"></span><span id="ultrasparc"></span><span id="ULTRASPARC"></span>**UltraSPARC** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>

<span data-ttu-id="41deb-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**УЛТРАСПАРК II** (85)</span><span class="sxs-lookup"><span data-stu-id="41deb-396"><span id="UltraSPARC_II"></span><span id="ultrasparc_ii"></span><span id="ULTRASPARC_II"></span>**UltraSPARC II** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="41deb-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**Ултраспарк III** (86)</span><span class="sxs-lookup"><span data-stu-id="41deb-397"><span id="UltraSPARC_IIi"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC IIi** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>

<span data-ttu-id="41deb-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**УЛТРАСПАРК III** (87)</span><span class="sxs-lookup"><span data-stu-id="41deb-398"><span id="UltraSPARC_III"></span><span id="ultrasparc_iii"></span><span id="ULTRASPARC_III"></span>**UltraSPARC III** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>

<span data-ttu-id="41deb-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**Ултраспарк ИИИИ** (88)</span><span class="sxs-lookup"><span data-stu-id="41deb-399"><span id="UltraSPARC_IIIi"></span><span id="ultrasparc_iiii"></span><span id="ULTRASPARC_IIII"></span>**UltraSPARC IIIi** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="68040"></span>

<span data-ttu-id="41deb-400"><span id="68040"></span>**68040** (96)</span><span class="sxs-lookup"><span data-stu-id="41deb-400"><span id="68040"></span>**68040** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>

<span data-ttu-id="41deb-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**семейство 68xxx** (97)</span><span class="sxs-lookup"><span data-stu-id="41deb-401"><span id="68xxx_Family"></span><span id="68xxx_family"></span><span id="68XXX_FAMILY"></span>**68xxx Family** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="68000"></span>

<span data-ttu-id="41deb-402"><span id="68000"></span>**68000** (98)</span><span class="sxs-lookup"><span data-stu-id="41deb-402"><span id="68000"></span>**68000** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="68010"></span>

<span data-ttu-id="41deb-403"><span id="68010"></span>**68010** (99)</span><span class="sxs-lookup"><span data-stu-id="41deb-403"><span id="68010"></span>**68010** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="68020"></span>

<span data-ttu-id="41deb-404"><span id="68020"></span>**68020** (100)</span><span class="sxs-lookup"><span data-stu-id="41deb-404"><span id="68020"></span>**68020** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="68030"></span>

<span data-ttu-id="41deb-405"><span id="68030"></span>**68030** (101)</span><span class="sxs-lookup"><span data-stu-id="41deb-405"><span id="68030"></span>**68030** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>

<span data-ttu-id="41deb-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Семейство Хоббит** (112)</span><span class="sxs-lookup"><span data-stu-id="41deb-406"><span id="Hobbit_Family"></span><span id="hobbit_family"></span><span id="HOBBIT_FAMILY"></span>**Hobbit Family** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>

<span data-ttu-id="41deb-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Семейство крусое (TM) TM5000** (120)</span><span class="sxs-lookup"><span data-stu-id="41deb-407"><span id="Crusoe_TM__TM5000_Family"></span><span id="crusoe_tm__tm5000_family"></span><span id="CRUSOE_TM__TM5000_FAMILY"></span>**Crusoe(TM) TM5000 Family** (120)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-408">Семейство крусое TM5000</span><span class="sxs-lookup"><span data-stu-id="41deb-408">Crusoe TM5000 Family</span></span>

</dd> <dt>

<span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>

<span data-ttu-id="41deb-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Семейство крусое (TM) TM3000** (121)</span><span class="sxs-lookup"><span data-stu-id="41deb-409"><span id="Crusoe_TM__TM3000_Family"></span><span id="crusoe_tm__tm3000_family"></span><span id="CRUSOE_TM__TM3000_FAMILY"></span>**Crusoe(TM) TM3000 Family** (121)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-410">Семейство крусое TM3000</span><span class="sxs-lookup"><span data-stu-id="41deb-410">Crusoe TM3000 Family</span></span>

</dd> <dt>

<span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>

<span data-ttu-id="41deb-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Семейство еффицеон (TM) TM8000** (122)</span><span class="sxs-lookup"><span data-stu-id="41deb-411"><span id="Efficeon_TM__TM8000_Family"></span><span id="efficeon_tm__tm8000_family"></span><span id="EFFICEON_TM__TM8000_FAMILY"></span>**Efficeon(TM) TM8000 Family** (122)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-412">Семейство Efficeon8000</span><span class="sxs-lookup"><span data-stu-id="41deb-412">Efficeon8000 Family</span></span>

</dd> <dt>

<span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>

<span data-ttu-id="41deb-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Веитек** (128)</span><span class="sxs-lookup"><span data-stu-id="41deb-413"><span id="Weitek"></span><span id="weitek"></span><span id="WEITEK"></span>**Weitek** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>

<span data-ttu-id="41deb-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Процессор Itanium (TM)** (130)</span><span class="sxs-lookup"><span data-stu-id="41deb-414"><span id="Itanium_TM__Processor"></span><span id="itanium_tm__processor"></span><span id="ITANIUM_TM__PROCESSOR"></span>**Itanium(TM) Processor** (130)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-415">Процессор Itanium</span><span class="sxs-lookup"><span data-stu-id="41deb-415">Itanium  Processor</span></span>

</dd> <dt>

<span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>

<span data-ttu-id="41deb-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**Семейство процессоров AMD Athlon (TM) 64** (131)</span><span class="sxs-lookup"><span data-stu-id="41deb-416"><span id="AMD_Athlon_TM__64_Processor_Family"></span><span id="amd_athlon_tm__64_processor_family"></span><span id="AMD_ATHLON_TM__64_PROCESSOR_FAMILY"></span>**AMD Athlon(TM) 64 Processor Family** (131)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-417">AMD Athlon</span><span class="sxs-lookup"><span data-stu-id="41deb-417">AMD Athlon</span></span> 

</dd> <dt>

<span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>

<span data-ttu-id="41deb-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**Семейство AMD Opteron (TM)** (132)</span><span class="sxs-lookup"><span data-stu-id="41deb-418"><span id="AMD_Opteron_TM__Family"></span><span id="amd_opteron_tm__family"></span><span id="AMD_OPTERON_TM__FAMILY"></span>**AMD Opteron(TM) Family** (132)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-419">Семейство AMD Opteron</span><span class="sxs-lookup"><span data-stu-id="41deb-419">AMD Opteron  Family</span></span>

</dd> <dt>

<span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>

<span data-ttu-id="41deb-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**PA — семейство RISC** (144)</span><span class="sxs-lookup"><span data-stu-id="41deb-420"><span id="PA-RISC_Family"></span><span id="pa-risc_family"></span><span id="PA-RISC_FAMILY"></span>**PA-RISC Family** (144)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>

<span data-ttu-id="41deb-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)</span><span class="sxs-lookup"><span data-stu-id="41deb-421"><span id="PA-RISC_8500"></span><span id="pa-risc_8500"></span>**PA-RISC 8500** (145)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>

<span data-ttu-id="41deb-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)</span><span class="sxs-lookup"><span data-stu-id="41deb-422"><span id="PA-RISC_8000"></span><span id="pa-risc_8000"></span>**PA-RISC 8000** (146)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>

<span data-ttu-id="41deb-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)</span><span class="sxs-lookup"><span data-stu-id="41deb-423"><span id="PA-RISC_7300LC"></span><span id="pa-risc_7300lc"></span>**PA-RISC 7300LC** (147)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>

<span data-ttu-id="41deb-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)</span><span class="sxs-lookup"><span data-stu-id="41deb-424"><span id="PA-RISC_7200"></span><span id="pa-risc_7200"></span>**PA-RISC 7200** (148)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>

<span data-ttu-id="41deb-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)</span><span class="sxs-lookup"><span data-stu-id="41deb-425"><span id="PA-RISC_7100LC"></span><span id="pa-risc_7100lc"></span>**PA-RISC 7100LC** (149)</span></span>


</dt> <dd></dd> <dt>

<span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>

<span data-ttu-id="41deb-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)</span><span class="sxs-lookup"><span data-stu-id="41deb-426"><span id="PA-RISC_7100"></span><span id="pa-risc_7100"></span>**PA-RISC 7100** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>

<span data-ttu-id="41deb-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**Семейство V30** (160)</span><span class="sxs-lookup"><span data-stu-id="41deb-427"><span id="V30_Family"></span><span id="v30_family"></span><span id="V30_FAMILY"></span>**V30 Family** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>

<span data-ttu-id="41deb-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium (R) III Xeon (TM)** (176)</span><span class="sxs-lookup"><span data-stu-id="41deb-428"><span id="Pentium_R__III_Xeon_TM_"></span><span id="pentium_r__iii_xeon_tm_"></span><span id="PENTIUM_R__III_XEON_TM_"></span>**Pentium(R) III Xeon(TM)** (176)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-429">Pentium III Xeon</span><span class="sxs-lookup"><span data-stu-id="41deb-429">Pentium III Xeon</span></span>

</dd> <dt>

<span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>

<span data-ttu-id="41deb-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Процессор Pentium (r) III с технологией Intel (r) SpeedStep (TM)** (177)</span><span class="sxs-lookup"><span data-stu-id="41deb-430"><span id="Pentium_R__III_Processor_with_Intel_R__SpeedStep_TM__Technology"></span><span id="pentium_r__iii_processor_with_intel_r__speedstep_tm__technology"></span><span id="PENTIUM_R__III_PROCESSOR_WITH_INTEL_R__SPEEDSTEP_TM__TECHNOLOGY"></span>**Pentium(R) III Processor with Intel(R) SpeedStep(TM) Technology** (177)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-431">Процессор Pentium III с технологией Intel SpeedStep</span><span class="sxs-lookup"><span data-stu-id="41deb-431">Pentium III Processor with Intel SpeedStep Technology</span></span>

</dd> <dt>

<span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>

<span data-ttu-id="41deb-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium (R) 4** (178)</span><span class="sxs-lookup"><span data-stu-id="41deb-432"><span id="Pentium_R__4"></span><span id="pentium_r__4"></span><span id="PENTIUM_R__4"></span>**Pentium(R) 4** (178)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-433">Pentium 4</span><span class="sxs-lookup"><span data-stu-id="41deb-433">Pentium 4</span></span>

</dd> <dt>

<span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>

<span data-ttu-id="41deb-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel (R) Xeon (TM)** (179)</span><span class="sxs-lookup"><span data-stu-id="41deb-434"><span id="Intel_R__Xeon_TM_"></span><span id="intel_r__xeon_tm_"></span><span id="INTEL_R__XEON_TM_"></span>**Intel(R) Xeon(TM)** (179)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-435">Intel Xeon</span><span class="sxs-lookup"><span data-stu-id="41deb-435">Intel Xeon</span></span>

</dd> <dt>

<span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>

<span data-ttu-id="41deb-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**Семейство AS400** (180)</span><span class="sxs-lookup"><span data-stu-id="41deb-436"><span id="AS400_Family"></span><span id="as400_family"></span><span id="AS400_FAMILY"></span>**AS400 Family** (180)</span></span>


</dt> <dd></dd> <dt>

<span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>

<span data-ttu-id="41deb-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**Процессор Intel (R) Xeon (TM) MP** (181)</span><span class="sxs-lookup"><span data-stu-id="41deb-437"><span id="Intel_R__Xeon_TM__processor_MP"></span><span id="intel_r__xeon_tm__processor_mp"></span><span id="INTEL_R__XEON_TM__PROCESSOR_MP"></span>**Intel(R) Xeon(TM) processor MP** (181)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-438">Процессор Intel Xeon MP</span><span class="sxs-lookup"><span data-stu-id="41deb-438">Intel Xeon Processor MP</span></span>

</dd> <dt>

<span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>

<span data-ttu-id="41deb-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**Семейство AMD аслонксп (TM)** (182)</span><span class="sxs-lookup"><span data-stu-id="41deb-439"><span id="AMD_AthlonXP_TM__Family"></span><span id="amd_athlonxp_tm__family"></span><span id="AMD_ATHLONXP_TM__FAMILY"></span>**AMD AthlonXP(TM) Family** (182)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-440">Семейство AMD Аслонксп</span><span class="sxs-lookup"><span data-stu-id="41deb-440">AMD AthlonXP Family</span></span>

</dd> <dt>

<span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>

<span data-ttu-id="41deb-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**Семейство AMD аслонмп (TM)** (183)</span><span class="sxs-lookup"><span data-stu-id="41deb-441"><span id="AMD_AthlonMP_TM__Family"></span><span id="amd_athlonmp_tm__family"></span><span id="AMD_ATHLONMP_TM__FAMILY"></span>**AMD AthlonMP(TM) Family** (183)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-442">Семейство AMD Аслонмп</span><span class="sxs-lookup"><span data-stu-id="41deb-442">AMD AthlonMP Family</span></span>

</dd> <dt>

<span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>

<span data-ttu-id="41deb-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel (r) Itanium (r) 2** (184)</span><span class="sxs-lookup"><span data-stu-id="41deb-443"><span id="Intel_R__Itanium_R__2"></span><span id="intel_r__itanium_r__2"></span><span id="INTEL_R__ITANIUM_R__2"></span>**Intel(R) Itanium(R) 2** (184)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-444">Intel Itanium 2</span><span class="sxs-lookup"><span data-stu-id="41deb-444">Intel Itanium 2</span></span>

</dd> <dt>

<span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>

<span data-ttu-id="41deb-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Процессор Intel Pentium M** (185)</span><span class="sxs-lookup"><span data-stu-id="41deb-445"><span id="Intel_Pentium_M_Processor"></span><span id="intel_pentium_m_processor"></span><span id="INTEL_PENTIUM_M_PROCESSOR"></span>**Intel Pentium M Processor** (185)</span></span>


</dt> <dd></dd> <dt>

<span id="K7"></span><span id="k7"></span>

<span data-ttu-id="41deb-446"><span id="K7"></span><span id="k7"></span>**K7** (190)</span><span class="sxs-lookup"><span data-stu-id="41deb-446"><span id="K7"></span><span id="k7"></span>**K7** (190)</span></span>


</dt> <dd></dd> <dt>

<span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>

<span data-ttu-id="41deb-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**Семейство IBM390** (200)</span><span class="sxs-lookup"><span data-stu-id="41deb-447"><span id="IBM390_Family"></span><span id="ibm390_family"></span><span id="IBM390_FAMILY"></span>**IBM390 Family** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="G4"></span><span id="g4"></span>

<span data-ttu-id="41deb-448"><span id="G4"></span><span id="g4"></span>**G4** (201)</span><span class="sxs-lookup"><span data-stu-id="41deb-448"><span id="G4"></span><span id="g4"></span>**G4** (201)</span></span>


</dt> <dd></dd> <dt>

<span id="G5"></span><span id="g5"></span>

<span data-ttu-id="41deb-449"><span id="G5"></span><span id="g5"></span>**G5** (202)</span><span class="sxs-lookup"><span data-stu-id="41deb-449"><span id="G5"></span><span id="g5"></span>**G5** (202)</span></span>


</dt> <dd></dd> <dt>

<span id="G6"></span><span id="g6"></span>

<span data-ttu-id="41deb-450"><span id="G6"></span><span id="g6"></span>**G6** (203)</span><span class="sxs-lookup"><span data-stu-id="41deb-450"><span id="G6"></span><span id="g6"></span>**G6** (203)</span></span>


</dt> <dd></dd> <dt>

<span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>

<span data-ttu-id="41deb-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**основание z/архитектуры** (204)</span><span class="sxs-lookup"><span data-stu-id="41deb-451"><span id="z_Architecture_base"></span><span id="z_architecture_base"></span><span id="Z_ARCHITECTURE_BASE"></span>**z/Architecture base** (204)</span></span>


</dt> <dd></dd> <dt>

<span id="i860"></span><span id="I860"></span>

<span data-ttu-id="41deb-452"><span id="i860"></span><span id="I860"></span>**i860** (250)</span><span class="sxs-lookup"><span data-stu-id="41deb-452"><span id="i860"></span><span id="I860"></span>**i860** (250)</span></span>


</dt> <dd></dd> <dt>

<span id="i960"></span><span id="I960"></span>

<span data-ttu-id="41deb-453"><span id="i960"></span><span id="I960"></span>Процессоры **i960** (251)</span><span class="sxs-lookup"><span data-stu-id="41deb-453"><span id="i960"></span><span id="I960"></span>**i960** (251)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-3"></span><span id="sh-3"></span>

<span data-ttu-id="41deb-454"><span id="SH-3"></span><span id="sh-3"></span>**Sh-3** (260)</span><span class="sxs-lookup"><span data-stu-id="41deb-454"><span id="SH-3"></span><span id="sh-3"></span>**SH-3** (260)</span></span>


</dt> <dd></dd> <dt>

<span id="SH-4"></span><span id="sh-4"></span>

<span data-ttu-id="41deb-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)</span><span class="sxs-lookup"><span data-stu-id="41deb-455"><span id="SH-4"></span><span id="sh-4"></span>**SH-4** (261)</span></span>


</dt> <dd></dd> <dt>

<span id="ARM"></span><span id="arm"></span>

<span data-ttu-id="41deb-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280)</span><span class="sxs-lookup"><span data-stu-id="41deb-456"><span id="ARM"></span><span id="arm"></span>**ARM** (280)</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>

<span data-ttu-id="41deb-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**Стронгарм** (281)</span><span class="sxs-lookup"><span data-stu-id="41deb-457"><span id="StrongARM"></span><span id="strongarm"></span><span id="STRONGARM"></span>**StrongARM** (281)</span></span>


</dt> <dd></dd> <dt>

<span id="6x86"></span><span id="6X86"></span>

<span data-ttu-id="41deb-458"><span id="6x86"></span><span id="6X86"></span>**6x86** (300)</span><span class="sxs-lookup"><span data-stu-id="41deb-458"><span id="6x86"></span><span id="6X86"></span>**6x86** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>

<span data-ttu-id="41deb-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**Медиагкс** (301)</span><span class="sxs-lookup"><span data-stu-id="41deb-459"><span id="MediaGX"></span><span id="mediagx"></span><span id="MEDIAGX"></span>**MediaGX** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="MII"></span><span id="mii"></span>

<span data-ttu-id="41deb-460"><span id="MII"></span><span id="mii"></span>**Мии** (302)</span><span class="sxs-lookup"><span data-stu-id="41deb-460"><span id="MII"></span><span id="mii"></span>**MII** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>

<span data-ttu-id="41deb-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**Винчип** (320)</span><span class="sxs-lookup"><span data-stu-id="41deb-461"><span id="WinChip"></span><span id="winchip"></span><span id="WINCHIP"></span>**WinChip** (320)</span></span>


</dt> <dd></dd> <dt>

<span id="DSP"></span><span id="dsp"></span>

<span data-ttu-id="41deb-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350)</span><span class="sxs-lookup"><span data-stu-id="41deb-462"><span id="DSP"></span><span id="dsp"></span>**DSP** (350)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>

<span data-ttu-id="41deb-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Процессор видео** (500)</span><span class="sxs-lookup"><span data-stu-id="41deb-463"><span id="Video_Processor"></span><span id="video_processor"></span><span id="VIDEO_PROCESSOR"></span>**Video Processor** (500)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41deb-464">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="41deb-464">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-465">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="41deb-465">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-466">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-467">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="41deb-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-468">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="41deb-468">Date and time the object was installed.</span></span> <span data-ttu-id="41deb-469">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="41deb-469">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="41deb-470">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41deb-470">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-471">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="41deb-471">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-472">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41deb-472">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-473">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-473">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41deb-474">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="41deb-474">Last error code reported by the logical device.</span></span>

<span data-ttu-id="41deb-475">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-476">**лоадперцентаже**</span><span class="sxs-lookup"><span data-stu-id="41deb-476">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-477">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41deb-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-478">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-479">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрпроцессорлоад "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" процент ")</span><span class="sxs-lookup"><span data-stu-id="41deb-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrProcessorLoad"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-480">Время загрузки процессора, усредненного за последнюю минуту, в процентах.</span><span class="sxs-lookup"><span data-stu-id="41deb-480">Loading of the processor, averaged over the last minute, in a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="41deb-481">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="41deb-481">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-482">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41deb-482">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-483">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-484">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF- \| процессор \| 006,5 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" мегагерц ")</span><span class="sxs-lookup"><span data-stu-id="41deb-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-485">Максимальная скорость процессора (в мегагерцах).</span><span class="sxs-lookup"><span data-stu-id="41deb-485">Maximum speed (in megahertz) of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="41deb-486">**Name**</span><span class="sxs-lookup"><span data-stu-id="41deb-486">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-487">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-488">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-489">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="41deb-489">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-490">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="41deb-490">Label by which the object is known.</span></span> <span data-ttu-id="41deb-491">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="41deb-491">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="41deb-492">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41deb-492">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-493">**осерфамилидескриптион**</span><span class="sxs-lookup"><span data-stu-id="41deb-493">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-494">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-495">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-496">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ процессор CIM**.**Family**")</span><span class="sxs-lookup"><span data-stu-id="41deb-496">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-497">Описание типа семейства процессоров.</span><span class="sxs-lookup"><span data-stu-id="41deb-497">Description of the processor family type.</span></span> <span data-ttu-id="41deb-498">Это свойство используется, если свойство **Family** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="41deb-498">This property is used when the **Family** property is set to 1 ("Other").</span></span> <span data-ttu-id="41deb-499">Для этой строки следует задать значение null, если свойство **Family** имеет значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="41deb-499">This string should be set to null when the **Family** property is a value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="41deb-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="41deb-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-501">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-502">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-503">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="41deb-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-504">Самонастраивающийся идентификатор устройства логического устройства.</span><span class="sxs-lookup"><span data-stu-id="41deb-504">Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="41deb-505">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="41deb-506">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="41deb-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="41deb-507">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="41deb-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-508">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="41deb-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41deb-509">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41deb-510">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="41deb-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="41deb-511">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41deb-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="41deb-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="41deb-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="41deb-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="41deb-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="41deb-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="41deb-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="41deb-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-516">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="41deb-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="41deb-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="41deb-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-518">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="41deb-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="41deb-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="41deb-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-520">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="41deb-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="41deb-521">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="41deb-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="41deb-522">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="41deb-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="41deb-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="41deb-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-524">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="41deb-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="41deb-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="41deb-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-526">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="41deb-526">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="41deb-527">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="41deb-527">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-528">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="41deb-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-529">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41deb-530">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="41deb-530">If **True**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="41deb-531">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="41deb-531">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="41deb-532">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="41deb-532">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="41deb-533">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="41deb-533">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="41deb-534">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-534">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-535">**Роль**</span><span class="sxs-lookup"><span data-stu-id="41deb-535">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-536">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-536">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-537">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41deb-538">Произвольная строка, описывающая роль процессора.</span><span class="sxs-lookup"><span data-stu-id="41deb-538">Free-form string that describes the role of the processor.</span></span> <span data-ttu-id="41deb-539">Например, "Центральный процессор" или "математический процессор".</span><span class="sxs-lookup"><span data-stu-id="41deb-539">For example, "Central Processor" or "Math Processor".</span></span>

</dd> <dt>

<span data-ttu-id="41deb-540">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="41deb-540">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-541">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-542">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-543">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="41deb-543">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-544">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="41deb-544">Current status of the object.</span></span>

<span data-ttu-id="41deb-545">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41deb-545">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="41deb-546">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="41deb-546">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="41deb-547">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="41deb-547">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="41deb-548">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="41deb-548">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="41deb-549">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="41deb-549">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41deb-550">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="41deb-550">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="41deb-551">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="41deb-551">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="41deb-552">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="41deb-552">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="41deb-553">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="41deb-553">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="41deb-554">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="41deb-554">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="41deb-555">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="41deb-555">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="41deb-556">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="41deb-556">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="41deb-557">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="41deb-557">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="41deb-558">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="41deb-558">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41deb-559">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="41deb-559">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-560">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41deb-560">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-561">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-562">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="41deb-562">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-563">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="41deb-563">State of the logical device.</span></span> <span data-ttu-id="41deb-564">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="41deb-564">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="41deb-565">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-565">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="41deb-566">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="41deb-566">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41deb-567">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="41deb-567">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="41deb-568">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="41deb-568">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="41deb-569">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="41deb-569">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="41deb-570">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="41deb-570">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41deb-571">**Отладка по шагам**</span><span class="sxs-lookup"><span data-stu-id="41deb-571">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-572">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-572">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-573">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-573">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-574">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ процессор CIM**.**Family**")</span><span class="sxs-lookup"><span data-stu-id="41deb-574">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Processor**.**Family**")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-575">Произвольная строка, указывающая уровень редакции процессора в семействе процессоров.</span><span class="sxs-lookup"><span data-stu-id="41deb-575">Free-form string that indicates the revision level of the processor within the processor family.</span></span>

</dd> <dt>

<span data-ttu-id="41deb-576">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="41deb-576">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-577">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-578">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-579">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="41deb-579">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="41deb-580">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="41deb-580">Scoping system's creation class name.</span></span>

<span data-ttu-id="41deb-581">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-581">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-582">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="41deb-582">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-583">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-584">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-585">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="41deb-585">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="41deb-586">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="41deb-586">Scoping system's name.</span></span>

<span data-ttu-id="41deb-587">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="41deb-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41deb-588">**UniqueId**</span><span class="sxs-lookup"><span data-stu-id="41deb-588">**UniqueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-589">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="41deb-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-590">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-590">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41deb-591">Глобальный уникальный идентификатор процессора.</span><span class="sxs-lookup"><span data-stu-id="41deb-591">Globally unique identifier for the processor.</span></span> <span data-ttu-id="41deb-592">Этот идентификатор может быть уникальным только в пределах семейства процессоров.</span><span class="sxs-lookup"><span data-stu-id="41deb-592">This identifier can only be unique within a processor family.</span></span>

</dd> <dt>

<span data-ttu-id="41deb-593">**упградемесод**</span><span class="sxs-lookup"><span data-stu-id="41deb-593">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41deb-594">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41deb-594">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41deb-595">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41deb-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41deb-596">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| \| -процессор 006,7 ")</span><span class="sxs-lookup"><span data-stu-id="41deb-596">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Processor\|006.7")</span></span>
</dt> </dl>

<span data-ttu-id="41deb-597">Сведения о сокете ЦП, включая данные о том, как обновить процессор (если обновления поддерживаются).</span><span class="sxs-lookup"><span data-stu-id="41deb-597">CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="41deb-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="41deb-598"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41deb-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="41deb-599"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>

<span data-ttu-id="41deb-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Дочерняя плата** (3)</span><span class="sxs-lookup"><span data-stu-id="41deb-600"><span id="Daughter_Board"></span><span id="daughter_board"></span><span id="DAUGHTER_BOARD"></span>**Daughter Board** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>

<span data-ttu-id="41deb-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**Сокет ЗИФ** (4)</span><span class="sxs-lookup"><span data-stu-id="41deb-601"><span id="ZIF_Socket"></span><span id="zif_socket"></span><span id="ZIF_SOCKET"></span>**ZIF Socket** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>

<span data-ttu-id="41deb-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Замена/свинка назад** (5)</span><span class="sxs-lookup"><span data-stu-id="41deb-602"><span id="Replacement_Piggy_Back"></span><span id="replacement_piggy_back"></span><span id="REPLACEMENT_PIGGY_BACK"></span>**Replacement/Piggy Back** (5)</span></span>


</dt> <dd>

<span data-ttu-id="41deb-603">Замена или свинка назад</span><span class="sxs-lookup"><span data-stu-id="41deb-603">Replacement or piggy back</span></span>

</dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="41deb-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (6)</span><span class="sxs-lookup"><span data-stu-id="41deb-604"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>

<span data-ttu-id="41deb-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**Сокет Лиф** (7)</span><span class="sxs-lookup"><span data-stu-id="41deb-605"><span id="LIF_Socket"></span><span id="lif_socket"></span><span id="LIF_SOCKET"></span>**LIF Socket** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>

<span data-ttu-id="41deb-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Слот 1** (8)</span><span class="sxs-lookup"><span data-stu-id="41deb-606"><span id="Slot_1"></span><span id="slot_1"></span><span id="SLOT_1"></span>**Slot 1** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>

<span data-ttu-id="41deb-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Слот 2** (9)</span><span class="sxs-lookup"><span data-stu-id="41deb-607"><span id="Slot_2"></span><span id="slot_2"></span><span id="SLOT_2"></span>**Slot 2** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>

<span data-ttu-id="41deb-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**370-контактный разъем** (10)</span><span class="sxs-lookup"><span data-stu-id="41deb-608"><span id="370_Pin_Socket"></span><span id="370_pin_socket"></span><span id="370_PIN_SOCKET"></span>**370 Pin Socket** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>

<span data-ttu-id="41deb-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Слот A** (11)</span><span class="sxs-lookup"><span data-stu-id="41deb-609"><span id="Slot_A"></span><span id="slot_a"></span><span id="SLOT_A"></span>**Slot A** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>

<span data-ttu-id="41deb-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Гнездо M** (12)</span><span class="sxs-lookup"><span data-stu-id="41deb-610"><span id="Slot_M"></span><span id="slot_m"></span><span id="SLOT_M"></span>**Slot M** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>

<span data-ttu-id="41deb-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Сокет 423** (13)</span><span class="sxs-lookup"><span data-stu-id="41deb-611"><span id="Socket_423"></span><span id="socket_423"></span><span id="SOCKET_423"></span>**Socket 423** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>

<span data-ttu-id="41deb-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Сокет A (сокет 462)** (14)</span><span class="sxs-lookup"><span data-stu-id="41deb-612"><span id="Socket_A__Socket_462_"></span><span id="socket_a__socket_462_"></span><span id="SOCKET_A__SOCKET_462_"></span>**Socket A (Socket 462)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>

<span data-ttu-id="41deb-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Сокет 478** (15)</span><span class="sxs-lookup"><span data-stu-id="41deb-613"><span id="Socket_478"></span><span id="socket_478"></span><span id="SOCKET_478"></span>**Socket 478** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>

<span data-ttu-id="41deb-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Сокет 754** (16)</span><span class="sxs-lookup"><span data-stu-id="41deb-614"><span id="Socket_754"></span><span id="socket_754"></span><span id="SOCKET_754"></span>**Socket 754** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>

<span data-ttu-id="41deb-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Сокет 940** (17)</span><span class="sxs-lookup"><span data-stu-id="41deb-615"><span id="Socket_940"></span><span id="socket_940"></span><span id="SOCKET_940"></span>**Socket 940** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>

<span data-ttu-id="41deb-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Сокет 939** (18)</span><span class="sxs-lookup"><span data-stu-id="41deb-616"><span id="Socket_939"></span><span id="socket_939"></span><span id="SOCKET_939"></span>**Socket 939** (18)</span></span>


<span data-ttu-id="41deb-617"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="41deb-617"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="41deb-618">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41deb-618">Remarks</span></span>

<span data-ttu-id="41deb-619">Класс **\_ процессора CIM** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="41deb-619">The **CIM\_Processor** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="41deb-620">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="41deb-620">WMI does not implement this class.</span></span> <span data-ttu-id="41deb-621">Сведения о классах WMI, производных от **\_ обработчика CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="41deb-621">For WMI classes derived from **CIM\_Processor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="41deb-622">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="41deb-622">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="41deb-623">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="41deb-623">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="41deb-624">Требования</span><span class="sxs-lookup"><span data-stu-id="41deb-624">Requirements</span></span>



| <span data-ttu-id="41deb-625">Требование</span><span class="sxs-lookup"><span data-stu-id="41deb-625">Requirement</span></span> | <span data-ttu-id="41deb-626">Значение</span><span class="sxs-lookup"><span data-stu-id="41deb-626">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41deb-627">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41deb-627">Minimum supported client</span></span><br/> | <span data-ttu-id="41deb-628">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41deb-628">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41deb-629">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41deb-629">Minimum supported server</span></span><br/> | <span data-ttu-id="41deb-630">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41deb-630">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41deb-631">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="41deb-631">Namespace</span></span><br/>                | <span data-ttu-id="41deb-632">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="41deb-632">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41deb-633">MOF</span><span class="sxs-lookup"><span data-stu-id="41deb-633">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41deb-634"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41deb-634"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41deb-635">DLL</span><span class="sxs-lookup"><span data-stu-id="41deb-635">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41deb-636"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41deb-636"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41deb-637">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41deb-637">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41deb-638">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="41deb-638">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

