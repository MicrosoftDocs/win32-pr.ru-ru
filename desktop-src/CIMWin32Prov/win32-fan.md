---
description: '\_Класс WMI вентилятора Win32 представляет свойства устройства вентиляторов в компьютерной системе. Например, Вентилятор охлаждения процессора.'
ms.assetid: ff48b788-d759-45cf-812f-a80dba0c9192
ms.tgt_platform: multiple
title: Класс Win32_Fan
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Fan
- Win32_Fan.Reset
- Win32_Fan.SetPowerState
- Win32_Fan.SetSpeed
- Win32_Fan.ActiveCooling
- Win32_Fan.Availability
- Win32_Fan.Caption
- Win32_Fan.ConfigManagerErrorCode
- Win32_Fan.ConfigManagerUserConfig
- Win32_Fan.CreationClassName
- Win32_Fan.Description
- Win32_Fan.DesiredSpeed
- Win32_Fan.DeviceID
- Win32_Fan.ErrorCleared
- Win32_Fan.ErrorDescription
- Win32_Fan.InstallDate
- Win32_Fan.LastErrorCode
- Win32_Fan.Name
- Win32_Fan.PNPDeviceID
- Win32_Fan.PowerManagementCapabilities
- Win32_Fan.PowerManagementSupported
- Win32_Fan.Status
- Win32_Fan.StatusInfo
- Win32_Fan.SystemCreationClassName
- Win32_Fan.SystemName
- Win32_Fan.VariableSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67f248b74fa665f30c9c3b9ffa51cb8cee5a5782
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538471"
---
# <a name="win32_fan-class"></a><span data-ttu-id="1c646-104">\_Класс вентилятора Win32</span><span class="sxs-lookup"><span data-stu-id="1c646-104">Win32\_Fan class</span></span>

<span data-ttu-id="1c646-105">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ вентилятора Win32** представляет свойства устройства вентиляторов в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="1c646-105">The **Win32\_Fan** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a fan device in the computer system.</span></span> <span data-ttu-id="1c646-106">Например, Вентилятор охлаждения процессора.</span><span class="sxs-lookup"><span data-stu-id="1c646-106">For example, the CPU cooling fan.</span></span>

