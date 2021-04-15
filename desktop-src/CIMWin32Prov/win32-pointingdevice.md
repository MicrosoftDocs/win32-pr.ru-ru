---
description: '\_Класс WMI поинтингдевице инструментария Win32 представляет устройство ввода, используемое для указания и выбора регионов на дисплее компьютерной системы под Windows.'
ms.assetid: ed81abe3-3d8f-48aa-ab64-9e6c87e44f64
ms.tgt_platform: multiple
title: Класс Win32_PointingDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PointingDevice
- Win32_PointingDevice.Reset
- Win32_PointingDevice.SetPowerState
- Win32_PointingDevice.Availability
- Win32_PointingDevice.Caption
- Win32_PointingDevice.ConfigManagerErrorCode
- Win32_PointingDevice.ConfigManagerUserConfig
- Win32_PointingDevice.CreationClassName
- Win32_PointingDevice.Description
- Win32_PointingDevice.DeviceID
- Win32_PointingDevice.DeviceInterface
- Win32_PointingDevice.DoubleSpeedThreshold
- Win32_PointingDevice.ErrorCleared
- Win32_PointingDevice.ErrorDescription
- Win32_PointingDevice.Handedness
- Win32_PointingDevice.HardwareType
- Win32_PointingDevice.InfFileName
- Win32_PointingDevice.InfSection
- Win32_PointingDevice.InstallDate
- Win32_PointingDevice.IsLocked
- Win32_PointingDevice.LastErrorCode
- Win32_PointingDevice.Manufacturer
- Win32_PointingDevice.Name
- Win32_PointingDevice.NumberOfButtons
- Win32_PointingDevice.PNPDeviceID
- Win32_PointingDevice.PointingType
- Win32_PointingDevice.PowerManagementCapabilities
- Win32_PointingDevice.PowerManagementSupported
- Win32_PointingDevice.QuadSpeedThreshold
- Win32_PointingDevice.Resolution
- Win32_PointingDevice.SampleRate
- Win32_PointingDevice.Status
- Win32_PointingDevice.StatusInfo
- Win32_PointingDevice.Synch
- Win32_PointingDevice.SystemCreationClassName
- Win32_PointingDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e4f2359e19476dfae111fc361f48e6f73d8cfac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655701"
---
# <a name="win32_pointingdevice-class"></a><span data-ttu-id="7f647-103">\_Класс Win32 поинтингдевице</span><span class="sxs-lookup"><span data-stu-id="7f647-103">Win32\_PointingDevice class</span></span>

<span data-ttu-id="7f647-104">Класс **WMI \_ поинтингдевице** [инструментария](../wmisdk/retrieving-a-class.md) Win32 представляет устройство ввода, используемое для указания и выбора регионов на дисплее компьютерной системы под Windows.</span><span class="sxs-lookup"><span data-stu-id="7f647-104">The **Win32\_PointingDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents an input device used to point to and select regions on the display of a computer system running Windows.</span></span> <span data-ttu-id="7f647-105">Все устройства, используемые для работы с указателем, или указывают на отображение на компьютере, работающем под Windows, являются членами этого класса.</span><span class="sxs-lookup"><span data-stu-id="7f647-105">Any device used to manipulate a pointer, or point to the display on a computer system running Windows is a member of this class.</span></span>

<span data-ttu-id="7f647-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7f647-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7f647-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7f647-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f647-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f647-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PointingDevice : CIM_PointingDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DeviceInterface;
  uint32   DoubleSpeedThreshold;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Handedness;
  string   HardwareType;
  string   InfFileName;
  string   InfSection;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  uint8    NumberOfButtons;
  string   PNPDeviceID;
  uint16   PointingType;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   QuadSpeedThreshold;
  uint32   Resolution;
  uint32   SampleRate;
  string   Status;
  uint16   StatusInfo;
  uint32   Synch;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="7f647-109">Члены</span><span class="sxs-lookup"><span data-stu-id="7f647-109">Members</span></span>

<span data-ttu-id="7f647-110">Класс **Win32 \_ поинтингдевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7f647-110">The **Win32\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="7f647-111">Методы</span><span class="sxs-lookup"><span data-stu-id="7f647-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f647-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7f647-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f647-113">Методы</span><span class="sxs-lookup"><span data-stu-id="7f647-113">Methods</span></span>

