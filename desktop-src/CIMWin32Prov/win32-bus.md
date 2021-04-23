---
description: '\_Класс WMI шины Win32 представляет физическую шину, как видно на компьютере, работающем под управлением операционной системы Windows. Любой экземпляр шины Windows — это потомок (или член) этого класса.'
ms.assetid: 76ba15f4-8c7b-4713-b5a2-e444fbab064a
ms.tgt_platform: multiple
title: Класс Win32_Bus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Bus
- Win32_Bus.Reset
- Win32_Bus.SetPowerState
- Win32_Bus.Availability
- Win32_Bus.BusNum
- Win32_Bus.BusType
- Win32_Bus.Caption
- Win32_Bus.ConfigManagerErrorCode
- Win32_Bus.ConfigManagerUserConfig
- Win32_Bus.CreationClassName
- Win32_Bus.Description
- Win32_Bus.DeviceID
- Win32_Bus.ErrorCleared
- Win32_Bus.ErrorDescription
- Win32_Bus.InstallDate
- Win32_Bus.LastErrorCode
- Win32_Bus.Name
- Win32_Bus.PNPDeviceID
- Win32_Bus.PowerManagementCapabilities
- Win32_Bus.PowerManagementSupported
- Win32_Bus.Status
- Win32_Bus.StatusInfo
- Win32_Bus.SystemCreationClassName
- Win32_Bus.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac31a2187ee7e4974e1ddedbf084efd482748753
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895597"
---
# <a name="win32_bus-class"></a><span data-ttu-id="f4012-104">\_Класс шины Win32</span><span class="sxs-lookup"><span data-stu-id="f4012-104">Win32\_Bus class</span></span>

<span data-ttu-id="f4012-105">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ шины Win32** представляет физическую шину, как видно на компьютере, работающем под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="f4012-105">The **Win32\_Bus** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical bus as seen by a computer running a Windows operating system.</span></span> <span data-ttu-id="f4012-106">Любой экземпляр шины Windows — это потомок (или член) этого класса.</span><span class="sxs-lookup"><span data-stu-id="f4012-106">Any instance of a Windows bus is a descendant (or member) of this class.</span></span>

<span data-ttu-id="f4012-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f4012-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4012-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4012-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Bus : CIM_LogicalDevice
{
  uint16   Availability;
  uint32   BusNum;
  uint32   BusType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="f4012-109">Члены</span><span class="sxs-lookup"><span data-stu-id="f4012-109">Members</span></span>

<span data-ttu-id="f4012-110">Класс **\_ шины Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f4012-110">The **Win32\_Bus** class has these types of members:</span></span>

-   [<span data-ttu-id="f4012-111">Методы</span><span class="sxs-lookup"><span data-stu-id="f4012-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="f4012-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f4012-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f4012-113">Методы</span><span class="sxs-lookup"><span data-stu-id="f4012-113">Methods</span></span>

<span data-ttu-id="f4012-114">Класс **\_ шины Win32** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f4012-114">The **Win32\_Bus** class has these methods.</span></span>



| <span data-ttu-id="f4012-115">Метод</span><span class="sxs-lookup"><span data-stu-id="f4012-115">Method</span></span>            | <span data-ttu-id="f4012-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f4012-116">Description</span></span>                                                                                                                                                                                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4012-117">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="f4012-117">**Reset**</span></span>         | <span data-ttu-id="f4012-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="f4012-118">Not implemented.</span></span> <span data-ttu-id="f4012-119">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_**](cim-logicaldevice.md) .</span><span class="sxs-lookup"><span data-stu-id="f4012-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="f4012-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f4012-120">**SetPowerState**</span></span> | <span data-ttu-id="f4012-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="f4012-121">Not implemented.</span></span> <span data-ttu-id="f4012-122">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_**](cim-logicaldevice.md) .</span><span class="sxs-lookup"><span data-stu-id="f4012-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f4012-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="f4012-123">Properties</span></span>

<span data-ttu-id="f4012-124">Класс **\_ шины Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f4012-124">The **Win32\_Bus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4012-125">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="f4012-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4012-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="f4012-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-129">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="f4012-129">Availability and status of the device.</span></span>

