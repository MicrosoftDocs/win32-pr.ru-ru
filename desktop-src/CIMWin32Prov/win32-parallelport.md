---
description: '&Win32 \_ параллелпорт \# 32; Класс WMI представляет свойства параллельного порта в компьютерной системе под Windows.'
ms.assetid: 986bd27f-71b0-4a40-a421-a8bfc0f081be
ms.tgt_platform: multiple
title: Класс Win32_ParallelPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ParallelPort
- Win32_ParallelPort.Reset
- Win32_ParallelPort.SetPowerState
- Win32_ParallelPort.Availability
- Win32_ParallelPort.Capabilities
- Win32_ParallelPort.CapabilityDescriptions
- Win32_ParallelPort.Caption
- Win32_ParallelPort.ConfigManagerErrorCode
- Win32_ParallelPort.ConfigManagerUserConfig
- Win32_ParallelPort.CreationClassName
- Win32_ParallelPort.Description
- Win32_ParallelPort.DeviceID
- Win32_ParallelPort.DMASupport
- Win32_ParallelPort.ErrorCleared
- Win32_ParallelPort.ErrorDescription
- Win32_ParallelPort.InstallDate
- Win32_ParallelPort.LastErrorCode
- Win32_ParallelPort.MaxNumberControlled
- Win32_ParallelPort.Name
- Win32_ParallelPort.OSAutoDiscovered
- Win32_ParallelPort.PNPDeviceID
- Win32_ParallelPort.PowerManagementCapabilities
- Win32_ParallelPort.PowerManagementSupported
- Win32_ParallelPort.ProtocolSupported
- Win32_ParallelPort.Status
- Win32_ParallelPort.StatusInfo
- Win32_ParallelPort.SystemCreationClassName
- Win32_ParallelPort.SystemName
- Win32_ParallelPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: da2ed3b34f3655067fd5ae41c31424e7599789c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142460"
---
# <a name="win32_parallelport-class"></a><span data-ttu-id="bf3f5-103">\_Класс Win32 параллелпорт</span><span class="sxs-lookup"><span data-stu-id="bf3f5-103">Win32\_ParallelPort class</span></span>

<span data-ttu-id="bf3f5-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ параллелпорт для Win32** представляет свойства параллельного порта в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-104">The **Win32\_ParallelPort** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a parallel port on a computer system running Windows.</span></span>

<span data-ttu-id="bf3f5-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bf3f5-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf3f5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf3f5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class  Win32_ParallelPort : CIM_ParallelController
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
  boolean  OSAutoDiscovered;
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

## <a name="members"></a><span data-ttu-id="bf3f5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="bf3f5-108">Members</span></span>

<span data-ttu-id="bf3f5-109">Класс **Win32 \_ параллелпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bf3f5-109">The **Win32\_ParallelPort** class has these types of members:</span></span>

