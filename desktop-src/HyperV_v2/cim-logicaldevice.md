---
description: Абстракция или Эмуляция аппаратной сущности, которая может быть не основана на физическом оборудовании.
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: Класс CIM_LogicalDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.OtherIdentifyingInfo
- CIM_LogicalDevice.PowerOnHours
- CIM_LogicalDevice.TotalPowerOnHours
- CIM_LogicalDevice.IdentifyingDescriptions
- CIM_LogicalDevice.AdditionalAvailability
- CIM_LogicalDevice.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 471b10f8d3c8640cfcc4277d0151bdd46d59db86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808392"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="21173-103">Класс CIM_LogicalDevice (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="21173-103">CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="21173-104">Абстракция или Эмуляция аппаратной сущности, которая может быть не основана на физическом оборудовании.</span><span class="sxs-lookup"><span data-stu-id="21173-104">An abstraction or emulation of a hardware entity that may or may not be based on physical hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="21173-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21173-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_LogicalDevice : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  DeviceID;
  boolean PowerManagementSupported;
  uint16  PowerManagementCapabilities[];
  uint16  Availability;
  uint16  StatusInfo;
  uint32  LastErrorCode;
  string  ErrorDescription;
  boolean ErrorCleared;
  string  OtherIdentifyingInfo[];
  uint64  PowerOnHours;
  uint64  TotalPowerOnHours;
  string  IdentifyingDescriptions[];
  uint16  AdditionalAvailability[];
  uint64  MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="21173-106">Члены</span><span class="sxs-lookup"><span data-stu-id="21173-106">Members</span></span>

<span data-ttu-id="21173-107">Класс **класса \_ CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="21173-107">The **CIM\_LogicalDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="21173-108">Методы</span><span class="sxs-lookup"><span data-stu-id="21173-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="21173-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="21173-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="21173-110">Методы</span><span class="sxs-lookup"><span data-stu-id="21173-110">Methods</span></span>

<span data-ttu-id="21173-111">Класс **класса \_ CIM** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="21173-111">The **CIM\_LogicalDevice** class has these methods.</span></span>



| <span data-ttu-id="21173-112">Метод</span><span class="sxs-lookup"><span data-stu-id="21173-112">Method</span></span>                                                           | <span data-ttu-id="21173-113">Описание</span><span class="sxs-lookup"><span data-stu-id="21173-113">Description</span></span>                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21173-114">**енабледевице**</span><span class="sxs-lookup"><span data-stu-id="21173-114">**EnableDevice**</span></span>](cim-logicaldevice-enabledevice.md)           | <span data-ttu-id="21173-115">Этот метод является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="21173-115">This method is deprecated.</span></span> <span data-ttu-id="21173-116">Вместо этого используйте метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="21173-116">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="21173-117">**Нерекомендуемое описание:** Включает или отключает логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="21173-117">**Deprecated description:** Enables or disables the logical device.</span></span><br/>                                                                     |
| [<span data-ttu-id="21173-118">**онлинедевице**</span><span class="sxs-lookup"><span data-stu-id="21173-118">**OnlineDevice**</span></span>](cim-logicaldevice-onlinedevice.md)           | <span data-ttu-id="21173-119">Этот метод является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="21173-119">This method is deprecated.</span></span> <span data-ttu-id="21173-120">Вместо этого используйте метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="21173-120">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="21173-121">**Нерекомендуемое описание:** Переводит логическое устройство в режим «в сети», чтобы он мог принимать запросы или в режиме «вне сети», чтобы он больше не мог принимать запросы.</span><span class="sxs-lookup"><span data-stu-id="21173-121">**Deprecated description:** Brings the logical device online so it can accept requests, or offline so it can no longer accept requests.</span></span><br/> |
| [<span data-ttu-id="21173-122">**куиесцедевице**</span><span class="sxs-lookup"><span data-stu-id="21173-122">**QuiesceDevice**</span></span>](cim-logicaldevice-quiescedevice.md)         | <span data-ttu-id="21173-123">Этот метод является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="21173-123">This method is deprecated.</span></span> <span data-ttu-id="21173-124">Вместо этого используйте метод **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="21173-124">Instead, use the **RequestStateChange** method.</span></span><br/> <span data-ttu-id="21173-125">**Нерекомендуемое описание:** Временно приостанавливает действие на логическом устройстве или повторно включает действие.</span><span class="sxs-lookup"><span data-stu-id="21173-125">**Deprecated description:** Temporarily suspends activity on the logical device, or re-enables the activity.</span></span><br/>                            |
| [<span data-ttu-id="21173-126">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="21173-126">**Reset**</span></span>](cim-logicaldevice-reset.md)                         | <span data-ttu-id="21173-127">Сбрасывает логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="21173-127">Resets the logical device.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="21173-128">**ресторепропертиес**</span><span class="sxs-lookup"><span data-stu-id="21173-128">**RestoreProperties**</span></span>](cim-logicaldevice-restoreproperties.md) | <span data-ttu-id="21173-129">Восстанавливает предыдущую конфигурацию и состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="21173-129">Restores a previous configuration and state of the logical device.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="21173-130">**савепропертиес**</span><span class="sxs-lookup"><span data-stu-id="21173-130">**SaveProperties**</span></span>](cim-logicaldevice-saveproperties.md)       | <span data-ttu-id="21173-131">Сохраняет конфигурацию и состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="21173-131">Saves the configuration and state of the logical device.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="21173-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="21173-132">**SetPowerState**</span></span>](cim-logicaldevice-setpowerstate.md)         | <span data-ttu-id="21173-133">Этот метод является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="21173-133">This method is deprecated.</span></span> <span data-ttu-id="21173-134">Вместо этого используйте свойство **SetPowerState** класса **CIM \_ поверманажементсервице** .</span><span class="sxs-lookup"><span data-stu-id="21173-134">Instead, use the **SetPowerState** property of the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="21173-135">**Нерекомендуемое описание:** Задает состояние электропитания логического устройства.</span><span class="sxs-lookup"><span data-stu-id="21173-135">**Deprecated description:** Sets the power state of the logical device.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="21173-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="21173-136">Properties</span></span>

