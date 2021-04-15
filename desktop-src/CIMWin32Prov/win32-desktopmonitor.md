---
description: Представляет тип монитора или устройства отображения, подключенного к компьютерной системе.
ms.assetid: 922be3c1-3c7b-4418-a72f-ab5ada91a7a4
ms.tgt_platform: multiple
title: Класс Win32_DesktopMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DesktopMonitor
- Win32_DesktopMonitor.Reset
- Win32_DesktopMonitor.SetPowerState
- Win32_DesktopMonitor.Availability
- Win32_DesktopMonitor.Bandwidth
- Win32_DesktopMonitor.Caption
- Win32_DesktopMonitor.ConfigManagerErrorCode
- Win32_DesktopMonitor.ConfigManagerUserConfig
- Win32_DesktopMonitor.CreationClassName
- Win32_DesktopMonitor.Description
- Win32_DesktopMonitor.DeviceID
- Win32_DesktopMonitor.DisplayType
- Win32_DesktopMonitor.ErrorCleared
- Win32_DesktopMonitor.ErrorDescription
- Win32_DesktopMonitor.InstallDate
- Win32_DesktopMonitor.IsLocked
- Win32_DesktopMonitor.LastErrorCode
- Win32_DesktopMonitor.MonitorManufacturer
- Win32_DesktopMonitor.MonitorType
- Win32_DesktopMonitor.Name
- Win32_DesktopMonitor.PixelsPerXLogicalInch
- Win32_DesktopMonitor.PixelsPerYLogicalInch
- Win32_DesktopMonitor.PNPDeviceID
- Win32_DesktopMonitor.PowerManagementCapabilities
- Win32_DesktopMonitor.PowerManagementSupported
- Win32_DesktopMonitor.ScreenHeight
- Win32_DesktopMonitor.ScreenWidth
- Win32_DesktopMonitor.Status
- Win32_DesktopMonitor.StatusInfo
- Win32_DesktopMonitor.SystemCreationClassName
- Win32_DesktopMonitor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccf986957d73dd93837b0ab7a1e10b50aec5e8f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539371"
---
# <a name="win32_desktopmonitor-class"></a><span data-ttu-id="67275-103">\_Класс Win32 десктопмонитор</span><span class="sxs-lookup"><span data-stu-id="67275-103">Win32\_DesktopMonitor class</span></span>

<span data-ttu-id="67275-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ десктопмонитор для Win32** представляет тип монитора или устройства отображения, подключенного к компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="67275-104">The **Win32\_DesktopMonitor** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the type of monitor or display device attached to the computer system.</span></span>