<span data-ttu-id="7f647-114">Класс **Win32 \_ поинтингдевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7f647-114">The **Win32\_PointingDevice** class has these methods.</span></span>



| <span data-ttu-id="7f647-115">Метод</span><span class="sxs-lookup"><span data-stu-id="7f647-115">Method</span></span>            | <span data-ttu-id="7f647-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7f647-116">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f647-117">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="7f647-117">**Reset**</span></span>         | <span data-ttu-id="7f647-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="7f647-118">Not implemented.</span></span> <span data-ttu-id="7f647-119">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ поинтингдевице**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/>                 |
| <span data-ttu-id="7f647-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7f647-120">**SetPowerState**</span></span> | <span data-ttu-id="7f647-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="7f647-121">Not implemented.</span></span> <span data-ttu-id="7f647-122">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ поинтингдевице**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7f647-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="7f647-123">Properties</span></span>

<span data-ttu-id="7f647-124">Класс **Win32 \_ поинтингдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7f647-124">The **Win32\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f647-125">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="7f647-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f647-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-128">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="7f647-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-129">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="7f647-129">Availability and status of the device.</span></span>

<span data-ttu-id="7f647-130">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f647-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7f647-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f647-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7f647-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7f647-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="7f647-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-134">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="7f647-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7f647-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="7f647-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7f647-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="7f647-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7f647-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="7f647-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7f647-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="7f647-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7f647-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="7f647-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7f647-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="7f647-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7f647-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="7f647-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7f647-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="7f647-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7f647-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="7f647-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7f647-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="7f647-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="7f647-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7f647-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="7f647-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="7f647-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7f647-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="7f647-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="7f647-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7f647-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="7f647-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7f647-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="7f647-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="7f647-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7f647-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="7f647-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="7f647-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7f647-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="7f647-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="7f647-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7f647-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="7f647-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="7f647-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7f647-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="7f647-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="7f647-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f647-161">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7f647-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-164">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7f647-164">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-165">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7f647-165">Short description of the object.</span></span>