<span data-ttu-id="21173-137">Класс **класса \_ CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="21173-137">The **CIM\_LogicalDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21173-138">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="21173-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-139">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="21173-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="21173-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-141">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ -модель**".**Доступность**)</span><span class="sxs-lookup"><span data-stu-id="21173-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**Availability**")</span></span>
</dt> </dl>

<span data-ttu-id="21173-142">Массив, содержащий сведения о доступности логического устройства в дополнение к свойству **доступности** .</span><span class="sxs-lookup"><span data-stu-id="21173-142">An array that contains availability information about of the logical device, in addition to the that of the **Availability** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21173-143">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="21173-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21173-144">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="21173-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="21173-145">**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="21173-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="21173-146">**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="21173-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="21173-147">**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="21173-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="21173-148">**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="21173-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="21173-149">**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="21173-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="21173-150">Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="21173-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="21173-151">Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="21173-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="21173-152">**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="21173-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="21173-153">**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="21173-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="21173-154">**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="21173-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="21173-155">Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="21173-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="21173-156">Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="21173-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="21173-157">Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="21173-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="21173-158">**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="21173-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="21173-159">Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="21173-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="21173-160">**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="21173-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="21173-161">**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="21173-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="21173-162">**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="21173-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="21173-163">**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="21173-163">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21173-164">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="21173-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-165">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21173-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21173-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-167">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 006,5 "," MIB. В файле IETF \| Host-Resources-MIB. хрдевицестатус "," MIF. DMTF \| Host Device \| 001,5 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_**-оборудование ".**Аддитионалаваилабилити**")</span><span class="sxs-lookup"><span data-stu-id="21173-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus", "MIF.DMTF\|Host Device\|001.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**AdditionalAvailability**")</span></span>
</dt> </dl>

<span data-ttu-id="21173-168">Содержит сведения о доступности логического устройства.</span><span class="sxs-lookup"><span data-stu-id="21173-168">Contains the availability of the logical device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21173-169">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="21173-169">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21173-170">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="21173-170">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="21173-171">**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="21173-171">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="21173-172">**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="21173-172">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="21173-173">**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="21173-173">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="21173-174">**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="21173-174">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="21173-175">**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="21173-175">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="21173-176">Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="21173-176">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="21173-177">Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="21173-177">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="21173-178">**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="21173-178">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="21173-179">**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="21173-179">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="21173-180">**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="21173-180">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="21173-181">Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="21173-181">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="21173-182">Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="21173-182">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="21173-183">Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="21173-183">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="21173-184">**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="21173-184">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="21173-185">Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="21173-185">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="21173-186">**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="21173-186">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="21173-187">**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="21173-187">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="21173-188">**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="21173-188">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="21173-189">**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="21173-189">**Quiesced** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21173-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="21173-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21173-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21173-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-193">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="21173-193">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="21173-194">Имя класса, используемое для создания экземпляра логического устройства.</span><span class="sxs-lookup"><span data-stu-id="21173-194">The class name used to create an instance of the logical device.</span></span> <span data-ttu-id="21173-195">**Свойство CreationClassName** объединяется с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="21173-195">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="21173-196">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="21173-196">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-197">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21173-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21173-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-199">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="21173-199">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="21173-200">Уникальный идентификатор логического устройства, например адрес.</span><span class="sxs-lookup"><span data-stu-id="21173-200">A unique identifier of the logical device, such as the address.</span></span>

</dd> <dt>