<span data-ttu-id="67275-105">Оборудование, несовместимое с моделью драйвера Windows (WDDM), возвращает неточные значения свойств для экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="67275-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="67275-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="67275-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="67275-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="67275-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="67275-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67275-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF0-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_DesktopMonitor : CIM_DesktopMonitor
{
  uint16   Availability;
  uint32   Bandwidth;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="67275-109">Члены</span><span class="sxs-lookup"><span data-stu-id="67275-109">Members</span></span>

<span data-ttu-id="67275-110">Класс **Win32 \_ десктопмонитор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="67275-110">The **Win32\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="67275-111">Методы</span><span class="sxs-lookup"><span data-stu-id="67275-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="67275-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="67275-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="67275-113">Методы</span><span class="sxs-lookup"><span data-stu-id="67275-113">Methods</span></span>

<span data-ttu-id="67275-114">Класс **Win32 \_ десктопмонитор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="67275-114">The **Win32\_DesktopMonitor** class has these methods.</span></span>



| <span data-ttu-id="67275-115">Метод</span><span class="sxs-lookup"><span data-stu-id="67275-115">Method</span></span>            | <span data-ttu-id="67275-116">Описание</span><span class="sxs-lookup"><span data-stu-id="67275-116">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67275-117">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="67275-117">**Reset**</span></span>         | <span data-ttu-id="67275-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="67275-118">Not implemented.</span></span> <span data-ttu-id="67275-119">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ десктопмонитор**](cim-desktopmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="67275-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="67275-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="67275-120">**SetPowerState**</span></span> | <span data-ttu-id="67275-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="67275-121">Not implemented.</span></span> <span data-ttu-id="67275-122">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ десктопмонитор**](cim-desktopmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="67275-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="67275-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="67275-123">Properties</span></span>

<span data-ttu-id="67275-124">Класс **Win32 \_ десктопмонитор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="67275-124">The **Win32\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67275-125">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="67275-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67275-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67275-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="67275-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="67275-129">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="67275-129">Availability and status of the device.</span></span>

<span data-ttu-id="67275-130">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67275-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="67275-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67275-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="67275-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="67275-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="67275-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="67275-134">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="67275-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="67275-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="67275-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="67275-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="67275-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="67275-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="67275-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="67275-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="67275-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="67275-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="67275-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="67275-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="67275-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="67275-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="67275-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="67275-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="67275-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="67275-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="67275-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="67275-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="67275-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="67275-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="67275-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="67275-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="67275-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="67275-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="67275-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="67275-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="67275-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="67275-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="67275-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="67275-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="67275-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="67275-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="67275-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="67275-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="67275-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="67275-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="67275-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="67275-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="67275-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="67275-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="67275-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="67275-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="67275-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="67275-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="67275-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="67275-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="67275-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="67275-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="67275-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="67275-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="67275-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67275-161">**Пропускная способность**</span><span class="sxs-lookup"><span data-stu-id="67275-161">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67275-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67275-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-164">Квалификаторы: [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) ("мегагерц")</span><span class="sxs-lookup"><span data-stu-id="67275-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="67275-165">Пропускная способность монитора в мегагерцах.</span><span class="sxs-lookup"><span data-stu-id="67275-165">Monitor's bandwidth in megahertz.</span></span> <span data-ttu-id="67275-166">Если значение неизвестно, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="67275-166">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="67275-167">Это свойство наследуется от [**CIM \_ десктопмонитор**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="67275-167">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-168">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="67275-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-171">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="67275-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="67275-172">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="67275-172">Short description of the object.</span></span>

<span data-ttu-id="67275-173">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67275-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-174">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="67275-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-175">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67275-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67275-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-177">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="67275-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="67275-178">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="67275-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="67275-179">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="67275-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="67275-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="67275-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="67275-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="67275-182">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="67275-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="67275-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="67275-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="67275-184">(1)</span><span class="sxs-lookup"><span data-stu-id="67275-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="67275-185">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="67275-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="67275-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="67275-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="67275-187">(2)</span><span class="sxs-lookup"><span data-stu-id="67275-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="67275-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="67275-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="67275-189">(3)</span><span class="sxs-lookup"><span data-stu-id="67275-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="67275-190">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67275-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="67275-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="67275-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="67275-192">(4)</span><span class="sxs-lookup"><span data-stu-id="67275-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="67275-193">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="67275-193">Device is not working properly.</span></span> <span data-ttu-id="67275-194">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="67275-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="67275-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="67275-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="67275-196">(5)</span><span class="sxs-lookup"><span data-stu-id="67275-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="67275-197">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="67275-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="67275-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="67275-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="67275-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="67275-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="67275-200">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="67275-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="67275-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="67275-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="67275-202">(7)</span><span class="sxs-lookup"><span data-stu-id="67275-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="67275-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="67275-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="67275-204">(8)</span><span class="sxs-lookup"><span data-stu-id="67275-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="67275-205">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="67275-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="67275-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="67275-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="67275-207">(9)</span><span class="sxs-lookup"><span data-stu-id="67275-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="67275-208">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="67275-208">Device is not working properly.</span></span> <span data-ttu-id="67275-209">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="67275-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="67275-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="67275-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="67275-211">(10)</span><span class="sxs-lookup"><span data-stu-id="67275-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="67275-212">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="67275-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="67275-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="67275-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="67275-214">(11)</span><span class="sxs-lookup"><span data-stu-id="67275-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="67275-215">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="67275-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="67275-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="67275-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="67275-217">(12)</span><span class="sxs-lookup"><span data-stu-id="67275-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="67275-218">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="67275-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="67275-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="67275-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="67275-220">(13)</span><span class="sxs-lookup"><span data-stu-id="67275-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="67275-221">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="67275-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="67275-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="67275-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="67275-223">(14)</span><span class="sxs-lookup"><span data-stu-id="67275-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="67275-224">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="67275-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="67275-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="67275-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="67275-226">(15)</span><span class="sxs-lookup"><span data-stu-id="67275-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="67275-227">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="67275-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="67275-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="67275-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="67275-229">(16)</span><span class="sxs-lookup"><span data-stu-id="67275-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="67275-230">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="67275-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="67275-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="67275-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="67275-232">(17)</span><span class="sxs-lookup"><span data-stu-id="67275-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="67275-233">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="67275-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="67275-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="67275-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="67275-235">(18)</span><span class="sxs-lookup"><span data-stu-id="67275-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="67275-236">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="67275-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="67275-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="67275-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="67275-238">(19)</span><span class="sxs-lookup"><span data-stu-id="67275-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="67275-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="67275-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="67275-240">(20)</span><span class="sxs-lookup"><span data-stu-id="67275-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="67275-241">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="67275-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="67275-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="67275-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="67275-243">(21)</span><span class="sxs-lookup"><span data-stu-id="67275-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="67275-244">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="67275-244">System failure.</span></span> <span data-ttu-id="67275-245">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="67275-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="67275-246">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="67275-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="67275-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="67275-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="67275-248">(22)</span><span class="sxs-lookup"><span data-stu-id="67275-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="67275-249">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="67275-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="67275-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="67275-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="67275-251">(23)</span><span class="sxs-lookup"><span data-stu-id="67275-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="67275-252">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="67275-252">System failure.</span></span> <span data-ttu-id="67275-253">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="67275-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="67275-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="67275-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="67275-255">(24)</span><span class="sxs-lookup"><span data-stu-id="67275-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="67275-256">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="67275-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="67275-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="67275-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="67275-258">(25)</span><span class="sxs-lookup"><span data-stu-id="67275-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="67275-259">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="67275-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="67275-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="67275-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="67275-261">(26)</span><span class="sxs-lookup"><span data-stu-id="67275-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="67275-262">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="67275-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="67275-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="67275-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="67275-264">(27)</span><span class="sxs-lookup"><span data-stu-id="67275-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="67275-265">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="67275-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="67275-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="67275-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="67275-267">(28)</span><span class="sxs-lookup"><span data-stu-id="67275-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="67275-268">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="67275-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="67275-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="67275-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="67275-270">(29)</span><span class="sxs-lookup"><span data-stu-id="67275-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="67275-271">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="67275-271">Device is disabled.</span></span> <span data-ttu-id="67275-272">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="67275-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="67275-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="67275-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="67275-274">(30)</span><span class="sxs-lookup"><span data-stu-id="67275-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="67275-275">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="67275-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="67275-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="67275-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="67275-277">1-31</span><span class="sxs-lookup"><span data-stu-id="67275-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="67275-278">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="67275-278">Device is not working properly.</span></span> <span data-ttu-id="67275-279">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="67275-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67275-280">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="67275-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-281">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="67275-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67275-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-283">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="67275-283">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="67275-284">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="67275-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="67275-285">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="67275-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-287">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-289">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67275-289">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67275-290">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="67275-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="67275-291">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="67275-291">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="67275-292">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-293">**Описание**</span><span class="sxs-lookup"><span data-stu-id="67275-293">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-294">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-296">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="67275-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="67275-297">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="67275-297">Description of the object.</span></span>

<span data-ttu-id="67275-298">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67275-298">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-299">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="67275-299">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-302">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**МАППИНГСТРИНГС**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Windows GDI \| хмонитор")</span><span class="sxs-lookup"><span data-stu-id="67275-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows GDI\|HMONITOR")</span></span>
</dt> </dl>