-   [<span data-ttu-id="bf3f5-110">Методы</span><span class="sxs-lookup"><span data-stu-id="bf3f5-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bf3f5-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="bf3f5-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bf3f5-112">Методы</span><span class="sxs-lookup"><span data-stu-id="bf3f5-112">Methods</span></span>

<span data-ttu-id="bf3f5-113">Класс **Win32 \_ параллелпорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-113">The **Win32\_ParallelPort** class has these methods.</span></span>



| <span data-ttu-id="bf3f5-114">Метод</span><span class="sxs-lookup"><span data-stu-id="bf3f5-114">Method</span></span>            | <span data-ttu-id="bf3f5-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bf3f5-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf3f5-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-116">**Reset**</span></span>         | <span data-ttu-id="bf3f5-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-117">Not implemented.</span></span> <span data-ttu-id="bf3f5-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ параллелконтроллер**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="bf3f5-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-119">**SetPowerState**</span></span> | <span data-ttu-id="bf3f5-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-120">Not implemented.</span></span> <span data-ttu-id="bf3f5-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ параллелконтроллер**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bf3f5-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="bf3f5-122">Properties</span></span>

<span data-ttu-id="bf3f5-123">Класс **Win32 \_ параллелпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-123">The **Win32\_ParallelPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf3f5-124">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-127">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-128">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-128">Availability and status of the device.</span></span>

<span data-ttu-id="bf3f5-129">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bf3f5-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bf3f5-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="bf3f5-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-133">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="bf3f5-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="bf3f5-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="bf3f5-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bf3f5-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="bf3f5-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="bf3f5-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="bf3f5-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bf3f5-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="bf3f5-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="bf3f5-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="bf3f5-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-144">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="bf3f5-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-146">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="bf3f5-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-148">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="bf3f5-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="bf3f5-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-151">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="bf3f5-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-153">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="bf3f5-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-155">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="bf3f5-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-157">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="bf3f5-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-159">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf3f5-160">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-160">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-161">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="bf3f5-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-163">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. \|Параллельные порты DMTF \| 003,8 "), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ параллелконтроллер**](cim-parallelcontroller.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-163">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.8"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-164">Массив возможностей параллельного контроллера.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-164">Array of the capabilities of the parallel controller.</span></span>

<span data-ttu-id="bf3f5-165">Это свойство наследуется от [**CIM \_ параллелконтроллер**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-165">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bf3f5-166">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bf3f5-167">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-167">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="bf3f5-168">**XT/AT-совместимый** (2)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-168">**XT/AT Compatible** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2_Compatible"></span><span id="ps_2_compatible"></span><span id="PS_2_COMPATIBLE"></span>

<span data-ttu-id="bf3f5-169">**Совместимость с PS/2** (3)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-169">**PS/2 Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ECP"></span><span id="ecp"></span>

<span data-ttu-id="bf3f5-170">**ECP** (4)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-170">**ECP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EPP"></span><span id="epp"></span>

<span data-ttu-id="bf3f5-171">**EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-171">**EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="bf3f5-172">**PC-98** (6)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-172">**PC-98** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="bf3f5-173">**PC-98-хиресо** (7)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-173">**PC-98-Hireso** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="bf3f5-174">**PC-H98** (8)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-174">**PC-H98** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf3f5-175">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-176">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-178">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ параллелконтроллер**](cim-parallelcontroller.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-178">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-179">Массив более подробных объяснений для любой из функций параллельного контроллера, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="bf3f5-179">Array of more detailed explanations for any of the parallel controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="bf3f5-180">Каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-180">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="bf3f5-181">Это свойство наследуется от [**CIM \_ параллелконтроллер**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-181">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-182">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-185">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-186">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-186">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="bf3f5-187">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-188">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-189">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-191">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-191">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-192">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="bf3f5-193">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="bf3f5-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="bf3f5-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-196">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="bf3f5-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="bf3f5-198">(1)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-199">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bf3f5-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="bf3f5-201">(2)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="bf3f5-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="bf3f5-203">(3)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-204">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bf3f5-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="bf3f5-206">(4)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-207">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-207">Device is not working properly.</span></span> <span data-ttu-id="bf3f5-208">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="bf3f5-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="bf3f5-210">(5)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-211">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="bf3f5-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="bf3f5-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-214">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="bf3f5-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="bf3f5-216">(7)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="bf3f5-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="bf3f5-218">(8)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-219">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="bf3f5-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="bf3f5-221">(9)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-222">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-222">Device is not working properly.</span></span> <span data-ttu-id="bf3f5-223">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="bf3f5-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="bf3f5-225">(10)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-226">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="bf3f5-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="bf3f5-228">(11)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-229">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="bf3f5-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="bf3f5-231">(12)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-232">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="bf3f5-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="bf3f5-234">(13)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-235">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="bf3f5-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="bf3f5-237">(14)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-238">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="bf3f5-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="bf3f5-240">(15)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-241">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="bf3f5-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="bf3f5-243">(16)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-244">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="bf3f5-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="bf3f5-246">(17)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-247">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bf3f5-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="bf3f5-249">(18)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-250">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="bf3f5-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="bf3f5-252">(19)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bf3f5-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="bf3f5-254">(20)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-255">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="bf3f5-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="bf3f5-257">(21)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-258">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-258">System failure.</span></span> <span data-ttu-id="bf3f5-259">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="bf3f5-260">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="bf3f5-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="bf3f5-262">(22)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-263">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="bf3f5-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="bf3f5-265">(23)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-266">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-266">System failure.</span></span> <span data-ttu-id="bf3f5-267">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="bf3f5-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="bf3f5-269">(24)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-270">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bf3f5-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bf3f5-272">(25)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-273">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bf3f5-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bf3f5-275">(26)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-276">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="bf3f5-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="bf3f5-278">(27)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-279">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="bf3f5-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="bf3f5-281">(28)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-282">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="bf3f5-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="bf3f5-284">(29)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-285">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-285">Device is disabled.</span></span> <span data-ttu-id="bf3f5-286">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="bf3f5-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="bf3f5-288">(30)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-289">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bf3f5-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="bf3f5-291">1-31</span><span class="sxs-lookup"><span data-stu-id="bf3f5-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-292">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-292">Device is not working properly.</span></span> <span data-ttu-id="bf3f5-293">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf3f5-294">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-295">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-297">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-297">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-298">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="bf3f5-299">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-303">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-303">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-304">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-304">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="bf3f5-305">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-305">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="bf3f5-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-307">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-308">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-310">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-310">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-311">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-311">Description of the object.</span></span>

<span data-ttu-id="bf3f5-312">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-314">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-316">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-316">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-317">Идентификатор параллельного порта.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-317">Identifier of the parallel port.</span></span>

<span data-ttu-id="bf3f5-318">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-319">**дмасуппорт**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-319">**DMASupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-320">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-322">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Параллельные порты DMTF \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-322">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-323">Если **значение — true**, параллельный порт поддерживает DMA.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-323">If **TRUE**, the parallel port supports DMA.</span></span>

<span data-ttu-id="bf3f5-324">Это свойство наследуется от [**CIM \_ параллелконтроллер**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-324">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-325">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-325">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-326">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-328">Если **значение — true**, ошибка, обнаруженная в **ластерроркоде** , удаляется.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-328">If **TRUE**, the error reported in **LastErrorCode** is cleared.</span></span>

<span data-ttu-id="bf3f5-329">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-330">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-330">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-333">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-333">More information about the error recorded in **LastErrorCode**, and information about corrective actions that might be taken.</span></span>

<span data-ttu-id="bf3f5-334">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-336">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-338">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-339">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-339">Date and time the object was installed.</span></span> <span data-ttu-id="bf3f5-340">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="bf3f5-341">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-342">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-343">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-345">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="bf3f5-346">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-347">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-347">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-348">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-350">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-351">Максимальное число напрямую предоставляемых сущностей, которые поддерживаются этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-351">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="bf3f5-352">Если число неизвестно, следует использовать значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-352">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="bf3f5-353">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-353">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-354">**Name**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-354">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-357">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-357">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-358">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-358">Label by which the object is known.</span></span> <span data-ttu-id="bf3f5-359">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-359">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="bf3f5-360">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-360">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-361">**осаутодисковеред**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-361">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-362">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-364">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-364">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-365">Если **значение равно true**, то параллельный порт был автоматически обнаружен операционной системой.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-365">If **TRUE**, the parallel port was automatically detected by the operating system.</span></span> <span data-ttu-id="bf3f5-366">Если **значение равно false**, порт был обнаружен другими средствами (например, вручную добавленными через панель управления).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-366">If **FALSE**, the port was detected by other means (such as being manually added through the Control Panel).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-367">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-367">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-368">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-370">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-370">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-371">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-371">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="bf3f5-372">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="bf3f5-373">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="bf3f5-373">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-374">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-374">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-375">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="bf3f5-375">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-377">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-377">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="bf3f5-378">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-378">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bf3f5-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="bf3f5-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bf3f5-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bf3f5-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-383">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-383">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="bf3f5-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-385">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-385">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="bf3f5-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-387">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="bf3f5-387">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="bf3f5-388">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-388">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="bf3f5-389">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-389">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="bf3f5-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-391">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-391">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="bf3f5-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bf3f5-393">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="bf3f5-393">Timed Power-On Supported</span></span>

<span data-ttu-id="bf3f5-394">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-394">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf3f5-395">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-396">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-398">Если **значение — true**, устройство может управляться с помощью управления питанием. Это означает, что его можно перевести в режим приостановки и т. д.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-398">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="bf3f5-399">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-399">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="bf3f5-400">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-401">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-401">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-402">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-404">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-405">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-405">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="bf3f5-406">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-406">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="bf3f5-407">Значения показаны в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-407">Values are shown in the following list.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bf3f5-408">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-408">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bf3f5-409">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-409">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="bf3f5-410">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-410">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="bf3f5-411">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-411">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="bf3f5-412">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-412">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="bf3f5-413">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-413">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="bf3f5-414">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-414">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="bf3f5-415">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-415">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="bf3f5-416">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-416">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="bf3f5-417">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-417">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="bf3f5-418">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-418">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="bf3f5-419">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-419">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="bf3f5-420">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-420">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="bf3f5-421">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-421">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="bf3f5-422">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-422">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="bf3f5-423">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-423">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="bf3f5-424">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-424">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="bf3f5-425">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-425">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="bf3f5-426">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-426">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="bf3f5-427">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-427">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="bf3f5-428">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-428">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="bf3f5-429">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-429">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="bf3f5-430">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-430">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="bf3f5-431">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-431">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="bf3f5-432">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-432">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="bf3f5-433">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-433">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="bf3f5-434">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-434">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="bf3f5-435">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-435">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="bf3f5-436">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-436">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="bf3f5-437">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-437">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="bf3f5-438">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-438">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="bf3f5-439">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-439">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="bf3f5-440">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-440">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="bf3f5-441">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-441">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="bf3f5-442">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-442">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="bf3f5-443">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-443">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="bf3f5-444">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-444">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="bf3f5-445">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-445">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="bf3f5-446">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-446">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="bf3f5-447">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-447">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="bf3f5-448">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-448">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="bf3f5-449">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-449">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="bf3f5-450">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-450">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="bf3f5-451">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-451">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="bf3f5-452">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-452">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="bf3f5-453">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-453">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="bf3f5-454">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-454">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf3f5-455">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-456">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-457">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-458">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-458">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-459">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-459">Current status of the object.</span></span> <span data-ttu-id="bf3f5-460">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="bf3f5-461">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="bf3f5-462">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="bf3f5-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bf3f5-463">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-463">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bf3f5-464">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-464">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bf3f5-465">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bf3f5-466">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="bf3f5-466">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bf3f5-467">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bf3f5-468">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bf3f5-469">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bf3f5-470">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bf3f5-471">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bf3f5-472">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bf3f5-473">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bf3f5-474">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bf3f5-475">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bf3f5-476">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bf3f5-477">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bf3f5-478">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf3f5-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-480">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-482">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="bf3f5-482">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-483">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-483">State of the logical device.</span></span> <span data-ttu-id="bf3f5-484">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="bf3f5-485">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bf3f5-486">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bf3f5-487">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bf3f5-488">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bf3f5-489">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bf3f5-490">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf3f5-491">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-492">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-493">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-494">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-494">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-495">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-495">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="bf3f5-496">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-496">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-497">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-497">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-498">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-499">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-500">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bf3f5-500">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-501">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-501">Name of the scoping system.</span></span>

<span data-ttu-id="bf3f5-502">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf3f5-503">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-503">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3f5-504">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-504">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bf3f5-505">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf3f5-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf3f5-506">Дата и время последнего сброса контроллера.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-506">Date and time the controller was last reset.</span></span> <span data-ttu-id="bf3f5-507">Это может означать, что контроллер был отключен или инициализирован повторно.</span><span class="sxs-lookup"><span data-stu-id="bf3f5-507">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="bf3f5-508">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-508">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf3f5-509">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf3f5-509">Remarks</span></span>

<span data-ttu-id="bf3f5-510">Класс **Win32 \_ параллелпорт** является производным от [**CIM \_ параллелконтроллер**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="bf3f5-510">The **Win32\_ParallelPort** class is derived from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf3f5-511">Требования</span><span class="sxs-lookup"><span data-stu-id="bf3f5-511">Requirements</span></span>



| <span data-ttu-id="bf3f5-512">Требование</span><span class="sxs-lookup"><span data-stu-id="bf3f5-512">Requirement</span></span> | <span data-ttu-id="bf3f5-513">Значение</span><span class="sxs-lookup"><span data-stu-id="bf3f5-513">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf3f5-514">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf3f5-514">Minimum supported client</span></span><br/> | <span data-ttu-id="bf3f5-515">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf3f5-515">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf3f5-516">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf3f5-516">Minimum supported server</span></span><br/> | <span data-ttu-id="bf3f5-517">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf3f5-517">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf3f5-518">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bf3f5-518">Namespace</span></span><br/>                | <span data-ttu-id="bf3f5-519">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bf3f5-519">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bf3f5-520">MOF</span><span class="sxs-lookup"><span data-stu-id="bf3f5-520">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf3f5-521"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf3f5-521"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf3f5-522">DLL</span><span class="sxs-lookup"><span data-stu-id="bf3f5-522">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf3f5-523"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf3f5-523"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf3f5-524">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf3f5-524">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf3f5-525">**\_ПАРАЛЛЕЛКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="bf3f5-525">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dt>

[<span data-ttu-id="bf3f5-526">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="bf3f5-526">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
