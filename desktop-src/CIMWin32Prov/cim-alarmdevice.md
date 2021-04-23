---
description: Класс CIM \_ алармдевице — это сигнальное устройство, которое отправляет звуковые или видимые события, связанные с проблемной ситуацией.
ms.assetid: 1f64aea4-d0a4-480b-9802-e2c21e71c754
ms.tgt_platform: multiple
title: Класс CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice
- CIM_AlarmDevice.Caption
- CIM_AlarmDevice.Description
- CIM_AlarmDevice.InstallDate
- CIM_AlarmDevice.Name
- CIM_AlarmDevice.Status
- CIM_AlarmDevice.Availability
- CIM_AlarmDevice.ConfigManagerErrorCode
- CIM_AlarmDevice.ConfigManagerUserConfig
- CIM_AlarmDevice.CreationClassName
- CIM_AlarmDevice.DeviceID
- CIM_AlarmDevice.PowerManagementCapabilities
- CIM_AlarmDevice.ErrorCleared
- CIM_AlarmDevice.ErrorDescription
- CIM_AlarmDevice.LastErrorCode
- CIM_AlarmDevice.PNPDeviceID
- CIM_AlarmDevice.PowerManagementSupported
- CIM_AlarmDevice.StatusInfo
- CIM_AlarmDevice.SystemCreationClassName
- CIM_AlarmDevice.SystemName
- CIM_AlarmDevice.AudibleAlarm
- CIM_AlarmDevice.Urgency
- CIM_AlarmDevice.VisibleAlarm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 622a6031f36140e23514b925835cebae84b35025
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539074"
---
# <a name="cim_alarmdevice-class"></a><span data-ttu-id="2b1e8-103">\_Класс CIM алармдевице</span><span class="sxs-lookup"><span data-stu-id="2b1e8-103">CIM\_AlarmDevice class</span></span>

<span data-ttu-id="2b1e8-104">Класс **CIM \_ алармдевице** — это сигнальное устройство, которое отправляет звуковые или видимые события, связанные с проблемной ситуацией.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-104">The **CIM\_AlarmDevice** class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

