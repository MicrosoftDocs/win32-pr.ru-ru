---
description: Ассоциация CIM \_ параллелконтроллер относится к возможностям и управлению логическим устройством параллельного порта.
ms.assetid: c05e79b6-f3a6-48cc-a831-b67e216f43eb
ms.tgt_platform: multiple
title: Класс CIM_ParallelController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParallelController
- CIM_ParallelController.Availability
- CIM_ParallelController.Capabilities
- CIM_ParallelController.CapabilityDescriptions
- CIM_ParallelController.Caption
- CIM_ParallelController.ConfigManagerErrorCode
- CIM_ParallelController.ConfigManagerUserConfig
- CIM_ParallelController.CreationClassName
- CIM_ParallelController.Description
- CIM_ParallelController.DeviceID
- CIM_ParallelController.DMASupport
- CIM_ParallelController.ErrorCleared
- CIM_ParallelController.ErrorDescription
- CIM_ParallelController.InstallDate
- CIM_ParallelController.LastErrorCode
- CIM_ParallelController.MaxNumberControlled
- CIM_ParallelController.Name
- CIM_ParallelController.PNPDeviceID
- CIM_ParallelController.PowerManagementCapabilities
- CIM_ParallelController.PowerManagementSupported
- CIM_ParallelController.ProtocolSupported
- CIM_ParallelController.Status
- CIM_ParallelController.StatusInfo
- CIM_ParallelController.SystemCreationClassName
- CIM_ParallelController.SystemName
- CIM_ParallelController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc21290de08b6e22c0bc69ec127f3c996ee5b65e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539170"
---
# <a name="cim_parallelcontroller-class"></a><span data-ttu-id="6f93c-103">\_Класс CIM параллелконтроллер</span><span class="sxs-lookup"><span data-stu-id="6f93c-103">CIM\_ParallelController class</span></span>

<span data-ttu-id="6f93c-104">Ассоциация **CIM \_ параллелконтроллер** относится к возможностям и управлению логическим устройством параллельного порта.</span><span class="sxs-lookup"><span data-stu-id="6f93c-104">The **CIM\_ParallelController** association relates to the capabilities and management of the parallel port logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f93c-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6f93c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6f93c-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6f93c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6f93c-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6f93c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6f93c-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6f93c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f93c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f93c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C552-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ParallelController : CIM_Controller
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  DMASupport;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxNumberControlled;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="6f93c-110">Члены</span><span class="sxs-lookup"><span data-stu-id="6f93c-110">Members</span></span>

<span data-ttu-id="6f93c-111">Класс **CIM \_ параллелконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6f93c-111">The **CIM\_ParallelController** class has these types of members:</span></span>

-   [<span data-ttu-id="6f93c-112">Методы</span><span class="sxs-lookup"><span data-stu-id="6f93c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="6f93c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f93c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6f93c-114">Методы</span><span class="sxs-lookup"><span data-stu-id="6f93c-114">Methods</span></span>

<span data-ttu-id="6f93c-115">Класс **CIM \_ параллелконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6f93c-115">The **CIM\_ParallelController** class has these methods.</span></span>



| <span data-ttu-id="6f93c-116">Метод</span><span class="sxs-lookup"><span data-stu-id="6f93c-116">Method</span></span>                                                                        | <span data-ttu-id="6f93c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="6f93c-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f93c-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="6f93c-118">**Reset**</span></span>](reset-method-in-class-cim-parallelcontroller.md)                 | <span data-ttu-id="6f93c-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="6f93c-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="6f93c-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6f93c-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="6f93c-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6f93c-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-parallelcontroller.md) | <span data-ttu-id="6f93c-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="6f93c-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="6f93c-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6f93c-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6f93c-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f93c-124">Properties</span></span>

<span data-ttu-id="6f93c-125">Класс **CIM \_ параллелконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6f93c-125">The **CIM\_ParallelController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f93c-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="6f93c-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f93c-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="6f93c-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="6f93c-130">Availability and status of the device.</span></span>