<span data-ttu-id="21173-201">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="21173-201">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-202">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21173-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21173-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-204">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="21173-204">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="21173-205">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="21173-205">This property is deprecated.</span></span> <span data-ttu-id="21173-206">Вместо этого используйте свойство **OperationalStatus** из класса **CIM \_ манажедсистемелемент** .</span><span class="sxs-lookup"><span data-stu-id="21173-206">Instead, use the **OperationalStatus** property from the **CIM\_ManagedSystemElement** class.</span></span>

<span data-ttu-id="21173-207">**Нерекомендуемое описание:** Указывает, удаляется ли ошибка, сообщаемая свойством **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="21173-207">**Deprecated description:** Indicates whether an error reported by the **LastErrorCode** property is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="21173-208">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="21173-208">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-209">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21173-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21173-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-211">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ девицееррордата. ErrorDescription")</span><span class="sxs-lookup"><span data-stu-id="21173-211">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.ErrorDescription")</span></span>
</dt> </dl>

<span data-ttu-id="21173-212">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="21173-212">This property is deprecated.</span></span> <span data-ttu-id="21173-213">Вместо этого используйте свойство **ErrorDescription** класса **CIM \_ девицееррордата** .</span><span class="sxs-lookup"><span data-stu-id="21173-213">Instead, use the **ErrorDescription** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="21173-214">**Нерекомендуемое описание:** Дополнительные сведения об ошибке, о которых сообщает свойство **ластерроркоде** .</span><span class="sxs-lookup"><span data-stu-id="21173-214">**Deprecated description:** Additional information about the error reported by the **LastErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="21173-215">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="21173-215">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-216">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="21173-216">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="21173-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-218">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ -модель**".**Осеридентифингинфо**")</span><span class="sxs-lookup"><span data-stu-id="21173-218">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**OtherIdentifyingInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="21173-219">Массив строк, описывающих элементы массива **осеридентифингинфо** одного индекса.</span><span class="sxs-lookup"><span data-stu-id="21173-219">An array of strings that describe the **OtherIdentifyingInfo** array items of the same index.</span></span>

</dd> <dt>

<span data-ttu-id="21173-220">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="21173-220">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-221">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21173-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21173-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-223">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ девицееррордата. ластерроркоде")</span><span class="sxs-lookup"><span data-stu-id="21173-223">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_DeviceErrorData.LastErrorCode")</span></span>
</dt> </dl>

<span data-ttu-id="21173-224">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="21173-224">This property is deprecated.</span></span> <span data-ttu-id="21173-225">Вместо этого мы используем свойство **ластерроркоде** из класса **CIM \_ девицееррордата** .</span><span class="sxs-lookup"><span data-stu-id="21173-225">Instead, we use the **LastErrorCode** property from the **CIM\_DeviceErrorData** class.</span></span>

<span data-ttu-id="21173-226">**Нерекомендуемое описание:** Последний код ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="21173-226">**Deprecated description:** The last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="21173-227">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="21173-227">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-228">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="21173-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="21173-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-230">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунд")</span><span class="sxs-lookup"><span data-stu-id="21173-230">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="21173-231">Это свойство является устаревшим и не должно использоваться.</span><span class="sxs-lookup"><span data-stu-id="21173-231">This property is deprecated and should not be used.</span></span>

<span data-ttu-id="21173-232">**Нерекомендуемое описание:** Максимальное время в миллисекундах, в течение которого устройство может оставаться в временно отключенном состоянии (свойства **доступности** и **аддитионалаваилабилити** задано как "21" загружена).</span><span class="sxs-lookup"><span data-stu-id="21173-232">**Deprecated description:** The maximum time in milliseconds, that a device can remain in a temporarily disabled state (**Availability** and **AdditionalAvailability** properties set to "21"   quiescent ).</span></span> <span data-ttu-id="21173-233">Значение "0" указывает, что логическое устройство может оставаться в временно отключенном состоянии в течение неограниченного времени.</span><span class="sxs-lookup"><span data-stu-id="21173-233">A value of "0" indicates that the logical device can remain in a temporarily disabled state indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="21173-234">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="21173-234">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-235">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="21173-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="21173-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-237">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ -модель**".**Идентифингдескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="21173-237">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalDevice**.**IdentifyingDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="21173-238">Сведения, идентифицирующие логическое устройство, отличное от **DeviceID**.</span><span class="sxs-lookup"><span data-stu-id="21173-238">Information that identifies the logical device, other than **DeviceID**.</span></span>

</dd> <dt>