<span data-ttu-id="7f647-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-167">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="7f647-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f647-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-170">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7f647-170">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-171">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7f647-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7f647-172">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7f647-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="7f647-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7f647-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="7f647-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-175">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="7f647-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7f647-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="7f647-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7f647-177">(1)</span><span class="sxs-lookup"><span data-stu-id="7f647-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-178">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="7f647-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7f647-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7f647-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7f647-180">(2)</span><span class="sxs-lookup"><span data-stu-id="7f647-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7f647-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="7f647-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7f647-182">(3)</span><span class="sxs-lookup"><span data-stu-id="7f647-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-183">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7f647-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7f647-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="7f647-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7f647-185">(4)</span><span class="sxs-lookup"><span data-stu-id="7f647-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-186">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="7f647-186">Device is not working properly.</span></span> <span data-ttu-id="7f647-187">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="7f647-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7f647-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="7f647-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7f647-189">(5)</span><span class="sxs-lookup"><span data-stu-id="7f647-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-190">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="7f647-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7f647-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="7f647-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7f647-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="7f647-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-193">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="7f647-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7f647-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="7f647-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7f647-195">(7)</span><span class="sxs-lookup"><span data-stu-id="7f647-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7f647-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="7f647-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7f647-197">(8)</span><span class="sxs-lookup"><span data-stu-id="7f647-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-198">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="7f647-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7f647-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="7f647-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7f647-200">(9)</span><span class="sxs-lookup"><span data-stu-id="7f647-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-201">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="7f647-201">Device is not working properly.</span></span> <span data-ttu-id="7f647-202">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="7f647-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7f647-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="7f647-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7f647-204">(10)</span><span class="sxs-lookup"><span data-stu-id="7f647-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-205">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="7f647-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7f647-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="7f647-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7f647-207">(11)</span><span class="sxs-lookup"><span data-stu-id="7f647-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-208">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="7f647-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7f647-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="7f647-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7f647-210">(12)</span><span class="sxs-lookup"><span data-stu-id="7f647-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-211">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="7f647-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7f647-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7f647-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7f647-213">(13)</span><span class="sxs-lookup"><span data-stu-id="7f647-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-214">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="7f647-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7f647-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="7f647-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7f647-216">(14)</span><span class="sxs-lookup"><span data-stu-id="7f647-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-217">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="7f647-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7f647-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="7f647-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7f647-219">(15)</span><span class="sxs-lookup"><span data-stu-id="7f647-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-220">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="7f647-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7f647-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="7f647-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7f647-222">(16)</span><span class="sxs-lookup"><span data-stu-id="7f647-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-223">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="7f647-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7f647-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="7f647-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7f647-225">(17)</span><span class="sxs-lookup"><span data-stu-id="7f647-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-226">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="7f647-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7f647-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7f647-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7f647-228">(18)</span><span class="sxs-lookup"><span data-stu-id="7f647-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-229">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="7f647-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7f647-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="7f647-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7f647-231">(19)</span><span class="sxs-lookup"><span data-stu-id="7f647-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7f647-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="7f647-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7f647-233">(20)</span><span class="sxs-lookup"><span data-stu-id="7f647-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-234">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="7f647-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7f647-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="7f647-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7f647-236">(21)</span><span class="sxs-lookup"><span data-stu-id="7f647-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-237">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="7f647-237">System failure.</span></span> <span data-ttu-id="7f647-238">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="7f647-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7f647-239">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="7f647-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7f647-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="7f647-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7f647-241">(22)</span><span class="sxs-lookup"><span data-stu-id="7f647-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-242">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="7f647-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7f647-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="7f647-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7f647-244">(23)</span><span class="sxs-lookup"><span data-stu-id="7f647-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-245">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="7f647-245">System failure.</span></span> <span data-ttu-id="7f647-246">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="7f647-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7f647-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="7f647-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7f647-248">(24)</span><span class="sxs-lookup"><span data-stu-id="7f647-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-249">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="7f647-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7f647-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="7f647-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7f647-251">(25)</span><span class="sxs-lookup"><span data-stu-id="7f647-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-252">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="7f647-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7f647-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="7f647-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7f647-254">(26)</span><span class="sxs-lookup"><span data-stu-id="7f647-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-255">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="7f647-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7f647-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="7f647-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7f647-257">(27)</span><span class="sxs-lookup"><span data-stu-id="7f647-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-258">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="7f647-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7f647-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="7f647-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7f647-260">(28)</span><span class="sxs-lookup"><span data-stu-id="7f647-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-261">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="7f647-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7f647-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="7f647-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7f647-263">(29)</span><span class="sxs-lookup"><span data-stu-id="7f647-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-264">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="7f647-264">Device is disabled.</span></span> <span data-ttu-id="7f647-265">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="7f647-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7f647-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="7f647-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7f647-267">(30)</span><span class="sxs-lookup"><span data-stu-id="7f647-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-268">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="7f647-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7f647-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7f647-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7f647-270">1-31</span><span class="sxs-lookup"><span data-stu-id="7f647-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-271">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="7f647-271">Device is not working properly.</span></span> <span data-ttu-id="7f647-272">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="7f647-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f647-273">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="7f647-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-274">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7f647-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-276">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7f647-276">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-277">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="7f647-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7f647-278">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-279">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7f647-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-282">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7f647-282">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7f647-283">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7f647-283">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="7f647-284">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="7f647-284">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7f647-285">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-286">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7f647-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-287">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-289">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="7f647-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-290">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7f647-290">Description of the object.</span></span>

<span data-ttu-id="7f647-291">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-292">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7f647-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-295">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="7f647-295">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-296">Уникальный идентификатор указывающего устройства с другими устройствами в системе.</span><span class="sxs-lookup"><span data-stu-id="7f647-296">Unique identifier of the pointing device with other devices on the system.</span></span>

<span data-ttu-id="7f647-297">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-298">**девицеинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="7f647-298">**DeviceInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-299">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f647-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-301">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 21 \| interface")</span><span class="sxs-lookup"><span data-stu-id="7f647-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 21\|Interface")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-302">Тип интерфейса, используемого для указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="7f647-302">Type of interface used for the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f647-303">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7f647-303">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f647-304">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7f647-304">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial"></span><span id="serial"></span><span id="SERIAL"></span>