<span data-ttu-id="6f93c-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6f93c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6f93c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f93c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="6f93c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6f93c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="6f93c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6f93c-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="6f93c-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6f93c-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="6f93c-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6f93c-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="6f93c-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6f93c-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="6f93c-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6f93c-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="6f93c-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6f93c-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="6f93c-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6f93c-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="6f93c-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6f93c-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="6f93c-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6f93c-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="6f93c-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6f93c-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="6f93c-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="6f93c-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6f93c-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="6f93c-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="6f93c-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6f93c-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="6f93c-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="6f93c-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6f93c-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="6f93c-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6f93c-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="6f93c-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="6f93c-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6f93c-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="6f93c-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="6f93c-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6f93c-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="6f93c-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="6f93c-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6f93c-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="6f93c-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="6f93c-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6f93c-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="6f93c-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="6f93c-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f93c-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="6f93c-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-162">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="6f93c-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-164">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Параллельные порты DMTF \| 003,8 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ параллелконтроллер**.**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="6f93c-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Parallel Ports\|003.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ParallelController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-165">Возможности параллельного контроллера.</span><span class="sxs-lookup"><span data-stu-id="6f93c-165">Capabilities of the parallel controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f93c-166">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="6f93c-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6f93c-167">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6f93c-167">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="6f93c-168">**XT/AT-совместимый** (2)</span><span class="sxs-lookup"><span data-stu-id="6f93c-168">**XT/AT Compatible** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2_Compatible"></span><span id="ps_2_compatible"></span><span id="PS_2_COMPATIBLE"></span>

<span data-ttu-id="6f93c-169">**Совместимость с PS/2** (3)</span><span class="sxs-lookup"><span data-stu-id="6f93c-169">**PS/2 Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ECP"></span><span id="ecp"></span>

<span data-ttu-id="6f93c-170">**ECP** (4)</span><span class="sxs-lookup"><span data-stu-id="6f93c-170">**ECP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EPP"></span><span id="epp"></span>

<span data-ttu-id="6f93c-171">**EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="6f93c-171">**EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="6f93c-172">**PC-98** (6)</span><span class="sxs-lookup"><span data-stu-id="6f93c-172">**PC-98** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="6f93c-173">**PC-98-хиресо** (7)</span><span class="sxs-lookup"><span data-stu-id="6f93c-173">**PC-98-Hireso** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="6f93c-174">**PC-H98** (8)</span><span class="sxs-lookup"><span data-stu-id="6f93c-174">**PC-H98** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f93c-175">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="6f93c-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-176">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="6f93c-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-178">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ параллелконтроллер**.**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="6f93c-178">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ParallelController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-179">Строки произвольной формы, содержащие подробные объяснения для функций параллельного контроллера, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="6f93c-179">Free-form strings that provide detailed explanations for the parallel controller features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="6f93c-180">Каждая запись этого массива связана с записью в массиве **capabilities** , которая находится в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="6f93c-180">Each entry of this array is related to the entry in the **Capabilities** array, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="6f93c-181">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6f93c-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f93c-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-184">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6f93c-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-185">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6f93c-185">Short textual description of the object.</span></span>