<span data-ttu-id="f4012-130">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f4012-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f4012-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4012-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f4012-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f4012-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="f4012-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-134">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="f4012-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f4012-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="f4012-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f4012-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="f4012-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f4012-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="f4012-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f4012-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="f4012-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f4012-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="f4012-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f4012-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="f4012-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f4012-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="f4012-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f4012-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="f4012-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f4012-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="f4012-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f4012-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="f4012-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="f4012-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f4012-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="f4012-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="f4012-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f4012-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="f4012-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="f4012-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f4012-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="f4012-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f4012-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="f4012-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="f4012-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f4012-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="f4012-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="f4012-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f4012-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="f4012-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="f4012-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f4012-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="f4012-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="f4012-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f4012-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="f4012-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="f4012-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f4012-161">**буснум**</span><span class="sxs-lookup"><span data-stu-id="f4012-161">**BusNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4012-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-164">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f4012-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-165">Логический номер, назначенный физической шине.</span><span class="sxs-lookup"><span data-stu-id="f4012-165">Logical number assigned to the physical bus.</span></span>

<span data-ttu-id="f4012-166">Пример: 1</span><span class="sxs-lookup"><span data-stu-id="f4012-166">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="f4012-167">**BusType**</span><span class="sxs-lookup"><span data-stu-id="f4012-167">**BusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4012-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-170">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| тип интерфейса Win32API чврес \_ ")</span><span class="sxs-lookup"><span data-stu-id="f4012-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|cHwRes\|INTERFACE\_TYPE")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-171">Тип физической шины.</span><span class="sxs-lookup"><span data-stu-id="f4012-171">Type of the physical bus.</span></span> <span data-ttu-id="f4012-172">Это значение будет одним из значений в перечислении **\_ типа интерфейса** , определенного в Bus. h.</span><span class="sxs-lookup"><span data-stu-id="f4012-172">This value will be one of the values in the **INTERFACE\_TYPE** enumeration defined in Bus.h.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f4012-173">Не **определено** (-1)</span><span class="sxs-lookup"><span data-stu-id="f4012-173">**Undefined** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="f4012-174">**Внутренний** (0)</span><span class="sxs-lookup"><span data-stu-id="f4012-174">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="f4012-175">**ISA** (1)</span><span class="sxs-lookup"><span data-stu-id="f4012-175">**ISA** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="f4012-176">**EISA** (2)</span><span class="sxs-lookup"><span data-stu-id="f4012-176">**EISA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MicroChannel"></span><span id="microchannel"></span><span id="MICROCHANNEL"></span>

<span data-ttu-id="f4012-177">**Микроканал** (3)</span><span class="sxs-lookup"><span data-stu-id="f4012-177">**MicroChannel** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TurboChannel"></span><span id="turbochannel"></span><span id="TURBOCHANNEL"></span>

<span data-ttu-id="f4012-178">**Турбочаннел** (4)</span><span class="sxs-lookup"><span data-stu-id="f4012-178">**TurboChannel** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Bus"></span><span id="pci_bus"></span><span id="PCI_BUS"></span>

<span data-ttu-id="f4012-179">**Шина PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="f4012-179">**PCI Bus** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="f4012-180">**Шина вме** (6)</span><span class="sxs-lookup"><span data-stu-id="f4012-180">**VME Bus** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="f4012-181">**Нубус** (7)</span><span class="sxs-lookup"><span data-stu-id="f4012-181">**NuBus** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Bus"></span><span id="pcmcia_bus"></span><span id="PCMCIA_BUS"></span>

<span data-ttu-id="f4012-182">**Шина PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="f4012-182">**PCMCIA Bus** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="C_Bus"></span><span id="c_bus"></span><span id="C_BUS"></span>

<span data-ttu-id="f4012-183">**Шина C** (9)</span><span class="sxs-lookup"><span data-stu-id="f4012-183">**C Bus** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MPI_Bus"></span><span id="mpi_bus"></span><span id="MPI_BUS"></span>

<span data-ttu-id="f4012-184">**Шина MPI** (10)</span><span class="sxs-lookup"><span data-stu-id="f4012-184">**MPI Bus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MPSA_Bus"></span><span id="mpsa_bus"></span><span id="MPSA_BUS"></span>

<span data-ttu-id="f4012-185">**Шина MPSA** (11)</span><span class="sxs-lookup"><span data-stu-id="f4012-185">**MPSA Bus** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Processor"></span><span id="internal_processor"></span><span id="INTERNAL_PROCESSOR"></span>