<span data-ttu-id="21173-239">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="21173-239">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-240">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="21173-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="21173-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-242">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ поверманажементкапабилитиес. поверкапабилитиес")</span><span class="sxs-lookup"><span data-stu-id="21173-242">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="21173-243">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="21173-243">This property is deprecated.</span></span> <span data-ttu-id="21173-244">Вместо этого используйте класс **CIM \_ поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="21173-244">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="21173-245">**Нерекомендуемое описание:** Массив, содержащий возможности управления питанием устройства.</span><span class="sxs-lookup"><span data-stu-id="21173-245">**Deprecated description:** An array that contains the power management capabilities of the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21173-246">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="21173-246">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="21173-247">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="21173-247">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="21173-248">**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="21173-248">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="21173-249">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="21173-249">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="21173-250">**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="21173-250">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="21173-251">**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="21173-251">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="21173-252">**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="21173-252">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="21173-253">**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="21173-253">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21173-254">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="21173-254">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-255">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="21173-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="21173-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-257">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ поверманажементкапабилитиес")</span><span class="sxs-lookup"><span data-stu-id="21173-257">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities")</span></span>
</dt> </dl>

<span data-ttu-id="21173-258">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="21173-258">This property is deprecated.</span></span> <span data-ttu-id="21173-259">Вместо этого используйте класс **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="21173-259">Instead, use the **PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="21173-260">**Нерекомендуемое описание: true** , если логическое устройство может управляться питанием; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="21173-260">**Deprecated description:  true** if the logical device can be power managed; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="21173-261">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="21173-261">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-262">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="21173-262">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="21173-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-264">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("Часы"), **Счетчик**</span><span class="sxs-lookup"><span data-stu-id="21173-264">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="21173-265">Число последовательных часов, на которое было включено логическое устройство, с момента его последнего цикла питания.</span><span class="sxs-lookup"><span data-stu-id="21173-265">The number of consecutive hours the logical device has been powered, since its last power cycle.</span></span>

</dd> <dt>

<span data-ttu-id="21173-266">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="21173-266">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-267">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="21173-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="21173-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-269">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md).**EnabledState**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Рабочее состояние DMTF \| 006,4 ")</span><span class="sxs-lookup"><span data-stu-id="21173-269">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|006.4")</span></span>
</dt> </dl>

<span data-ttu-id="21173-270">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="21173-270">This property is deprecated.</span></span> <span data-ttu-id="21173-271">Вместо этого используйте класс **CIM \_ поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="21173-271">Instead, use the **CIM\_PowerManagementCapabilities** class.</span></span>

<span data-ttu-id="21173-272">**Нерекомендуемое описание:** Указывает, включено ли логическое устройство или находится в связанном состоянии.</span><span class="sxs-lookup"><span data-stu-id="21173-272">**Deprecated description:** Indicates whether the logical device is enabled or in a related state.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="21173-273">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="21173-273">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="21173-274">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="21173-274">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="21173-275">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="21173-275">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="21173-276">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="21173-276">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="21173-277">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="21173-277">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="21173-278">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="21173-278">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21173-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21173-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-281">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="21173-281">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="21173-282">Имя класса, используемое для создания экземпляра системы, содержащей логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="21173-282">The class name used to create an instance of the system that contains the logical device.</span></span> <span data-ttu-id="21173-283">**Системкреатионкласснаме** сочетается с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="21173-283">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="21173-284">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="21173-284">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-285">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21173-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21173-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-287">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**")</span><span class="sxs-lookup"><span data-stu-id="21173-287">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="21173-288">Имя системы, содержащей логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="21173-288">The name of the system that contains the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="21173-289">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="21173-289">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21173-290">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="21173-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="21173-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21173-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21173-292">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("Часы"), **Счетчик**</span><span class="sxs-lookup"><span data-stu-id="21173-292">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hours"), **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="21173-293">Общее число часов, в течение которых логическое устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="21173-293">The total number of hours the logical device has been powered.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21173-294">Требования</span><span class="sxs-lookup"><span data-stu-id="21173-294">Requirements</span></span>



| <span data-ttu-id="21173-295">Требование</span><span class="sxs-lookup"><span data-stu-id="21173-295">Requirement</span></span> | <span data-ttu-id="21173-296">Значение</span><span class="sxs-lookup"><span data-stu-id="21173-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21173-297">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21173-297">Minimum supported client</span></span><br/> | <span data-ttu-id="21173-298">Windows 8</span><span class="sxs-lookup"><span data-stu-id="21173-298">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="21173-299">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21173-299">Minimum supported server</span></span><br/> | <span data-ttu-id="21173-300">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21173-300">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="21173-301">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="21173-301">Namespace</span></span><br/>                | <span data-ttu-id="21173-302">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="21173-302">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="21173-303">MOF</span><span class="sxs-lookup"><span data-stu-id="21173-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21173-304"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21173-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="21173-305">DLL</span><span class="sxs-lookup"><span data-stu-id="21173-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21173-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="21173-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="21173-307">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21173-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21173-308">**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="21173-308">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