<span data-ttu-id="6f93c-186">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f93c-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-187">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="6f93c-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-188">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f93c-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-190">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6f93c-190">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-191">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6f93c-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="6f93c-192">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6f93c-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6f93c-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="6f93c-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-195">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="6f93c-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6f93c-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6f93c-197">(1)</span><span class="sxs-lookup"><span data-stu-id="6f93c-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-198">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="6f93c-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6f93c-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6f93c-200">(2)</span><span class="sxs-lookup"><span data-stu-id="6f93c-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6f93c-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6f93c-202">(3)</span><span class="sxs-lookup"><span data-stu-id="6f93c-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-203">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6f93c-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6f93c-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6f93c-205">(4)</span><span class="sxs-lookup"><span data-stu-id="6f93c-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-206">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="6f93c-206">Device is not working properly.</span></span> <span data-ttu-id="6f93c-207">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="6f93c-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6f93c-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6f93c-209">(5)</span><span class="sxs-lookup"><span data-stu-id="6f93c-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-210">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="6f93c-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6f93c-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6f93c-212"> (6)</span><span class="sxs-lookup"><span data-stu-id="6f93c-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-213">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="6f93c-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6f93c-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6f93c-215">(7)</span><span class="sxs-lookup"><span data-stu-id="6f93c-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6f93c-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6f93c-217">(8)</span><span class="sxs-lookup"><span data-stu-id="6f93c-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-218">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="6f93c-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6f93c-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6f93c-220">(9)</span><span class="sxs-lookup"><span data-stu-id="6f93c-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-221">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="6f93c-221">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6f93c-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6f93c-223">(10)</span><span class="sxs-lookup"><span data-stu-id="6f93c-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-224">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="6f93c-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6f93c-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6f93c-226">(11)</span><span class="sxs-lookup"><span data-stu-id="6f93c-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-227">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="6f93c-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6f93c-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6f93c-229">(12)</span><span class="sxs-lookup"><span data-stu-id="6f93c-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-230">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="6f93c-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6f93c-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6f93c-232">(13)</span><span class="sxs-lookup"><span data-stu-id="6f93c-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-233">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="6f93c-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6f93c-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6f93c-235">(14)</span><span class="sxs-lookup"><span data-stu-id="6f93c-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-236">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="6f93c-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6f93c-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6f93c-238">(15)</span><span class="sxs-lookup"><span data-stu-id="6f93c-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-239">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="6f93c-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6f93c-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6f93c-241">(16)</span><span class="sxs-lookup"><span data-stu-id="6f93c-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-242">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="6f93c-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6f93c-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6f93c-244">(17)</span><span class="sxs-lookup"><span data-stu-id="6f93c-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-245">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="6f93c-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6f93c-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6f93c-247">(18)</span><span class="sxs-lookup"><span data-stu-id="6f93c-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-248">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="6f93c-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6f93c-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6f93c-250">(19)</span><span class="sxs-lookup"><span data-stu-id="6f93c-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6f93c-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6f93c-252">(20)</span><span class="sxs-lookup"><span data-stu-id="6f93c-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-253">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="6f93c-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6f93c-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6f93c-255">(21)</span><span class="sxs-lookup"><span data-stu-id="6f93c-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-256">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="6f93c-256">System failure.</span></span> <span data-ttu-id="6f93c-257">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="6f93c-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6f93c-258">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="6f93c-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6f93c-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6f93c-260">(22)</span><span class="sxs-lookup"><span data-stu-id="6f93c-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-261">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="6f93c-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6f93c-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6f93c-263">(23)</span><span class="sxs-lookup"><span data-stu-id="6f93c-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-264">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="6f93c-264">System failure.</span></span> <span data-ttu-id="6f93c-265">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="6f93c-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6f93c-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6f93c-267">(24)</span><span class="sxs-lookup"><span data-stu-id="6f93c-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-268">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="6f93c-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6f93c-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6f93c-270">(25)</span><span class="sxs-lookup"><span data-stu-id="6f93c-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-271">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="6f93c-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6f93c-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6f93c-273">(26)</span><span class="sxs-lookup"><span data-stu-id="6f93c-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-274">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="6f93c-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6f93c-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6f93c-276">(27)</span><span class="sxs-lookup"><span data-stu-id="6f93c-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-277">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="6f93c-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6f93c-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6f93c-279">(28)</span><span class="sxs-lookup"><span data-stu-id="6f93c-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-280">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="6f93c-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6f93c-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6f93c-282">(29)</span><span class="sxs-lookup"><span data-stu-id="6f93c-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-283">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="6f93c-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6f93c-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6f93c-285">(30)</span><span class="sxs-lookup"><span data-stu-id="6f93c-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-286">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="6f93c-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6f93c-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="6f93c-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6f93c-288">1-31</span><span class="sxs-lookup"><span data-stu-id="6f93c-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-289">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="6f93c-289">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f93c-290">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="6f93c-290">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-291">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6f93c-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-293">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6f93c-293">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-294">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="6f93c-294">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6f93c-295">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-296">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6f93c-296">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f93c-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-299">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f93c-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-300">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="6f93c-300">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6f93c-301">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="6f93c-301">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6f93c-302">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-303">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6f93c-303">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f93c-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-306">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="6f93c-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-307">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6f93c-307">Textual description of the object.</span></span>

