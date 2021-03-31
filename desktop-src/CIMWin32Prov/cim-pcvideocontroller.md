---
description: CIM \_ пквидеоконтроллер представляет возможности и управление видеоконтроллером персональных компьютеров, подтипом видеоконтроллера.
ms.assetid: bf937727-a332-445b-9397-7d87d58c4a5b
ms.tgt_platform: multiple
title: Класс CIM_PCVideoController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCVideoController
- CIM_PCVideoController.AcceleratorCapabilities
- CIM_PCVideoController.Availability
- CIM_PCVideoController.CapabilityDescriptions
- CIM_PCVideoController.Caption
- CIM_PCVideoController.ConfigManagerErrorCode
- CIM_PCVideoController.ConfigManagerUserConfig
- CIM_PCVideoController.CreationClassName
- CIM_PCVideoController.CurrentBitsPerPixel
- CIM_PCVideoController.CurrentHorizontalResolution
- CIM_PCVideoController.CurrentNumberOfColors
- CIM_PCVideoController.CurrentNumberOfColumns
- CIM_PCVideoController.CurrentNumberOfRows
- CIM_PCVideoController.CurrentRefreshRate
- CIM_PCVideoController.CurrentScanMode
- CIM_PCVideoController.CurrentVerticalResolution
- CIM_PCVideoController.Description
- CIM_PCVideoController.DeviceID
- CIM_PCVideoController.ErrorCleared
- CIM_PCVideoController.ErrorDescription
- CIM_PCVideoController.InstallDate
- CIM_PCVideoController.LastErrorCode
- CIM_PCVideoController.MaxMemorySupported
- CIM_PCVideoController.MaxNumberControlled
- CIM_PCVideoController.MaxRefreshRate
- CIM_PCVideoController.MinRefreshRate
- CIM_PCVideoController.Name
- CIM_PCVideoController.NumberOfColorPlanes
- CIM_PCVideoController.NumberOfVideoPages
- CIM_PCVideoController.PNPDeviceID
- CIM_PCVideoController.PowerManagementCapabilities
- CIM_PCVideoController.PowerManagementSupported
- CIM_PCVideoController.ProtocolSupported
- CIM_PCVideoController.Status
- CIM_PCVideoController.StatusInfo
- CIM_PCVideoController.SystemCreationClassName
- CIM_PCVideoController.SystemName
- CIM_PCVideoController.TimeOfLastReset
- CIM_PCVideoController.VideoArchitecture
- CIM_PCVideoController.VideoMemoryType
- CIM_PCVideoController.VideoMode
- CIM_PCVideoController.VideoProcessor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94465862c34cc9c6fb645f63c0add48d0fded56b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423382"
---
# <a name="cim_pcvideocontroller-class"></a><span data-ttu-id="7b6dd-103">\_Класс CIM пквидеоконтроллер</span><span class="sxs-lookup"><span data-stu-id="7b6dd-103">CIM\_PCVideoController class</span></span>