<span data-ttu-id="1c646-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1c646-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1c646-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1c646-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c646-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c646-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB5-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_Fan : CIM_Fan
{
  boolean  ActiveCooling;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint64   DesiredSpeed;
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
  boolean  VariableSpeed;
};
```

## <a name="members"></a><span data-ttu-id="1c646-110">Члены</span><span class="sxs-lookup"><span data-stu-id="1c646-110">Members</span></span>

<span data-ttu-id="1c646-111">Класс **\_ вентилятора Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1c646-111">The **Win32\_Fan** class has these types of members:</span></span>

-   [<span data-ttu-id="1c646-112">Методы</span><span class="sxs-lookup"><span data-stu-id="1c646-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1c646-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c646-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1c646-114">Методы</span><span class="sxs-lookup"><span data-stu-id="1c646-114">Methods</span></span>

<span data-ttu-id="1c646-115">Класс **\_ вентилятора Win32** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1c646-115">The **Win32\_Fan** class has these methods.</span></span>



| <span data-ttu-id="1c646-116">Метод</span><span class="sxs-lookup"><span data-stu-id="1c646-116">Method</span></span>            | <span data-ttu-id="1c646-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1c646-117">Description</span></span>                                                                                                                                                                                  |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c646-118">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="1c646-118">**Reset**</span></span>         | <span data-ttu-id="1c646-119">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="1c646-119">Not implemented.</span></span> <span data-ttu-id="1c646-120">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в разделе " [**\_ вентилятор CIM**](cim-fan.md) ".</span><span class="sxs-lookup"><span data-stu-id="1c646-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Fan**](cim-fan.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="1c646-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1c646-121">**SetPowerState**</span></span> | <span data-ttu-id="1c646-122">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="1c646-122">Not implemented.</span></span> <span data-ttu-id="1c646-123">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в разделе " [**\_ вентилятор CIM**](cim-fan.md) ".</span><span class="sxs-lookup"><span data-stu-id="1c646-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Fan**](cim-fan.md) for documentation.</span></span><br/> |
| <span data-ttu-id="1c646-124">**сетспид**</span><span class="sxs-lookup"><span data-stu-id="1c646-124">**SetSpeed**</span></span>      | <span data-ttu-id="1c646-125">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="1c646-125">Not implemented.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="1c646-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c646-126">Properties</span></span>

<span data-ttu-id="1c646-127">Класс **\_ вентилятора Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1c646-127">The **Win32\_Fan** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c646-128">**активекулинг**</span><span class="sxs-lookup"><span data-stu-id="1c646-128">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1c646-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c646-131">Если **значение равно true**, устройство охлаждения обеспечивает охлаждение (в отличие от пассивного).</span><span class="sxs-lookup"><span data-stu-id="1c646-131">If **True**, the cooling device provides active (as opposed to passive) cooling.</span></span>

<span data-ttu-id="1c646-132">Это свойство наследуется от [**CIM \_ кулингдевице**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="1c646-132">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-133">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="1c646-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-134">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c646-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-136">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="1c646-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-137">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="1c646-137">Availability and status of the device.</span></span>

<span data-ttu-id="1c646-138">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1c646-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1c646-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c646-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="1c646-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1c646-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="1c646-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-142">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="1c646-142">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1c646-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="1c646-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1c646-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="1c646-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1c646-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="1c646-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1c646-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="1c646-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1c646-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="1c646-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1c646-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="1c646-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1c646-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="1c646-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1c646-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="1c646-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1c646-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="1c646-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1c646-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="1c646-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-153">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="1c646-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1c646-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="1c646-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-155">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="1c646-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1c646-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="1c646-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-157">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="1c646-157">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1c646-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="1c646-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1c646-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="1c646-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-160">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="1c646-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1c646-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="1c646-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-162">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="1c646-162">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1c646-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="1c646-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-164">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="1c646-164">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1c646-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="1c646-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-166">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="1c646-166">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1c646-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="1c646-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-168">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="1c646-168">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1c646-169">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="1c646-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c646-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-172">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1c646-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-173">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="1c646-173">Short description of the object a one-line string.</span></span>

<span data-ttu-id="1c646-174">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1c646-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-175">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="1c646-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-176">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c646-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-178">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1c646-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-179">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="1c646-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="1c646-180">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1c646-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="1c646-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="1c646-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="1c646-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-183">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="1c646-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1c646-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="1c646-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="1c646-185">(1)</span><span class="sxs-lookup"><span data-stu-id="1c646-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-186">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="1c646-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1c646-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1c646-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1c646-188">(2)</span><span class="sxs-lookup"><span data-stu-id="1c646-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1c646-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="1c646-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1c646-190">(3)</span><span class="sxs-lookup"><span data-stu-id="1c646-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-191">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c646-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1c646-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="1c646-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1c646-193">(4)</span><span class="sxs-lookup"><span data-stu-id="1c646-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-194">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="1c646-194">Device is not working properly.</span></span> <span data-ttu-id="1c646-195">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="1c646-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1c646-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="1c646-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1c646-197">(5)</span><span class="sxs-lookup"><span data-stu-id="1c646-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-198">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="1c646-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1c646-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="1c646-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1c646-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="1c646-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-201">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="1c646-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1c646-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="1c646-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="1c646-203">(7)</span><span class="sxs-lookup"><span data-stu-id="1c646-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1c646-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="1c646-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1c646-205">(8)</span><span class="sxs-lookup"><span data-stu-id="1c646-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-206">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="1c646-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1c646-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="1c646-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1c646-208">(9)</span><span class="sxs-lookup"><span data-stu-id="1c646-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-209">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="1c646-209">Device is not working properly.</span></span> <span data-ttu-id="1c646-210">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="1c646-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1c646-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="1c646-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="1c646-212">(10)</span><span class="sxs-lookup"><span data-stu-id="1c646-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-213">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="1c646-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1c646-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="1c646-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="1c646-215">(11)</span><span class="sxs-lookup"><span data-stu-id="1c646-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-216">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="1c646-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1c646-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="1c646-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1c646-218">(12)</span><span class="sxs-lookup"><span data-stu-id="1c646-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-219">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="1c646-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1c646-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1c646-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1c646-221">(13)</span><span class="sxs-lookup"><span data-stu-id="1c646-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-222">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="1c646-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1c646-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="1c646-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1c646-224">(14)</span><span class="sxs-lookup"><span data-stu-id="1c646-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-225">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="1c646-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1c646-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="1c646-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1c646-227">(15)</span><span class="sxs-lookup"><span data-stu-id="1c646-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-228">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="1c646-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1c646-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="1c646-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1c646-230">(16)</span><span class="sxs-lookup"><span data-stu-id="1c646-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-231">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="1c646-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1c646-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="1c646-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1c646-233">(17)</span><span class="sxs-lookup"><span data-stu-id="1c646-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-234">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="1c646-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1c646-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1c646-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1c646-236">(18)</span><span class="sxs-lookup"><span data-stu-id="1c646-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-237">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="1c646-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1c646-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="1c646-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="1c646-239">(19)</span><span class="sxs-lookup"><span data-stu-id="1c646-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1c646-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="1c646-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="1c646-241">(20)</span><span class="sxs-lookup"><span data-stu-id="1c646-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-242">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="1c646-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1c646-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="1c646-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1c646-244">(21)</span><span class="sxs-lookup"><span data-stu-id="1c646-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-245">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="1c646-245">System failure.</span></span> <span data-ttu-id="1c646-246">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="1c646-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="1c646-247">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="1c646-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1c646-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="1c646-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="1c646-249">(22)</span><span class="sxs-lookup"><span data-stu-id="1c646-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-250">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="1c646-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1c646-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="1c646-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1c646-252">(23)</span><span class="sxs-lookup"><span data-stu-id="1c646-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-253">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="1c646-253">System failure.</span></span> <span data-ttu-id="1c646-254">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="1c646-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1c646-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="1c646-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1c646-256">(24)</span><span class="sxs-lookup"><span data-stu-id="1c646-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-257">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="1c646-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1c646-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="1c646-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1c646-259">(25)</span><span class="sxs-lookup"><span data-stu-id="1c646-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-260">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="1c646-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1c646-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="1c646-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1c646-262">(26)</span><span class="sxs-lookup"><span data-stu-id="1c646-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-263">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="1c646-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1c646-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="1c646-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1c646-265">(27)</span><span class="sxs-lookup"><span data-stu-id="1c646-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-266">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="1c646-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1c646-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="1c646-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1c646-268">(28)</span><span class="sxs-lookup"><span data-stu-id="1c646-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-269">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="1c646-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1c646-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="1c646-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1c646-271">(29)</span><span class="sxs-lookup"><span data-stu-id="1c646-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-272">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="1c646-272">Device is disabled.</span></span> <span data-ttu-id="1c646-273">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="1c646-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1c646-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="1c646-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1c646-275">(30)</span><span class="sxs-lookup"><span data-stu-id="1c646-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-276">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="1c646-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1c646-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="1c646-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1c646-278">1-31</span><span class="sxs-lookup"><span data-stu-id="1c646-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-279">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="1c646-279">Device is not working properly.</span></span> <span data-ttu-id="1c646-280">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="1c646-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1c646-281">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="1c646-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-282">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1c646-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-284">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1c646-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-285">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="1c646-285">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1c646-286">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1c646-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c646-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-290">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1c646-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1c646-291">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="1c646-291">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1c646-292">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="1c646-292">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="1c646-293">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-294">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1c646-294">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-295">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c646-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-297">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="1c646-297">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-298">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="1c646-298">Description of the object.</span></span>

<span data-ttu-id="1c646-299">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1c646-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-300">**десиредспид**</span><span class="sxs-lookup"><span data-stu-id="1c646-300">**DesiredSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-301">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c646-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-303">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("революция в минуту")</span><span class="sxs-lookup"><span data-stu-id="1c646-303">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("revolutions per minute")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-304">Текущая запрошенная скорость вентилятора, определенная в революциях в минуту, при поддержке вентилятора с переменной скоростью (**вариаблеспид** имеет **значение true**).</span><span class="sxs-lookup"><span data-stu-id="1c646-304">Currently requested fan speed, defined in revolutions per minute, when a variable speed fan is supported (**VariableSpeed** is **TRUE**).</span></span> <span data-ttu-id="1c646-305">Текущая скорость определяется датчиком ([**CIM \_ тахометр**](cim-tachometer.md)), связанным с вентилятором с помощью отношения [**CIM \_ ассоЦиатедсенсор**](cim-associatedsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="1c646-305">The current speed is determined by a sensor ([**CIM\_Tachometer**](cim-tachometer.md)) that is associated with the fan using the [**CIM\_AssociatedSensor**](cim-associatedsensor.md) relationship.</span></span>

<span data-ttu-id="1c646-306">Это свойство наследуется [**от \_ вентилятора CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="1c646-306">This property is inherited from [**CIM\_Fan**](cim-fan.md).</span></span>

<span data-ttu-id="1c646-307">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1c646-307">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-308">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1c646-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c646-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-311">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1c646-311">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-312">Идентифицирует устройство вентиляторов.</span><span class="sxs-lookup"><span data-stu-id="1c646-312">Identifies the fan device.</span></span> <span data-ttu-id="1c646-313">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-314">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="1c646-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-315">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1c646-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c646-317">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="1c646-317">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="1c646-318">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1c646-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-320">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c646-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c646-322">Произвольная строка, предоставляя дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="1c646-322">Free-form string supplying more information about the error recorded in **LastErrorCode** property, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="1c646-323">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-324">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1c646-324">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-325">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1c646-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-327">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="1c646-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-328">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="1c646-328">Date and time the object was installed.</span></span> <span data-ttu-id="1c646-329">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="1c646-329">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1c646-330">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1c646-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-331">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="1c646-331">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-332">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c646-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c646-334">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="1c646-334">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1c646-335">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-336">**Name**</span><span class="sxs-lookup"><span data-stu-id="1c646-336">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c646-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-339">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="1c646-339">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-340">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="1c646-340">Label by which the object is known.</span></span> <span data-ttu-id="1c646-341">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="1c646-341">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="1c646-342">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1c646-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-343">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1c646-343">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-344">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c646-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-346">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1c646-346">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-347">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="1c646-347">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="1c646-348">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1c646-349">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1c646-349">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="1c646-350">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="1c646-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-351">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="1c646-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1c646-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c646-353">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="1c646-353">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="1c646-354">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-354">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c646-355"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1c646-355"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1c646-356"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="1c646-356"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-357">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="1c646-357">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1c646-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="1c646-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1c646-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="1c646-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-360">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="1c646-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1c646-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="1c646-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-362">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="1c646-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1c646-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="1c646-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-364">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="1c646-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="1c646-365">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="1c646-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="1c646-366">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="1c646-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1c646-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="1c646-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-368">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="1c646-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1c646-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="1c646-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1c646-370">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="1c646-370">Timed Power-On Supported</span></span>

<span data-ttu-id="1c646-371">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="1c646-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1c646-372">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="1c646-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-373">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1c646-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c646-375">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="1c646-375">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="1c646-376">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="1c646-376">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="1c646-377">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-378">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1c646-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c646-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-381">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="1c646-381">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-382">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="1c646-382">Current status of the object.</span></span> <span data-ttu-id="1c646-383">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="1c646-383">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1c646-384">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="1c646-384">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1c646-385">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="1c646-385">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1c646-386">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="1c646-386">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1c646-387">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="1c646-387">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1c646-388">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1c646-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1c646-389">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="1c646-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1c646-390">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="1c646-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1c646-391">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="1c646-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1c646-392">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="1c646-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c646-393">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="1c646-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1c646-394">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="1c646-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1c646-395">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="1c646-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1c646-396">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="1c646-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1c646-397">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="1c646-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1c646-398">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="1c646-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1c646-399">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="1c646-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1c646-400">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="1c646-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1c646-401">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="1c646-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c646-402">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1c646-402">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-403">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c646-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-405">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="1c646-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1c646-406">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="1c646-406">State of the logical device.</span></span> <span data-ttu-id="1c646-407">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="1c646-407">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="1c646-408">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1c646-409">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="1c646-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c646-410">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="1c646-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1c646-411">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="1c646-411">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1c646-412">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="1c646-412">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1c646-413">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="1c646-413">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c646-414">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="1c646-414">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-415">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c646-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-417">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1c646-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1c646-418">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="1c646-418">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="1c646-419">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-420">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1c646-420">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-421">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1c646-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c646-423">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1c646-423">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1c646-424">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="1c646-424">Name of the scoping system.</span></span>

<span data-ttu-id="1c646-425">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="1c646-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c646-426">**вариаблеспид**</span><span class="sxs-lookup"><span data-stu-id="1c646-426">**VariableSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c646-427">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="1c646-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1c646-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c646-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c646-429">**Значение true** показывает, что вентилятор поддерживает переменные скорости.</span><span class="sxs-lookup"><span data-stu-id="1c646-429">If **True**, the fan supports variable speeds.</span></span>

<span data-ttu-id="1c646-430">Это свойство наследуется [**от \_ вентилятора CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="1c646-430">This property is inherited from [**CIM\_Fan**](cim-fan.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c646-431">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c646-431">Remarks</span></span>

<span data-ttu-id="1c646-432">Класс **\_ вентилятора Win32** является производным от [**\_ вентилятора CIM**](cim-fan.md).</span><span class="sxs-lookup"><span data-stu-id="1c646-432">The **Win32\_Fan** class is derived from [**CIM\_Fan**](cim-fan.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1c646-433">Примеры</span><span class="sxs-lookup"><span data-stu-id="1c646-433">Examples</span></span>

<span data-ttu-id="1c646-434">Пример " [список сведений о вентиляторе компьютера](https://Gallery.TechNet.Microsoft.Com/d1534503-704f-4450-8dab-f3e760bf818c) " извлекает сведения о вентиляторах охлаждения, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1c646-434">The [List Computer Fan Information](https://Gallery.TechNet.Microsoft.Com/d1534503-704f-4450-8dab-f3e760bf818c) PowerShell sample retrieves information about the cooling fans installed in a computer.</span></span>

<span data-ttu-id="1c646-435">В следующем примере извлекаются сведения о охлаждающих вентиляторах, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1c646-435">The following sample retrieves information about the cooling fans installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_Fan") 
 
For Each objItem in colItems 
    Wscript.Echo "Active Cooling: " & objItem.ActiveCooling 
    Wscript.Echo "Availability: " & objItem.Availability 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Status Information: " & objItem.StatusInfo 
    Wscript.Echo 
Next
```