<span data-ttu-id="6f93c-308">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f93c-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-309">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="6f93c-309">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f93c-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-312">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f93c-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-313">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="6f93c-313">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="6f93c-314">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-315">**дмасуппорт**</span><span class="sxs-lookup"><span data-stu-id="6f93c-315">**DMASupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-316">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6f93c-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-318">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Параллельные порты DMTF \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="6f93c-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Parallel Ports\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-319">Если **значение равно true**, то поддерживается прямой доступ к памяти (DMA).</span><span class="sxs-lookup"><span data-stu-id="6f93c-319">If **TRUE**, direct memory access (DMA) is supported.</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-320">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="6f93c-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-321">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6f93c-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-323">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="6f93c-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="6f93c-324">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6f93c-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f93c-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-328">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="6f93c-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="6f93c-329">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-330">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6f93c-330">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-331">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6f93c-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-333">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="6f93c-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-334">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="6f93c-334">Date and time the object was installed.</span></span> <span data-ttu-id="6f93c-335">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="6f93c-335">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6f93c-336">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f93c-336">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-337">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="6f93c-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-338">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f93c-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-340">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="6f93c-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6f93c-341">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-342">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="6f93c-342">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-343">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f93c-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-345">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="6f93c-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-346">Максимальное количество напрямую обрабатываемых сущностей, поддерживаемых контроллером.</span><span class="sxs-lookup"><span data-stu-id="6f93c-346">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="6f93c-347">Если число неизвестно или неограниченно, следует использовать значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="6f93c-347">A value of 0 (zero) should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="6f93c-348">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="6f93c-348">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-349">**Name**</span><span class="sxs-lookup"><span data-stu-id="6f93c-349">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-350">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f93c-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-352">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="6f93c-352">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-353">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="6f93c-353">Label by which the object is known.</span></span> <span data-ttu-id="6f93c-354">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="6f93c-354">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6f93c-355">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f93c-355">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-356">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6f93c-356">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-357">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f93c-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-359">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6f93c-359">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-360">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="6f93c-360">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="6f93c-361">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6f93c-362">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6f93c-362">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-363">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="6f93c-363">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-364">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="6f93c-364">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-366">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="6f93c-366">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="6f93c-367">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-367">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f93c-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="6f93c-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6f93c-369"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="6f93c-369"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6f93c-370"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="6f93c-370"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6f93c-371"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="6f93c-371"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-372">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="6f93c-372">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6f93c-373"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="6f93c-373"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-374">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="6f93c-374">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6f93c-375"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="6f93c-375"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-376">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="6f93c-376">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="6f93c-377">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="6f93c-377">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="6f93c-378">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="6f93c-378">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6f93c-379"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="6f93c-379"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-380">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="6f93c-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6f93c-381"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="6f93c-381"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6f93c-382">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="6f93c-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6f93c-383">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="6f93c-383">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-384">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="6f93c-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-386">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="6f93c-386">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="6f93c-387">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="6f93c-387">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="6f93c-388">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="6f93c-388">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="6f93c-389">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="6f93c-389">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="6f93c-390">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-391">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="6f93c-391">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-392">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f93c-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-394">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="6f93c-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-395">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="6f93c-395">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="6f93c-396">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="6f93c-396">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="6f93c-397">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6f93c-397">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6f93c-398">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6f93c-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f93c-399">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="6f93c-399">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="6f93c-400">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="6f93c-400">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="6f93c-401">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="6f93c-401">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="6f93c-402">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="6f93c-402">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="6f93c-403">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="6f93c-403">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="6f93c-404">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="6f93c-404">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="6f93c-405">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="6f93c-405">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="6f93c-406">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="6f93c-406">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="6f93c-407">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="6f93c-407">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="6f93c-408">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="6f93c-408">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="6f93c-409">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="6f93c-409">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="6f93c-410">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="6f93c-410">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="6f93c-411">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="6f93c-411">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="6f93c-412">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="6f93c-412">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="6f93c-413">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="6f93c-413">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="6f93c-414">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="6f93c-414">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="6f93c-415">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="6f93c-415">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="6f93c-416">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="6f93c-416">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="6f93c-417">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="6f93c-417">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="6f93c-418">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="6f93c-418">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="6f93c-419">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="6f93c-419">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="6f93c-420">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="6f93c-420">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="6f93c-421">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="6f93c-421">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="6f93c-422">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="6f93c-422">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="6f93c-423">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="6f93c-423">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="6f93c-424">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="6f93c-424">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="6f93c-425">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="6f93c-425">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="6f93c-426">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="6f93c-426">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="6f93c-427">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="6f93c-427">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="6f93c-428">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="6f93c-428">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="6f93c-429">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="6f93c-429">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="6f93c-430">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="6f93c-430">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="6f93c-431">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="6f93c-431">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="6f93c-432">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="6f93c-432">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="6f93c-433">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="6f93c-433">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="6f93c-434">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="6f93c-434">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="6f93c-435">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="6f93c-435">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="6f93c-436">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="6f93c-436">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="6f93c-437">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="6f93c-437">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="6f93c-438">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="6f93c-438">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="6f93c-439">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="6f93c-439">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="6f93c-440">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="6f93c-440">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="6f93c-441">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="6f93c-441">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="6f93c-442">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="6f93c-442">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="6f93c-443">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="6f93c-443">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="6f93c-444">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="6f93c-444">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f93c-445">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="6f93c-445">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-446">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f93c-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-447">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-448">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="6f93c-448">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-449">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="6f93c-449">Current status of the object.</span></span> <span data-ttu-id="6f93c-450">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6f93c-450">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6f93c-451">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="6f93c-451">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6f93c-452">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="6f93c-452">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6f93c-453">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="6f93c-453">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6f93c-454">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="6f93c-454">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f93c-455">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="6f93c-455">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6f93c-456">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="6f93c-456">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6f93c-457">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="6f93c-457">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6f93c-458">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="6f93c-458">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6f93c-459">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="6f93c-459">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6f93c-460">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="6f93c-460">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6f93c-461">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="6f93c-461">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6f93c-462">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="6f93c-462">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6f93c-463">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="6f93c-463">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f93c-464">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6f93c-464">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-465">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f93c-465">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-466">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-467">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="6f93c-467">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-468">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="6f93c-468">State of the logical device.</span></span> <span data-ttu-id="6f93c-469">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="6f93c-469">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6f93c-470">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6f93c-471">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="6f93c-471">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6f93c-472">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="6f93c-472">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6f93c-473">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="6f93c-473">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6f93c-474">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="6f93c-474">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6f93c-475">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="6f93c-475">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f93c-476">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="6f93c-476">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-477">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f93c-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-478">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-479">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f93c-479">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-480">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="6f93c-480">Scoping system's creation class name.</span></span>