<span data-ttu-id="7f647-305">**Последовательный** (3)</span><span class="sxs-lookup"><span data-stu-id="7f647-305">**Serial** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="7f647-306">**PS/2** (4)</span><span class="sxs-lookup"><span data-stu-id="7f647-306">**PS/2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="7f647-307">**Инфракрасная связь** (5)</span><span class="sxs-lookup"><span data-stu-id="7f647-307">**Infrared** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="7f647-308">**HP-Хил** (6)</span><span class="sxs-lookup"><span data-stu-id="7f647-308">**HP-HIL** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="7f647-309">**Мышь шины** (7)</span><span class="sxs-lookup"><span data-stu-id="7f647-309">**Bus mouse** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB__Apple_Desktop_Bus_"></span><span id="adb__apple_desktop_bus_"></span><span id="ADB__APPLE_DESKTOP_BUS_"></span>

<span data-ttu-id="7f647-310">**ADB (шина Apple для настольных систем)** (8)</span><span class="sxs-lookup"><span data-stu-id="7f647-310">**ADB (Apple Desktop Bus)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_DB-9"></span><span id="bus_mouse_db-9"></span><span id="BUS_MOUSE_DB-9"></span>

<span data-ttu-id="7f647-311">**Мышь шины DB-9** (160)</span><span class="sxs-lookup"><span data-stu-id="7f647-311">**Bus mouse DB-9** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_micro-DIN"></span><span id="bus_mouse_micro-din"></span><span id="BUS_MOUSE_MICRO-DIN"></span>

<span data-ttu-id="7f647-312">**Мышь Bus Micro-DIN** (161)</span><span class="sxs-lookup"><span data-stu-id="7f647-312">**Bus mouse micro-DIN** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="7f647-313">**USB** (162)</span><span class="sxs-lookup"><span data-stu-id="7f647-313">**USB** (162)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7f647-314">**даублеспидсрешолд**</span><span class="sxs-lookup"><span data-stu-id="7f647-314">**DoubleSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-315">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f647-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-317">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information functions \| Системпараметерсинфо"), [**Units**](../wmisdk/standard-qualifiers.md) ("миккэйс")</span><span class="sxs-lookup"><span data-stu-id="7f647-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-318">Одно из двух значений ускорения.</span><span class="sxs-lookup"><span data-stu-id="7f647-318">One of two acceleration values.</span></span> <span data-ttu-id="7f647-319">Чувствительность указывающего устройства удваивается (переключается с первого на второе значение), когда указывающее устройство перемещает расстояние, превышающее это пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="7f647-319">The sensitivity of the pointing device doubles (toggles from the first to the second value) when the pointing device moves a distance greater than this threshold value.</span></span>

</dd> <dt>

<span data-ttu-id="7f647-320">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="7f647-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-321">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7f647-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f647-323">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="7f647-323">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="7f647-324">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7f647-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f647-328">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="7f647-328">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="7f647-329">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-330">**Правой или левой**</span><span class="sxs-lookup"><span data-stu-id="7f647-330">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-331">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f647-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f647-333">Конфигурация указывающего устройства для левой или правой операции.</span><span class="sxs-lookup"><span data-stu-id="7f647-333">Configuration of the pointing device for left-hand or right-hand operation.</span></span>

<span data-ttu-id="7f647-334">Это свойство наследуется от [**CIM \_ поинтингдевице**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-334">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f647-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7f647-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7f647-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (1)</span><span class="sxs-lookup"><span data-stu-id="7f647-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="7f647-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Правая операция** (2)</span><span class="sxs-lookup"><span data-stu-id="7f647-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Right Handed Operation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-338">Right-Handed операция</span><span class="sxs-lookup"><span data-stu-id="7f647-338">Right-Handed Operation</span></span>

</dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="7f647-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Левая операция** (3)</span><span class="sxs-lookup"><span data-stu-id="7f647-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Left Handed Operation** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-340">Left-Handed операция</span><span class="sxs-lookup"><span data-stu-id="7f647-340">Left-Handed Operation</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f647-341">**хардваретипе**</span><span class="sxs-lookup"><span data-stu-id="7f647-341">**HardwareType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-342">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-344">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hKey \_ локальный \_ компьютер \\ \\ System \\ \\ ControlSet001 \\ \\ \\ \\ класс управления \| дривердеск")</span><span class="sxs-lookup"><span data-stu-id="7f647-344">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\ControlSet001\\\\Control\\\\Class\|DriverDesc")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-345">Тип оборудования, используемого для указывающего устройства Windows.</span><span class="sxs-lookup"><span data-stu-id="7f647-345">Type of hardware used for the Windows pointing device.</span></span>