<span data-ttu-id="67275-303">Уникальный идентификатор монитора рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="67275-303">Unique identifier of a desktop monitor.</span></span>

<span data-ttu-id="67275-304">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-305">**дисплайтипе**</span><span class="sxs-lookup"><span data-stu-id="67275-305">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-306">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67275-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67275-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67275-308">Тип настольного монитора или CRT.</span><span class="sxs-lookup"><span data-stu-id="67275-308">Type of desktop monitor or CRT.</span></span>

<span data-ttu-id="67275-309">Это свойство наследуется от [**CIM \_ десктопмонитор**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="67275-309">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67275-310">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="67275-310">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67275-311">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="67275-311">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="67275-312">**Цвет для многосканирования** (2)</span><span class="sxs-lookup"><span data-stu-id="67275-312">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="67275-313">**Многосканерная Монохромная** (3)</span><span class="sxs-lookup"><span data-stu-id="67275-313">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="67275-314">**Фиксированный цвет частоты** (4)</span><span class="sxs-lookup"><span data-stu-id="67275-314">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="67275-315">**Фиксированная частота монохромных** (5)</span><span class="sxs-lookup"><span data-stu-id="67275-315">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67275-316">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="67275-316">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-317">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="67275-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67275-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67275-319">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="67275-319">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="67275-320">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-321">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="67275-321">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67275-324">Строка свободной формы, предоставляя дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="67275-324">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="67275-325">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-326">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="67275-326">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-327">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="67275-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67275-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-329">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="67275-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="67275-330">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="67275-330">Date and time the object was installed.</span></span> <span data-ttu-id="67275-331">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="67275-331">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="67275-332">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67275-332">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-333">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="67275-333">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-334">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="67275-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67275-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67275-336">**Значение true** показывает, что устройство заблокировано, что предотвращает ввод или вывод пользователя.</span><span class="sxs-lookup"><span data-stu-id="67275-336">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="67275-337">Это свойство наследуется от [**CIM \_ усердевице**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="67275-337">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-338">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="67275-338">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-339">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67275-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67275-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67275-341">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="67275-341">Last error code reported by the logical device.</span></span>

<span data-ttu-id="67275-342">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-343">**монитормануфактурер**</span><span class="sxs-lookup"><span data-stu-id="67275-343">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-344">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-346">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="67275-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="67275-347">Имя изготовителя монитора.</span><span class="sxs-lookup"><span data-stu-id="67275-347">Name of the monitor manufacturer.</span></span>

<span data-ttu-id="67275-348">Пример: "NEC"</span><span class="sxs-lookup"><span data-stu-id="67275-348">Example: "NEC"</span></span>

</dd> <dt>

<span data-ttu-id="67275-349">**Тип монитора "**</span><span class="sxs-lookup"><span data-stu-id="67275-349">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-350">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-352">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="67275-352">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="67275-353">Тип монитора.</span><span class="sxs-lookup"><span data-stu-id="67275-353">Type of monitor.</span></span>

<span data-ttu-id="67275-354">Пример: "NEC 5FGp"</span><span class="sxs-lookup"><span data-stu-id="67275-354">Example: "NEC 5FGp"</span></span>

</dd> <dt>

<span data-ttu-id="67275-355">**Name**</span><span class="sxs-lookup"><span data-stu-id="67275-355">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-356">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-358">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="67275-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="67275-359">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="67275-359">Label by which the object is known.</span></span> <span data-ttu-id="67275-360">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="67275-360">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="67275-361">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67275-361">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-362">**пикселсперкслогикалинч**</span><span class="sxs-lookup"><span data-stu-id="67275-362">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-363">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67275-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67275-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-365">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей на логический дюйм")</span><span class="sxs-lookup"><span data-stu-id="67275-365">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="67275-366">Разрешение по оси x (горизонтальное направление) монитора.</span><span class="sxs-lookup"><span data-stu-id="67275-366">Resolution along the x-axis (horizontal direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="67275-367">**пикселсперилогикалинч**</span><span class="sxs-lookup"><span data-stu-id="67275-367">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-368">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67275-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67275-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-370">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIные \| функции контекста \| [**жетдевицекапс**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей на логический дюйм")</span><span class="sxs-lookup"><span data-stu-id="67275-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="67275-371">Разрешение по оси y (вертикальное направление) монитора.</span><span class="sxs-lookup"><span data-stu-id="67275-371">Resolution along the y-axis (vertical direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="67275-372">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="67275-372">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-373">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-375">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="67275-375">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="67275-376">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="67275-376">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="67275-377">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="67275-378">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="67275-378">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="67275-379">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="67275-379">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-380">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="67275-380">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="67275-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67275-382">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="67275-382">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="67275-383">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-383">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67275-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="67275-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="67275-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="67275-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="67275-386">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="67275-386">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="67275-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="67275-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="67275-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="67275-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="67275-389">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="67275-389">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="67275-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="67275-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="67275-391">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="67275-391">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="67275-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="67275-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="67275-393">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="67275-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="67275-394">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="67275-394">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="67275-395">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="67275-395">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="67275-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="67275-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="67275-397">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="67275-397">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="67275-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="67275-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="67275-399">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="67275-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67275-400">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="67275-400">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-401">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="67275-401">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67275-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67275-403">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="67275-403">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="67275-404">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="67275-404">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="67275-405">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-406">**скринхеигхт**</span><span class="sxs-lookup"><span data-stu-id="67275-406">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-407">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67275-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67275-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67275-409">Логическая высота экрана в координатах экрана.</span><span class="sxs-lookup"><span data-stu-id="67275-409">Logical height of the display in screen coordinates.</span></span>

<span data-ttu-id="67275-410">Это свойство наследуется от [**CIM \_ десктопмонитор**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="67275-410">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-411">**скринвидс**</span><span class="sxs-lookup"><span data-stu-id="67275-411">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-412">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67275-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67275-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67275-414">Логическая ширина экрана в экранных координатах.</span><span class="sxs-lookup"><span data-stu-id="67275-414">Logical width of the display in screen coordinates.</span></span>

<span data-ttu-id="67275-415">Это свойство наследуется от [**CIM \_ десктопмонитор**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="67275-415">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-416">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="67275-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-417">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-419">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="67275-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="67275-420">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="67275-420">Current status of the object.</span></span> <span data-ttu-id="67275-421">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="67275-421">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="67275-422">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="67275-422">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="67275-423">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="67275-423">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="67275-424">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="67275-424">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="67275-425">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="67275-425">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="67275-426">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="67275-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="67275-427">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="67275-427">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="67275-428">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="67275-428">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="67275-429">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="67275-429">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="67275-430">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="67275-430">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67275-431">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="67275-431">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="67275-432">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="67275-432">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="67275-433">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="67275-433">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="67275-434">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="67275-434">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="67275-435">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="67275-435">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="67275-436">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="67275-436">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="67275-437">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="67275-437">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="67275-438">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="67275-438">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="67275-439">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="67275-439">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67275-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="67275-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-441">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67275-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67275-442">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-443">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="67275-443">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="67275-444">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="67275-444">State of the logical device.</span></span> <span data-ttu-id="67275-445">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="67275-445">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="67275-446">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67275-447">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="67275-447">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67275-448">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="67275-448">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="67275-449">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="67275-449">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="67275-450">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="67275-450">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="67275-451">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="67275-451">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67275-452">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="67275-452">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-453">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-454">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-455">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67275-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67275-456">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="67275-456">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="67275-457">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="67275-458">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="67275-458">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67275-459">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="67275-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67275-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="67275-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67275-461">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="67275-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="67275-462">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="67275-462">Name of the scoping system.</span></span>

<span data-ttu-id="67275-463">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="67275-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67275-464">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67275-464">Remarks</span></span>

<span data-ttu-id="67275-465">Класс **Win32 \_ десктопмонитор** является производным от [**CIM \_ десктопмонитор**](cim-desktopmonitor.md), который является производным от [**CIM- \_ дисплеев**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="67275-465">The **Win32\_DesktopMonitor** class is derived from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), which derives from [**CIM\_Display**](cim-display.md).</span></span> <span data-ttu-id="67275-466">**Модель CIM \_ Отображение** является производным от [**CIM \_ усердевице**](cim-userdevice.md), который является производным от CIM-класса. [**\_**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="67275-466">**CIM\_Display** is derived from [**CIM\_UserDevice**](cim-userdevice.md), which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="67275-467">Примеры</span><span class="sxs-lookup"><span data-stu-id="67275-467">Examples</span></span>

<span data-ttu-id="67275-468">С [помощью примера Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell в коллекции TechNet для взаимодействия с моделью автоматизации Visio для создания рисунка Visio используется **Win32 \_ десктопмонитор** .</span><span class="sxs-lookup"><span data-stu-id="67275-468">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_DesktopMonitor** to interact with the Visio automation model to create a Visio drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="67275-469">Требования</span><span class="sxs-lookup"><span data-stu-id="67275-469">Requirements</span></span>



| <span data-ttu-id="67275-470">Требование</span><span class="sxs-lookup"><span data-stu-id="67275-470">Requirement</span></span> | <span data-ttu-id="67275-471">Значение</span><span class="sxs-lookup"><span data-stu-id="67275-471">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67275-472">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67275-472">Minimum supported client</span></span><br/> | <span data-ttu-id="67275-473">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67275-473">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67275-474">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67275-474">Minimum supported server</span></span><br/> | <span data-ttu-id="67275-475">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67275-475">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67275-476">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="67275-476">Namespace</span></span><br/>                | <span data-ttu-id="67275-477">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="67275-477">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="67275-478">MOF</span><span class="sxs-lookup"><span data-stu-id="67275-478">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67275-479"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67275-479"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="67275-480">DLL</span><span class="sxs-lookup"><span data-stu-id="67275-480">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67275-481"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67275-481"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67275-482">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67275-482">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67275-483">**\_ДЕСКТОПМОНИТОР CIM**</span><span class="sxs-lookup"><span data-stu-id="67275-483">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dt>

[<span data-ttu-id="67275-484">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="67275-484">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="67275-485">Задачи WMI: управление рабочим столом</span><span class="sxs-lookup"><span data-stu-id="67275-485">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