<span data-ttu-id="2b1e8-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2b1e8-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-106">Properties are listed in alphabetic order, not MOF order.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b1e8-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2b1e8-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2b1e8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2b1e8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b1e8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B66-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AlarmDevice : CIM_LogicalDevice
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
  boolean  AudibleAlarm;
  uint16   Urgency;
  boolean  VisibleAlarm;
};
```

## <a name="members"></a><span data-ttu-id="2b1e8-110">Члены</span><span class="sxs-lookup"><span data-stu-id="2b1e8-110">Members</span></span>

<span data-ttu-id="2b1e8-111">Класс **CIM \_ алармдевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2b1e8-111">The **CIM\_AlarmDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="2b1e8-112">Методы</span><span class="sxs-lookup"><span data-stu-id="2b1e8-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2b1e8-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b1e8-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2b1e8-114">Методы</span><span class="sxs-lookup"><span data-stu-id="2b1e8-114">Methods</span></span>

<span data-ttu-id="2b1e8-115">Класс **CIM \_ алармдевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-115">The **CIM\_AlarmDevice** class has these methods.</span></span>



| <span data-ttu-id="2b1e8-116">Метод</span><span class="sxs-lookup"><span data-stu-id="2b1e8-116">Method</span></span>                                                                 | <span data-ttu-id="2b1e8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2b1e8-117">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b1e8-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-118">**Reset**</span></span>](reset-method-in-class-cim-alarmdevice.md)                 | <span data-ttu-id="2b1e8-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-119">Requests a logical device reset.</span></span> <span data-ttu-id="2b1e8-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-120">Not implemented by WMI.</span></span><br/>                                                                     |
| [<span data-ttu-id="2b1e8-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-alarmdevice.md) | <span data-ttu-id="2b1e8-122">Задает требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-122">Sets the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="2b1e8-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-123">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="2b1e8-124">**сетурженци**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-124">**SetUrgency**</span></span>](seturgency-method-in-class-cim-alarmdevice.md)       | <span data-ttu-id="2b1e8-125">Задает требуемый уровень срочности сигнала.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-125">Sets the desired urgency level for the alarm.</span></span> <span data-ttu-id="2b1e8-126">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-126">Not implemented by WMI.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="2b1e8-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="2b1e8-127">Properties</span></span>

<span data-ttu-id="2b1e8-128">Класс **CIM \_ алармдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-128">The **CIM\_AlarmDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b1e8-129">**аудиблеаларм**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-129">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-130">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-132">**Значение true** показывает, что сигнал является звуковым.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-132">If **TRUE**, the alarm is audible.</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-133">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-134">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-136">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-137">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-137">Availability and status of the device.</span></span>

<span data-ttu-id="2b1e8-138">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2b1e8-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b1e8-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2b1e8-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2b1e8-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2b1e8-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2b1e8-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2b1e8-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2b1e8-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2b1e8-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2b1e8-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2b1e8-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2b1e8-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2b1e8-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-152">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2b1e8-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-154">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2b1e8-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-156">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-156">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2b1e8-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2b1e8-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-159">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2b1e8-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-161">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2b1e8-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-163">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2b1e8-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-165">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2b1e8-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-167">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2b1e8-168">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-171">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-172">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-172">A short textual description of the object.</span></span>

<span data-ttu-id="2b1e8-173">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b1e8-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-174">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-175">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-177">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-178">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2b1e8-179">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2b1e8-180">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-180">**This device is working properly.**</span></span> <span data-ttu-id="2b1e8-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-181">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2b1e8-182">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-182">**This device is not configured correctly.**</span></span> <span data-ttu-id="2b1e8-183">(1)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-183">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2b1e8-184">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-184">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2b1e8-185">(2)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-185">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2b1e8-186">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-186">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2b1e8-187">(3)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-187">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2b1e8-188">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-188">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2b1e8-189">(4)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-189">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2b1e8-190">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-190">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2b1e8-191">(5)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-191">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2b1e8-192">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-192">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2b1e8-193"> (6)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-193">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2b1e8-194">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-194">**Cannot filter.**</span></span> <span data-ttu-id="2b1e8-195">(7)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2b1e8-196">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-196">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2b1e8-197">(8)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-197">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2b1e8-198">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-198">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2b1e8-199">(9)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-199">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2b1e8-200">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-200">**This device cannot start.**</span></span> <span data-ttu-id="2b1e8-201">(10)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-201">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2b1e8-202">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-202">**This device failed.**</span></span> <span data-ttu-id="2b1e8-203">(11)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-203">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2b1e8-204">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-204">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2b1e8-205">(12)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-205">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2b1e8-206">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-206">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2b1e8-207">(13)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-207">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2b1e8-208">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-208">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2b1e8-209">(14)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-209">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2b1e8-210">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-210">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2b1e8-211">(15)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-211">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2b1e8-212">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-212">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2b1e8-213">(16)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-213">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2b1e8-214">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-214">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2b1e8-215">(17)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-215">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2b1e8-216">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-216">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2b1e8-217">(18)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-217">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2b1e8-218">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-218">**Failure using the VxD loader.**</span></span> <span data-ttu-id="2b1e8-219">(19)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-219">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2b1e8-220">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-220">**Your registry might be corrupted.**</span></span> <span data-ttu-id="2b1e8-221">(20)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-221">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2b1e8-222">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-222">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2b1e8-223">(21)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-223">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2b1e8-224">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-224">**This device is disabled.**</span></span> <span data-ttu-id="2b1e8-225">(22)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-225">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2b1e8-226">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-226">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2b1e8-227">(23)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-227">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2b1e8-228">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-228">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2b1e8-229">(24)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-229">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2b1e8-230">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-230">**Windows is still setting up this device.**</span></span> <span data-ttu-id="2b1e8-231">(25)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-231">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2b1e8-232">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-232">**Windows is still setting up this device.**</span></span> <span data-ttu-id="2b1e8-233">(26)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-233">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2b1e8-234">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-234">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2b1e8-235">(27)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-235">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2b1e8-236">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-236">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2b1e8-237">(28)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-237">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2b1e8-238">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-238">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2b1e8-239">(29)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-239">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2b1e8-240">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-240">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2b1e8-241">(30)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-241">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2b1e8-242">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-242">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2b1e8-243">1-31</span><span class="sxs-lookup"><span data-stu-id="2b1e8-243">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2b1e8-244">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-244">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-245">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-247">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-247">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-248">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-248">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2b1e8-249">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-249">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-250">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-250">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-253">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-253">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-254">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-254">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2b1e8-255">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-255">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2b1e8-256">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-256">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-257">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-257">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-258">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-260">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-260">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-261">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-261">A textual description of the object.</span></span>

<span data-ttu-id="2b1e8-262">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b1e8-262">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-263">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-263">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-265">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-266">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-266">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-267">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-267">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2b1e8-268">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-268">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-269">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-269">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-270">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-271">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-272">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-272">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2b1e8-273">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-273">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-274">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-274">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-275">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-277">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-277">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2b1e8-278">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-280">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-282">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-282">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-283">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-283">Indicates when the object was installed.</span></span> <span data-ttu-id="2b1e8-284">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-284">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2b1e8-285">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b1e8-285">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-286">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-286">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-287">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-289">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-289">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2b1e8-290">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-291">**Name**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-291">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-294">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-294">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-295">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-295">Label by which the object is known.</span></span> <span data-ttu-id="2b1e8-296">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-296">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2b1e8-297">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b1e8-297">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-298">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-298">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-299">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-301">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-301">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-302">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-302">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="2b1e8-303">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2b1e8-303">Example: "\*PNP030b"</span></span>

<span data-ttu-id="2b1e8-304">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-305">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-305">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-306">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="2b1e8-306">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-308">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-308">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="2b1e8-309">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b1e8-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-311">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-311">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2b1e8-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-312"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-313">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-313">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2b1e8-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-314"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-315">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-315">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2b1e8-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-316"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-317">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-317">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2b1e8-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-318"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-319">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-319">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2b1e8-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-320"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-321">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="2b1e8-321">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="2b1e8-322">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-322">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="2b1e8-323">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2b1e8-323">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2b1e8-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-324"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-325">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="2b1e8-325">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2b1e8-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-326"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-327">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2b1e8-328">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-328">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-329">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-331">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-331">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2b1e8-332">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="2b1e8-332">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2b1e8-333">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-333">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2b1e8-334">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="2b1e8-334">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2b1e8-335">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-336">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-339">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-339">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-340">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-340">String that indicates the current status of the object.</span></span> <span data-ttu-id="2b1e8-341">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-341">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2b1e8-342">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="2b1e8-342">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2b1e8-343">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="2b1e8-343">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2b1e8-344">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="2b1e8-344">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2b1e8-345">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-345">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2b1e8-346">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-346">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2b1e8-347">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2b1e8-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2b1e8-348">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="2b1e8-348">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2b1e8-349">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-349">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2b1e8-350">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-350">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2b1e8-351">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-351">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b1e8-352">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-352">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2b1e8-353">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-353">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2b1e8-354">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-354">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2b1e8-355">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-355">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2b1e8-356">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-356">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2b1e8-357">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-357">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2b1e8-358">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-358">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2b1e8-359">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-359">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2b1e8-360">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-360">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2b1e8-361">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-361">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-362">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-364">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2b1e8-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-365">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-365">State of the logical device.</span></span> <span data-ttu-id="2b1e8-366">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="2b1e8-366">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="2b1e8-367">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2b1e8-368">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-368">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b1e8-369">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-369">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2b1e8-370">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-370">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2b1e8-371">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-371">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2b1e8-372">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-372">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2b1e8-373">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-373">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-374">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-376">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-376">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-377">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-377">The scoping system's creation class name.</span></span>

<span data-ttu-id="2b1e8-378">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-379">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-379">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-380">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-382">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-382">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-383">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-383">The scoping system's name.</span></span>

<span data-ttu-id="2b1e8-384">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-384">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b1e8-385">**"Срочность";**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-385">**Urgency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-386">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-386">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-388">Перечислимое значение, указывающее относительную частоту, с которой будильник мигает, вибратес или выдает звуковые сигналы.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-388">Enumerated value that indicates the relative frequency at which the alarm flashes, vibrates, or emits audible tones.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b1e8-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-389"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-390">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-390">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2b1e8-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-391"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-392">Другое</span><span class="sxs-lookup"><span data-stu-id="2b1e8-392">Other.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2b1e8-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-394">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-394">Not supported.</span></span>

</dd> <dt>

<span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>

<span data-ttu-id="2b1e8-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Информационные** (3)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-395"><span id="Informational"></span><span id="informational"></span><span id="INFORMATIONAL"></span>**Informational** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-396">Извещен.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-396">Informational.</span></span>

</dd> <dt>

<span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>

<span data-ttu-id="2b1e8-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Не критическое** (4)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-397"><span id="Non-Critical"></span><span id="non-critical"></span><span id="NON-CRITICAL"></span>**Non-Critical** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-398">Не является критическим.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-398">Non-critical.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="2b1e8-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (5)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-399"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-400">Критическое —</span><span class="sxs-lookup"><span data-stu-id="2b1e8-400">Critical.</span></span>

</dd> <dt>

<span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>

<span data-ttu-id="2b1e8-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Невосстанавливаемый** (6)</span><span class="sxs-lookup"><span data-stu-id="2b1e8-401"><span id="Unrecoverable"></span><span id="unrecoverable"></span><span id="UNRECOVERABLE"></span>**Unrecoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2b1e8-402">Неустранимая.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-402">Unrecoverable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2b1e8-403">**висиблеаларм**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-403">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b1e8-404">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b1e8-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2b1e8-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b1e8-406">**Значение true** показывает, что сигнал является видимым.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-406">If **TRUE**, the alarm is visible.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b1e8-407">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b1e8-407">Remarks</span></span>

<span data-ttu-id="2b1e8-408">Класс **CIM \_ алармдевице** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-408">The **CIM\_AlarmDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2b1e8-409">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-409">WMI does not implement this class.</span></span>

<span data-ttu-id="2b1e8-410">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-410">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2b1e8-411">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="2b1e8-411">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b1e8-412">Требования</span><span class="sxs-lookup"><span data-stu-id="2b1e8-412">Requirements</span></span>



| <span data-ttu-id="2b1e8-413">Требование</span><span class="sxs-lookup"><span data-stu-id="2b1e8-413">Requirement</span></span> | <span data-ttu-id="2b1e8-414">Значение</span><span class="sxs-lookup"><span data-stu-id="2b1e8-414">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b1e8-415">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b1e8-415">Minimum supported client</span></span><br/> | <span data-ttu-id="2b1e8-416">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b1e8-416">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b1e8-417">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b1e8-417">Minimum supported server</span></span><br/> | <span data-ttu-id="2b1e8-418">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b1e8-418">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b1e8-419">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2b1e8-419">Namespace</span></span><br/>                | <span data-ttu-id="2b1e8-420">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2b1e8-420">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2b1e8-421">MOF</span><span class="sxs-lookup"><span data-stu-id="2b1e8-421">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b1e8-422"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b1e8-422"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b1e8-423">DLL</span><span class="sxs-lookup"><span data-stu-id="2b1e8-423">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b1e8-424"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b1e8-424"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b1e8-425">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b1e8-425">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b1e8-426">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="2b1e8-426">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