<span data-ttu-id="7f647-346">Пример: "мышь MICROSOFT PS2"</span><span class="sxs-lookup"><span data-stu-id="7f647-346">Example: "MICROSOFT PS2 MOUSE"</span></span>

</dd> <dt>

<span data-ttu-id="7f647-347">**инффиленаме**</span><span class="sxs-lookup"><span data-stu-id="7f647-347">**InfFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-348">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-350">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hKey \_ локальный \_ компьютер \\ \\ System \\ \\ CurrentControlSet \\ \\ \\ \\ класс управления \| инфпас")</span><span class="sxs-lookup"><span data-stu-id="7f647-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-351">Имя INF-файла для указывающего устройства Windows.</span><span class="sxs-lookup"><span data-stu-id="7f647-351">Name of the .inf file for the Windows pointing device.</span></span>

<span data-ttu-id="7f647-352">Пример: "AB. INF"</span><span class="sxs-lookup"><span data-stu-id="7f647-352">Example: "ab.inf"</span></span>

</dd> <dt>

<span data-ttu-id="7f647-353">**инфсектион**</span><span class="sxs-lookup"><span data-stu-id="7f647-353">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-354">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-356">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hKey \_ локальный \_ компьютер \\ \\ System \\ \\ CurrentControlSet \\ \\ \\ \\ класс управления \| инфсектион")</span><span class="sxs-lookup"><span data-stu-id="7f647-356">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-357">Файл INF, содержащий сведения о конфигурации для указывающего устройства Windows.</span><span class="sxs-lookup"><span data-stu-id="7f647-357">Section of the .inf file that holds configuration information for the Windows pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="7f647-358">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7f647-358">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-359">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7f647-359">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-360">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-361">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="7f647-361">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-362">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="7f647-362">Date and time the object was installed.</span></span> <span data-ttu-id="7f647-363">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="7f647-363">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7f647-364">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-365">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="7f647-365">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-366">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7f647-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f647-368">**Значение true** показывает, что устройство заблокировано, что предотвращает ввод или вывод пользователя.</span><span class="sxs-lookup"><span data-stu-id="7f647-368">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="7f647-369">Это свойство наследуется от [**CIM \_ усердевице**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-369">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-370">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="7f647-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-371">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f647-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f647-373">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="7f647-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7f647-374">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-375">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="7f647-375">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-376">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-378">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="7f647-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-379">Имя изготовителя процессора.</span><span class="sxs-lookup"><span data-stu-id="7f647-379">Name of the processor's manufacturer.</span></span>

<span data-ttu-id="7f647-380">Пример: "Женуинесиликон"</span><span class="sxs-lookup"><span data-stu-id="7f647-380">Example: "GenuineSilicon"</span></span>

</dd> <dt>

<span data-ttu-id="7f647-381">**Name**</span><span class="sxs-lookup"><span data-stu-id="7f647-381">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-382">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-384">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="7f647-384">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-385">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="7f647-385">Label by which the object is known.</span></span> <span data-ttu-id="7f647-386">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="7f647-386">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="7f647-387">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-388">**нумберофбуттонс**</span><span class="sxs-lookup"><span data-stu-id="7f647-388">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-389">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7f647-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f647-391">Число кнопок на указывающем устройстве.</span><span class="sxs-lookup"><span data-stu-id="7f647-391">Number of buttons on the pointing device.</span></span>

<span data-ttu-id="7f647-392">Это свойство наследуется от [**CIM \_ поинтингдевице**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-392">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="7f647-393">Пример: 2</span><span class="sxs-lookup"><span data-stu-id="7f647-393">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="7f647-394">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7f647-394">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-395">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-395">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-397">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7f647-397">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-398">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7f647-398">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="7f647-399">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7f647-400">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7f647-400">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7f647-401">**поинтингтипе**</span><span class="sxs-lookup"><span data-stu-id="7f647-401">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-402">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f647-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-404">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Указывающее устройство в DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="7f647-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Pointing Device\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-405">Тип указывающего устройства.</span><span class="sxs-lookup"><span data-stu-id="7f647-405">Type of pointing device.</span></span>

<span data-ttu-id="7f647-406">Это свойство наследуется от [**CIM \_ поинтингдевице**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-406">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f647-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7f647-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f647-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7f647-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="7f647-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Мышь** (3)</span><span class="sxs-lookup"><span data-stu-id="7f647-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="7f647-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Отслеживание шарика** (4)</span><span class="sxs-lookup"><span data-stu-id="7f647-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-411">Трекбол</span><span class="sxs-lookup"><span data-stu-id="7f647-411">Trackball</span></span>

</dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="7f647-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Точка трассировки** (5)</span><span class="sxs-lookup"><span data-stu-id="7f647-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="7f647-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Точка глиде** (6)</span><span class="sxs-lookup"><span data-stu-id="7f647-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="7f647-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Сенсорная панель** (7)</span><span class="sxs-lookup"><span data-stu-id="7f647-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="7f647-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Сенсорный экран** (8)</span><span class="sxs-lookup"><span data-stu-id="7f647-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="7f647-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Оптический датчик мыши** (9)</span><span class="sxs-lookup"><span data-stu-id="7f647-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7f647-417">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="7f647-417">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-418">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7f647-418">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7f647-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f647-420">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="7f647-420">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7f647-421">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-421">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f647-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7f647-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7f647-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="7f647-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7f647-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="7f647-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7f647-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="7f647-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-426">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="7f647-426">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7f647-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="7f647-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-428">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="7f647-428">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7f647-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="7f647-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-430">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="7f647-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7f647-431">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="7f647-431">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7f647-432">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-432">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7f647-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="7f647-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-434">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="7f647-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7f647-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="7f647-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7f647-436">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="7f647-436">Timed Power-On Supported</span></span>

<span data-ttu-id="7f647-437">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="7f647-437">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7f647-438">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="7f647-438">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-439">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7f647-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f647-441">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="7f647-441">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="7f647-442">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="7f647-442">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="7f647-443">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-444">**куадспидсрешолд**</span><span class="sxs-lookup"><span data-stu-id="7f647-444">**QuadSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-445">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f647-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-447">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information functions \| Системпараметерсинфо"), [**Units**](../wmisdk/standard-qualifiers.md) ("миккэйс")</span><span class="sxs-lookup"><span data-stu-id="7f647-447">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-448">Одно из двух пороговых значений ускорения.</span><span class="sxs-lookup"><span data-stu-id="7f647-448">One of two acceleration threshold values.</span></span> <span data-ttu-id="7f647-449">Система удваивает скорость перемещения указателя, когда указатель мыши перемещает расстояние больше этого значения.</span><span class="sxs-lookup"><span data-stu-id="7f647-449">The system doubles the speed of the pointer movement when the pointer device moves a distance greater than this value.</span></span> <span data-ttu-id="7f647-450">Так как это увеличение скорости происходит после того, как значение **даублеспидсрешолд** выполнено, указатель эффективно перемещается в четыре раза больше его исходной скорости.</span><span class="sxs-lookup"><span data-stu-id="7f647-450">Because this speed increase occurs after the **DoubleSpeedThreshold** value has been met, the pointer effectively moves at four times its original speed.</span></span>

</dd> <dt>

<span data-ttu-id="7f647-451">**Решение**</span><span class="sxs-lookup"><span data-stu-id="7f647-451">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-452">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f647-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-454">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("число счетчиков на дюйм")</span><span class="sxs-lookup"><span data-stu-id="7f647-454">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("counts per inch")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-455">Разрешение отслеживания.</span><span class="sxs-lookup"><span data-stu-id="7f647-455">Tracking resolution.</span></span>

<span data-ttu-id="7f647-456">Это свойство наследуется от [**CIM \_ поинтингдевице**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-456">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="7f647-457">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="7f647-457">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="7f647-458">**SampleRate**</span><span class="sxs-lookup"><span data-stu-id="7f647-458">**SampleRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-459">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f647-459">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-461">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SampleRate"), [**Units**](../wmisdk/standard-qualifiers.md) ("Герц")</span><span class="sxs-lookup"><span data-stu-id="7f647-461">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SampleRate"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-462">Скорость опроса указывающего устройства на наличие входных данных.</span><span class="sxs-lookup"><span data-stu-id="7f647-462">Rate at which the pointing device is polled for input information.</span></span>

</dd> <dt>

<span data-ttu-id="7f647-463">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="7f647-463">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-464">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-465">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-466">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="7f647-466">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-467">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="7f647-467">Current status of the object.</span></span> <span data-ttu-id="7f647-468">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="7f647-468">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7f647-469">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="7f647-469">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7f647-470">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="7f647-470">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7f647-471">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="7f647-471">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7f647-472">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="7f647-472">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7f647-473">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-473">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7f647-474">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="7f647-474">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7f647-475">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="7f647-475">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7f647-476">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="7f647-476">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7f647-477">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="7f647-477">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f647-478">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="7f647-478">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7f647-479">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="7f647-479">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7f647-480">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="7f647-480">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7f647-481">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="7f647-481">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7f647-482">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="7f647-482">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7f647-483">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="7f647-483">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7f647-484">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="7f647-484">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7f647-485">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="7f647-485">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7f647-486">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="7f647-486">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7f647-487">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7f647-487">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-488">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f647-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-489">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-490">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7f647-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-491">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7f647-491">State of the logical device.</span></span> <span data-ttu-id="7f647-492">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="7f647-492">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7f647-493">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-493">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f647-494">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7f647-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f647-495">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7f647-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7f647-496">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="7f647-496">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7f647-497">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="7f647-497">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7f647-498">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="7f647-498">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7f647-499">**Синхронизация**</span><span class="sxs-lookup"><span data-stu-id="7f647-499">**Synch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-500">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f647-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-501">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-502">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| MouseSynchIn100ns"), [**units**](../wmisdk/standard-qualifiers.md) ("100 наносекунд")</span><span class="sxs-lookup"><span data-stu-id="7f647-502">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|MouseSynchIn100ns"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="7f647-503">Период времени, после которого предполагается следующее прерывание, указывающее на начало нового пакета устройства (частичные пакеты отбрасываются).</span><span class="sxs-lookup"><span data-stu-id="7f647-503">Length of time after which the next interrupt is assumed to indicate the start of a new device packet (partial packets are discarded).</span></span> <span data-ttu-id="7f647-504">В случае потери прерывания это позволяет драйверу указывающего устройства синхронизировать внутреннее представление состояния пакета с состоянием оборудования.</span><span class="sxs-lookup"><span data-stu-id="7f647-504">In the event that an interrupt is lost, this allows the pointing device driver to synchronize its internal representation of the packet state with the hardware state.</span></span>

</dd> <dt>

<span data-ttu-id="7f647-505">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="7f647-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-506">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-507">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-508">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7f647-508">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7f647-509">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="7f647-509">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="7f647-510">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f647-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7f647-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f647-512">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f647-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f647-513">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f647-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f647-514">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7f647-514">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7f647-515">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="7f647-515">Name of the scoping system.</span></span>

<span data-ttu-id="7f647-516">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7f647-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f647-517">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f647-517">Remarks</span></span>

<span data-ttu-id="7f647-518">Класс **Win32 \_ поинтингдевице** является производным от [**CIM \_ поинтингдевице**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="7f647-518">The **Win32\_PointingDevice** class is derived from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f647-519">Требования</span><span class="sxs-lookup"><span data-stu-id="7f647-519">Requirements</span></span>



| <span data-ttu-id="7f647-520">Требование</span><span class="sxs-lookup"><span data-stu-id="7f647-520">Requirement</span></span> | <span data-ttu-id="7f647-521">Значение</span><span class="sxs-lookup"><span data-stu-id="7f647-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f647-522">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f647-522">Minimum supported client</span></span><br/> | <span data-ttu-id="7f647-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f647-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f647-524">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f647-524">Minimum supported server</span></span><br/> | <span data-ttu-id="7f647-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f647-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f647-526">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7f647-526">Namespace</span></span><br/>                | <span data-ttu-id="7f647-527">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7f647-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7f647-528">MOF</span><span class="sxs-lookup"><span data-stu-id="7f647-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f647-529"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f647-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f647-530">DLL</span><span class="sxs-lookup"><span data-stu-id="7f647-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f647-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f647-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f647-532">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f647-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f647-533">**\_ПОИНТИНГДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="7f647-533">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="7f647-534">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="7f647-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