```PowerShell
$colItems = Get-WmiObject Win32_Fan -Namespace "root\cimv2"
foreach ($objItem in $colItems)
{
    "Active Cooling: " + $objItem.ActiveCooling 
    "Availability: " + $objItem.Availability 
    "Device ID: " + $objItem.DeviceID 
    "Name: " + $objItem.Name 
    "Status Information: " + $objItem.StatusInfo 
}
```





## <a name="requirements"></a><span data-ttu-id="1c646-436">Требования</span><span class="sxs-lookup"><span data-stu-id="1c646-436">Requirements</span></span>



| <span data-ttu-id="1c646-437">Требование</span><span class="sxs-lookup"><span data-stu-id="1c646-437">Requirement</span></span> | <span data-ttu-id="1c646-438">Значение</span><span class="sxs-lookup"><span data-stu-id="1c646-438">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c646-439">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c646-439">Minimum supported client</span></span><br/> | <span data-ttu-id="1c646-440">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c646-440">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c646-441">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c646-441">Minimum supported server</span></span><br/> | <span data-ttu-id="1c646-442">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c646-442">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c646-443">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1c646-443">Namespace</span></span><br/>                | <span data-ttu-id="1c646-444">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1c646-444">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c646-445">MOF</span><span class="sxs-lookup"><span data-stu-id="1c646-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c646-446"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c646-446"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c646-447">DLL</span><span class="sxs-lookup"><span data-stu-id="1c646-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c646-448"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c646-448"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c646-449">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c646-449">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c646-450">**\_Вентилятор CIM**</span><span class="sxs-lookup"><span data-stu-id="1c646-450">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dt>

[<span data-ttu-id="1c646-451">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="1c646-451">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

