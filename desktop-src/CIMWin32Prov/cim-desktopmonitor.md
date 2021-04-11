---
description: Класс CIM \_ десктопмонитор представляет возможности и управление логическим устройством с настольным монитором (CRT).
ms.assetid: dc65aa38-5255-4a40-8ffc-f05f9af71dc6
ms.tgt_platform: multiple
title: Класс CIM_DesktopMonitor (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DesktopMonitor
- CIM_DesktopMonitor.Caption
- CIM_DesktopMonitor.Description
- CIM_DesktopMonitor.InstallDate
- CIM_DesktopMonitor.Name
- CIM_DesktopMonitor.Status
- CIM_DesktopMonitor.Availability
- CIM_DesktopMonitor.ConfigManagerErrorCode
- CIM_DesktopMonitor.ConfigManagerUserConfig
- CIM_DesktopMonitor.CreationClassName
- CIM_DesktopMonitor.DeviceID
- CIM_DesktopMonitor.PowerManagementCapabilities
- CIM_DesktopMonitor.ErrorCleared
- CIM_DesktopMonitor.ErrorDescription
- CIM_DesktopMonitor.LastErrorCode
- CIM_DesktopMonitor.PNPDeviceID
- CIM_DesktopMonitor.PowerManagementSupported
- CIM_DesktopMonitor.StatusInfo
- CIM_DesktopMonitor.SystemCreationClassName
- CIM_DesktopMonitor.SystemName
- CIM_DesktopMonitor.IsLocked
- CIM_DesktopMonitor.Bandwidth
- CIM_DesktopMonitor.DisplayType
- CIM_DesktopMonitor.ScreenHeight
- CIM_DesktopMonitor.ScreenWidth
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b22d0b681491bbddf0ee357b394da5f1a77aa0e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262674"
---
# <a name="cim_desktopmonitor-class-cimwin32-wmi-providers"></a><span data-ttu-id="a2d73-103">Класс CIM_DesktopMonitor (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="a2d73-103">CIM_DesktopMonitor class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a2d73-104">Класс **CIM \_ десктопмонитор** представляет возможности и управление логическим устройством с настольным монитором (CRT).</span><span class="sxs-lookup"><span data-stu-id="a2d73-104">The **CIM\_DesktopMonitor** class represents the capabilities and management of the desktop monitor (CRT) logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2d73-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="a2d73-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a2d73-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a2d73-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a2d73-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a2d73-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a2d73-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a2d73-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2d73-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2d73-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE8-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_DesktopMonitor : CIM_Display
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
  boolean  IsLocked;
  uint32   Bandwidth;
  uint16   DisplayType;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
};
```

## <a name="members"></a><span data-ttu-id="a2d73-110">Члены</span><span class="sxs-lookup"><span data-stu-id="a2d73-110">Members</span></span>

<span data-ttu-id="a2d73-111">Класс **CIM \_ десктопмонитор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a2d73-111">The **CIM\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="a2d73-112">Методы</span><span class="sxs-lookup"><span data-stu-id="a2d73-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a2d73-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a2d73-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a2d73-114">Методы</span><span class="sxs-lookup"><span data-stu-id="a2d73-114">Methods</span></span>

<span data-ttu-id="a2d73-115">Класс **CIM \_ десктопмонитор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a2d73-115">The **CIM\_DesktopMonitor** class has these methods.</span></span>



| <span data-ttu-id="a2d73-116">Метод</span><span class="sxs-lookup"><span data-stu-id="a2d73-116">Method</span></span>                                                                    | <span data-ttu-id="a2d73-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a2d73-117">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2d73-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="a2d73-118">**Reset**</span></span>](reset-method-in-class-cim-desktopmonitor.md)                 | <span data-ttu-id="a2d73-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a2d73-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="a2d73-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="a2d73-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="a2d73-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a2d73-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-desktopmonitor.md) | <span data-ttu-id="a2d73-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="a2d73-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="a2d73-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="a2d73-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a2d73-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="a2d73-124">Properties</span></span>

<span data-ttu-id="a2d73-125">Класс **CIM \_ десктопмонитор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a2d73-125">The **CIM\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2d73-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="a2d73-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2d73-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="a2d73-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="a2d73-130">Availability and status of the device.</span></span>

<span data-ttu-id="a2d73-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a2d73-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="a2d73-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2d73-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="a2d73-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a2d73-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="a2d73-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a2d73-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="a2d73-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a2d73-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="a2d73-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a2d73-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="a2d73-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a2d73-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="a2d73-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a2d73-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="a2d73-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a2d73-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="a2d73-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a2d73-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="a2d73-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a2d73-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="a2d73-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a2d73-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="a2d73-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a2d73-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="a2d73-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="a2d73-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a2d73-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="a2d73-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="a2d73-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a2d73-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="a2d73-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="a2d73-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a2d73-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="a2d73-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a2d73-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="a2d73-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="a2d73-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a2d73-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="a2d73-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="a2d73-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a2d73-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="a2d73-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="a2d73-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a2d73-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="a2d73-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="a2d73-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a2d73-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="a2d73-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="a2d73-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a2d73-161">**Пропускная способность**</span><span class="sxs-lookup"><span data-stu-id="a2d73-161">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2d73-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-164">Квалификаторы: [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("мегагерц")</span><span class="sxs-lookup"><span data-stu-id="a2d73-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-165">Пропускная способность монитора в МГц.</span><span class="sxs-lookup"><span data-stu-id="a2d73-165">Monitor's bandwidth in MHz.</span></span> <span data-ttu-id="a2d73-166">Если значение неизвестно, используйте 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="a2d73-166">If unknown, use 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-167">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a2d73-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2d73-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-170">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a2d73-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-171">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a2d73-171">A short textual description of the object.</span></span>

<span data-ttu-id="a2d73-172">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2d73-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-173">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="a2d73-173">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-174">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2d73-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-176">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a2d73-176">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-177">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a2d73-177">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a2d73-178">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-178">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a2d73-179">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-179">**This device is working properly.**</span></span> <span data-ttu-id="a2d73-180"> (0)</span><span class="sxs-lookup"><span data-stu-id="a2d73-180">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a2d73-181">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-181">**This device is not configured correctly.**</span></span> <span data-ttu-id="a2d73-182">(1)</span><span class="sxs-lookup"><span data-stu-id="a2d73-182">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a2d73-183">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-183">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a2d73-184">(2)</span><span class="sxs-lookup"><span data-stu-id="a2d73-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a2d73-185">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-185">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a2d73-186">(3)</span><span class="sxs-lookup"><span data-stu-id="a2d73-186">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a2d73-187">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-187">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a2d73-188">(4)</span><span class="sxs-lookup"><span data-stu-id="a2d73-188">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a2d73-189">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-189">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a2d73-190">(5)</span><span class="sxs-lookup"><span data-stu-id="a2d73-190">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a2d73-191">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-191">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a2d73-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="a2d73-192">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a2d73-193">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-193">**Cannot filter.**</span></span> <span data-ttu-id="a2d73-194">(7)</span><span class="sxs-lookup"><span data-stu-id="a2d73-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a2d73-195">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-195">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a2d73-196">(8)</span><span class="sxs-lookup"><span data-stu-id="a2d73-196">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a2d73-197">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-197">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a2d73-198">(9)</span><span class="sxs-lookup"><span data-stu-id="a2d73-198">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a2d73-199">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-199">**This device cannot start.**</span></span> <span data-ttu-id="a2d73-200">(10)</span><span class="sxs-lookup"><span data-stu-id="a2d73-200">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a2d73-201">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-201">**This device failed.**</span></span> <span data-ttu-id="a2d73-202">(11)</span><span class="sxs-lookup"><span data-stu-id="a2d73-202">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a2d73-203">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-203">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a2d73-204">(12)</span><span class="sxs-lookup"><span data-stu-id="a2d73-204">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a2d73-205">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-205">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a2d73-206">(13)</span><span class="sxs-lookup"><span data-stu-id="a2d73-206">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a2d73-207">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-207">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a2d73-208">(14)</span><span class="sxs-lookup"><span data-stu-id="a2d73-208">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a2d73-209">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-209">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a2d73-210">(15)</span><span class="sxs-lookup"><span data-stu-id="a2d73-210">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a2d73-211">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-211">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a2d73-212">(16)</span><span class="sxs-lookup"><span data-stu-id="a2d73-212">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a2d73-213">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-213">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a2d73-214">(17)</span><span class="sxs-lookup"><span data-stu-id="a2d73-214">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a2d73-215">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-215">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a2d73-216">(18)</span><span class="sxs-lookup"><span data-stu-id="a2d73-216">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a2d73-217">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-217">**Failure using the VxD loader.**</span></span> <span data-ttu-id="a2d73-218">(19)</span><span class="sxs-lookup"><span data-stu-id="a2d73-218">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a2d73-219">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-219">**Your registry might be corrupted.**</span></span> <span data-ttu-id="a2d73-220">(20)</span><span class="sxs-lookup"><span data-stu-id="a2d73-220">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a2d73-221">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-221">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a2d73-222">(21)</span><span class="sxs-lookup"><span data-stu-id="a2d73-222">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a2d73-223">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-223">**This device is disabled.**</span></span> <span data-ttu-id="a2d73-224">(22)</span><span class="sxs-lookup"><span data-stu-id="a2d73-224">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a2d73-225">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-225">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a2d73-226">(23)</span><span class="sxs-lookup"><span data-stu-id="a2d73-226">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a2d73-227">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-227">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a2d73-228">(24)</span><span class="sxs-lookup"><span data-stu-id="a2d73-228">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a2d73-229">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-229">**Windows is still setting up this device.**</span></span> <span data-ttu-id="a2d73-230">(25)</span><span class="sxs-lookup"><span data-stu-id="a2d73-230">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a2d73-231">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-231">**Windows is still setting up this device.**</span></span> <span data-ttu-id="a2d73-232">(26)</span><span class="sxs-lookup"><span data-stu-id="a2d73-232">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a2d73-233">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-233">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a2d73-234">(27)</span><span class="sxs-lookup"><span data-stu-id="a2d73-234">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a2d73-235">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-235">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a2d73-236">(28)</span><span class="sxs-lookup"><span data-stu-id="a2d73-236">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a2d73-237">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-237">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a2d73-238">(29)</span><span class="sxs-lookup"><span data-stu-id="a2d73-238">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a2d73-239">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-239">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a2d73-240">(30)</span><span class="sxs-lookup"><span data-stu-id="a2d73-240">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a2d73-241">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="a2d73-241">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a2d73-242">1-31</span><span class="sxs-lookup"><span data-stu-id="a2d73-242">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2d73-243">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="a2d73-243">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-244">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2d73-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-246">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a2d73-246">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-247">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a2d73-247">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a2d73-248">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-248">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-249">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a2d73-249">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-250">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2d73-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-252">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a2d73-252">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-253">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a2d73-253">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a2d73-254">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="a2d73-254">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a2d73-255">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-255">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-256">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a2d73-256">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2d73-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-259">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="a2d73-259">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-260">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a2d73-260">A textual description of the object.</span></span>

<span data-ttu-id="a2d73-261">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2d73-261">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-262">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a2d73-262">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-263">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2d73-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-265">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a2d73-265">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-266">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a2d73-266">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="a2d73-267">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-267">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-268">**дисплайтипе**</span><span class="sxs-lookup"><span data-stu-id="a2d73-268">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-269">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2d73-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-271">Тип настольного монитора или CRT.</span><span class="sxs-lookup"><span data-stu-id="a2d73-271">Type of desktop monitor or CRT.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2d73-272">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a2d73-272">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a2d73-273">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="a2d73-273">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="a2d73-274">**Цвет для многосканирования** (2)</span><span class="sxs-lookup"><span data-stu-id="a2d73-274">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="a2d73-275">**Многосканерная Монохромная** (3)</span><span class="sxs-lookup"><span data-stu-id="a2d73-275">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="a2d73-276">**Фиксированный цвет частоты** (4)</span><span class="sxs-lookup"><span data-stu-id="a2d73-276">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="a2d73-277">**Фиксированная частота монохромных** (5)</span><span class="sxs-lookup"><span data-stu-id="a2d73-277">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2d73-278">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="a2d73-278">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-279">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2d73-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-281">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="a2d73-281">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="a2d73-282">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-283">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a2d73-283">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-284">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2d73-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-286">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="a2d73-286">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="a2d73-287">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-288">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a2d73-288">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-289">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a2d73-289">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-291">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="a2d73-291">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-292">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="a2d73-292">Indicates when the object was installed.</span></span> <span data-ttu-id="a2d73-293">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="a2d73-293">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a2d73-294">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2d73-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-295">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="a2d73-295">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-296">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2d73-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-298">**Значение true** показывает, что устройство заблокировано, что предотвращает ввод или вывод пользователя.</span><span class="sxs-lookup"><span data-stu-id="a2d73-298">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="a2d73-299">Это свойство наследуется от [**CIM \_ усердевице**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a2d73-299">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-300">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="a2d73-300">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-301">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2d73-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-303">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="a2d73-303">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a2d73-304">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-305">**Name**</span><span class="sxs-lookup"><span data-stu-id="a2d73-305">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-306">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2d73-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-308">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="a2d73-308">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-309">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="a2d73-309">Label by which the object is known.</span></span> <span data-ttu-id="a2d73-310">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="a2d73-310">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a2d73-311">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2d73-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-312">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a2d73-312">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2d73-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-315">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a2d73-315">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-316">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a2d73-316">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a2d73-317">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a2d73-317">Example: "\*PNP030b"</span></span>

<span data-ttu-id="a2d73-318">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-319">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="a2d73-319">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-320">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a2d73-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-322">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="a2d73-322">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="a2d73-323">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2d73-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a2d73-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-325">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="a2d73-325">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a2d73-326"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="a2d73-326"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-327">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="a2d73-327">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a2d73-328"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="a2d73-328"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-329">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="a2d73-329">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a2d73-330"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="a2d73-330"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-331">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="a2d73-331">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a2d73-332"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="a2d73-332"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-333">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="a2d73-333">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a2d73-334"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="a2d73-334"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-335">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="a2d73-335">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="a2d73-336">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="a2d73-336">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="a2d73-337">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="a2d73-337">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a2d73-338"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="a2d73-338"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-339">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="a2d73-339">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a2d73-340"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="a2d73-340"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a2d73-341">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="a2d73-341">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a2d73-342">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="a2d73-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-343">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a2d73-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-345">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="a2d73-345">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="a2d73-346">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="a2d73-346">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a2d73-347">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a2d73-347">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="a2d73-348">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="a2d73-348">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a2d73-349">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-350">**скринхеигхт**</span><span class="sxs-lookup"><span data-stu-id="a2d73-350">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-351">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2d73-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-353">Логическая высота дисплея в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="a2d73-353">Logical height of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-354">**скринвидс**</span><span class="sxs-lookup"><span data-stu-id="a2d73-354">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-355">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2d73-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-357">Логическая ширина дисплея в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="a2d73-357">Logical width of the display, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-358">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a2d73-358">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-359">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2d73-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-360">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-361">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="a2d73-361">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-362">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a2d73-362">String that indicates the current status of the object.</span></span> <span data-ttu-id="a2d73-363">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="a2d73-363">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a2d73-364">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="a2d73-364">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a2d73-365">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="a2d73-365">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a2d73-366">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="a2d73-366">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a2d73-367">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="a2d73-367">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a2d73-368">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="a2d73-368">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a2d73-369">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a2d73-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a2d73-370">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="a2d73-370">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a2d73-371">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="a2d73-371">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a2d73-372">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="a2d73-372">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a2d73-373">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="a2d73-373">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2d73-374">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="a2d73-374">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a2d73-375">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="a2d73-375">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a2d73-376">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="a2d73-376">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a2d73-377">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="a2d73-377">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a2d73-378">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="a2d73-378">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a2d73-379">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="a2d73-379">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a2d73-380">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="a2d73-380">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a2d73-381">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="a2d73-381">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a2d73-382">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="a2d73-382">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2d73-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a2d73-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-384">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a2d73-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-386">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a2d73-386">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-387">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a2d73-387">State of the logical device.</span></span> <span data-ttu-id="a2d73-388">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="a2d73-388">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="a2d73-389">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a2d73-390">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="a2d73-390">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a2d73-391">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="a2d73-391">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a2d73-392">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="a2d73-392">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a2d73-393">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="a2d73-393">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a2d73-394">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="a2d73-394">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a2d73-395">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="a2d73-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-396">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2d73-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-398">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a2d73-398">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-399">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="a2d73-399">The scoping system's creation class name.</span></span>

<span data-ttu-id="a2d73-400">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a2d73-401">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a2d73-401">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2d73-402">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a2d73-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a2d73-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2d73-404">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a2d73-404">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a2d73-405">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="a2d73-405">The scoping system's name.</span></span>

<span data-ttu-id="a2d73-406">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a2d73-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2d73-407">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2d73-407">Remarks</span></span>

<span data-ttu-id="a2d73-408">Класс **CIM \_ десктопмонитор** является производным от [**CIM- \_ дисплеев**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="a2d73-408">The **CIM\_DesktopMonitor** class is derived from [**CIM\_Display**](cim-display.md).</span></span>

<span data-ttu-id="a2d73-409">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="a2d73-409">WMI does not implement this class.</span></span> <span data-ttu-id="a2d73-410">Дополнительные сведения о классах, производных от **CIM \_ десктопмонитор**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a2d73-410">For more information about classes derived from **CIM\_DesktopMonitor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a2d73-411">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="a2d73-411">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a2d73-412">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a2d73-412">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2d73-413">Требования</span><span class="sxs-lookup"><span data-stu-id="a2d73-413">Requirements</span></span>



| <span data-ttu-id="a2d73-414">Требование</span><span class="sxs-lookup"><span data-stu-id="a2d73-414">Requirement</span></span> | <span data-ttu-id="a2d73-415">Значение</span><span class="sxs-lookup"><span data-stu-id="a2d73-415">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d73-416">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2d73-416">Minimum supported client</span></span><br/> | <span data-ttu-id="a2d73-417">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a2d73-417">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a2d73-418">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2d73-418">Minimum supported server</span></span><br/> | <span data-ttu-id="a2d73-419">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a2d73-419">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a2d73-420">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a2d73-420">Namespace</span></span><br/>                | <span data-ttu-id="a2d73-421">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a2d73-421">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a2d73-422">MOF</span><span class="sxs-lookup"><span data-stu-id="a2d73-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2d73-423"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2d73-423"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a2d73-424">DLL</span><span class="sxs-lookup"><span data-stu-id="a2d73-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2d73-425"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2d73-425"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2d73-426">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2d73-426">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d73-427">**\_Отображение CIM**</span><span class="sxs-lookup"><span data-stu-id="a2d73-427">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