<span data-ttu-id="6f93c-481">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-481">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-482">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6f93c-482">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-483">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6f93c-483">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-484">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-485">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6f93c-485">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-486">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="6f93c-486">Scoping system's name.</span></span>

<span data-ttu-id="6f93c-487">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="6f93c-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f93c-488">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="6f93c-488">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f93c-489">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6f93c-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6f93c-490">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f93c-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f93c-491">Дата и время последнего сброса контроллера, означающее, что контроллер был отключен или инициализирован повторно.</span><span class="sxs-lookup"><span data-stu-id="6f93c-491">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="6f93c-492">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="6f93c-492">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f93c-493">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f93c-493">Remarks</span></span>

<span data-ttu-id="6f93c-494">Класс **CIM \_ параллелконтроллер** является производным от [**\_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="6f93c-494">The **CIM\_ParallelController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="6f93c-495">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="6f93c-495">WMI does not implement this class.</span></span> <span data-ttu-id="6f93c-496">Сведения о классах WMI, которые являются производными от **CIM \_ параллелконтроллер**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6f93c-496">For WMI classes that are derived from **CIM\_ParallelController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6f93c-497">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6f93c-497">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6f93c-498">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6f93c-498">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f93c-499">Требования</span><span class="sxs-lookup"><span data-stu-id="6f93c-499">Requirements</span></span>



| <span data-ttu-id="6f93c-500">Требование</span><span class="sxs-lookup"><span data-stu-id="6f93c-500">Requirement</span></span> | <span data-ttu-id="6f93c-501">Значение</span><span class="sxs-lookup"><span data-stu-id="6f93c-501">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f93c-502">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f93c-502">Minimum supported client</span></span><br/> | <span data-ttu-id="6f93c-503">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f93c-503">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f93c-504">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f93c-504">Minimum supported server</span></span><br/> | <span data-ttu-id="6f93c-505">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f93c-505">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f93c-506">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6f93c-506">Namespace</span></span><br/>                | <span data-ttu-id="6f93c-507">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6f93c-507">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6f93c-508">MOF</span><span class="sxs-lookup"><span data-stu-id="6f93c-508">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f93c-509"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f93c-509"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f93c-510">DLL</span><span class="sxs-lookup"><span data-stu-id="6f93c-510">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f93c-511"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f93c-511"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f93c-512">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f93c-512">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f93c-513">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="6f93c-513">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