<span data-ttu-id="f4012-186">**Внутренний процессор** (12)</span><span class="sxs-lookup"><span data-stu-id="f4012-186">**Internal Processor** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Power_Bus"></span><span id="internal_power_bus"></span><span id="INTERNAL_POWER_BUS"></span>

<span data-ttu-id="f4012-187">**Внутренняя шина питания** (13)</span><span class="sxs-lookup"><span data-stu-id="f4012-187">**Internal Power Bus** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PNP_ISA_Bus"></span><span id="pnp_isa_bus"></span><span id="PNP_ISA_BUS"></span>

<span data-ttu-id="f4012-188">**Шина PnP ISA** (14)</span><span class="sxs-lookup"><span data-stu-id="f4012-188">**PNP ISA Bus** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PNP_Bus"></span><span id="pnp_bus"></span><span id="PNP_BUS"></span>

<span data-ttu-id="f4012-189">**Шина PnP** (15)</span><span class="sxs-lookup"><span data-stu-id="f4012-189">**PNP Bus** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum_Interface_Type"></span><span id="maximum_interface_type"></span><span id="MAXIMUM_INTERFACE_TYPE"></span>

<span data-ttu-id="f4012-190">**Максимальный тип интерфейса** (16)</span><span class="sxs-lookup"><span data-stu-id="f4012-190">**Maximum Interface Type** (16)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f4012-191">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f4012-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4012-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-194">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f4012-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-195">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="f4012-195">Short description of the object a one-line string.</span></span>