<span data-ttu-id="7b6dd-104">**CIM \_ пквидеоконтроллер** представляет возможности и управление видеоконтроллером персональных компьютеров, подтипом видеоконтроллера.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-104">The **CIM\_PCVideoController** represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b6dd-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7b6dd-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7b6dd-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7b6dd-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b6dd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b6dd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE6-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_PCVideoController : CIM_VideoController
{
  uint16   AcceleratorCapabilities[];
  uint16   Availability;
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint32   CurrentBitsPerPixel;
  uint32   CurrentHorizontalResolution;
  uint64   CurrentNumberOfColors;
  uint32   CurrentNumberOfColumns;
  uint32   CurrentNumberOfRows;
  uint32   CurrentRefreshRate;
  uint16   CurrentScanMode;
  uint32   CurrentVerticalResolution;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxMemorySupported;
  uint32   MaxNumberControlled;
  uint32   MaxRefreshRate;
  uint32   MinRefreshRate;
  string   Name;
  uint16   NumberOfColorPlanes;
  uint32   NumberOfVideoPages;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint16   VideoArchitecture;
  uint16   VideoMemoryType;
  uint16   VideoMode;
  string   VideoProcessor;
};
```

## <a name="members"></a><span data-ttu-id="7b6dd-110">Члены</span><span class="sxs-lookup"><span data-stu-id="7b6dd-110">Members</span></span>

<span data-ttu-id="7b6dd-111">Класс **CIM \_ пквидеоконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7b6dd-111">The **CIM\_PCVideoController** class has these types of members:</span></span>

-   [<span data-ttu-id="7b6dd-112">Методы</span><span class="sxs-lookup"><span data-stu-id="7b6dd-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7b6dd-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b6dd-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7b6dd-114">Методы</span><span class="sxs-lookup"><span data-stu-id="7b6dd-114">Methods</span></span>

<span data-ttu-id="7b6dd-115">Класс **CIM \_ пквидеоконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-115">The **CIM\_PCVideoController** class has these methods.</span></span>



| <span data-ttu-id="7b6dd-116">Метод</span><span class="sxs-lookup"><span data-stu-id="7b6dd-116">Method</span></span>                                                                       | <span data-ttu-id="7b6dd-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7b6dd-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b6dd-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-118">**Reset**</span></span>](reset-method-in-class-cim-pcvideocontroller.md)                 | <span data-ttu-id="7b6dd-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="7b6dd-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="7b6dd-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcvideocontroller.md) | <span data-ttu-id="7b6dd-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="7b6dd-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7b6dd-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b6dd-124">Properties</span></span>

<span data-ttu-id="7b6dd-125">Класс **CIM \_ пквидеоконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-125">The **CIM\_PCVideoController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b6dd-126">**акцелераторкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-126">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-127">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7b6dd-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-129">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-129">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-130">Графические и трехмерные возможности видеоконтроллера.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-130">Graphics and 3-D capabilities of the video controller.</span></span>

<span data-ttu-id="7b6dd-131">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-131">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b6dd-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7b6dd-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="7b6dd-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Графический ускоритель** (2)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-134"><span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="7b6dd-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**трехмерный ускоритель** (3)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-135"><span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>**3D Accelerator** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-136">трехмерный ускоритель</span><span class="sxs-lookup"><span data-stu-id="7b6dd-136">3-D accelerator</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6dd-137">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-138">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-140">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-141">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-141">Availability and status of the device.</span></span>

<span data-ttu-id="7b6dd-142">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7b6dd-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b6dd-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7b6dd-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-146">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="7b6dd-146">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7b6dd-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7b6dd-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7b6dd-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7b6dd-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7b6dd-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7b6dd-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7b6dd-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7b6dd-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7b6dd-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7b6dd-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-157">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7b6dd-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-159">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7b6dd-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-161">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7b6dd-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7b6dd-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-164">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7b6dd-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-166">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7b6dd-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-168">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7b6dd-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-170">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7b6dd-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-172">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6dd-173">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-173">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-174">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-176">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Видеоконтроллер**](cim-videocontroller.md).**Акцелераторкапабилитиес**")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-176">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-177">Строки произвольной формы, содержащие подробные объяснения для функций ускорителя видео, указанных в массиве **акцелераторкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="7b6dd-177">Free-form strings that provide detailed explanations for video accelerator features indicated in the **AcceleratorCapabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="7b6dd-178">Каждая запись массива связана с записью в массиве **акцелераторкапабилитиес** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-178">Each array entry is related to the entry in the **AcceleratorCapabilities** array that is located at the same index.</span></span>

 

<span data-ttu-id="7b6dd-179">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-179">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-180">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-180">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-183">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-183">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-184">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-184">Short textual description of the object.</span></span>

<span data-ttu-id="7b6dd-185">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-185">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-186">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-187">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-189">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-190">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-190">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="7b6dd-191">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7b6dd-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7b6dd-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-194">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7b6dd-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7b6dd-196">(1)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-197">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7b6dd-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7b6dd-199">(2)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7b6dd-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7b6dd-201">(3)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-202">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7b6dd-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7b6dd-204">(4)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-205">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-205">Device is not working properly.</span></span> <span data-ttu-id="7b6dd-206">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7b6dd-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7b6dd-208">(5)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-209">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7b6dd-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7b6dd-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-212">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7b6dd-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7b6dd-214">(7)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7b6dd-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7b6dd-216">(8)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-217">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7b6dd-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7b6dd-219">(9)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-220">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-220">Device is not working properly.</span></span> <span data-ttu-id="7b6dd-221">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7b6dd-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7b6dd-223">(10)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-224">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7b6dd-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7b6dd-226">(11)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-227">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7b6dd-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7b6dd-229">(12)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-230">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7b6dd-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7b6dd-232">(13)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-233">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7b6dd-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7b6dd-235">(14)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-236">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7b6dd-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7b6dd-238">(15)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-239">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7b6dd-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7b6dd-241">(16)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-242">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7b6dd-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7b6dd-244">(17)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-245">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7b6dd-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7b6dd-247">(18)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-248">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7b6dd-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7b6dd-250">(19)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7b6dd-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7b6dd-252">(20)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-253">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7b6dd-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7b6dd-255">(21)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-256">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-256">System failure.</span></span> <span data-ttu-id="7b6dd-257">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7b6dd-258">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7b6dd-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7b6dd-260">(22)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-261">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7b6dd-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7b6dd-263">(23)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-264">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-264">System failure.</span></span> <span data-ttu-id="7b6dd-265">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7b6dd-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7b6dd-267">(24)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-268">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7b6dd-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7b6dd-270">(25)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-271">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7b6dd-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7b6dd-273">(26)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-274">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7b6dd-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7b6dd-276">(27)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-277">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7b6dd-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7b6dd-279">(28)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-280">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7b6dd-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7b6dd-282">(29)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-283">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-283">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7b6dd-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-284"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7b6dd-285">(30)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-285">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-286">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-286">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7b6dd-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-287"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7b6dd-288">1-31</span><span class="sxs-lookup"><span data-stu-id="7b6dd-288">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-289">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-289">Device is not working properly.</span></span> <span data-ttu-id="7b6dd-290">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-290">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6dd-291">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-292">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-294">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-295">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7b6dd-296">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-298">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-300">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-301">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7b6dd-302">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7b6dd-303">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-304">**куррентбитсперпиксел**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-304">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-305">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-305">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-307">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,12 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" BITS ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-308">Число битов, используемых для вывода каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-308">Number of bits used to display each pixel.</span></span>

<span data-ttu-id="7b6dd-309">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-309">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-310">**курренсоризонталресолутион**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-310">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-311">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-313">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-314">Текущее число точек по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-314">Current number of horizontal pixels.</span></span>

<span data-ttu-id="7b6dd-315">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-315">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-316">**куррентнумберофколорс**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-316">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-317">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-319">Число цветов, поддерживаемое в текущих разрешениях.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-319">Number of colors supported at the current resolutions.</span></span>

<span data-ttu-id="7b6dd-320">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-320">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="7b6dd-321">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-321">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-322">**куррентнумберофколумнс**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-322">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-323">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-325">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,14 ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.14")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-326">Если в символьном режиме, число столбцов для видеоконтроллера; в противном случае введите 0.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-326">If in character mode, number of columns for the video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="7b6dd-327">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-327">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-328">**куррентнумберофровс**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-328">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-329">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-331">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-332">Если в символьном режиме, число строк для этого видеоконтроллера; в противном случае введите 0.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-332">If in character mode, number of rows for this video controller; otherwise, enter 0.</span></span>

<span data-ttu-id="7b6dd-333">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-333">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-334">**куррентрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-334">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-335">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-337">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,15 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-338">Текущая частота обновления в герцах.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-338">Current refresh rate in hertz.</span></span>

<span data-ttu-id="7b6dd-339">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-339">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-340">**куррентсканмоде**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-340">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-341">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-343">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,8 ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-344">Текущий режим просмотра.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-344">Current scan mode.</span></span> <span data-ttu-id="7b6dd-345">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-345">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7b6dd-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b6dd-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-347"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

<span data-ttu-id="7b6dd-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>С **чередованием** (3)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-348"><span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>**Interlaced** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

<span data-ttu-id="7b6dd-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Без чередования** (4)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-349"><span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>**Non Interlaced** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-350">Без чередования</span><span class="sxs-lookup"><span data-stu-id="7b6dd-350">Non-interlaced</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6dd-351">**куррентвертикалресолутион**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-351">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-352">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-352">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-354">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,10 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" пикселей ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-355">Текущее число пикселей по вертикали.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-355">Current number of vertical pixels.</span></span>

<span data-ttu-id="7b6dd-356">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-356">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-357">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-357">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-358">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-360">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-360">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-361">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-361">Textual description of the object.</span></span>

<span data-ttu-id="7b6dd-362">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-363">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-363">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-364">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-366">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-366">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-367">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-367">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="7b6dd-368">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-368">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-369">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-369">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-370">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-372">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-372">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="7b6dd-373">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-374">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-374">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-375">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-377">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-377">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="7b6dd-378">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-379">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-379">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-380">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-380">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-382">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-383">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-383">Date and time the object was installed.</span></span> <span data-ttu-id="7b6dd-384">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-384">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7b6dd-385">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-386">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-386">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-387">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-389">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-389">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7b6dd-390">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-391">**максмеморисуппортед**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-391">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-392">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-394">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-394">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-395">Максимальный поддерживаемый объем памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-395">Maximum amount of memory supported, in bytes.</span></span>

<span data-ttu-id="7b6dd-396">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-396">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-397">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-397">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-398">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-400">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-401">Максимальное количество напрямую обрабатываемых сущностей, поддерживаемых контроллером.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-401">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="7b6dd-402">Если число неизвестно или неограниченно, следует использовать значение 0.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-402">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="7b6dd-403">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-403">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-404">**максрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-404">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-405">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-405">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-407">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,5 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-408">Максимальная частота обновления видеоконтроллера в герцах.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-408">Maximum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="7b6dd-409">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-409">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-410">**минрефрешрате**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-410">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-411">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-412">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-413">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,4 "), [**единицы измерения**](/windows/desktop/WmiSdk/standard-qualifiers) (" Герц ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-413">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-414">Минимальная частота обновления видеоконтроллера в герцах.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-414">Minimum refresh rate of the video controller in hertz.</span></span>

<span data-ttu-id="7b6dd-415">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-415">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-416">**Name**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-416">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-417">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-419">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-419">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-420">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-420">Label by which the object is known.</span></span> <span data-ttu-id="7b6dd-421">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-421">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7b6dd-422">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-423">**нумберофколорпланес**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-423">**NumberOfColorPlanes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-424">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-426">Текущее число цветовых плоскостей.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-426">Current number of color planes.</span></span> <span data-ttu-id="7b6dd-427">Если это значение неприменимо для текущей конфигурации видео, введите 0.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-427">If this value is not applicable for the current video configuration, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-428">**нумберофвидеопажес**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-428">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-429">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-431">Количество поддерживаемых видео страниц с учетом текущих разрешений и доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-431">Number of video pages supported given the current resolutions and available memory.</span></span>

<span data-ttu-id="7b6dd-432">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-432">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-433">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-433">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-436">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-436">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-437">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-437">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="7b6dd-438">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7b6dd-439">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7b6dd-439">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-440">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-440">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-441">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7b6dd-441">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-442">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-443">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-443">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7b6dd-444">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-444">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b6dd-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-445"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7b6dd-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-446"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7b6dd-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-447"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7b6dd-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-448"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-449">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-449">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7b6dd-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-450"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-451">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-451">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7b6dd-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-452"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-453">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="7b6dd-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7b6dd-454">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-454">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7b6dd-455">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-455">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7b6dd-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-456"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-457">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-457">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7b6dd-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-458"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7b6dd-459">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-459">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6dd-460">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-460">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-461">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-461">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-462">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-463">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-463">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="7b6dd-464">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="7b6dd-464">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7b6dd-465">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-465">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="7b6dd-466">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="7b6dd-466">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="7b6dd-467">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-468">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-468">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-469">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-471">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-471">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-472">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-472">Protocol used by the controller to access 'controlled' devices.</span></span>

<span data-ttu-id="7b6dd-473">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-473">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="7b6dd-474">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7b6dd-474">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7b6dd-475">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b6dd-476">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="7b6dd-477">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-477">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="7b6dd-478">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-478">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="7b6dd-479">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-479">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="7b6dd-480">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-480">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="7b6dd-481">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-481">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="7b6dd-482">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-482">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="7b6dd-483">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-483">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="7b6dd-484">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-484">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="7b6dd-485">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-485">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="7b6dd-486">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-486">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="7b6dd-487">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-487">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="7b6dd-488">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-488">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="7b6dd-489">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-489">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="7b6dd-490">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-490">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="7b6dd-491">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-491">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="7b6dd-492">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-492">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="7b6dd-493">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-493">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="7b6dd-494">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-494">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="7b6dd-495">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-495">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="7b6dd-496">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-496">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="7b6dd-497">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-497">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="7b6dd-498">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-498">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="7b6dd-499">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-499">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="7b6dd-500">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-500">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="7b6dd-501">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-501">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="7b6dd-502">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-502">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="7b6dd-503">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-503">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="7b6dd-504">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-504">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="7b6dd-505">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-505">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="7b6dd-506">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-506">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="7b6dd-507">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-507">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="7b6dd-508">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-508">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="7b6dd-509">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-509">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="7b6dd-510">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-510">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="7b6dd-511">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-511">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="7b6dd-512">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-512">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="7b6dd-513">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-513">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="7b6dd-514">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-514">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="7b6dd-515">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-515">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="7b6dd-516">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-516">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="7b6dd-517">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-517">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="7b6dd-518">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-518">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="7b6dd-519">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-519">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="7b6dd-520">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-520">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="7b6dd-521">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-521">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6dd-522">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-523">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-524">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-525">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-526">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-526">Current status of the object.</span></span> <span data-ttu-id="7b6dd-527">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-527">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7b6dd-528">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="7b6dd-528">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7b6dd-529">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-529">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7b6dd-530">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-530">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7b6dd-531">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-531">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b6dd-532">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-532">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7b6dd-533">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-533">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7b6dd-534">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-534">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7b6dd-535">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-535">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7b6dd-536">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-536">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7b6dd-537">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-537">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7b6dd-538">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-538">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7b6dd-539">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-539">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7b6dd-540">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-540">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6dd-541">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-541">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-542">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-542">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-543">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-544">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-545">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-545">State of the logical device.</span></span> <span data-ttu-id="7b6dd-546">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-546">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7b6dd-547">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-547">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7b6dd-548">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-548">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b6dd-549">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-549">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7b6dd-550">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-550">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7b6dd-551">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-551">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7b6dd-552">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-552">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6dd-553">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-553">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-554">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-554">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-555">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-555">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-556">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-556">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-557">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-557">Scoping system's creation class name.</span></span>

<span data-ttu-id="7b6dd-558">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-558">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-559">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-559">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-560">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-561">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-562">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-562">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-563">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-563">Scoping system's name.</span></span>

<span data-ttu-id="7b6dd-564">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-564">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-565">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-565">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-566">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-566">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-567">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-567">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-568">Дата и время последнего сброса этого контроллера, означающие, что контроллер был выключен или повторно инициализирован.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-568">Date and time this controller was last reset meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="7b6dd-569">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-569">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-570">**видеоарчитектуре**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-570">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-571">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-572">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-573">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-574">Архитектура видео.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-574">Video architecture.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7b6dd-575">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-575">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b6dd-576">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-576">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="7b6dd-577">**КГА** (3)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-577">**CGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="7b6dd-578">**Ега** (4)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-578">**EGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="7b6dd-579">**VGA** (5)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-579">**VGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="7b6dd-580">**SVGA** (6)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-580">**SVGA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="7b6dd-581">**MDA** (7)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-581">**MDA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="7b6dd-582">**ХГК** (8)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-582">**HGC** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="7b6dd-583">**Мкга** (9)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-583">**MCGA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="7b6dd-584">**8514A** (10)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-584">**8514A** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="7b6dd-585">**Разрешение XGA** (11)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-585">**XGA** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="7b6dd-586">**Буфер линейного фрейма** (12)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-586">**Linear Frame Buffer** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="7b6dd-587">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-587">**PC-98** (160)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6dd-588">**видеомеморитипе**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-588">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-589">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-589">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-590">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-591">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,6 ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-591">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.6")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-592">Тип видеопамяти.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-592">Type of video memory.</span></span>

<span data-ttu-id="7b6dd-593">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-593">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7b6dd-594">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-594">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b6dd-595">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-595">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="7b6dd-596">**Видеопамять** (3)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-596">**VRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="7b6dd-597">**DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-597">**DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="7b6dd-598">**SRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-598">**SRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="7b6dd-599">**Врам** (6)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-599">**WRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="7b6dd-600">**ОЗУ Эдо** (7)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-600">**EDO RAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="7b6dd-601">**Пакетная синхронная DRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-601">**Burst Synchronous DRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="7b6dd-602">**Конвейерный пакет SRAM** (9)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-602">**Pipelined Burst SRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="7b6dd-603">**Кдрам** (10)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-603">**CDRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="7b6dd-604">**3DRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-604">**3DRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="7b6dd-605">**SDRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-605">**SDRAM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="7b6dd-606">**Сграм** (13)</span><span class="sxs-lookup"><span data-stu-id="7b6dd-606">**SGRAM** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7b6dd-607">**видеомоде**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-607">**VideoMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-608">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-608">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-609">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-609">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-610">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7b6dd-610">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-611">Текущий видеорежим.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-611">Current video mode.</span></span>

</dd> <dt>

<span data-ttu-id="7b6dd-612">**видеопроцессор**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-612">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b6dd-613">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b6dd-614">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b6dd-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b6dd-615">Произвольная строка, описывающая процессор или контроллер видео.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-615">Free-form string that describes the video processor/controller.</span></span>

<span data-ttu-id="7b6dd-616">Это свойство наследуется от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-616">This property is inherited from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b6dd-617">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b6dd-617">Remarks</span></span>

<span data-ttu-id="7b6dd-618">Класс **CIM \_ пквидеоконтроллер** является производным от [**CIM \_ Видеоконтроллер**](cim-videocontroller.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-618">The **CIM\_PCVideoController** class is derived from [**CIM\_VideoController**](cim-videocontroller.md).</span></span>

<span data-ttu-id="7b6dd-619">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-619">WMI does not implement this class.</span></span> <span data-ttu-id="7b6dd-620">Классы WMI, производные от [**CIM \_ пквидеоконтроллер**](cim-videocontroller.md), см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7b6dd-620">For WMI classes derived from [**CIM\_PCVideoController**](cim-videocontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7b6dd-621">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-621">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7b6dd-622">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7b6dd-622">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b6dd-623">Требования</span><span class="sxs-lookup"><span data-stu-id="7b6dd-623">Requirements</span></span>



| <span data-ttu-id="7b6dd-624">Требование</span><span class="sxs-lookup"><span data-stu-id="7b6dd-624">Requirement</span></span> | <span data-ttu-id="7b6dd-625">Значение</span><span class="sxs-lookup"><span data-stu-id="7b6dd-625">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b6dd-626">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b6dd-626">Minimum supported client</span></span><br/> | <span data-ttu-id="7b6dd-627">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b6dd-627">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b6dd-628">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b6dd-628">Minimum supported server</span></span><br/> | <span data-ttu-id="7b6dd-629">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b6dd-629">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b6dd-630">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7b6dd-630">Namespace</span></span><br/>                | <span data-ttu-id="7b6dd-631">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7b6dd-631">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b6dd-632">MOF</span><span class="sxs-lookup"><span data-stu-id="7b6dd-632">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b6dd-633"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b6dd-633"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b6dd-634">DLL</span><span class="sxs-lookup"><span data-stu-id="7b6dd-634">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b6dd-635"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b6dd-635"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b6dd-636">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b6dd-636">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b6dd-637">**\_ВИДЕОКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="7b6dd-637">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> </dl>

 