<span data-ttu-id="f4012-196">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f4012-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-197">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="f4012-197">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-198">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4012-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-200">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f4012-200">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-201">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f4012-201">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f4012-202">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-202">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f4012-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="f4012-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="f4012-204"> (0)</span><span class="sxs-lookup"><span data-stu-id="f4012-204">(0)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-205">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="f4012-205">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f4012-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="f4012-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="f4012-207">(1)</span><span class="sxs-lookup"><span data-stu-id="f4012-207">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-208">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="f4012-208">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f4012-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f4012-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f4012-210">(2)</span><span class="sxs-lookup"><span data-stu-id="f4012-210">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f4012-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="f4012-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f4012-212">(3)</span><span class="sxs-lookup"><span data-stu-id="f4012-212">(3)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-213">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4012-213">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f4012-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="f4012-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f4012-215">(4)</span><span class="sxs-lookup"><span data-stu-id="f4012-215">(4)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-216">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="f4012-216">Device is not working properly.</span></span> <span data-ttu-id="f4012-217">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="f4012-217">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f4012-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="f4012-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f4012-219">(5)</span><span class="sxs-lookup"><span data-stu-id="f4012-219">(5)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-220">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="f4012-220">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f4012-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="f4012-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f4012-222"> (6)</span><span class="sxs-lookup"><span data-stu-id="f4012-222">(6)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-223">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="f4012-223">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f4012-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="f4012-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="f4012-225">(7)</span><span class="sxs-lookup"><span data-stu-id="f4012-225">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f4012-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="f4012-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f4012-227">(8)</span><span class="sxs-lookup"><span data-stu-id="f4012-227">(8)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-228">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="f4012-228">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f4012-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="f4012-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f4012-230">(9)</span><span class="sxs-lookup"><span data-stu-id="f4012-230">(9)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-231">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="f4012-231">Device is not working properly.</span></span> <span data-ttu-id="f4012-232">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="f4012-232">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f4012-233"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="f4012-233"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="f4012-234">(10)</span><span class="sxs-lookup"><span data-stu-id="f4012-234">(10)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-235">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="f4012-235">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f4012-236"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="f4012-236"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="f4012-237">(11)</span><span class="sxs-lookup"><span data-stu-id="f4012-237">(11)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-238">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="f4012-238">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f4012-239"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="f4012-239"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f4012-240">(12)</span><span class="sxs-lookup"><span data-stu-id="f4012-240">(12)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-241">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="f4012-241">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f4012-242"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f4012-242"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f4012-243">(13)</span><span class="sxs-lookup"><span data-stu-id="f4012-243">(13)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-244">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="f4012-244">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f4012-245"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="f4012-245"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f4012-246">(14)</span><span class="sxs-lookup"><span data-stu-id="f4012-246">(14)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-247">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="f4012-247">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f4012-248"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="f4012-248"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f4012-249">(15)</span><span class="sxs-lookup"><span data-stu-id="f4012-249">(15)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-250">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="f4012-250">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f4012-251"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="f4012-251"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f4012-252">(16)</span><span class="sxs-lookup"><span data-stu-id="f4012-252">(16)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-253">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="f4012-253">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f4012-254"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="f4012-254"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f4012-255">(17)</span><span class="sxs-lookup"><span data-stu-id="f4012-255">(17)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-256">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="f4012-256">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f4012-257"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f4012-257"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f4012-258">(18)</span><span class="sxs-lookup"><span data-stu-id="f4012-258">(18)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-259">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="f4012-259">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f4012-260"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="f4012-260"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="f4012-261">(19)</span><span class="sxs-lookup"><span data-stu-id="f4012-261">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f4012-262"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="f4012-262"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="f4012-263">(20)</span><span class="sxs-lookup"><span data-stu-id="f4012-263">(20)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-264">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="f4012-264">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f4012-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="f4012-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f4012-266">(21)</span><span class="sxs-lookup"><span data-stu-id="f4012-266">(21)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-267">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="f4012-267">System failure.</span></span> <span data-ttu-id="f4012-268">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="f4012-268">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="f4012-269">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="f4012-269">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f4012-270"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="f4012-270"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="f4012-271">(22)</span><span class="sxs-lookup"><span data-stu-id="f4012-271">(22)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-272">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="f4012-272">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f4012-273"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="f4012-273"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f4012-274">(23)</span><span class="sxs-lookup"><span data-stu-id="f4012-274">(23)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-275">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="f4012-275">System failure.</span></span> <span data-ttu-id="f4012-276">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="f4012-276">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f4012-277"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="f4012-277"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f4012-278">(24)</span><span class="sxs-lookup"><span data-stu-id="f4012-278">(24)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-279">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="f4012-279">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f4012-280"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="f4012-280"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f4012-281">(25)</span><span class="sxs-lookup"><span data-stu-id="f4012-281">(25)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-282">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="f4012-282">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f4012-283"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="f4012-283"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="f4012-284">(26)</span><span class="sxs-lookup"><span data-stu-id="f4012-284">(26)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-285">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="f4012-285">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f4012-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="f4012-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f4012-287">(27)</span><span class="sxs-lookup"><span data-stu-id="f4012-287">(27)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-288">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="f4012-288">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f4012-289"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="f4012-289"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f4012-290">(28)</span><span class="sxs-lookup"><span data-stu-id="f4012-290">(28)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-291">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="f4012-291">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f4012-292"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="f4012-292"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f4012-293">(29)</span><span class="sxs-lookup"><span data-stu-id="f4012-293">(29)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-294">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="f4012-294">Device is disabled.</span></span> <span data-ttu-id="f4012-295">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f4012-295">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f4012-296"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="f4012-296"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f4012-297">(30)</span><span class="sxs-lookup"><span data-stu-id="f4012-297">(30)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-298">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="f4012-298">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f4012-299"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f4012-299"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f4012-300">1-31</span><span class="sxs-lookup"><span data-stu-id="f4012-300">(31)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-301">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="f4012-301">Device is not working properly.</span></span> <span data-ttu-id="f4012-302">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="f4012-302">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f4012-303">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="f4012-303">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-304">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f4012-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-306">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f4012-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-307">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f4012-307">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f4012-308">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-309">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f4012-309">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4012-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-312">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f4012-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f4012-313">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f4012-313">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="f4012-314">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="f4012-314">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="f4012-315">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-316">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f4012-316">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4012-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-319">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="f4012-319">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-320">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f4012-320">Description of the object.</span></span>

<span data-ttu-id="f4012-321">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f4012-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-322">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f4012-322">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-323">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4012-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-325">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="f4012-325">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-326">Уникальное имя, идентифицирующее шину.</span><span class="sxs-lookup"><span data-stu-id="f4012-326">Unique name that identifies the bus.</span></span>

<span data-ttu-id="f4012-327">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-328">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="f4012-328">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-329">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f4012-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4012-331">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="f4012-331">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="f4012-332">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-333">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f4012-333">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4012-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4012-336">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="f4012-336">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="f4012-337">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f4012-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-339">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f4012-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-341">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="f4012-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-342">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="f4012-342">Date and time the object was installed.</span></span> <span data-ttu-id="f4012-343">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="f4012-343">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f4012-344">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f4012-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-345">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="f4012-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-346">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4012-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4012-348">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="f4012-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f4012-349">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-350">**Name**</span><span class="sxs-lookup"><span data-stu-id="f4012-350">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-351">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4012-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-353">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="f4012-353">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-354">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="f4012-354">Label by which the object is known.</span></span> <span data-ttu-id="f4012-355">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="f4012-355">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f4012-356">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f4012-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-357">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f4012-357">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-358">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4012-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-360">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f4012-360">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-361">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f4012-361">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f4012-362">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="f4012-363">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f4012-363">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="f4012-364">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="f4012-364">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-365">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f4012-365">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f4012-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4012-367">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="f4012-367">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="f4012-368">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-368">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4012-369"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f4012-369"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f4012-370"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="f4012-370"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f4012-371"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="f4012-371"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f4012-372"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="f4012-372"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-373">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="f4012-373">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f4012-374"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="f4012-374"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-375">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="f4012-375">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f4012-376"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="f4012-376"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-377">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="f4012-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="f4012-378">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="f4012-378">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="f4012-379">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="f4012-379">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f4012-380"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="f4012-380"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-381">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState*, установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="f4012-381">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f4012-382"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="f4012-382"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f4012-383">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="f4012-383">Timed Power-On Supported</span></span>

<span data-ttu-id="f4012-384">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="f4012-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f4012-385">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="f4012-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-386">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f4012-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4012-388">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f4012-388">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="f4012-389">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="f4012-389">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="f4012-390">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-391">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f4012-391">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-392">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4012-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-394">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="f4012-394">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-395">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f4012-395">Current status of the object.</span></span> <span data-ttu-id="f4012-396">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="f4012-396">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f4012-397">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="f4012-397">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f4012-398">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="f4012-398">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f4012-399">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="f4012-399">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f4012-400">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="f4012-400">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f4012-401">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f4012-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f4012-402">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="f4012-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f4012-403">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="f4012-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f4012-404">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="f4012-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f4012-405">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="f4012-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4012-406">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="f4012-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f4012-407">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="f4012-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f4012-408">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="f4012-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f4012-409">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="f4012-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f4012-410">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="f4012-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f4012-411">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="f4012-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f4012-412">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="f4012-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f4012-413">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="f4012-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f4012-414">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="f4012-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f4012-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f4012-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-416">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4012-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-418">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f4012-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f4012-419">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f4012-419">State of the logical device.</span></span> <span data-ttu-id="f4012-420">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="f4012-420">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="f4012-421">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f4012-422">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f4012-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4012-423">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f4012-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f4012-424">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="f4012-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f4012-425">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="f4012-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f4012-426">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="f4012-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f4012-427">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="f4012-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-428">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4012-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-430">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f4012-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f4012-431">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="f4012-431">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="f4012-432">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4012-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f4012-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4012-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f4012-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4012-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f4012-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4012-436">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f4012-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f4012-437">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="f4012-437">Name of the scoping system.</span></span>

<span data-ttu-id="f4012-438">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f4012-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4012-439">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4012-439">Remarks</span></span>

<span data-ttu-id="f4012-440">Класс **\_ шины Win32** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="f4012-440">The **Win32\_Bus** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4012-441">Требования</span><span class="sxs-lookup"><span data-stu-id="f4012-441">Requirements</span></span>



| <span data-ttu-id="f4012-442">Требование</span><span class="sxs-lookup"><span data-stu-id="f4012-442">Requirement</span></span> | <span data-ttu-id="f4012-443">Значение</span><span class="sxs-lookup"><span data-stu-id="f4012-443">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4012-444">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4012-444">Minimum supported client</span></span><br/> | <span data-ttu-id="f4012-445">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4012-445">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4012-446">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4012-446">Minimum supported server</span></span><br/> | <span data-ttu-id="f4012-447">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4012-447">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4012-448">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f4012-448">Namespace</span></span><br/>                | <span data-ttu-id="f4012-449">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f4012-449">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f4012-450">MOF</span><span class="sxs-lookup"><span data-stu-id="f4012-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4012-451"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4012-451"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4012-452">DLL</span><span class="sxs-lookup"><span data-stu-id="f4012-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4012-453"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4012-453"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4012-454">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4012-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4012-455">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="f4012-455">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="f4012-456">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="f4012-456">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

